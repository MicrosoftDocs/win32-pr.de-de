---
title: DownloadCollection.item-Methode
description: Hinweis In diesem Abschnitt werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt. Die Item-Methode ruft ein ausstehendes Downloadobjekt ab.
ms.assetid: a79db9db-e80c-48db-aee6-9bd8f77a7dff
keywords:
- item-Methode Windows Media Player
- item-Methode Windows Media Player , DownloadCollection-Klasse
- DownloadCollection-Klasse Windows Media Player , Item-Methode
topic_type:
- apiref
api_name:
- DownloadCollection.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a82a903236038c2f0372786137eec48ad5c5f502d7fd614eb8944f3f4684aea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997039"
---
# <a name="downloadcollectionitem-method"></a>DownloadCollection.item-Methode

> [!Note]  
> In diesem Abschnitt werden funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Die **Item-Methode** ruft ein ausstehendes Downloadobjekt ab.

## <a name="syntax"></a>Syntax


```JScript
retVal = DownloadCollection.item(
  itemId
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*itemId* \[ In\]
</dt> <dd>

**Number** (**long**), die den Index des abzurufenden **DownloadItem** angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein **DownloadItem-Objekt** zurück.

## <a name="remarks"></a>Hinweise

Der *itemID-Wert* ist nullbasiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9er Serie oder höher<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DownloadCollection-Objekt**](downloadcollection-object.md)
</dt> <dt>

[**DownloadItem-Objekt**](downloaditem-object.md)
</dt> </dl>

 

 





