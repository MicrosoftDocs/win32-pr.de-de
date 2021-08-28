---
description: Die State-Eigenschaft gibt den Installationsstatus dieser Instanz des Produkts zurück.
ms.assetid: ae4c7a43-d4af-4e06-a3f8-d7c2d0715d84
title: Product.State-Eigenschaft
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
ms.openlocfilehash: befa632feae7b4c57983f13a28e695051842cb5d1a2ff0908e6ffd011c6e4918
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753950"
---
# <a name="productstate-property"></a>Product.State-Eigenschaft

Die **State-Eigenschaft** gibt den Installationsstatus dieser Instanz des Produkts zurück.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Product.State
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Hinweise

Diese Eigenschaft gibt einen der folgenden Werte zurück.



| Installationsstatus       | Bedeutung                                |
|--------------------------|----------------------------------------|
| INSTALLSTATE \_ DEFAULT    | Lokal installierte Instanz des Produkts. |
| INSTALLSTATE \_ ANGEKÜNDIGT | Die Instanz des angekündigten Produkts.        |
| INSTALLSTATE \_ UNKNOWN    | Die Instanz des Produkts ist unbekannt.           |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm 3.0 oder höher auf Windows Server 2003, Windows XP und Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IProduct ist als 000C10A0-0000-0000-C000-000000000046 definiert.<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Produkt**](product-object.md)
</dt> <dt>

[Nicht unterstützt in Windows Installer 2.0 und früher](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




