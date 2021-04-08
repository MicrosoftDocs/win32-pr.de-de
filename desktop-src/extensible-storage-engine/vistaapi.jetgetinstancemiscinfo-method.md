---
description: 'Weitere Informationen finden Sie hier: vistaapi. jetgetinstancefehlinfo-Methode'
title: Vistaapi. jetgetinstancefehlinfo-Methode (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'JetGetInstanceMiscInfo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetInstanceMiscInfo(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_SIGNATURE@,Microsoft.Isam.Esent.Interop.Vista.JET_InstanceMiscInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetgetinstancemiscinfo(v=EXCHG.10)
ms:contentKeyID: 55104187
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetInstanceMiscInfo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetInstanceMiscInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 204beee343a717d5b45d8003e123bbbe186437d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863692"
---
# <a name="vistaapijetgetinstancemiscinfo-method"></a>Vistaapi. jetgetinstancefehlinfo-Methode

Ruft Informationen zu einer-Instanz ab.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub JetGetInstanceMiscInfo ( _
    instance As JET_INSTANCE, _
    <OutAttribute> ByRef signature As JET_SIGNATURE, _
    infoLevel As JET_InstanceMiscInfo _
)
'Usage
Dim instance As JET_INSTANCE
Dim signature As JET_SIGNATURE
Dim infoLevel As JET_InstanceMiscInfoVistaApi.JetGetInstanceMiscInfo(instance, _
    signature, infoLevel)
```

``` csharp
public static void JetGetInstanceMiscInfo(
    JET_INSTANCE instance,
    out JET_SIGNATURE signature,
    JET_InstanceMiscInfo infoLevel
)
```

#### <a name="parameters"></a>Parameter

  - instance  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Die-Instanz, über die Informationen erhalten werden.

<!-- end list -->

  - signature  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_SIGNATURE](./jet-signature-structure2.md)  
    
    Informationen wurden abgerufen.

<!-- end list -->

  - infolevel  
    Typ: [Microsoft.ISAM.ESENT.Interop.Vista.JET_InstanceMiscInfo](./jet-instancemiscinfo-enumeration.md)  
    
    Der Typ der abzurufenden Informationen.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Vistaapi-Klasse](./vistaapi-class.md)

[Vistaapi-Member](./vistaapi-members.md)

[Microsoft. ISAM. ESENT. Interop. Vista-Namespace](./microsoft.isam.esent.interop.vista-namespace.md)
