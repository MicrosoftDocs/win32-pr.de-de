---
title: Player. currentmediaitemavailable-Ereignis
description: Das currentmediaitemavailable-Ereignis tritt auf, wenn ein grafisches Metadatenelement im aktuellen Medien Element verfügbar wird. | Player. currentmediaitemavailable-Ereignis
ms.assetid: dc692b14-67d3-4867-8f99-ddfcf7d1610c
keywords:
- Currentmediaitemavailable-Ereignisfenster Media Player
- Currentmediaitemavailable-Ereignis, Windows Media Player, Player-Klasse
- Windows Media Player Player-Klasse, currentmediaitemavailable-Ereignis
topic_type:
- apiref
api_name:
- Player.CurrentMediaItemAvailable
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7f25d085c354cf18966ec37f822a080db56cf16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368363"
---
# <a name="playercurrentmediaitemavailable-event"></a>Player. currentmediaitemavailable-Ereignis

Das **currentmediaitemavailable** -Ereignis tritt auf, wenn ein grafisches Metadatenelement im aktuellen Medien Element verfügbar wird.

## <a name="syntax"></a>Syntax


```JScript
Player.CurrentMediaItemAvailable(
  bstrItemName
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstritemname* 
</dt> <dd>

**Zeichenfolge** , die den Namen des aktuellen Medien Elements enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Da die Wiedergabe beginnen kann, bevor ein Medien Element vollständig heruntergeladen wird, sind alle im Medien Element enthaltenen metadatengrafiken (z. b. Albumcover Art) möglicherweise nicht verfügbar, wenn die Wiedergabe gestartet wird. Dieses Ereignis warnt Sie, wenn ein metadatengrafieelement den Download abgeschlossen hat. Sie können dann das **Medien** Objekt abrufen, indem Sie den Wert von *bstritemname* an *mediacollection* übergeben. **getByName** -Methode, nach der Sie auf das metadatengrafieelement mithilfe von *Medien* zugreifen können. **getItemInfoByType** und Angeben von **WM/Bild** für den Attributnamen.

Der Wert von Ereignis Parametern wird von Windows Media Player festgelegt, und der Zugriff auf und die Übergabe an eine Methode in einer importierten JScript-Datei mithilfe des angegebenen Parameter namens ist möglich. Dieser Parameter Name muss genau wie gezeigt eingegeben werden, einschließlich der Groß-/Kleinschreibung.

**Windows Media Player 10 Mobile:** Dieses Ereignis wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Medienobjekt**](media-object.md)
</dt> <dt>

[**Media. getItemInfoByType**](media-getiteminfobytype.md)
</dt> <dt>

[**Mediacollection. getByName**](mediacollection-getbyname.md)
</dt> <dt>

[**Player-Objekt**](player-object.md)
</dt> </dl>

 

 





