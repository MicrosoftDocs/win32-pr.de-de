---
description: Die State-Eigenschaft gibt den Installationsstatus dieser Instanz des Produkts zurück.
ms.assetid: ae4c7a43-d4af-4e06-a3f8-d7c2d0715d84
title: Product. State (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.State
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 64d2f5d39a516fc4a0c00b8e18c159e1f2496e22
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368657"
---
# <a name="productstate-property"></a>Product. State (Eigenschaft)

Die **State** -Eigenschaft gibt den Installationsstatus dieser Instanz des Produkts zurück.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Product.State
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft gibt einen der folgenden Werte zurück.



| Installationsstatus       | Bedeutung                                |
|--------------------------|----------------------------------------|
| InstallState ( \_ Standard)    | Die lokal installierte Instanz des Produkts. |
| InstallState \_ angekündigt | Die Instanz des angekündigten Produkts.        |
| InstallState \_ unbekannt    | Unbekannte Produkt Instanz.           |



 

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

[Wird in Windows Installer 2,0 und früher nicht unterstützt.](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




