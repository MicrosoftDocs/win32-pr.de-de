---
title: Downloadcollection. RemoveItem-Methode
description: In diesem Abschnitt werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt. Mit der RemoveItem-Methode wird ein Download Element aus einer Download Sammlung entfernt.
ms.assetid: 0008752e-c81a-4f91-a582-9d6b46569479
keywords:
- RemoveItem-Methode, Windows-Media Player
- RemoveItem-Methode, Windows Media Player, downloadcollection-Klasse
- Download Collection-Klasse, Windows Media Player, RemoveItem-Methode
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
ms.openlocfilehash: a1798665b79327b7956c1b78509b55cc6e6dd70c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370843"
---
# <a name="downloadcollectionremoveitem-method"></a>Downloadcollection. RemoveItem-Methode

> [!Note]  
> In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Mit der **RemoveItem** -Methode wird ein Download Element aus einer Download Sammlung entfernt.

## <a name="syntax"></a>Syntax


```JScript
DownloadCollection.removeItem(
  itemID
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ItemID* \[ in\]
</dt> <dd>

**Number** (**Long**), der den Index des zu entfernenden **Download** Elements angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn der von der *ItemID* dargestellte Download ausgeführt wird, wird der Download durch diese Methode abgebrochen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Download Collection. Item**](downloadcollection-item.md)
</dt> <dt>

[**Download Collection-Objekt**](downloadcollection-object.md)
</dt> </dl>

 

 





