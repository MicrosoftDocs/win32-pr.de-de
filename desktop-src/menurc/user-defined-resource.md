---
title: User-Defined-Ressource
description: Eine benutzerdefinierte Ressourcen Definitions Anweisung definiert eine Ressource, die anwendungsspezifische Daten enthält.
ms.assetid: b1cfec71-5733-4900-97f6-c1cbb350c728
keywords:
- benutzerdefinierte Ressource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 909352c7f0643ed67b1d199fafba1ac8f15d2a9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206693"
---
# <a name="user-defined-resource"></a>User-Defined-Ressource

Eine benutzerdefinierte Ressourcen Definitions Anweisung definiert eine Ressource, die anwendungsspezifische Daten enthält. Die Daten können ein beliebiges Format aufweisen und können entweder als Inhalt einer bestimmten Datei (wenn der *filename* -Parameter angegeben ist) oder als eine Reihe von Zahlen und Zeichen folgen (wenn der *RAW-Data-* Block angegeben ist) definiert werden.

``` syntax
nameID typeID filename
```

Der *Dateiname* gibt den Namen einer Datei an, die die Binärdaten der Ressource enthält. Der Inhalt der Datei ist als Ressource enthalten. RC interpretiert die Binärdaten in keiner Weise. Der Programmierer ist dafür verantwortlich, sicherzustellen, dass die Daten für die Zielcomputer Architektur ordnungsgemäß ausgerichtet werden.

Eine benutzerdefinierte Ressource kann auch vollständig im Ressourcen Skript definiert werden. verwenden Sie dazu die folgende Syntax:

``` syntax
nameID typeID  {  raw-data  }
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*NameID*
</dt> <dd>

Eindeutiger Name oder eine 16-Bit-Ganzzahl ohne Vorzeichen, die die Ressource identifiziert.

</dd> <dt>

<span id="typeID"></span><span id="typeid"></span><span id="TYPEID"></span>*TypeId*
</dt> <dd>

Eindeutiger Name oder eine 16-Bit-Ganzzahl ohne Vorzeichen, die den Ressourcentyp identifiziert. Wenn eine Zahl angegeben wird, muss sie größer als 255 sein. Die Zahlen 1 bis 255 sind für vorhandene und zukünftige neu definierte Ressourcentypen reserviert.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*Einfügen*
</dt> <dd>

Der Name der Datei, die die Ressourcen Daten enthält. Der-Parameter muss ein gültiger Dateiname sein. Es muss sich um einen vollständigen Pfad handeln, wenn sich die Datei nicht im aktuellen Arbeitsverzeichnis befindet.

</dd> <dt>

<span id="raw-data"></span><span id="RAW-DATA"></span>*Rohdaten*
</dt> <dd>

Rohdaten, die aus einer oder mehreren Ganzzahlen oder Zeichen folgen bestehen. Ganze Zahlen können im Dezimal-, Oktal-oder Hexadezimal Format angegeben werden. Um mit 16-Bit-Fenstern kompatibel zu sein, werden ganze Zahlen als Word-Werte gespeichert. Sie können eine ganze Zahl als DWORD-Wert speichern, indem Sie die ganze Zahl mit dem Suffix "L" qualifizieren.

Zeichen folgen werden in Anführungszeichen eingeschlossen. RC fügt kein abschließendes NULL-Zeichen automatisch an eine Zeichenfolge an. Jede Zeichenfolge ist eine Sequenz der angegebenen ANSI-Zeichen, es sei denn, Sie qualifizieren Sie als breit Zeichen-Zeichenfolge mit dem Präfix "L".

Der Datenblock beginnt an einer **DWORD** -Grenze, und RC führt keine Auffüll-oder Ausrichtungs Daten im *RAW-Data-* Block aus. Der Programmierer ist dafür verantwortlich, die ordnungsgemäße Ausrichtung der Daten innerhalb des Blocks sicherzustellen.

</dd> </dl>

## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt mehrere benutzerdefinierte-Anweisungen:

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

 

 




