---
description: Die FeatureUsageDate-Eigenschaft ist eine schreibgeschützte Eigenschaft, die das Datum zurückgibt, an dem das angegebene Feature zuletzt verwendet wurde.
ms.assetid: 444e54b2-94e7-44ea-8d7b-eeac984e3715
title: Installer.FeatureUsageDate-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FeatureUsageDate
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 15c628b95f6dab2d671e660c9783e071e1e4385c165363fdf9ad39abd571510e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118631067"
---
# <a name="installerfeatureusagedate-property"></a>Installer.FeatureUsageDate-Eigenschaft

Die **FeatureUsageDate-Eigenschaft** ist eine schreibgeschützte Eigenschaft, die das Datum zurückgibt, an dem das angegebene Feature zuletzt verwendet wurde.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.FeatureUsageDate
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Hinweise

Die Verwendung der Methoden [**UseFeature,**](installer-usefeature.md) [**ProvideComponent**](installer-providecomponent.md) oder [**ProvideQualifiedComponent**](installer-providequalifiedcomponent.md) oder deren API-Entsprechungen für das angegebene Feature legt diese Eigenschaft fest.

Das Datum liegt im MS-DOS-Datumsformat vor, wie in der folgenden Tabelle dargestellt.



| Bits | Inhalte                                            |
|------|-----------------------------------------------------|
| 0–4  | Tag des Monats (1–31)                             |
| 5-8  | Monat (1 = Januar, 2 = Februar usw.)        |
| 9-15 | Jahresoffset von 1980 (1980 hinzufügen, um das tatsächliche Jahr zu erhalten) |



 

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

 

 




