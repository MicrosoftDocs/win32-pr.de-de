---
description: 'Weitere Informationen finden Sie unter: Api.JetSetSystemParameter-Methode (JET_INSTANCE, JET_SESID, JET_param, JET_CALLBACK, String).'
title: Api.JetSetSystemParameter-Methode (JET_INSTANCE, JET_SESID, JET_param, JET_CALLBACK, String)
TOCTitle: JetSetSystemParameter method (JET_INSTANCE, JET_SESID, JET_param, JET_CALLBACK, String)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetSystemParameter(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_param,Microsoft.Isam.Esent.Interop.JET_CALLBACK,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetsystemparameter(v=EXCHG.10)
ms:contentKeyID: 55100819
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetSystemParameter
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 600155fd91dea4091e84e81db42b9781ea72e6d5bc8274c743738b3e76e3e3e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118497807"
---
# <a name="apijetsetsystemparameter-method-jet_instance-jet_sesid-jet_param-jet_callback-string"></a>Api.JetSetSystemParameter-Methode (JET_INSTANCE, JET_SESID, JET_param, JET_CALLBACK, String)

Legt Datenbankkonfigurationsoptionen fest.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Function JetSetSystemParameter ( _
    instance As JET_INSTANCE, _
    sesid As JET_SESID, _
    paramid As JET_param, _
    paramValue As JET_CALLBACK, _
    paramString As String _
) As JET_wrn
'Usage
Dim instance As JET_INSTANCE
Dim sesid As JET_SESID
Dim paramid As JET_param
Dim paramValue As JET_CALLBACK
Dim paramString As String
Dim returnValue As JET_wrn

returnValue = Api.JetSetSystemParameter(instance, _
    sesid, paramid, paramValue, paramString)
```

``` csharp
public static JET_wrn JetSetSystemParameter(
    JET_INSTANCE instance,
    JET_SESID sesid,
    JET_param paramid,
    JET_CALLBACK paramValue,
    string paramString
)
```

#### <a name="parameters"></a>Parameter

  - instance  
    Typ: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Die Instanz, für die die Option auf oder [Nil](./jet-instance.nil-property.md) festgelegt werden soll, um die Option auf allen Instanzen festzulegen.

<!-- end list -->

  - sesid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Sitzung.

<!-- end list -->

  - paramid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_param](./jet-param-enumeration.md)  
    
    Der festzulegende Parameter.

<!-- end list -->

  - Paramvalue  
    Typ: [Microsoft.Isam.Esent.Interop.JET_CALLBACK](./jet-callback-delegate.md)  
    
    Der Wert des festzulegende Parameters, wenn der Parameter ein JET_CALLBACK ist.

<!-- end list -->

  - paramString  
    Typ: [System.String](/dotnet/api/system.string)  
    
    Der Wert des festzulegende Parameters, wenn der Parameter ein Zeichenfolgentyp ist.

#### <a name="return-value"></a>Rückgabewert

Typ: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)  
Ein ESENT-Warnungscode.  

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[API-Klasse](./api-class.md)

[API-Member](./api-members.md)

[JetSetSystemParameter-Überladung](./api.jetsetsystemparameter-method.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
