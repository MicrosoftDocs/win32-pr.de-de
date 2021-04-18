---
title: Player. uiMode
description: Mit der uiMode-Eigenschaft wird ein Wert angegeben oder abgerufen, der angibt, welche Steuerelemente in der Benutzeroberfläche angezeigt werden.
ms.assetid: 6297d22b-e8ed-4f28-83f6-b74d3265c520
keywords:
- Player. uiMode-Windows-Media Player
topic_type:
- apiref
api_name:
- Player.uiMode
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b1fd2e8e3a2ac6314255cd6ebc350b2ace8cb63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357639"
---
# <a name="playeruimode"></a>Player. uiMode

Mit der **uiMode** -Eigenschaft wird ein Wert angegeben oder abgerufen, der angibt, welche Steuerelemente in der Benutzeroberfläche angezeigt werden.

## <a name="syntax"></a>Syntax

*Player* . **uiMode**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine Lese- **/schreibzeichenfolge**.



| Wert     | BESCHREIBUNG                                                                                                                                                                                                           | Audiobeispiel                                          | Video Beispiel                                          |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|--------------------------------------------------------|
| Unsichtbar | Windows Media Player ist ohne sichtbare Benutzeroberfläche eingebettet (Steuerelemente, Video-oder Visualisierungs Fenster).                                                                                                        | (Nichts wird angezeigt.)                                | (Nichts wird angezeigt.)                                |
| none      | Windows Media Player ist ohne Steuerelemente eingebettet, und nur das Video-oder Visualisierungs Fenster wird angezeigt.                                                                                                         | !["None" mit Audiodaten](images/uimode-none-audio-v11.png) | !["None" mit Video](images/uimode-none-video-v11.png) |
| Minibar      | Windows Media Player ist in das Fenster "Status", "Wiedergabe", "anhalten", "anhalten", "stumm" und "Lautstärke" neben dem Video-oder Visualisierungs Fenster eingebettet                                                          | !["Mini" mit Audiodaten](images/uimode-mini-audio-v11.png) | !["Mini" mit Video](images/uimode-mini-video-v11.png) |
| Voll      | Standard. Windows Media Player ist neben dem Video-oder Visualisierungs Fenster in die Steuerelemente "Status", "suchen", "Wiedergabe", "anhalten", "stumm Schaltung", "weiter", "schnell vorwärts", "schnelles umkehren" und "Handels@@ | !["Full" mit Audiodaten](images/uimode-full-audio-v11.png) | !["Full" mit Video](images/uimode-full-video-v11.png) |
| custom    | Windows Media Player ist mit einer benutzerdefinierten Benutzeroberfläche eingebettet. Kann nur in C++-Programmen verwendet werden.                                                                                                                      | (Benutzerdefinierte Benutzeroberfläche wird angezeigt.)                  | (Benutzerdefinierte Benutzeroberfläche wird angezeigt.)                  |



 

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft gibt die Darstellung der eingebetteten Windows-Media Player an. Wenn **uiMode** auf "None", "Mini" oder "Full" festgelegt ist, ist ein Fenster für die Anzeige von Videoclips und Audiovisualisierungen vorhanden. Dieses Fenster kann im Mini-oder vollständigen Modus ausgeblendet werden, indem das **height** -Attribut des **Object** -Tags auf 40 festgelegt wird. dieses Fenster wird von unten gemessen und lässt den Steuerelement Teil der Benutzeroberfläche sichtbar. Wenn keine eingebettete Schnittstelle gewünscht ist, legen Sie die Attribute " **Width** " und " **height** " auf NULL fest.

Wenn **uiMode** auf "unsichtbar" festgelegt ist, wird keine Benutzeroberfläche angezeigt, aber der Leerraum ist nach wie vor durch **Breite** und **Höhe** angegeben. Dies ist nützlich, um das Seitenlayout beizubehalten, wenn **uiMode** geändert werden kann. Außerdem ist der reservierte Speicherplatz transparent, sodass alle Elemente hinter dem Steuerelement sichtbar sind.

Wenn **uiMode** auf "Full" oder "Mini" festgelegt ist, zeigt Windows Media Player Transport Steuerelemente im Vollbildmodus an. Wenn **uiMode** auf "None" festgelegt ist, werden keine Steuerelemente im Vollbildmodus angezeigt.

Wenn das Fenster sichtbar ist und Audioinhalt wiedergegeben wird, wird die Visualisierung angezeigt, die zuletzt in Windows Media Player verwendet wurde.

Wenn **uiMode** in einem C++-Programm, das **iwmpremotemediaservices** implementiert, auf "Custom" festgelegt ist, wird die von **iwmpremotemediaservices:: getcustomuimode** angezeigte Skin-Datei angezeigt.

Während der Vollbildwiedergabe blendet Windows Media Player den Mauszeiger aus, wenn **enablecontextmenu** den Wert false hat und **uiMode** den Wert "None" hat.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein HTML-SELECT-Element erstellt, das es dem Benutzer ermöglicht, die Benutzeroberfläche für ein eingebettetes **Player** -Objekt zu ändern. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```
<!-- Create an HTML SELECT element. -->
<SELECT  ID = UI  LANGUAGE="JScript"

         /* Specify the UI mode the user selects. */
         onChange = "Player.uiMode = UI.value">

/* These are the four UI mode options. */
<OPTION VALUE="invisible">Invisible
<OPTION VALUE="none">No Controls
<OPTION VALUE="mini">Mini Player
<OPTION VALUE="full">Full Player
</SELECT>

```



Windows Media Player 10 Mobile: Diese Eigenschaft akzeptiert nur die Werte "None" oder "Full" oder gibt Sie zurück. Auf Smartphone-Geräten werden nur Wiedergabe Status und ein Counter angezeigt, wenn *uiMode* auf "Full" festgelegt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher. Windows Media Player 9 oder höher für "unsichtbar" oder "Benutzer definiert".<br/> |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpremotemediaservices-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices)
</dt> <dt>

[**Iwmpremotemediaservices:: getcustomuimode**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getcustomuimode)
</dt> <dt>

[**Player-Objekt**](player-object.md)
</dt> </dl>

 

 





