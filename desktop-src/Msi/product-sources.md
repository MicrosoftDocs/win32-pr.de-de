---
description: Die Sources-Eigenschaft listet alle Quellen für die Produkt Instanz auf.
ms.assetid: 26602099-d0e0-4269-91d9-82943859811a
title: Product. Sources (Eigenschaft)
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
ms.openlocfilehash: a82363f6a61ebb9c441dfcfeeeafe3760e63c462
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371660"
---
# <a name="productsources-property"></a>Product. Sources (Eigenschaft)

Die **Sources** -Eigenschaft listet alle Quellen für die Produkt Instanz auf. Diese Eigenschaft ruft " [**msisourcelistenumschlag sources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa) " auf und gibt das Array von Zeichen folgen zurück. der Quelltyp wird als Argument akzeptiert. Der Quelltyp kann das msisourcetype- \_ Netzwerk oder die msisourcetype- \_ URL sein.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Product.Sources
```



## <a name="property-value"></a>Eigenschaftswert

Der Typ der aufzuzählenden Quelle. Der Wert kann *msiinstallsourcetymessetwork* (1) oder *msiinstallsourcetypeurl* (2) sein.

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

[**Msisourcelistenumschlag Quellen**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa)
</dt> <dt>

[Wird in Windows Installer 2,0 und früher nicht unterstützt.](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




