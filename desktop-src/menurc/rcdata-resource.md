---
title: RCDATA-Ressource
description: Definiert eine Rohdaten Ressource für eine Anwendung. Rohdaten Ressourcen ermöglichen die direkte Einbindung von Binärdaten in die ausführbare Datei.
ms.assetid: 7535cb06-858b-4726-aaa5-43519f84d0e4
keywords:
- RCDATA-Ressourcen Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- RCDATA
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44de0e71e3ba744f668535950224129b91bc3653
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103948250"
---
# <a name="rcdata-resource"></a>RCDATA-Ressource

Definiert eine Rohdaten Ressource für eine Anwendung. Rohdaten Ressourcen ermöglichen die direkte Einbindung von Binärdaten in die ausführbare Datei.

``` syntax
nameID RCDATA  [optional-statements] {raw-data  ...}
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*NameID*
</dt> <dd>

Eindeutiger Name oder ein 16-Bit-ganz Zahl Wert ohne Vorzeichen, der die Ressource identifiziert.

</dd> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optionale-Anweisungen*
</dt> <dd>

Dieser Parameter kann NULL oder mehr der folgenden-Anweisungen sein.



| -Anweisung.                                                        | BESCHREIBUNG                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Merkmale**](characteristics-statement.md) *DWORD*     | Benutzerdefinierte Informationen zu einer Ressource, die von Tools verwendet werden kann, die Ressourcen Dateien lesen und schreiben. Weitere Informationen finden Sie unter [**Merkmale**](characteristics-statement.md). |
| [**Sprach**](language-statement.md) *Sprache*, *unter Sprache* | Sprache für die Ressource. Weitere Informationen finden Sie unter [**Sprache**](language-statement.md).                                                                                            |
| [**Version**](version-statement.md) *DWORD*                     | Eine benutzerdefinierte Versionsnummer für die Ressource, die von Tools verwendet werden kann, die Ressourcen Dateien lesen und schreiben. Weitere Informationen finden Sie unter [**Version**](version-statement.md).              |



 

</dd> <dt>

<span id="raw-data"></span><span id="RAW-DATA"></span>*Rohdaten*
</dt> <dd>

Rohdaten, die aus einer oder mehreren Ganzzahlen oder Zeichen folgen bestehen. Ganze Zahlen können im Dezimal-, Oktal-oder Hexadezimal Format angegeben werden. Um mit 16-Bit-Fenstern kompatibel zu sein, werden ganze Zahlen als **Word** -Werte gespeichert. Sie können eine ganze Zahl als **DWORD** -Wert speichern, indem Sie die ganze Zahl mit dem Suffix "L" qualifizieren.

Zeichen folgen werden in Anführungszeichen eingeschlossen. RC fügt kein abschließendes NULL-Zeichen automatisch an eine Zeichenfolge an. Jede Zeichenfolge ist eine Sequenz der angegebenen ANSI-Zeichen, es sei denn, Sie qualifizieren Sie als breit Zeichen-Zeichenfolge mit dem L-Präfix.

Der Datenblock beginnt an einer **DWORD** -Grenze, und RC führt keine Auffüll-oder Ausrichtungs Daten im *RAW-Data-* Block aus. Es liegt in ihrer Verantwortung, die richtige Ausrichtung der Daten innerhalb des Blocks sicherzustellen.

</dd> </dl>

Bestimmte Attribute werden auch aus Gründen der Abwärtskompatibilität unterstützt. Weitere Informationen finden Sie unter [allgemeine Ressourcen Attribute](common-resource-attributes.md).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Verwendung der **RCDATA** -Anweisung veranschaulicht:

``` syntax
resname RCDATA
{
   "Here is an ANSI string\0",    // explicitly null-terminated 
   L"Here is a Unicode string\0", // explicitly null-terminated 
   1024,                          // integer, stored as WORD 
   7L,                            // integer, stored as DWORD 
   0x029a,                        // hex integer 
   0o733,                         // octal integer 
}
```

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Accelerators**](accelerators-resource.md)
</dt> <dt>

[**Charakteristik**](characteristics-statement.md)
</dt> <dt>

[**Kurse**](language-statement.md)
</dt> <dt>

[**Stehen**](menu-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[**Version**](version-statement.md)
</dt> </dl>

 

 




