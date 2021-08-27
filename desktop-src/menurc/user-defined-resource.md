---
title: User-Defined Ressource
description: Eine benutzerdefinierte Ressourcendefinitions-Anweisung definiert eine Ressource, die anwendungsspezifische Daten enthält.
ms.assetid: b1cfec71-5733-4900-97f6-c1cbb350c728
keywords:
- Benutzerdefinierte Ressource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b383b7c4d1f9acfc4ce6c9db24efa77f3bfed943c1f299186d42a1facee2b43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118472617"
---
# <a name="user-defined-resource"></a>User-Defined Ressource

Eine benutzerdefinierte Ressourcendefinitions-Anweisung definiert eine Ressource, die anwendungsspezifische Daten enthält. Die Daten können ein beliebiges Format haben und entweder als  Inhalt einer bestimmten Datei (wenn der Dateinamenparameter  angegeben wird) oder als eine Reihe von Zahlen und Zeichenfolgen definiert werden (wenn der Rohdatenblock angegeben ist).

``` syntax
nameID typeID filename
```

Der *Dateiname gibt* den Namen einer Datei an, die die Binärdaten der Ressource enthält. Der Inhalt der Datei ist als Ressource enthalten. RC interpretiert die Binärdaten in irgendeiner Weise. Es liegt in der Verantwortung des Programmierers, sicherzustellen, dass die Daten ordnungsgemäß auf die Zielcomputerarchitektur abgestimmt sind.

Eine benutzerdefinierte Ressource kann auch vollständig im Ressourcenskript mit der folgenden Syntax definiert werden:

``` syntax
nameID typeID  {  raw-data  }
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Eindeutiger Name oder eine 16-Bit-Ganzzahl ohne Vorzeichen, die die Ressource identifiziert.

</dd> <dt>

<span id="typeID"></span><span id="typeid"></span><span id="TYPEID"></span>*Typeid*
</dt> <dd>

Eindeutiger Name oder eine 16-Bit-Ganzzahl ohne Vorzeichen, die den Ressourcentyp identifiziert. Wenn eine Zahl angegeben wird, muss sie größer als 255 sein. Die Zahlen 1 bis 255 sind für vorhandene und zukünftige neu definierte Ressourcentypen reserviert.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*Dateiname*
</dt> <dd>

Name der Datei, die die Ressourcendaten enthält. Der Parameter muss ein gültiger Dateiname sein. es muss ein vollständiger Pfad sein, wenn sich die Datei nicht im aktuellen Arbeitsverzeichnis befindet.

</dd> <dt>

<span id="raw-data"></span><span id="RAW-DATA"></span>*raw-data*
</dt> <dd>

Rohdaten, die aus einer oder mehreren ganzen Zahlen oder Zeichenfolgen von Zeichen bestehen. Ganze Zahlen können im Dezimal-, Oktal- oder Hexadezimalformat angegeben werden. Um mit 16-Bit-Windows kompatibel zu sein, werden ganze Zahlen als WORD-Werte gespeichert. Sie können eine ganze Zahl als DWORD-Wert speichern, indem Sie die ganze Zahl mit dem Suffix "L" qualifizieren.

Zeichenfolgen werden in Anführungszeichen eingeschlossen. RC fügt nicht automatisch ein beendendes NULL-Zeichen an eine Zeichenfolge an. Jede Zeichenfolge ist eine Sequenz der angegebenen ANSI-Zeichen, es sei denn, Sie qualifizieren sie als Breitzeichenzeichenfolge mit dem Präfix "L".

Der Datenblock beginnt an einer **DWORD-Grenze,** und RC führt keine Auf padding oder Ausrichtung von Daten innerhalb des *Rohdatenblocks* aus. Es liegt in der Verantwortung des Programmierers, die richtige Ausrichtung der Daten innerhalb des Blocks sicherzustellen.

</dd> </dl>

## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt mehrere benutzerdefinierte Anweisungen:

``` syntax
array   MYRES   data.res
14      300     custom.res
18 MYRES2
{
   "Here is an ANSI string\0",    // explicitly null-terminated 
   L"Here is a Unicode string\0", // explicitly null-terminated 
   1024,                          // integer, stored as WORD 
   7L,                            // integer, stored as DWORD 
   0x029a,                        // hex integer 
   0o733,                         // octal integer 
}
```

 

 




