---
description: Die sourcelistforceresolution-Methode löscht die "LastUsedSource"-Eigenschaft.
ms.assetid: 554bc321-51d8-4595-b79c-7975bad8c555
title: Product. sourcelistforceresolution-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListForceResolution
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 668a74d2327dad918f1f2389bc163dcfde198c2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372174"
---
# <a name="productsourcelistforceresolution-method"></a>Product. sourcelistforceresolution-Methode

Die **sourcelistforceresolution** -Methode löscht die "LastUsedSource"-Eigenschaft. Dadurch wird das Installationsprogramm gezwungen, die Quell Liste nach einer gültigen Produkt Quelle zu durchsuchen, wenn eine Quelle das nächste Mal benötigt wird, z. b. wenn das Installationsprogramm eine Installation oder eine Neuinstallation ausführt oder wenn der Pfad erforderlich ist, damit eine Komponente von der Quelle ausgeführt werden kann.

Diese Methode ruft [**msisourcelistforceresolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)auf.

## <a name="syntax"></a>Syntax


```JScript
Product.SourceListForceResolution()
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
| IID<br/>     | IID \_ iproduct ist definiert als 000c10a0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Product**](product-object.md)
</dt> <dt>

[**Msisourcelistforceresolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)
</dt> <dt>

[Wird in Windows Installer 2,0 und früher nicht unterstützt.](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




