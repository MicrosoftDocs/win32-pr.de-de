---
description: Stellt den VSS-Gastdienst dar. Sie wird zum Abfragen von Gastclusterinformationen vom Hyper-V-Host verwendet.
ms.assetid: 82321456-a24e-4f67-9346-f0844e2913dc
title: Msvm_VssService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VssService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c84e9fd96ea4f82c5e89138cfb75f42e2bd184f66926d7139958f485273d6425
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014468"
---
# <a name="msvm_vssservice-class"></a>Msvm \_ VssService-Klasse

Stellt den VSS-Gastdienst dar. Sie wird zum Abfragen von Gastclusterinformationen vom Hyper-V-Host verwendet.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VssService : Msvm_GuestService
{
};
```

## <a name="members"></a>Member

Die **Msvm \_ VssService-Klasse** verfügt über folgende Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **Msvm \_ VssService-Klasse** verfügt über diese Methoden.



| Methode                                                                               | BESCHREIBUNG                                                                 |
|:-------------------------------------------------------------------------------------|:----------------------------------------------------------------------------|
| [**QueryGuestClusterInformation**](msvm-vssservice-queryguestclusterinformation.md) | Abfragen von Clusterinformationen vom Hyper-V-Host an den Gast.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msvm \_ GuestService**](msvm-guestservice.md)
</dt> </dl>

 

 




