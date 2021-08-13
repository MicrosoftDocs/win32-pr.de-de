---
description: 'Weitere Informationen finden Sie unter: Api.JetGetTableInfo-Methode (JET_SESID, JET_TABLEID, Int32, JET_TblInfo)'
title: Api.JetGetTableInfo-Methode (JET_SESID, JET_TABLEID, Int32, JET_TblInfo)
TOCTitle: JetGetTableInfo method (JET_SESID, JET_TABLEID, Int32, JET_TblInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Int32@,Microsoft.Isam.Esent.Interop.JET_TblInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettableinfo(v=EXCHG.10)
ms:contentKeyID: 55100741
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTableInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c5ef5f1cd80e12ffbb5a4c3405b238308a4bcf6d7dfb35abf6b4e6a06423f830
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118784008"
---
# <a name="apijetgettableinfo-method-jet_sesid-jet_tableid-int32-jet_tblinfo"></a>Api.JetGetTableInfo-Methode (JET_SESID, JET_TABLEID, Int32, JET_TblInfo)

Ruft verschiedene Informationen zu einer Tabelle in einer Datenbank ab.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub JetGetTableInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef result As Integer, _
    infoLevel As JET_TblInfo _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim result As Integer
Dim infoLevel As JET_TblInfoApi.JetGetTableInfo(sesid, tableid, _
    result, infoLevel)
```

``` csharp
public static void JetGetTableInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out int result,
    JET_TblInfo infoLevel
)
```

#### <a name="parameters"></a>Parameter

  - sesid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Sitzung.

<!-- end list -->

  - tableid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Die Tabelle, zu der Informationen abgerufen werden.

<!-- end list -->

  - result  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Abgerufene Informationen.

<!-- end list -->

  - infoLevel  
    Typ: [Microsoft.Isam.Esent.Interop.JET_TblInfo](./jet-tblinfo-enumeration.md)  
    
    Der Typ der abzurufenden Informationen.

## <a name="remarks"></a>Hinweise

Diese Überladung wird mit [SpaceOwned und](./jet-tblinfo-enumeration.md) [SpaceAvailable verwendet.](./jet-tblinfo-enumeration.md)

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[API-Klasse](./api-class.md)

[API-Member](./api-members.md)

[JetGetTableInfo-Überladung](./api.jetgettableinfo-method.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
