---
description: Die MediaDisks-Eigenschaft aufzählt alle Mediendatenträger für diese Produktinstanz. Diese Eigenschaft ruft msiSourceListEnumMediaDisks auf. Gibt die Datenträgerinformationen als Array von Record-Objekten zurück.
ms.assetid: 9ea7c9a8-4ff1-4b26-a8d5-c23510650566
title: Product.MediaDisks(Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.MediaDisks
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 00496739c9e51b5a735bf57788cdc47be0c41e177201ef445f58ea3748fb062f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042200"
---
# <a name="productmediadisks-property"></a>Product.MediaDisks(Eigenschaft)

Die **MediaDisks-Eigenschaft** aufzählt alle Mediendatenträger für diese Produktinstanz. Diese Eigenschaft ruft [**msiSourceListEnumMediaDisks auf.**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa) Gibt die Datenträgerinformationen als Array von [**Record-Objekten**](record-object.md) zurück.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Product.MediaDisks
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Hinweise

In jedem Datensatz enthält das erste Feld die Datenträger-ID, das zweite Feld enthält die Volumebezeichnung und das dritte Feld die Datenträgeraufforderung, die für den Datenträger registriert ist.

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

[**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)
</dt> <dt>

[Nicht unterstützt in Windows Installer 2.0 und früher](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




