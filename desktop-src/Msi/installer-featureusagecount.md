---
description: Die FeatureUsageCount-Eigenschaft ist eine schreibgeschützte Eigenschaft, die zurückgibt, wie oft das Feature verwendet wurde.
ms.assetid: 70171e22-d73a-4718-a360-df9d1722761b
title: Installer.FeatureUsageCount-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FeatureUsageCount
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8f0f8444909d07655949cd35d060eb455e5a153fc2b897e757c2fdde2d1d731d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118631199"
---
# <a name="installerfeatureusagecount-property"></a>Installer.FeatureUsageCount-Eigenschaft

Die **FeatureUsageCount-Eigenschaft** ist eine schreibgeschützte Eigenschaft, die zurückgibt, wie oft das Feature verwendet wurde.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.FeatureUsageCount
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Hinweise

Die Verwendung der Methoden [**UseFeature,**](installer-usefeature.md) [**ProvideComponent**](installer-providecomponent.md) oder [**ProvideQualifiedComponent**](installer-providequalifiedcomponent.md) oder deren API-Entsprechungen für das angegebene Feature erhöht diese Eigenschaft.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-0000000000046 definiert.<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**MsiGetFeatureUsage**](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea)
</dt> </dl>

 

 




