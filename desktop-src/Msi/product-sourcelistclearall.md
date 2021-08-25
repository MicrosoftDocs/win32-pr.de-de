---
description: Mit der SourceListClearAll-Methode entfernt das Product-Objekt alle Quellen für das Produkt. Der Typ der zu entfernenden Quelle kann angegeben werden.
ms.assetid: c8a63b54-7be6-424a-8653-0182b561faab
title: Product.SourceListClearAll-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListClearAll
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8718522de7395a4fc6811e210fac0ee7b9f7758f6ea4b632f9fec122ffd5be3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119925878"
---
# <a name="productsourcelistclearall-method"></a>Product.SourceListClearAll-Methode

Mit **der SourceListClearAll-Methode** entfernt das [**Product-Objekt**](product-object.md) alle Quellen für das Produkt. Der Typ der zu entfernenden Quelle kann angegeben werden.

## <a name="syntax"></a>Syntax


```JScript
Product.SourceListClearAll(
  Type
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Typ* 
</dt> <dd>

Typ der zu entfernenden Quelle: MSISOURCETYPE \_ MEDIA, MSISOURCETYPE \_ NETWORK oder MSISOURCETYPE \_ URL.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm 3.0 oder höher auf Windows Server 2003, Windows XP und Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IProduct ist als 000C10A0-0000-0000-C000-000000000046 definiert.<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Produkt**](product-object.md)
</dt> <dt>

[**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)
</dt> <dt>

[Nicht unterstützt in Windows Installer 2.0 und früher](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




