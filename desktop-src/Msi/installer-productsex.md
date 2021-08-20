---
description: Gibt ein RecordList-Objekt zurück, das die Liste der Produkte auflistet.
ms.assetid: 30735b9f-091b-4915-9b07-9688c9be2d26
title: Installer.ProductsEx (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductsEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9320ef38fefd32c60b7022923add5ca55d609d82ff01b8654104bb35b1dbf6be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074930"
---
# <a name="installerproductsex-property"></a>Installer.ProductsEx (Eigenschaft)

Die **ProductsEx-Eigenschaft** gibt ein [**RecordList-Objekt**](recordlist-object.md) zurück, das die Liste der Produkte auflistet. Diese Eigenschaft ruft [**MsiEnumProductsEx auf.**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.ProductsEx
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installer 3.0 oder höher auf Windows Server 2003 oder Windows XP.<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Installer**](installer-object.md)
</dt> <dt>

[**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[**Produkt**](product-object.md)
</dt> <dt>

[Nicht unterstützt in Windows Installer 2.0 und früher](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




