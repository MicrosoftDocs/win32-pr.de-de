---
description: Die SourceListClearSource-Methode entfernt ein Netzwerk oder eine URL-Quelle. Akzeptiert Type, den Quelltyp und SourcePath, den Quellpfad, als zu entfernende Parameter. Diese Methode ruft msiSourceListClearSource auf.
ms.assetid: a55676d4-795d-4ffe-8621-ef47c16a936c
title: Product.SourceListClearSource-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListClearSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9adeb342aa47162905814979eb29853edd1c5bc660e3771f3beabb8a485c6060
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118376693"
---
# <a name="productsourcelistclearsource-method"></a>Product.SourceListClearSource-Methode

Die **SourceListClearSource-Methode** entfernt ein Netzwerk oder eine URL-Quelle. Akzeptiert *Type*, den Quelltyp und *SourcePath*, den Quellpfad, als zu entfernende Parameter. Diese Methode ruft [**msiSourceListClearSource auf.**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)

## <a name="syntax"></a>Syntax


```JScript
Product.SourceListClearSource(
  Type,
  SourcePath
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Typ* 
</dt> <dd>

Typ der zu entfernenden Quelle: MSISOURCETYPE \_ NETWORK- oder MSISOURCETYPE-URL. \_

</dd> <dt>

*Sourcepath* 
</dt> <dd>

Pfad zur zu entfernenden Quelle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installer 3.0 oder höher auf Windows Server 2003, Windows XP und Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID IProduct ist als \_ 000C10A0-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Produkt**](product-object.md)
</dt> <dt>

[**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)
</dt> <dt>

[Nicht unterstützt in Windows Installer 2.0 und früher](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




