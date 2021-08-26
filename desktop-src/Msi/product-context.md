---
description: Die Context-Eigenschaft gibt den Kontext dieses Produkts zurück.
ms.assetid: aa772a95-eb4e-45af-9788-9833d62139e8
title: Product.Context-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.Context
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 21fb23a595b1f479f2468f0006cca7cd9218de03fc2cc76b794caae79ea45a24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129120"
---
# <a name="productcontext-property"></a>Product.Context-Eigenschaft

Die **Context-Eigenschaft** gibt den Kontext dieses Produkts zurück.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Product.Context
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Hinweise

Diese Eigenschaft kann einen der folgenden Werte zurückgeben.



| Kontext                        | Wert | Bedeutung                           |
|--------------------------------|-------|-----------------------------------|
| MSIINSTALLCONTEXT \_ USERMANAGED | 1     | Produkte im verwalteten Kontext.   |
| MSIINSTALLCONTEXT-BENUTZER \_        | 2     | Produkte im nicht verwalteten Kontext. |
| MSIINSTALLCONTEXT-COMPUTER \_     | 4     | Produkte im Computerkontext.   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installer 3.0 oder höher auf Windows Server 2003, Windows XP und Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID IProduct ist als \_ 000C10A0-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Produkt**](product-object.md)
</dt> <dt>

[Nicht unterstützt in Windows Installer 2.0 und früher](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




