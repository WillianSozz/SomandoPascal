unit Unit1;

{$mode objfpc}{$H+}

interface

uses
  Classes, SysUtils, Forms, Controls, Graphics, Dialogs, StdCtrls;

type

  { TPrograma }

  TPrograma = class(TForm)
    btnSomar: TButton;
    txtnum01: TEdit;
    txtnum02: TEdit;
    txtResposta: TEdit;
    titulo: TLabel;
    num01: TLabel;
    num02: TLabel;
    result: TLabel;
    procedure btnSomarClick(Sender: TObject);
  private

  public

  end;

var
  Programa: TPrograma;

implementation

{$R *.lfm}

{ TPrograma }

procedure TPrograma.btnSomarClick(Sender: TObject);

begin
      //  qualquer conjunto de caracteres (letras, simbolos, numeros)
      // sera tratado pelo pascal como String
      // letras, numeros, simbolos que sao unidos.
      // string --> str, numero --> float
      // passe de texto para numero --> StrToFloat
      // passe de numero para texto --> FloatToStr

      txtResposta.Text := FloatToStr(StrToFloat(txtnum01.Text) + StrToFloat(txtnum02.Text));
      txtnum01.Text := '';
      txtnum02.Text := '';
      txtnum01.SetFocus;
end;

end.
