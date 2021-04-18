---
title: Downloadcollection. Item-Methode
description: In diesem Abschnitt werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt. Die Item-Methode ruft ein ausstehendes Download Objekt ab.
ms.assetid: a79db9db-e80c-48db-aee6-9bd8f77a7dff
keywords:
- Element-Methoden Fenster Media Player
- Element-Methode, Windows Media Player, downloadcollection-Klasse
- Download Collection-Klasse, Windows Media Player, Element-Methode
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
ms.openlocfilehash: d57db60a776c71d9ff16eceb1584c79a125bbf46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354721"
---
# <a name="downloadcollectionitem-method"></a>Downloadcollection. Item-Methode

> [!Note]  
> In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Die **Item** -Methode ruft ein ausstehendes Download Objekt ab.

## <a name="syntax"></a>Syntax


```JScript
retVal = DownloadCollection.item(
  itemId
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ItemID* \[ in\]
</dt> <dd>

**Zahl** (**Long**), die den Index des abzurufenden **Download** Elements angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein-Objekt vom Typ " **Downloader** " zurück.

## <a name="remarks"></a>Bemerkungen

Der *ItemID* -Wert ist NULL basiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Download Collection-Objekt**](downloadcollection-object.md)
</dt> <dt>

[**Download Item-Objekt**](downloaditem-object.md)
</dt> </dl>

 

 





