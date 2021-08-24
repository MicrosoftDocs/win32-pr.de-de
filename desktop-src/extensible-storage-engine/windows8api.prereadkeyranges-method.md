---
description: 'Weitere Informationen zu: Windows8Api.PrereadKeyRanges-Methode'
title: Windows8Api.PrereadKeyRanges-Methode (Microsoft.Isam.Esent.Interop.Windows8)
TOCTitle: 'PrereadKeyRanges method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.PrereadKeyRanges(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[][],System.Int32[],System.Byte[][],System.Int32[],System.Int32,System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[],Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.prereadkeyranges(v=EXCHG.10)
ms:contentKeyID: 55104465
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.PrereadKeyRanges
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.PrereadKeyRanges
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 02328ddc47daec4fbd98f88222dd7519053ed92aa64d2a0048782340d626b03c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119452690"
---
# <a name="windows8apiprereadkeyranges-method"></a>Windows8Api.PrereadKeyRanges-Methode

Wenn sich die Datensätze mit den angegebenen Schlüsselbereichen nicht im Puffercache befinden, starten Sie asynchrone Lesezugriffe, um die Datensätze in den Datenbankpuffercache zu übertragen.

**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub PrereadKeyRanges ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    keysStart As Byte()(), _
    keyStartLengths As Integer(), _
    keysEnd As Byte()(), _
    keyEndLengths As Integer(), _
    rangeIndex As Integer, _
    rangeCount As Integer, _
    <OutAttribute> ByRef rangesPreread As Integer, _
    columnsPreread As JET_COLUMNID(), _
    grbit As PrereadIndexRangesGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim keysStart As Byte()()
Dim keyStartLengths As Integer()
Dim keysEnd As Byte()()
Dim keyEndLengths As Integer()
Dim rangeIndex As Integer
Dim rangeCount As Integer
Dim rangesPreread As Integer
Dim columnsPreread As JET_COLUMNID()
Dim grbit As PrereadIndexRangesGrbitWindows8Api.PrereadKeyRanges(sesid, tableid, _
    keysStart, keyStartLengths, keysEnd, _
    keyEndLengths, rangeIndex, rangeCount, _
    rangesPreread, columnsPreread, grbit)
```

``` csharp
public static void PrereadKeyRanges(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[][] keysStart,
    int[] keyStartLengths,
    byte[][] keysEnd,
    int[] keyEndLengths,
    int rangeIndex,
    int rangeCount,
    out int rangesPreread,
    JET_COLUMNID[] columnsPreread,
    PrereadIndexRangesGrbit grbit
)
```

#### <a name="parameters"></a>Parameter

  - sesid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Sitzung.

<!-- end list -->

  - tableid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Die Tabelle, für die die Prereads ausgegeben werden sollen.

<!-- end list -->

  - keysStart  
    Typ: \[\]  
    
    Der Anfang der vorab zu lesenden Schlüsselbereiche.

<!-- end list -->

  - keyStartLengths  
    Typ: \[\]  
    
    Die Längen der vorab zu lesenden Startschlüssel.

<!-- end list -->

  - keysEnd  
    Typ: \[\]  
    
    Das Ende der vorab zu lesenden Schlüsselbereiche.

<!-- end list -->

  - keyEndLengths  
    Typ: \[\]  
    
    Die Längen der vorab zu lesenden Endschlüssel.

<!-- end list -->

  - rangeIndex  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Der Index des ersten zu lesende Schlüsselbereichs im Array.

<!-- end list -->

  - rangeCount  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Die maximale Anzahl von Schlüsselbereichen, die vorab gelesen werden sollen.

<!-- end list -->

  - rangesPreread  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Gibt die Anzahl der Schlüssel zurück, die tatsächlich vorab gelesen wurden.

<!-- end list -->

  - columnsPreread  
    Typ: \[\]  
    
    Liste der Spalten-IDs für Spalten mit langen Werten, die vorab gelesen werden sollen.

<!-- end list -->

  - grbit  
    Typ: [Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit](./prereadindexrangesgrbit-enumeration.md)  
    
    Vorableseoptionen. Wird verwendet, um die Richtung des Prereads anzugeben.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[Windows8Api-Klasse](./windows8api-class.md)

[Windows8Api-Member](./windows8api-members.md)

[Microsoft.Isam.Esent.Interop.Windows8-Namespace](./microsoft.isam.esent.interop.windows8-namespace.md)
