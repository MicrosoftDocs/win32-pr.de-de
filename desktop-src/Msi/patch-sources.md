---
description: Die Sources-Eigenschaft listet alle Quellen für die Patchinstanz auf. Diese Eigenschaft ruft MsiSourceListEnumSources auf, gibt ein Array von Zeichenfolgen zurück und akzeptiert den Quelltyp als Argument.
ms.assetid: 4a052518-4d76-4a95-be9e-7acae36db626
title: Patch.Sources-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.Sources
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 2a2f190c7d8ae42e43ac934a043dfb1a98a5e15e142415736406ffbd7f3cbc4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042400"
---
# <a name="patchsources-property"></a>Patch.Sources-Eigenschaft

Die **Sources-Eigenschaft** listet alle Quellen für die Patchinstanz auf. Diese Eigenschaft ruft [**MsiSourceListEnumSources auf,**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa) gibt ein Array von Zeichenfolgen zurück und akzeptiert den Quelltyp als Argument.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Patch.Sources
```



## <a name="property-value"></a>Eigenschaftswert

Der Typ der aufzuzählenden Quelle. Der Wert kann *msiInstallSourceTypeNetwork* (1) oder *msiInstallSourceTypeURL* (2) sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm 3.0 oder höher auf Windows Server 2003, Windows XP und Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IPatch ist als 000C10A1-0000-0000-C000-0000000000046 definiert.<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Patch**](patch-object.md)
</dt> <dt>

[**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa)
</dt> <dt>

[Nicht unterstützt in Windows Installer 2.0 und früher](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




