---
description: Die Media Disks-Eigenschaft listet alle Medien Datenträger für diese Produkt Instanz auf. Diese Eigenschaft ruft msisourcelistenumschlag mediadisks auf. Gibt die Datenträger Informationen als Array von Datensatz-Objekten zurück.
ms.assetid: 9ea7c9a8-4ff1-4b26-a8d5-c23510650566
title: Product. mediadisks (Eigenschaft)
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
ms.openlocfilehash: e07af832837aaeb77759816c08cf68d04e14c255
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360342"
---
# <a name="productmediadisks-property"></a>Product. mediadisks (Eigenschaft)

Die Media **Disks** -Eigenschaft listet alle Medien Datenträger für diese Produkt Instanz auf. Diese Eigenschaft ruft [**msisourcelistenumschlag mediadisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)auf. Gibt die Datenträger Informationen als Array von [**Datensatz**](record-object.md) -Objekten zurück.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Product.MediaDisks
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Bemerkungen

In jedem Datensatz enthält das erste Feld die Datenträger-ID, das zweite Feld enthält die Volumebezeichnung, und das dritte Feld enthält die für den Datenträger registrierte Datenträger Aufforderung.

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

[**Msisourcelistenumschlag mediadisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)
</dt> <dt>

[Wird in Windows Installer 2,0 und früher nicht unterstützt.](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




