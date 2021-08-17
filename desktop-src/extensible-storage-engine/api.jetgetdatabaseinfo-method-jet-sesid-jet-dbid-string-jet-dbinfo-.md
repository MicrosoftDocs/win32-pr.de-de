---
description: 'Weitere Informationen finden Sie unter: Api.JetGetDatabaseInfo-Methode (JET_SESID, JET_DBID, String, JET_DbInfo)'
title: Api.JetGetDatabaseInfo-Methode (JET_SESID, JET_DBID, String, JET_DbInfo)
TOCTitle: JetGetDatabaseInfo method (JET_SESID, JET_DBID, String, JET_DbInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetDatabaseInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String@,Microsoft.Isam.Esent.Interop.JET_DbInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetdatabaseinfo(v=EXCHG.10)
ms:contentKeyID: 55100714
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetDatabaseInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4f0c25ca4460937705b8ff5ecd0472db0646ecbe8b88d84b84263a82b7c51d32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118784196"
---
# <a name="apijetgetdatabaseinfo-method-jet_sesid-jet_dbid-string-jet_dbinfo"></a>Api.JetGetDatabaseInfo-Methode (JET_SESID, JET_DBID, String, JET_DbInfo)

Ruft bestimmte Informationen zur angegebenen Datenbank ab.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub JetGetDatabaseInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    <OutAttribute> ByRef value As String, _
    infoLevel As JET_DbInfo _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim value As String
Dim infoLevel As JET_DbInfoApi.JetGetDatabaseInfo(sesid, dbid, _
    value, infoLevel)
```

``` csharp
public static void JetGetDatabaseInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    out string value,
    JET_DbInfo infoLevel
)
```

#### <a name="parameters"></a>Parameter

  - sesid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Sitzung.

<!-- end list -->

  - dbid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    Der Datenbankbezeichner.

<!-- end list -->

  - value  
    Typ: [System.String](/dotnet/api/system.string)  
    
    Der abzurufende Wert.

<!-- end list -->

  - infoLevel  
    Typ: [Microsoft.Isam.Esent.Interop.JET_DbInfo](./jet-dbinfo-enumeration.md)  
    
    Die spezifischen abzurufenden Daten.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[API-Klasse](./api-class.md)

[API-Member](./api-members.md)

[JetGetDatabaseInfo-Überladung](./api.jetgetdatabaseinfo-method.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
