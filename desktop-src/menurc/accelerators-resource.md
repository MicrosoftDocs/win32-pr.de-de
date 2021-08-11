---
title: ACCELERATORS-Ressource
description: Definiert einen oder mehrere Zugriffstasten für eine Anwendung. Eine Zugriffstaste ist eine Tastatureingabe, die von der Anwendung definiert wird, um dem Benutzer eine schnelle Möglichkeit zum Ausführen einer Aufgabe zu geben.
ms.assetid: 5953ee2d-b7a7-45d2-8445-4cba1207e272
keywords:
- ACCELERATORS-Ressourcenmenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- ACCELERATORS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e7ba2d19bbab6346f7a62afe56269f762cd94f7ef1730654fb6ac1abf317e4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118235739"
---
# <a name="accelerators-resource"></a>ACCELERATORS-Ressource

Definiert einen oder mehrere Zugriffstasten für eine Anwendung. Eine Zugriffstaste ist eine Tastatureingabe, die von der Anwendung definiert wird, um dem Benutzer eine schnelle Möglichkeit zum Ausführen einer Aufgabe zu geben.

``` syntax
acctablename ACCELERATORS [optional-statements] {event, idvalue, [type] [options]... }
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="acctablename"></span><span id="ACCTABLENAME"></span>*acctablename*
</dt> <dd>

Eindeutiger Name oder ein 16-Bit-Ganzzahlwert ohne Vorzeichen, der die Ressource identifiziert.

</dd> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optionale -Anweisungen*
</dt> <dd>

Null oder mehr der folgenden Anweisungen.



| -Anweisung.                                                        | BESCHREIBUNG                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CHARACTERISTICS**](characteristics-statement.md) *dword*     | Benutzerdefinierte Informationen zu einer Ressource, die von Tools verwendet werden können, die Ressourcendateien lesen und schreiben. Weitere Informationen finden Sie unter [**CHARACTERISTICS**](characteristics-statement.md). |
| [**LANGUAGE**](language-statement.md) *language*, *sublanguage* | Gibt die Sprache für die Ressource an. Weitere Informationen finden Sie unter [**LANGUAGE**](language-statement.md).                                                                              |
| [**VERSION**](version-statement.md) *dword*                     | Benutzerdefinierte Versionsnummer für die Ressource, die von Tools verwendet werden kann, die Ressourcendateien lesen und schreiben. Weitere Informationen finden Sie unter [**VERSION**](version-statement.md).              |



 

</dd> <dt>

<span id="event"></span><span id="EVENT"></span>*Ereignis*
</dt> <dd>

Tastatureingabe, die als Zugriffstaste verwendet werden soll. Dies kann einer der folgenden Zeichentypen sein.



| type                    | BESCHREIBUNG                                                                                                                                                                                                                                  |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "*char*"                | Ein einzelnes Zeichen, das in doppelte Anführungszeichen (") eingeschlossen ist. Dem Zeichen kann ein Caretzeichen (^) vorangestellt werden, was bedeutet, dass das Zeichen ein Steuerzeichen ist.                                                                                  |
| *Zeichen*             | Ein ganzzahliger Wert, der ein Zeichen darstellt. Der *Typparameter* muss **ASCII** sein.                                                                                                                                                           |
| *Virtuelles Schlüsselzeichen* | Ein ganzzahliger Wert, der einen virtuellen Schlüssel darstellt. Der virtuelle Schlüssel für alphanumerische Schlüssel kann angegeben werden, indem der Großbuchstabe oder die Zahl in doppelte Anführungszeichen gesetzt wird (z. B. "9" oder "C"). Der *Typparameter* muss **VIRTKEY** sein. |



 

</dd> <dt>

<span id="idvalue"></span><span id="IDVALUE"></span>*idvalue*
</dt> <dd>

ein 16-Bit-Ganzzahlwert ohne Vorzeichen, der die Zugriffstaste identifiziert.

</dd> <dt>

<span id="type"></span><span id="TYPE"></span>*Typ*
</dt> <dd>

Nur erforderlich, wenn der *Ereignisparameter* ein *Zeichen* oder ein *virtuelles Schlüsselzeichen* ist. Der *Typparameter* gibt entweder **ASCII** oder **VIRTKEY an.** der ganzzahlige Wert des *Ereignisses* wird entsprechend interpretiert. Wenn **VIRTKEY** angegeben wird und *das Ereignis* eine Zeichenfolge enthält, muss das *Ereignis* groß geschrieben werden.

</dd> <dt>

<span id="options"></span><span id="OPTIONS"></span>*Optionen*
</dt> <dd>

-Optionen, die die Zugriffstaste definieren. Bei diesem Parameter kann es sich um einen oder mehrere der folgenden Werte handelt.



| Option                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **NOINVERT**                       | Gibt an, dass kein Menüelement der obersten Ebene hervorgehoben wird, wenn die Zugriffstaste verwendet wird. Dies ist nützlich, wenn Sie Zugriffstasten für Aktionen wie Scrollen definieren, die keinem Menüelement entsprechen. Wenn **NOINVERT** ausgelassen wird, wird ein Menüelement der obersten Ebene hervorgehoben (sofern möglich), wenn die Zugriffstaste verwendet wird. Dieses Attribut ist veraltet und wird nur aus Gründen der Abwärtskompatibilität mit Ressourcendateien beibehalten, die für 16-Bit-Windows entwickelt wurden. |
| **ALT**                            | Bewirkt, dass die Zugriffstaste nur aktiviert wird, wenn die ALT-TASTE nicht aktiv ist. Gilt nur für virtuelle Schlüssel.                                                                                                                                                                                                                                                                                                                                            |
| **Umschalten**                          | Bewirkt, dass die Zugriffstaste nur aktiviert wird, wenn die UMSCHALTTASTE gedrückt ist. Gilt nur für virtuelle Schlüssel                                                                                                                                                                                                                                                                                                                                           |
| [**Steuerung**](control-control.md) | Definiert das Zeichen als Steuerzeichen (die Zugriffstaste wird nur aktiviert, wenn die CONTROL-Taste nicht aktiv ist). Dies hat die gleiche Auswirkung wie die Verwendung eines Caretzeichens (^) vor dem Zugriffstastenzeichen im *Ereignisparameter.* Gilt nur für virtuelle Schlüssel                                                                                                                                                                                           |



 

</dd> </dl>

Bestimmte Attribute werden auch aus Gründen der Abwärtskompatibilität unterstützt. Weitere Informationen finden Sie unter [Allgemeine Ressourcenattribute.](common-resource-attributes.md)

## <a name="remarks"></a>Hinweise

Die [**TranslateAccelerator-Funktion**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) wird verwendet, um Acceleratornachrichten aus der Anwendungswarteschlange in [**WM \_ COMMAND-**](./wm-command.md) oder [**WM \_ SYSCOMMAND-Nachrichten**](./wm-syscommand.md) zu übersetzen.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Verwendung von Zugriffstasten veranschaulicht.

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

[Verwenden von Tastenkombinationen](./using-keyboard-accelerators.md)
</dt> <dt>

[**Translateaccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[**Merkmale**](characteristics-statement.md)
</dt> <dt>

[**DIALOG**](dialog-resource.md)
</dt> <dt>

[**Sprache**](language-statement.md)
</dt> <dt>

[**Menü**](menu-resource.md)
</dt> <dt>

[**Rcdata**](rcdata-resource.md)
</dt> <dt>

[**Stringtable**](stringtable-resource.md)
</dt> <dt>

[**Version**](version-statement.md)
</dt> </dl>

 

 