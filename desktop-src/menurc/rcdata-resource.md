---
title: RCDATA-Ressource
description: Definiert eine Rohdatenressource für eine Anwendung. Rohdatenressourcen ermöglichen das direkte Einschließen von Binärdaten in die ausführbare Datei.
ms.assetid: 7535cb06-858b-4726-aaa5-43519f84d0e4
keywords:
- RCDATA-Ressourcenmenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- RCDATA
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62f813bde1195d8adcad708c40857cc11b1e7b70f696455168e174a4bf2f6cf3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847040"
---
# <a name="rcdata-resource"></a>RCDATA-Ressource

Definiert eine Rohdatenressource für eine Anwendung. Rohdatenressourcen ermöglichen das direkte Einschließen von Binärdaten in die ausführbare Datei.

``` syntax
nameID RCDATA  [optional-statements] {raw-data  ...}
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Eindeutiger Name oder ein 16-Bit-Ganzzahlwert ohne Vorzeichen, der die Ressource identifiziert.

</dd> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optionale -Anweisungen*
</dt> <dd>

Dieser Parameter kann null oder mehr der folgenden Anweisungen sein.



| -Anweisung.                                                        | BESCHREIBUNG                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CHARACTERISTICS**](characteristics-statement.md) *dword*     | Benutzerdefinierte Informationen zu einer Ressource, die von Tools verwendet werden können, die Ressourcendateien lesen und schreiben. Weitere Informationen finden Sie unter [**CHARACTERISTICS**](characteristics-statement.md). |
| [**LANGUAGE**](language-statement.md) *language*, *sublanguage* | Sprache für die Ressource. Weitere Informationen finden Sie unter [**LANGUAGE**](language-statement.md).                                                                                            |
| [**VERSION**](version-statement.md) *dword*                     | Benutzerdefinierte Versionsnummer für die Ressource, die von Tools verwendet werden kann, die Ressourcendateien lesen und schreiben. Weitere Informationen finden Sie unter [**VERSION**](version-statement.md).              |



 

</dd> <dt>

<span id="raw-data"></span><span id="RAW-DATA"></span>*Rohdaten*
</dt> <dd>

Rohdaten, die aus einer oder mehreren ganzen Zahlen oder Zeichenfolgen von Zeichen bestehen. Ganze Zahlen können im Dezimal-, Oktal- oder Hexadezimalformat angegeben werden. Um mit 16-Bit-Windows kompatibel zu sein, werden ganze Zahlen als **WORD-Werte** gespeichert. Sie können eine ganze Zahl als **DWORD-Wert** speichern, indem Sie die ganze Zahl mit dem Suffix "L" qualifizieren.

Zeichenfolgen werden in Anführungszeichen eingeschlossen. RC fügt nicht automatisch ein abschließendes NULL-Zeichen an eine Zeichenfolge an. Jede Zeichenfolge ist eine Sequenz der angegebenen ANSI-Zeichen, es sei denn, Sie qualifizieren sie als Breitzeichenzeichenfolge mit dem Präfix L.

Der Datenblock beginnt an einer **DWORD-Grenze,** und RC führt keine Auffüllung oder Ausrichtung der Daten innerhalb des *Rohdatenblocks* durch. Es liegt in Ihrer Verantwortung, die richtige Ausrichtung der Daten innerhalb des Blocks sicherzustellen.

</dd> </dl>

Bestimmte Attribute werden auch aus Gründen der Abwärtskompatibilität unterstützt. Weitere Informationen finden Sie unter [Allgemeine Ressourcenattribute.](common-resource-attributes.md)

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Verwendung der **RCDATA-Anweisung** veranschaulicht:

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

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Beschleuniger**](accelerators-resource.md)
</dt> <dt>

[**Merkmale**](characteristics-statement.md)
</dt> <dt>

[**Sprache**](language-statement.md)
</dt> <dt>

[**Menü**](menu-resource.md)
</dt> <dt>

[**Stringtable**](stringtable-resource.md)
</dt> <dt>

[**Version**](version-statement.md)
</dt> </dl>

 

 




