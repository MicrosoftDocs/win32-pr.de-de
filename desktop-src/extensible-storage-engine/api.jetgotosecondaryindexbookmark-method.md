---
description: 'Weitere Informationen finden Sie hier: API. jetgodesecondaryindexbookmark-Methode'
title: API. jetgodesecondaryindexbookmark-Methode
TOCTitle: 'JetGotoSecondaryIndexBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGotoSecondaryIndexBookmark(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Byte[],System.Int32,Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgotosecondaryindexbookmark(v=EXCHG.10)
ms:contentKeyID: 55100755
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGotoSecondaryIndexBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGotoSecondaryIndexBookmark
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: af146236a2a5398dfb0b7b81f42dcfc6227a6de9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359569"
---
# <a name="apijetgotosecondaryindexbookmark-method"></a>API. jetgodesecondaryindexbookmark-Methode

Positioniert einen Cursor auf einen Index Eintrag, der dem angegebenen sekundären Index Lesezeichen zugeordnet ist. Das sekundäre Index Lesezeichen muss mit demselben Index für dieselbe Tabelle verwendet werden, aus der es ursprünglich abgerufen wurde. Das sekundäre Index Lesezeichen für einen Index Eintrag kann mithilfe von jetgoessecondaryindexbookmark (JET_SESID, JET_TABLEID, \[ \] , Int32, \[ \] , Int32, GOTO secondaryindexbookmarkgrbit) abgerufen werden.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub JetGotoSecondaryIndexBookmark ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    secondaryKey As Byte(), _
    secondaryKeySize As Integer, _
    primaryKey As Byte(), _
    primaryKeySize As Integer, _
    grbit As GotoSecondaryIndexBookmarkGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim secondaryKey As Byte()
Dim secondaryKeySize As Integer
Dim primaryKey As Byte()
Dim primaryKeySize As Integer
Dim grbit As GotoSecondaryIndexBookmarkGrbitApi.JetGotoSecondaryIndexBookmark(sesid, _
    tableid, secondaryKey, secondaryKeySize, _
    primaryKey, primaryKeySize, grbit)
```

``` csharp
public static void JetGotoSecondaryIndexBookmark(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] secondaryKey,
    int secondaryKeySize,
    byte[] primaryKey,
    int primaryKeySize,
    GotoSecondaryIndexBookmarkGrbit grbit
)
```

#### <a name="parameters"></a>Parameter

  - -sid  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Sitzung.

<!-- end list -->

  - TableID  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Der zu positiongende Tabellen Cursor.

<!-- end list -->

  - secondaryKey  
    Sorte \[\]  
    
    Der Puffer, der den sekundären Schlüssel enthält.

<!-- end list -->

  - secondarykeysize  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Die Größe des sekundären Schlüssels.

<!-- end list -->

  - primaryKey  
    Sorte \[\]  
    
    Der Puffer, der den Primärschlüssel enthält.

<!-- end list -->

  - primarykeysize  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Die Größe des Primärschlüssels.

<!-- end list -->

  - grbit  
    Typ: [Microsoft. ISAM. ESENT. Interop. goessecondaryindexbookmarkgrbit](./gotosecondaryindexbookmarkgrbit-enumeration.md)  
    
    Optionen zum Positionieren des Lesezeichens.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[API-Klasse](./api-class.md)

[API-Mitglieder](./api-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
