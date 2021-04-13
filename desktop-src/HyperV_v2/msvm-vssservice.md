---
description: Stellt den Gast-VSS-Dienst dar. Sie wird zum Abfragen von Gast Cluster Informationen vom Hyper-V-Host verwendet.
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
ms.openlocfilehash: 298ced09537ffc6e17f98484f600b05155fe0d97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342769"
---
# <a name="msvm_vssservice-class"></a>MSVM- \_ VssService-Klasse

Stellt den Gast-VSS-Dienst dar. Sie wird zum Abfragen von Gast Cluster Informationen vom Hyper-V-Host verwendet.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VssService : Msvm_GuestService
{
};
```

## <a name="members"></a>Member

Die **MSVM \_ VssService** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **MSVM- \_ VssService** -Klasse verfügt über diese Methoden.



| Methode                                                                               | BESCHREIBUNG                                                                 |
|:-------------------------------------------------------------------------------------|:----------------------------------------------------------------------------|
| [**Queryguestclusterinformation**](msvm-vssservice-queryguestclusterinformation.md) | Abfragen von Cluster Informationen vom Hyper-V-Host zum Gast.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSVM- \_ guestservice**](msvm-guestservice.md)
</dt> </dl>

 

 




