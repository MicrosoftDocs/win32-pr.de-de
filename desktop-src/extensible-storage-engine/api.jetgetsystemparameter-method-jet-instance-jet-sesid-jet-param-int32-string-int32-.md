---
description: 'Weitere Informationen finden Sie unter: API. jetgetsystemparameter-Methode (JET_INSTANCE, JET_SESID, JET_param, Int32, String, Int32)'
title: API. jetgetsystemparameter-Methode (JET_INSTANCE, JET_SESID, JET_param, Int32, String, Int32)
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
ms.openlocfilehash: 840c17ef1d74b57b4bee75b9efafe5a314f09a57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862228"
---
# <a name="apijetgetsystemparameter-method-jet_instance-jet_sesid-jet_param-int32-string-int32"></a>API. jetgetsystemparameter-Methode (JET_INSTANCE, JET_SESID, JET_param, Int32, String, Int32)

Ruft Daten Bank Konfigurationsoptionen ab.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

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
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Die-Instanz, aus der die Optionen abgerufen werden sollen.

<!-- end list -->

  - -sid  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Sitzung.

<!-- end list -->

  - paramid  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_param](./jet-param-enumeration.md)  
    
    Der zu Get-Parameter.

<!-- end list -->

  - angegebene paramValue  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Gibt den Wert des-Parameters zurück, wenn der Wert eine ganze Zahl ist.

<!-- end list -->

  - paramString  
    Typ: [System. String](/dotnet/api/system.string)  
    
    Gibt den Wert des-Parameters zurück, wenn der Wert eine Zeichenfolge ist.

<!-- end list -->

  - maxparam  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Die maximale Größe der Parameter Zeichenfolge.

#### <a name="return-value"></a>Rückgabewert

Typ: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)  
Ein ESENT-Warnungs Code.  

## <a name="remarks"></a>Bemerkungen

[Errorto String](./jet-param-enumeration.md) übergibt die Fehlernummer im paramValue, weshalb es sich um einen ref-Parameter und nicht um einen out-Parameter handelt.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[API-Klasse](./api-class.md)

[API-Mitglieder](./api-members.md)

[Jetgetsystemparameter-Überladung](./api.jetgetsystemparameter-method.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
