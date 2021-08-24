---
description: 'Weitere Informationen finden Sie unter: Api.JetGotoSecondaryIndexBookmark-Methode'
title: Api.JetGotoSecondaryIndexBookmark-Methode
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
ms.openlocfilehash: 93d85897f81e27cc1e5704bd5524adf4abd921e86e9d5ad24f5893ee4384c427
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119455720"
---
# <a name="apijetgotosecondaryindexbookmark-method"></a>Api.JetGotoSecondaryIndexBookmark-Methode

Positioniert einen Cursor auf einen Indexeintrag, der dem angegebenen sekundären Indexlesezeichen zugeordnet ist. Das sekundäre Indexlesezeichen muss mit demselben Index für dieselbe Tabelle verwendet werden, aus der es ursprünglich abgerufen wurde. Das sekundäre Indexlesezeichen für einen Indexeintrag kann mit JetGotoSecondaryIndexBookmark(JET_SESID, JET_TABLEID, \[ \] , Int32, \[ \] , Int32, GotoSecondaryIndexBookmarkGrbit) abgerufen werden.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

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

  - sesid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Sitzung.

<!-- end list -->

  - tableid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Der zu positionierende Tabellencursor.

<!-- end list -->

  - secondaryKey  
    Typ: \[\]  
    
    Der Puffer, der den sekundären Schlüssel enthält.

<!-- end list -->

  - secondaryKeySize  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Die Größe des sekundären Schlüssels.

<!-- end list -->

  - primaryKey  
    Typ: \[\]  
    
    Der Puffer, der den Primärschlüssel enthält.

<!-- end list -->

  - primaryKeySize  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Die Größe des Primärschlüssels.

<!-- end list -->

  - grbit  
    Typ: [Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit](./gotosecondaryindexbookmarkgrbit-enumeration.md)  
    
    Optionen zum Positionieren des Lesezeichens.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[API-Klasse](./api-class.md)

[API-Member](./api-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
