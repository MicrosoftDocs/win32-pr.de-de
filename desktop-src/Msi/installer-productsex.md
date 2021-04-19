---
description: Gibt ein RecordList-Objekt zurück, das die Liste der Produkte auflistet.
ms.assetid: 30735b9f-091b-4915-9b07-9688c9be2d26
title: Installer. productsex (Eigenschaft)
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
ms.openlocfilehash: 17d5e8290ab61b85fa8269f8b23f3cdabd30e012
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354221"
---
# <a name="installerproductsex-property"></a>Installer. productsex (Eigenschaft)

Die **productsex** -Eigenschaft gibt ein [**RecordList**](recordlist-object.md) -Objekt zurück, das die Liste der Produkte auflistet. Diese Eigenschaft ruft " [**msienumschlag productsex**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)" auf.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.ProductsEx
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer 3,0 oder höher unter Windows Server 2003 oder Windows XP.<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Installationsprogramm**](installer-object.md)
</dt> <dt>

[**Msienumschlag**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[**Produkt**](product-object.md)
</dt> <dt>

[Wird in Windows Installer 2,0 und früher nicht unterstützt.](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




