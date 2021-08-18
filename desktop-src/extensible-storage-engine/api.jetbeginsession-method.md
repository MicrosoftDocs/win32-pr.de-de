---
description: 'Weitere Informationen finden Sie unter: Api.JetBeginSession-Methode'
title: Api.JetBeginSession-Methode
TOCTitle: 'JetBeginSession method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetBeginSession(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_SESID@,System.String,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetbeginsession(v=EXCHG.10)
ms:contentKeyID: 55107223
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetBeginSession
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetBeginSession
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7c305731c44fe779ca64edb502c64eac92e5b61e381748fe6b6bccf38fc51cca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118983630"
---
# <a name="apijetbeginsession-method"></a>Api.JetBeginSession-Methode

Initialisieren Sie eine neue ESENT-Sitzung.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub JetBeginSession ( _
    instance As JET_INSTANCE, _
    <OutAttribute> ByRef sesid As JET_SESID, _
    username As String, _
    password As String _
)
'Usage
Dim instance As JET_INSTANCE
Dim sesid As JET_SESID
Dim username As String
Dim password As StringApi.JetBeginSession(instance, sesid, _
    username, password)
```

``` csharp
public static void JetBeginSession(
    JET_INSTANCE instance,
    out JET_SESID sesid,
    string username,
    string password
)
```

#### <a name="parameters"></a>Parameter

  - instance  
    Typ: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Die initialisierte -Instanz, in der die Sitzung erstellt werden soll.

<!-- end list -->

  - sesid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Gibt die erstellte Sitzung zurück.

<!-- end list -->

  - username  
    Typ: [System.String](/dotnet/api/system.string)  
    
    Der -Parameter wird nicht verwendet.

<!-- end list -->

  - password  
    Typ: [System.String](/dotnet/api/system.string)  
    
    Der -Parameter wird nicht verwendet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[API-Klasse](./api-class.md)

[API-Member](./api-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
