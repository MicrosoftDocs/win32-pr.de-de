---
description: Die sourcelistclearall-Methode das Product-Objekt entfernt alle Quellen für das Produkt. Der Typ der zu entfernenden Quelle kann angegeben werden.
ms.assetid: c8a63b54-7be6-424a-8653-0182b561faab
title: Product. sourcelistclearall-Methode
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
ms.openlocfilehash: 4c921bd45b1acbac40444e4d11bb67d589149c45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357580"
---
# <a name="productsourcelistclearall-method"></a>Product. sourcelistclearall-Methode

Die **sourcelistclearall** -Methode das [**Product**](product-object.md) -Objekt entfernt alle Quellen für das Produkt. Der Typ der zu entfernenden Quelle kann angegeben werden.

## <a name="syntax"></a>Syntax


```JScript
Product.SourceListClearAll(
  Type
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Type* 
</dt> <dd>

Typ der zu entfernenden Quelle: msisourcetype- \_ Medien, msisourcetype- \_ Netzwerk oder msisourcetype- \_ URL.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

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

[**Msisourcelistclearsource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)
</dt> <dt>

[Wird in Windows Installer 2,0 und früher nicht unterstützt.](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




