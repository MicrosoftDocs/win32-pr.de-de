---
description: 'Weitere Informationen finden Sie unter: Api.JetGetSecondaryIndexBookmark-Methode'
title: Api.JetGetSecondaryIndexBookmark-Methode
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
ms.openlocfilehash: 9a1ca2430ae188b256fb1c6d026db7b6d78e45fdbfeaec158242019b7795d910
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042528"
---
# <a name="apijetgetsecondaryindexbookmark-method"></a>Api.JetGetSecondaryIndexBookmark-Methode

Ruft ein spezielles Lesezeichen für den sekundären Indexeintrag an der aktuellen Position eines Cursors ab. Dieses Lesezeichen kann dann verwendet werden, um den Cursor mit JetGotoSecondaryIndexBookmark effizient auf denselben Indexeintrag zurückzuordnen. Dies ist besonders nützlich, wenn die Neupositionierung auf einem sekundären Index mit doppelten Schlüsseln oder mehreren Indexeinträgen für denselben Datensatz verwendet wird.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

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

  - sesid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Sitzung.

<!-- end list -->

  - tableid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Der Cursor, aus dem das Lesezeichen abgerufen werden soll.

<!-- end list -->

  - secondaryKey  
    Typ: \[\]  
    
    Ausgabepuffer für den sekundären Schlüssel.

<!-- end list -->

  - secondaryKeySize  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Größe des sekundären Schlüsselpuffers.

<!-- end list -->

  - actualSecondaryKeySize  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Gibt die Größe des sekundären Schlüssels zurück.

<!-- end list -->

  - primaryKey  
    Typ: \[\]  
    
    Ausgabepuffer für den Primärschlüssel.

<!-- end list -->

  - primaryKeySize  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Größe des Primärschlüsselpuffers.

<!-- end list -->

  - actualPrimaryKeySize  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Gibt die Größe des Primärschlüssels zurück.

<!-- end list -->

  - grbit  
    Typ: [Microsoft.Isam.Esent.Interop.GetSecondaryIndexBookmarkGrbit](./getsecondaryindexbookmarkgrbit-enumeration.md)  
    
    Optionen für den Aufruf.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[API-Klasse](./api-class.md)

[API-Member](./api-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
