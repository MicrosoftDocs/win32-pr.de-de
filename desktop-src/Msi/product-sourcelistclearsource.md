---
description: Die sourcelistclearsource-Methode entfernt eine Netzwerk-oder URL-Quelle. Akzeptiert Typ, den Quelltyp und SourcePath, den Quellpfad, als Parameter, die entfernt werden sollen. Diese Methode ruft das msisourcelistclearsource-Element auf.
ms.assetid: a55676d4-795d-4ffe-8621-ef47c16a936c
title: Product. sourcelistclearsource-Methode
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
ms.openlocfilehash: 4988d0ba9003e087b6aeac58ae5587727067e01c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358293"
---
# <a name="productsourcelistclearsource-method"></a>Product. sourcelistclearsource-Methode

Die **sourcelistclearsource** -Methode entfernt eine Netzwerk-oder URL-Quelle. Akzeptiert *Typ*, den Quelltyp und *SourcePath*, den Quellpfad, als Parameter, die entfernt werden sollen. Diese Methode ruft das [**msisourcelistclearsource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)-Element auf.

## <a name="syntax"></a>Syntax


```JScript
Product.SourceListClearSource(
  Type,
  SourcePath
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Type* 
</dt> <dd>

Typ der zu entfernenden Quelle: msisourcetype \_ Network oder msisourcetype \_ URL.

</dd> <dt>

*SourcePath* 
</dt> <dd>

Der Pfad zur Quelle, die entfernt werden soll.

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

 

 




