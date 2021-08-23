---
title: External.showPopup-Methode
description: Hinweis In diesem Thema werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. | External.showPopup-Methode
ms.assetid: 17958543-dbed-45a5-9b02-4800a07cb820
keywords:
- showPopup-Windows Media Player
- showPopup-Methode Windows Media Player , Externe Klasse
- Externe Klasse Windows Media Player , showPopup-Methode
topic_type:
- apiref
api_name:
- External.showPopup
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a651add93e32c1c2eb82827a4089a338341f2506ba26d9fbb06061aa6d185d75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648340"
---
# <a name="externalshowpopup-method"></a>External.showPopup-Methode

> [!Note]  
> In diesem Thema werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Die **showPopup-Methode** weist Windows Media Player, eine Popupwebseite anzuzeigen. das heißt, eine Webseite, die in einem separaten Fenster angezeigt wird.

## <a name="syntax"></a>Syntax


```JScript
External.showPopup(
  PopupIndex,
  Parameters
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PopupIndex* \[ In\]
</dt> <dd>

**Number** (**long**), die den Index der Popupwebseite angibt.

</dd> <dt>

*Parameter* \[ In\]
</dt> <dd>

**Eine** Zeichenfolge Windows Media Player an die URL der Webseite angefügt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Der Popupindex wird von der -Windows Media Player. Indizes, die Popupwebseiten identifizieren, werden vom Onlineshop erstellt und haben nur eine Bedeutung für den Onlineshop.

Die folgenden Schritte zeigen, Windows Media Player die Parameter der **showPopup-Methode** verwendet, um eine URL für das Popupfenster zu erstellen.

1.  Das Skript auf einer Ermittlungsseite ruft **showPopup** auf und übergibt eine ganze Zahl in *PopupIndex* und eine Zeichenfolge in *Parameter*.

2.  Windows Media Player den Index an [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) weiter, um die URL der anzuzeigenden Webseite abzurufen.

3.  Windows Media Player parameter an *die* URL als Abfragezeichenfolge an. Wenn **GetItemInfo** beispielsweise "" zurückgibt und Parameter gleich https://www.Proseware.com/Pages/Popup1.htm "DlgX=800&DlgY=400&Greeting=Hi" ist, erstellt Windows Media Player die folgende URL: 

    https://www.Proseware.com/Pages/Popup1.htm?DlgX=800&DlgY=400&Greeting=Hi

Sie können Parameter *verwenden,* um die Größe des Popupfensters anzugeben. Wenn Sie parameter  beispielsweise auf "DlgX=800&DlgY=400" festlegen, hat das Popupfenster eine Größe von 800 x 400 Pixel.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Externes Objekt für Onlinespeicher vom Typ 1**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





