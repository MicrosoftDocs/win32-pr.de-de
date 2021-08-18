---
title: DownloadCollection.removeItem-Methode
description: Hinweis In diesem Abschnitt werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt. Die removeItem-Methode entfernt ein Downloadelement aus einer Downloadsammlung.
ms.assetid: 0008752e-c81a-4f91-a582-9d6b46569479
keywords:
- removeItem-Windows Media Player
- removeItem-Methode Windows Media Player , DownloadCollection-Klasse
- DownloadCollection-Klasse Windows Media Player , removeItem-Methode
topic_type:
- apiref
api_name:
- DownloadCollection.removeItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1d7eaa7b26a4d64070cae426d1bbc23418593fa8ec5472e870ed7529ce8a122
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997070"
---
# <a name="downloadcollectionremoveitem-method"></a>DownloadCollection.removeItem-Methode

> [!Note]  
> In diesem Abschnitt werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Die **removeItem-Methode** entfernt ein Downloadelement aus einer Downloadsammlung.

## <a name="syntax"></a>Syntax


```JScript
DownloadCollection.removeItem(
  itemID
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*itemID* \[ In\]
</dt> <dd>

**Number** (**long**) gibt den Index des **zu entfernenden DownloadItem** an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Wenn der durch *itemID dargestellte* Download in Bearbeitung ist, bricht diese Methode den Download ab.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DownloadCollection.item**](downloadcollection-item.md)
</dt> <dt>

[**DownloadCollection-Objekt**](downloadcollection-object.md)
</dt> </dl>

 

 





