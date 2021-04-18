---
description: Die sourcelistforceresolution-Methode löscht die zuletzt verwendete Source-Eigenschaft.
ms.assetid: 9ecfdf6e-4fed-46fc-8956-85d20cbe5327
title: Patch. sourcelistforceresolution-Methode
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
ms.openlocfilehash: f9a44d08c05b4ece24cf3c8c8d3be42e210aec32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364855"
---
# <a name="patchsourcelistforceresolution-method"></a>Patch. sourcelistforceresolution-Methode

Die **sourcelistforceresolution** -Methode löscht die zuletzt verwendete Source-Eigenschaft. Dadurch wird das Installationsprogramm gezwungen, die Quell Liste nach einer gültigen patchquelle zu durchsuchen, wenn die patchquelle das nächste Mal benötigt wird. Das Installationsprogramm erfordert beispielsweise, dass die patchquelle eine Installation oder Neuinstallation ausführt, wenn die lokale Cache Kopie des Patches fehlt. Diese Methode ruft [**msisourcelistforceresolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)auf.

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
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer 3,0 oder höher unter Windows Server 2003, Windows XP und Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ iPatch ist definiert als 000c10a1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Patch**](patch-object.md)
</dt> <dt>

[**Msisourcelistforceresolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)
</dt> <dt>

[Wird in Windows Installer 2,0 und früher nicht unterstützt.](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




