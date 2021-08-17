---
description: Die FeatureUsageDate-Eigenschaft ist eine schreibgeschützte Eigenschaft, die das Datum der letzten Verwendung des angegebenen Features zurückgibt.
ms.assetid: 444e54b2-94e7-44ea-8d7b-eeac984e3715
title: Installer.FeatureUsageDate (Eigenschaft)
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
# <a name="installerfeatureusagedate-property"></a>Installer.FeatureUsageDate (Eigenschaft)

Die **FeatureUsageDate-Eigenschaft** ist eine schreibgeschützte Eigenschaft, die das Datum der letzten Verwendung des angegebenen Features zurückgibt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.FeatureUsageDate
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Hinweise

Die Verwendung der [**Methoden UseFeature,**](installer-usefeature.md) [**ProvideComponent**](installer-providecomponent.md) oder [**ProvideQualifiedComponent**](installer-providequalifiedcomponent.md) oder ihrer API-Entsprechungen für das angegebene Feature legt diese Eigenschaft fest.

Das Datum hat das MS-DOS-Datumsformat, wie in der folgenden Tabelle gezeigt.



| Bits | Inhalte                                            |
|------|-----------------------------------------------------|
| 0–4  | Tag des Monats (1-31)                             |
| 5-8  | Monat (1 = Januar, 2 = Februar, und so weiter)        |
| 9-15 | Jahresoffset von 1980 (addieren Sie 1980, um das tatsächliche Jahr zu erhalten) |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MsiGetFeatureUsage**](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea)
</dt> </dl>

 

 




