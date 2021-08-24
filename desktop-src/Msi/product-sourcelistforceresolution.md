---
description: Die SourceListForceResolution-Methode entfernt die LastUsedSource-Eigenschaft.
ms.assetid: 554bc321-51d8-4595-b79c-7975bad8c555
title: Product.SourceListForceResolution-Methode
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
ms.openlocfilehash: 3215f5b43200cb8ca43fba36dc71e1a582aa24b92904e2c48268245921a2ccf1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754010"
---
# <a name="productsourcelistforceresolution-method"></a>Product.SourceListForceResolution-Methode

Die **SourceListForceResolution-Methode** entfernt die LastUsedSource-Eigenschaft. Dies zwingt das Installationsprogramm, die Quellliste nach einer gültigen Produktquelle zu durchsuchen, wenn das nächste Mal eine Quelle erforderlich ist, z. B. wenn das Installationsprogramm eine Installation oder Neuinstallation ausführt oder wenn der Pfad erforderlich ist, damit eine Komponente aus der Quelle ausgeführt werden kann.

Diese Methode ruft [**MsiSourceListForceResolution auf.**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)

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
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installer 3.0 oder höher auf Windows Server 2003, Windows XP und Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID IProduct ist als \_ 000C10A0-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Produkt**](product-object.md)
</dt> <dt>

[**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)
</dt> <dt>

[Nicht unterstützt in Windows Installer 2.0 und früher](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




