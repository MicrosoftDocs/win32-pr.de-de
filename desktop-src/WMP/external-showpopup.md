---
title: Extern. ShowPopup-Methode
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. | Extern. ShowPopup-Methode
ms.assetid: 17958543-dbed-45a5-9b02-4800a07cb820
keywords:
- Windows-Media Player der ShowPopup-Methode
- ShowPopup-Methode, Windows Media Player, externe Klasse
- Externe Klasse, Windows Media Player, ShowPopup-Methode
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
ms.openlocfilehash: acaecb559e7df60067e89ec754ec9432233500f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364619"
---
# <a name="externalshowpopup-method"></a>Extern. ShowPopup-Methode

> [!Note]  
> In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Die **ShowPopup** -Methode weist Windows Media Player an, eine Popup Webseite anzuzeigen. Das heißt, eine Webseite, die in einem separaten Fenster angezeigt wird.

## <a name="syntax"></a>Syntax


```JScript
External.showPopup(
  PopupIndex,
  Parameters
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Popupindex* \[ in\]
</dt> <dd>

**Number** (**Long**), der den Index der Popup Webseite angibt.

</dd> <dt>

*Parameter* \[ in\]
</dt> <dd>

Die **Zeichenfolge** , die von Windows Media Player an die URL der Webseite angefügt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Der Popup Index wird nicht von Windows Media Player interpretiert. Indizes, die Popup Webseiten identifizieren, werden vom Online Shop erstellt und sind nur im Online Store gemeint.

Die folgenden Schritte zeigen, wie Windows Media Player die Parameter der **ShowPopup** -Methode verwendet, um eine URL für das Popup Fenster zu erstellen.

1.  Skript auf einer Discovery-Seite ruft **ShowPopup** auf und übergibt eine Ganzzahl in *popupindex* und eine Zeichenfolge in *Parametern*.

2.  Windows Media Player übergibt den Index an [iwmpcontentpartner:: getiteminfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) , um die URL der Webseite abzurufen, die angezeigt werden soll.

3.  Windows Media Player fügt *Parameter* als Abfrage Zeichenfolge an die URL an. Wenn **getiteminfo** z. b. " https://www.Proseware.com/Pages/Popup1.htm " zurückgibt und *Parameter* gleich "dlgx = 800&dlgy = 400&Gruß = Hi", erstellt Windows Media Player die folgende URL:

    https://www.Proseware.com/Pages/Popup1.htm?DlgX=800&DlgY=400&Greeting=Hi

Sie können *Parameter* verwenden, um die Größe des Popup Fensters anzugeben. Wenn Sie z. b. *Parameter* auf "dlgx = 800&dlgy = 400" festlegen, hat das Popup Fenster eine Größe von 800 Pixel um 400 Pixel.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Externes Objekt für den Typ 1-Online Speicher**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





