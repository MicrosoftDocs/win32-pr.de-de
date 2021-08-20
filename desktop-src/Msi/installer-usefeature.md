---
description: Die UseFeature-Methode des Installer-Objekts erhöht die Nutzungsanzahl für ein bestimmtes Feature und gibt den Installationsstatus für dieses Feature zurück. Diese Methode sollte verwendet werden, um die Absicht einer Anwendung anzugeben, ein Feature zu verwenden.
ms.assetid: c9ea812c-2f95-4ba4-ad8e-b96f7fc14bb1
title: Installer.UseFeature-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.UseFeature
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b320ce72271bb7ee90ac85a376b103d868e6f740a2e853daf58bb478dc79ad6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142155"
---
# <a name="installerusefeature-method"></a>Installer.UseFeature-Methode

Die **UseFeature-Methode** des [**Installer-Objekts**](installer-object.md) erhöht die Nutzungsanzahl für ein bestimmtes Feature und gibt den Installationsstatus für dieses Feature zurück. Diese Methode sollte verwendet werden, um die Absicht einer Anwendung anzugeben, ein Feature zu verwenden.

## <a name="syntax"></a>Syntax


```JScript
Installer.UseFeature(
  Product,
  Feature,
  InstallMode
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Produkt* 
</dt> <dd>

Gibt den Produktcode des Produkts an.

</dd> <dt>

*Feature* 
</dt> <dd>

Identifiziert das zu verwendende Feature.

</dd> <dt>

*InstallMode* 
</dt> <dd>

Dieser Parameter muss *msiInstallModeNoDetection* sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **UseFeature-Methode** sollte nur für Features verwendet werden, von der bekannt ist, dass sie veröffentlicht werden. Die Anwendung sollte den Status des Features ermitteln, indem sie entweder die [**FeatureState-Eigenschaft**](installer-featurestate.md) oder [**die Features-Eigenschaft**](installer-features.md) oder ihre API-Entsprechungen aufruft.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-0000000000046 definiert.<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MsiUseFeatureEx**](/windows/desktop/api/Msi/nf-msi-msiusefeatureexa)
</dt> </dl>

 

 




