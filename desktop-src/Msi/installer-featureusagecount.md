---
description: Die featureusagecount-Eigenschaft ist eine schreibgeschützte Eigenschaft, die zurückgibt, wie oft die Funktion verwendet wurde.
ms.assetid: 70171e22-d73a-4718-a360-df9d1722761b
title: Installer. featureusagecount-Eigenschaft
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
ms.openlocfilehash: fbacb6b6fd5dc4d31d7c727d719e1253969c0d43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367443"
---
# <a name="installerfeatureusagecount-property"></a>Installer. featureusagecount-Eigenschaft

Die **featureusagecount** -Eigenschaft ist eine schreibgeschützte Eigenschaft, die zurückgibt, wie oft die Funktion verwendet wurde.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.FeatureUsageCount
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Bemerkungen

Die Verwendung der [**Funktionen usefeature**](installer-usefeature.md), [**providecomponent**](installer-providecomponent.md) oder [**providequalifiedcomponent**](installer-providequalifiedcomponent.md) oder ihrer API-Entsprechungen für die angegebene Funktion erhöht diese Eigenschaft.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msigetfeatureusage**](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea)
</dt> </dl>

 

 




