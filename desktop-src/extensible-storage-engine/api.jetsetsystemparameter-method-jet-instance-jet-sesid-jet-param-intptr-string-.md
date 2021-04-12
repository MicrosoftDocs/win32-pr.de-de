---
description: 'Weitere Informationen finden Sie unter: API. jetsetsystemparameter-Methode (JET_INSTANCE, JET_SESID, JET_param, IntPtr, String)'
title: API. jetsetsystemparameter-Methode (JET_INSTANCE, JET_SESID, JET_param, IntPtr, String)
TOCTitle: JetSetSystemParameter method (JET_INSTANCE, JET_SESID, JET_param, IntPtr, String)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetSystemParameter(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_param,System.IntPtr,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetsystemparameter(v=EXCHG.10)
ms:contentKeyID: 55100822
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetSystemParameter
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 72a92ea3d6b6d4b828e409cd08b896f54c4aa053
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217280"
---
# <a name="apijetsetsystemparameter-method-jet_instance-jet_sesid-jet_param-intptr-string"></a>API. jetsetsystemparameter-Methode (JET_INSTANCE, JET_SESID, JET_param, IntPtr, String)

Legt Daten Bank Konfigurationsoptionen fest.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Function JetSetSystemParameter ( _
    instance As JET_INSTANCE, _
    sesid As JET_SESID, _
    paramid As JET_param, _
    paramValue As IntPtr, _
    paramString As String _
) As JET_wrn
'Usage
Dim instance As JET_INSTANCE
Dim sesid As JET_SESID
Dim paramid As JET_param
Dim paramValue As IntPtr
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
    IntPtr paramValue,
    string paramString
)
```

#### <a name="parameters"></a>Parameter

  - instance  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Die Instanz, für die die Option festgelegt werden soll, oder [null](./jet-instance.nil-property.md) , um die Option für alle Instanzen festzulegen.

<!-- end list -->

  - -sid  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Sitzung.

<!-- end list -->

  - paramid  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_param](./jet-param-enumeration.md)  
    
    Der festzulegende Parameter.

<!-- end list -->

  - angegebene paramValue  
    Typ: [System. IntPtr](/dotnet/api/system.intptr)  
    
    Der Wert des festzulegenden Parameters, wenn der Parameter ein ganzzahliger Typ ist.

<!-- end list -->

  - paramString  
    Typ: [System. String](/dotnet/api/system.string)  
    
    Der Wert des festzulegenden Parameters, wenn der Parameter vom Typ String ist.

#### <a name="return-value"></a>Rückgabewert

Typ: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)  
Ein ESENT-Warnungs Code.  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[API-Klasse](./api-class.md)

[API-Mitglieder](./api-members.md)

[Jetsetsystemparameter-Überladung](./api.jetsetsystemparameter-method.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
