---
description: 'Weitere Informationen finden Sie unter: Api.JetGetObjectInfo-Methode (JET_SESID, JET_DBID, JET_objtyp, String, JET_OBJECTINFO)'
title: Api.JetGetObjectInfo-Methode (JET_SESID, JET_DBID, JET_objtyp, String, JET_OBJECTINFO)
TOCTitle: JetGetObjectInfo method (JET_SESID, JET_DBID, JET_objtyp, String, JET_OBJECTINFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetObjectInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,Microsoft.Isam.Esent.Interop.JET_objtyp,System.String,Microsoft.Isam.Esent.Interop.JET_OBJECTINFO@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetobjectinfo(v=EXCHG.10)
ms:contentKeyID: 55100733
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetObjectInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ffa80b7a3a1815d16d28682f45d553945988f4af1bbec3a05cba3a8592efb624
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042588"
---
# <a name="apijetgetobjectinfo-method-jet_sesid-jet_dbid-jet_objtyp-string-jet_objectinfo"></a>Api.JetGetObjectInfo-Methode (JET_SESID, JET_DBID, JET_objtyp, String, JET_OBJECTINFO)

Ruft Informationen zu Datenbankobjekten ab.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub JetGetObjectInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    objtyp As JET_objtyp, _
    objectName As String, _
    <OutAttribute> ByRef objectinfo As JET_OBJECTINFO _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim objtyp As JET_objtyp
Dim objectName As String
Dim objectinfo As JET_OBJECTINFOApi.JetGetObjectInfo(sesid, dbid, _
    objtyp, objectName, objectinfo)
```

``` csharp
public static void JetGetObjectInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    JET_objtyp objtyp,
    string objectName,
    out JET_OBJECTINFO objectinfo
)
```

#### <a name="parameters"></a>Parameter

  - sesid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Sitzung.

<!-- end list -->

  - dbid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    Die zu verwendende Datenbank.

<!-- end list -->

  - objtyp  
    Typ: [Microsoft.Isam.Esent.Interop.JET_objtyp](./jet-objtyp-enumeration.md)  
    
    Der Typ des Objekts.

<!-- end list -->

  - objectName  
    Typ: [System.String](/dotnet/api/system.string)  
    
    Der Objektname, über den Informationen abgerufen werden sollen.

<!-- end list -->

  - objectinfo  
    Typ: [Microsoft.Isam.Esent.Interop.JET_OBJECTINFO](./jet-objectinfo-class.md)  
    
    Ausgefüllt mit Informationen zu den Objekten in der Datenbank.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[API-Klasse](./api-class.md)

[API-Member](./api-members.md)

[JetGetObjectInfo-Überladung](./api.jetgetobjectinfo-method.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
