---
description: 'Weitere Informationen finden Sie unter: Windows8Api. prereadkeyranges-Methode'
title: Windows8Api. prereadkeyranges-Methode (Microsoft. ISAM. ESENT. Interop. Windows8)
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
ms.openlocfilehash: 091c1f92512fd9a55bb4acd4d824567acc19fdde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959197"
---
# <a name="windows8apiprereadkeyranges-method"></a>Windows8Api. prereadkeyranges-Methode

Wenn sich die Datensätze mit den angegebenen Schlüsselbereichen nicht im Puffer Cache befinden, starten Sie asynchrone Lesevorgänge, um die Datensätze in den Daten Bank Puffer Cache zu übertragen.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

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

  - -sid  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Sitzung.

<!-- end list -->

  - TableID  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Die Tabelle, für die die prereads ausgestellt werden sollen.

<!-- end list -->

  - keysstart  
    Sorte \[\]  
    
    Der Anfang der Schlüsselbereiche, die Voraussetzungen für die Voraussetzungen sind.

<!-- end list -->

  - keystartlängen  
    Sorte \[\]  
    
    Die Längen der Start Tasten, die Voraussetzungen sind.

<!-- end list -->

  - keysend  
    Sorte \[\]  
    
    Das Ende des rangess-Schlüssels, der sich im Voraus registriert.

<!-- end list -->

  - keyendlängen  
    Sorte \[\]  
    
    Die Länge der zu Preread enden Endschlüssel.

<!-- end list -->

  - rangeIndex  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Der Index des ersten zu lesenden Schlüsselbereichs im Array.

<!-- end list -->

  - rangecount  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Die maximale Anzahl von Schlüsselbereichen, die Voraussetzungen für die Voraussetzungen sind.

<!-- end list -->

  - rangespreread  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Gibt die Anzahl der Schlüssel zurück, die tatsächlich vorab registriert werden.

<!-- end list -->

  - columnspreread  
    Sorte \[\]  
    
    Liste der Spalten-IDs für lange Wert Spalten, die vorab registriert werden sollen.

<!-- end list -->

  - grbit  
    Typ: [Microsoft. ISAM. ESENT. Interop. Windows8. prereadindexrangesgrbit](./prereadindexrangesgrbit-enumeration.md)  
    
    Preread-Optionen. Wird verwendet, um die Richtung der Preread anzugeben.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Windows8Api-Klasse](./windows8api-class.md)

[Windows8Api-Member](./windows8api-members.md)

[Microsoft. ISAM. ESENT. Interop. Windows8-Namespace](./microsoft.isam.esent.interop.windows8-namespace.md)
