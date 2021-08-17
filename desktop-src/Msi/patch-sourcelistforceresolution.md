---
description: Die SourceListForceResolution-Methode löscht die zuletzt verwendete Quelleigenschaft.
ms.assetid: 9ecfdf6e-4fed-46fc-8956-85d20cbe5327
title: Patch.SourceListForceResolution-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListForceResolution
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a02e538a1d61fb0adf081542f10dea29f2a636e36b9ce936d7d282e30823339d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065860"
---
# <a name="patchsourcelistforceresolution-method"></a>Patch.SourceListForceResolution-Methode

Die **SourceListForceResolution-Methode** löscht die zuletzt verwendete Quelleigenschaft. Dadurch wird das Installationsprogramm gezwungen, die Quellliste nach einer gültigen Patchquelle zu durchsuchen, wenn die Patchquelle das nächste Mal benötigt wird. Beispielsweise erfordert das Installationsprogramm, dass die Patchquelle eine Installation oder Neuinstallation durchführt, wenn die lokale Cachekopie des Patches fehlt. Diese Methode ruft [**MsiSourceListForceResolution auf.**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)

## <a name="syntax"></a>Syntax


```JScript
Patch.SourceListForceResolution()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm 3.0 oder höher auf Windows Server 2003, Windows XP und Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IPatch ist als 000C10A1-0000-0000-C000-0000000000046 definiert.<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Patch**](patch-object.md)
</dt> <dt>

[**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)
</dt> <dt>

[Nicht unterstützt in Windows Installer 2.0 und früher](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




