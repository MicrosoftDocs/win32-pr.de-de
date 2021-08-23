---
description: Die Sources-Eigenschaft enumeriert alle Quellen für die Produktinstanz.
ms.assetid: 26602099-d0e0-4269-91d9-82943859811a
title: Product.Sources-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.Sources
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: c54b9563898b093af324b02ca6a5bf48fbddf62b31c22a3d492c1132c46f13f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753920"
---
# <a name="productsources-property"></a>Product.Sources-Eigenschaft

Die **Sources-Eigenschaft** enumeriert alle Quellen für die Produktinstanz. Diese Eigenschaft ruft [**MsiSourceListEnumSources auf**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa) und gibt das Array von Zeichenfolgen zurück und akzeptiert den Quelltyp als Argument. Der Quelltyp kann MSISOURCETYPE \_ NETWORK oder MSISOURCETYPE \_ URL sein.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Product.Sources
```



## <a name="property-value"></a>Eigenschaftswert

Der Typ der zu aufzählenden Quelle. Der Wert kann *msiInstallSourceTypeNetwork* (1) oder *msiInstallSourceTypeURL* (2) sein.

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

[**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa)
</dt> <dt>

[Nicht unterstützt in Windows Installer 2.0 und früher](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




