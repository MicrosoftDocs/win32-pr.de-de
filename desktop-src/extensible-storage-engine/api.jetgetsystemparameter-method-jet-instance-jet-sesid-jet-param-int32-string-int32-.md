---
description: 'Weitere Informationen finden Sie unter: Api.JetGetSystemParameter-Methode (JET_INSTANCE, JET_SESID, JET_param, Int32, String, Int32)'
title: Api.JetGetSystemParameter-Methode (JET_INSTANCE, JET_SESID, JET_param, Int32, String, Int32)
TOCTitle: JetGetSystemParameter method (JET_INSTANCE, JET_SESID, JET_param, Int32, String, Int32)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetSystemParameter(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_param,System.Int32@,System.String@,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetsystemparameter(v=EXCHG.10)
ms:contentKeyID: 55100727
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetSystemParameter
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e32129c40405c1a2982f4eeeae7cd412f994cb3c956157c288c578711cbaa05e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119455810"
---
# <a name="apijetgetsystemparameter-method-jet_instance-jet_sesid-jet_param-int32-string-int32"></a>Api.JetGetSystemParameter-Methode (JET_INSTANCE, JET_SESID, JET_param, Int32, String, Int32)

Ruft Datenbankkonfigurationsoptionen ab.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Function JetGetSystemParameter ( _
    instance As JET_INSTANCE, _
    sesid As JET_SESID, _
    paramid As JET_param, _
    ByRef paramValue As Integer, _
    <OutAttribute> ByRef paramString As String, _
    maxParam As Integer _
) As JET_wrn
'Usage
Dim instance As JET_INSTANCE
Dim sesid As JET_SESID
Dim paramid As JET_param
Dim paramValue As Integer
Dim paramString As String
Dim maxParam As Integer
Dim returnValue As JET_wrn

returnValue = Api.JetGetSystemParameter(instance, _
    sesid, paramid, paramValue, paramString, _
    maxParam)
```

``` csharp
public static JET_wrn JetGetSystemParameter(
    JET_INSTANCE instance,
    JET_SESID sesid,
    JET_param paramid,
    ref int paramValue,
    out string paramString,
    int maxParam
)
```

#### <a name="parameters"></a>Parameter

  - instance  
    Typ: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Die -Instanz, aus der die Optionen abgerufen werden.

<!-- end list -->

  - sesid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Sitzung.

<!-- end list -->

  - paramid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_param](./jet-param-enumeration.md)  
    
    Der zu erhaltende Parameter.

<!-- end list -->

  - Paramvalue  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Gibt den Wert des Parameters zurück, wenn der Wert eine ganze Zahl ist.

<!-- end list -->

  - paramString  
    Typ: [System.String](/dotnet/api/system.string)  
    
    Gibt den Wert des Parameters zurück, wenn der Wert eine Zeichenfolge ist.

<!-- end list -->

  - maxParam  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Die maximale Größe der Parameterzeichenfolge.

#### <a name="return-value"></a>Rückgabewert

Typ: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)  
Ein ESENT-Warnungscode.  

## <a name="remarks"></a>Hinweise

[ErrorToString übergibt](./jet-param-enumeration.md) die Fehlernummer in paramValue, weshalb es sich um einen ref-Parameter und nicht um einen out-Parameter handelt.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[API-Klasse](./api-class.md)

[API-Member](./api-members.md)

[JetGetSystemParameter-Überladung](./api.jetgetsystemparameter-method.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
