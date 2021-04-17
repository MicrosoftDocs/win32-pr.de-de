---
title: Accelerators-Ressource
description: Definiert einen oder mehrere Acceleratoren für eine Anwendung. Eine Zugriffstaste ist eine von der Anwendung definierte Tastatureingabe, um dem Benutzer eine schnelle Möglichkeit zum Ausführen einer Aufgabe zu geben.
ms.assetid: 5953ee2d-b7a7-45d2-8445-4cba1207e272
keywords:
- Ressourcen Menüs und andere Ressourcen für Accelerators
topic_type:
- apiref
api_name:
- ACCELERATORS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2aeb09ca52438f7b2f4903e5403eeb722e5d7d7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104516751"
---
# <a name="accelerators-resource"></a>Accelerators-Ressource

Definiert einen oder mehrere Acceleratoren für eine Anwendung. Eine Zugriffstaste ist eine von der Anwendung definierte Tastatureingabe, um dem Benutzer eine schnelle Möglichkeit zum Ausführen einer Aufgabe zu geben.

``` syntax
acctablename ACCELERATORS [optional-statements] {event, idvalue, [type] [options]... }
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="acctablename"></span><span id="ACCTABLENAME"></span>*acctablename*
</dt> <dd>

Eindeutiger Name oder ein 16-Bit-ganz Zahl Wert ohne Vorzeichen, der die Ressource identifiziert.

</dd> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optionale-Anweisungen*
</dt> <dd>

NULL oder mehr der folgenden Anweisungen.



| -Anweisung.                                                        | BESCHREIBUNG                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Merkmale**](characteristics-statement.md) *DWORD*     | Benutzerdefinierte Informationen zu einer Ressource, die von Tools verwendet werden kann, die Ressourcen Dateien lesen und schreiben. Weitere Informationen finden Sie unter [**Merkmale**](characteristics-statement.md). |
| [**Sprach**](language-statement.md) *Sprache*, *unter Sprache* | Gibt die Sprache für die Ressource an. Weitere Informationen finden Sie unter [**Sprache**](language-statement.md).                                                                              |
| [**Version**](version-statement.md) *DWORD*                     | Eine benutzerdefinierte Versionsnummer für die Ressource, die von Tools verwendet werden kann, die Ressourcen Dateien lesen und schreiben. Weitere Informationen finden Sie unter [**Version**](version-statement.md).              |



 

</dd> <dt>

<span id="event"></span><span id="EVENT"></span>*Veranstalter*
</dt> <dd>

Tastatureingabe, die als Zugriffstaste verwendet werden soll. Dabei kann es sich um einen der folgenden Zeichen Typen handeln:



| type                    | BESCHREIBUNG                                                                                                                                                                                                                                  |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "*char*"                | Ein einzelnes Zeichen, das in doppelte Anführungszeichen (") eingeschlossen ist. Dem Zeichen kann ein Caretzeichen (^) vorangestellt werden, was bedeutet, dass das Zeichen ein Steuerzeichen ist.                                                                                  |
| *Zeichen*             | Ein ganzzahliger Wert, der ein Zeichen darstellt. Der *Typparameter* muss **ASCII** sein.                                                                                                                                                           |
| *virtuelles Schlüsselzeichen* | Ein ganzzahliger Wert, der einen virtuellen Schlüssel darstellt. Der virtuelle Schlüssel für alphanumerische Schlüssel kann angegeben werden, indem der Großbuchstabe oder die Zahl in doppelte Anführungszeichen (z. b. "9" oder "C") platziert wird. Der *Typparameter* muss " **VIRTKEY**" lauten. |



 

</dd> <dt>

<span id="idvalue"></span><span id="IDVALUE"></span>*idvalue*
</dt> <dd>

ein 16-Bit-Ganzzahl-Wert ohne Vorzeichen, der die Zugriffstaste identifiziert.

</dd> <dt>

<span id="type"></span><span id="TYPE"></span>*Sorte*
</dt> <dd>

Nur erforderlich, wenn der *Ereignis* Parameter ein *Zeichen* oder ein *Virtuelles Schlüsselzeichen* ist. Der *Typparameter* gibt entweder **ASCII** oder **VIRTKEY** an. der ganzzahlige Wert des *Ereignisses* wird entsprechend interpretiert. Wenn **VIRTKEY** angegeben wird und das *Ereignis* eine Zeichenfolge enthält, muss das *Ereignis* in Großbuchstaben angegeben werden.

</dd> <dt>

<span id="options"></span><span id="OPTIONS"></span>*Optionen*
</dt> <dd>

Optionen, die die Zugriffstaste definieren. Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.



| Option                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Noinvert**                       | Gibt an, dass kein Menü Element der obersten Ebene hervorgehoben wird, wenn die Zugriffstaste verwendet wird. Dies ist hilfreich, wenn Sie schnell Infos für Aktionen definieren, z. b. durch Scrollen, die keinem Menü Element entsprechen. Wenn **noinvert** weggelassen wird, wird ein Menü Element der obersten Ebene (sofern möglich) hervorgehoben, wenn die Zugriffstaste verwendet wird. Dieses Attribut ist veraltet und wird nur aus Gründen der Abwärtskompatibilität mit Ressourcen Dateien, die für 16-Bit-Windows entwickelt wurden, beibehalten. |
| **ALT**                            | Bewirkt, dass die Zugriffstaste nur aktiviert wird, wenn die Alt-Taste gedrückt ist. Gilt nur für virtuelle Schlüssel.                                                                                                                                                                                                                                                                                                                                            |
| **Schuss**                          | Bewirkt, dass die Zugriffstaste nur aktiviert wird, wenn die UMSCHALTTASTE gedrückt ist. Gilt nur für virtuelle Schlüssel                                                                                                                                                                                                                                                                                                                                           |
| [**Steuerelement**](control-control.md) | Definiert das Zeichen als Steuerzeichen (die Zugriffstaste wird nur aktiviert, wenn die Steuertaste nicht aktiviert ist). Dies hat die gleiche Auswirkung wie die Verwendung eines Caretzeichen (^) vor dem Zugriffstasten Zeichen im *Ereignis* Parameter. Gilt nur für virtuelle Schlüssel                                                                                                                                                                                           |



 

</dd> </dl>

Bestimmte Attribute werden auch aus Gründen der Abwärtskompatibilität unterstützt. Weitere Informationen finden Sie unter [allgemeine Ressourcen Attribute](common-resource-attributes.md).

## <a name="remarks"></a>Bemerkungen

Die [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) -Funktion wird verwendet, um Accelerators-Nachrichten aus der Anwendungs Warteschlange in [**WM- \_ Befehl**](./wm-command.md) -oder [**WM- \_ syscommand**](./wm-syscommand.md) -Meldungen

## <a name="examples"></a>Beispiele

Das folgende Beispiel veranschaulicht die Verwendung von Zugriffstasten.

``` syntax
1 ACCELERATORS
{
  "^C",  IDDCLEAR         ; control C
  "K",   IDDCLEAR         ; shift K
  "k",   IDDELLIPSE, ALT  ; alt k
  98,    IDDRECT, ASCII   ; b
  66,    IDDSTAR, ASCII   ; B (shift b)
  "g",   IDDRECT          ; g
  "G",   IDDSTAR          ; G (shift G)
  VK_F1, IDDCLEAR, VIRTKEY                ; F1
  VK_F1, IDDSTAR, CONTROL, VIRTKEY        ; control F1
  VK_F1, IDDELLIPSE, SHIFT, VIRTKEY       ; shift F1
  VK_F1, IDDRECT, ALT, VIRTKEY            ; alt F1
  VK_F2, IDDCLEAR, ALT, SHIFT, VIRTKEY    ; alt shift F2
  VK_F2, IDDSTAR, CONTROL, SHIFT, VIRTKEY ; ctrl shift F2
  VK_F2, IDDRECT, ALT, CONTROL, VIRTKEY   ; alt control F2
}
```

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Verwenden von Tastatur Accelerators](./using-keyboard-accelerators.md)
</dt> <dt>

[**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[**Charakteristik**](characteristics-statement.md)
</dt> <dt>

[**Dialog**](dialog-resource.md)
</dt> <dt>

[**Kurse**](language-statement.md)
</dt> <dt>

[**Stehen**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[**Version**](version-statement.md)
</dt> </dl>

 

 