---
description: 'Weitere Informationen finden Sie hier: API. jetgetsecondaryindexbookmark-Methode'
title: API. jetgetsecondaryindexbookmark-Methode
TOCTitle: 'JetGetSecondaryIndexBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetSecondaryIndexBookmark(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.GetSecondaryIndexBookmarkGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetsecondaryindexbookmark(v=EXCHG.10)
ms:contentKeyID: 55100725
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetSecondaryIndexBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetSecondaryIndexBookmark
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b0a25e78ca291271a96d06e5c0bf61c691acd4de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041656"
---
# <a name="apijetgetsecondaryindexbookmark-method"></a>API. jetgetsecondaryindexbookmark-Methode

Ruft ein spezielles Lesezeichen für den sekundären Index Eintrag an der aktuellen Position eines Cursors ab. Dieses Lesezeichen kann dann verwendet werden, um den Cursor mithilfe von jetgoysecondaryindexbookmark effizient wieder in denselben Index Eintrag zu positionieren. Dies ist besonders nützlich, wenn Sie einen sekundären Index neu positionieren, der doppelte Schlüssel enthält oder mehrere Indexeinträge für denselben Datensatz enthält.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub JetGetSecondaryIndexBookmark ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    secondaryKey As Byte(), _
    secondaryKeySize As Integer, _
    <OutAttribute> ByRef actualSecondaryKeySize As Integer, _
    primaryKey As Byte(), _
    primaryKeySize As Integer, _
    <OutAttribute> ByRef actualPrimaryKeySize As Integer, _
    grbit As GetSecondaryIndexBookmarkGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim secondaryKey As Byte()
Dim secondaryKeySize As Integer
Dim actualSecondaryKeySize As Integer
Dim primaryKey As Byte()
Dim primaryKeySize As Integer
Dim actualPrimaryKeySize As Integer
Dim grbit As GetSecondaryIndexBookmarkGrbitApi.JetGetSecondaryIndexBookmark(sesid, _
    tableid, secondaryKey, secondaryKeySize, _
    actualSecondaryKeySize, primaryKey, _
    primaryKeySize, actualPrimaryKeySize, _
    grbit)
```

``` csharp
public static void JetGetSecondaryIndexBookmark(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] secondaryKey,
    int secondaryKeySize,
    out int actualSecondaryKeySize,
    byte[] primaryKey,
    int primaryKeySize,
    out int actualPrimaryKeySize,
    GetSecondaryIndexBookmarkGrbit grbit
)
```

#### <a name="parameters"></a>Parameter

  - -sid  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Sitzung.

<!-- end list -->

  - TableID  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Der Cursor, von dem das Lesezeichen abgerufen werden soll.

<!-- end list -->

  - secondaryKey  
    Sorte \[\]  
    
    Ausgabepuffer für den sekundären Schlüssel.

<!-- end list -->

  - secondarykeysize  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Größe des sekundären Schlüssel Puffers.

<!-- end list -->

  - actualsecondarykeysize  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Gibt die Größe des sekundären Schlüssels zurück.

<!-- end list -->

  - primaryKey  
    Sorte \[\]  
    
    Ausgabepuffer für den Primärschlüssel.

<!-- end list -->

  - primarykeysize  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Größe des Primärschlüssel Puffers.

<!-- end list -->

  - actualprimarykeysize  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Gibt die Größe des Primärschlüssels zurück.

<!-- end list -->

  - grbit  
    Typ: [Microsoft. ISAM. ESENT. Interop. getsecondaryindexbookmarkgrbit](./getsecondaryindexbookmarkgrbit-enumeration.md)  
    
    Optionen für den-Befehl.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[API-Klasse](./api-class.md)

[API-Mitglieder](./api-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
