---
description: Die featureusagedate-Eigenschaft ist eine schreibgeschützte Eigenschaft, die das Datum zurückgibt, an dem die angegebene Funktion zuletzt verwendet wurde.
ms.assetid: 444e54b2-94e7-44ea-8d7b-eeac984e3715
title: Installer. featureusagedate (Eigenschaft)
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
ms.openlocfilehash: b393f9a24b9d1ebeb82de86d26483f703d7854c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365910"
---
# <a name="installerfeatureusagedate-property"></a>Installer. featureusagedate (Eigenschaft)

Die **featureusagedate** -Eigenschaft ist eine schreibgeschützte Eigenschaft, die das Datum zurückgibt, an dem die angegebene Funktion zuletzt verwendet wurde.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.FeatureUsageDate
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wird von der Verwendung der [**Funktionen usefeature**](installer-usefeature.md), [**providecomponent**](installer-providecomponent.md) oder [**providequalifiedcomponent**](installer-providequalifiedcomponent.md) oder ihrer API-Entsprechungen für die angegebene Funktion festgelegt.

Das Datum liegt im MS-DOS-Datumsformat vor, wie in der folgenden Tabelle dargestellt.



| Bits | Inhalte                                            |
|------|-----------------------------------------------------|
| 0–4  | Tag des Monats (1-31)                             |
| 5-8  | Monat (1 = Januar, 2 = Februar usw.)        |
| 9-15 | Jahr Offset von 1980 (Hinzufügen von 1980, um das tatsächliche Jahr zu erhalten) |



 

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

 

 




