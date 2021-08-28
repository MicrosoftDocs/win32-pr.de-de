---
description: Weitere Informationen zur Api.JetGetIndexInfo-Methode (JET_SESID, JET_DBID, String, String, Int32, JET_IdxInfo)
title: Api.JetGetIndexInfo-Methode (JET_SESID, JET_DBID, String, String, Int32, JET_IdxInfo)
TOCTitle: JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, Int32, JET_IdxInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,System.Int32@,Microsoft.Isam.Esent.Interop.JET_IdxInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetindexinfo(v=EXCHG.10)
ms:contentKeyID: 55100775
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5bbdbf14caebfa29c93d3aea8ea91eae1d52103bf2b19871de53c6c18a643013
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119840920"
---
# <a name="apijetgetindexinfo-method-jet_sesid-jet_dbid-string-string-int32-jet_idxinfo"></a>Api.JetGetIndexInfo-Methode (JET_SESID, JET_DBID, String, String, Int32, JET_IdxInfo)

Ruft Informationen zu Indizes für eine Tabelle ab.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub JetGetIndexInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    indexname As String, _
    <OutAttribute> ByRef result As Integer, _
    infoLevel As JET_IdxInfo _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim indexname As String
Dim result As Integer
Dim infoLevel As JET_IdxInfoApi.JetGetIndexInfo(sesid, dbid, _
    tablename, indexname, result, infoLevel)
```

``` csharp
public static void JetGetIndexInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    string indexname,
    out int result,
    JET_IdxInfo infoLevel
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

  - Tabellenname  
    Typ: [System.String](/dotnet/api/system.string)  
    
    Der Name der Tabelle, zu der Indexinformationen abgerufen werden sollen.

<!-- end list -->

  - indexname  
    Typ: [System.String](/dotnet/api/system.string)  
    
    Der Name des Indexes, zu dem Informationen abgerufen werden sollen.

<!-- end list -->

  - result  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Wird mit Informationen zu Indizes für die Tabelle ausgefüllt.

<!-- end list -->

  - infoLevel  
    Typ: [Microsoft.Isam.Esent.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)  
    
    Der Typ der abzurufende Informationen.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[API-Klasse](./api-class.md)

[API-Member](./api-members.md)

[JetGetIndexInfo-Überladung](./api.jetgetindexinfo-method.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
