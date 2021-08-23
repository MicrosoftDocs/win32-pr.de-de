---
description: Die FeatureInfo-Methode des Session-Objekts gibt ein FeatureInfo-Objekt zurück, das beschreibende Informationen für das angegebene Feature enthält.
ms.assetid: f5391fd4-984e-44cc-8b6c-fd97834e0674
title: Session.FeatureInfo-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b4d6e44a16305d4a46525cfed631068ff0137c642b09b8dc6a9eca169a104548
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625198"
---
# <a name="sessionfeatureinfo-method"></a>Session.FeatureInfo-Methode

Die **FeatureInfo-Methode** des [**Session-Objekts**](session-object.md) gibt ein **FeatureInfo-Objekt** zurück, das beschreibende Informationen für das angegebene Feature enthält.

## <a name="syntax"></a>Syntax


```JScript
Session.FeatureInfo(
  Feature
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Feature* 
</dt> <dd>

Identifiziert die funktion von Interesse.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID ISession ist als \_ 000C109E-0000-0000-C000-000000000046 definiert.<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MsiGetFeatureInfo**](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa)
</dt> </dl>

 

 




