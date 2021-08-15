---
title: Player.uiMode
description: Die uiMode-Eigenschaft gibt einen Wert an, der angibt, welche Steuerelemente auf der Benutzeroberfläche angezeigt werden, oder ruft einen Wert ab.
ms.assetid: 6297d22b-e8ed-4f28-83f6-b74d3265c520
keywords:
- Player.uiMode Windows Media Player
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
ms.openlocfilehash: f082da34ffc3b77869e84ceb576b4e6273ccaff15a5f95e66d98cae93697c251
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118835337"
---
# <a name="playeruimode"></a>Player.uiMode

Die **uiMode-Eigenschaft** gibt einen Wert an, der angibt, welche Steuerelemente auf der Benutzeroberfläche angezeigt werden, oder ruft einen Wert ab.

## <a name="syntax"></a>Syntax

*Player* . **uiMode**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine **Zeichenfolge** mit Lese-/Schreibzugriff.



| Wert     | BESCHREIBUNG                                                                                                                                                                                                           | Audiobeispiel                                          | Videobeispiel                                          |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|--------------------------------------------------------|
| Unsichtbar | Windows Media Player wird ohne sichtbare Benutzeroberfläche (Steuerelemente, Video oder Visualisierungsfenster) eingebettet.                                                                                                        | (Es wird nichts angezeigt.)                                | (Es wird nichts angezeigt.)                                |
| Keine      | Windows Media Player wird ohne Steuerelemente eingebettet, und nur das Video- oder Visualisierungsfenster wird angezeigt.                                                                                                         | !["none" mit Audio](images/uimode-none-audio-v11.png) | !["none" mit Video](images/uimode-none-video-v11.png) |
| Mini      | Windows Media Player wird in die Steuerelemente Statusfenster, Wiedergabe/Pause, Beenden, Stummschalten und Lautstärke eingebettet, die zusätzlich zum Video- oder Visualisierungsfenster angezeigt werden.                                                          | !["mini" mit Audio](images/uimode-mini-audio-v11.png) | !["mini" mit Video](images/uimode-mini-video-v11.png) |
| Voll      | Standard. Windows Media Player ist zusätzlich zum Video- oder Visualisierungsfenster in das Statusfenster, suchleisten-, wiedergabe-/pausen-, stop-, mute-, next-, previous-, fast forward-, fast reverse- und volume-Steuerelemente eingebettet. | !["vollständig" mit Audio](images/uimode-full-audio-v11.png) | !["vollständig" mit Video](images/uimode-full-video-v11.png) |
| custom    | Windows Media Player ist mit einer benutzerdefinierten Benutzeroberfläche eingebettet. Kann nur in C++-Programmen verwendet werden.                                                                                                                      | (Benutzerdefinierte Benutzeroberfläche wird angezeigt.)                  | (Benutzerdefinierte Benutzeroberfläche wird angezeigt.)                  |



 

## <a name="remarks"></a>Hinweise

Diese Eigenschaft gibt die Darstellung des eingebetteten Windows Media Player an. Wenn **uiMode** auf "none", "mini" oder "full" festgelegt ist, ist ein Fenster für die Anzeige von Videoclips und Audiovisualisierungen vorhanden. Dieses Fenster kann im Mini- oder Vollmodus ausgeblendet werden, indem das **Height-Attribut** des **OBJECT-Tags** auf 40 festgelegt wird, das von unten gemessen wird, und lässt den Steuerelementteil der Benutzeroberfläche sichtbar. Wenn keine eingebettete Schnittstelle gewünscht wird, legen Sie sowohl das **Breiten-** als auch das **Höhenattribute** auf 0 (null) fest.

Wenn **uiMode** auf "invisible" festgelegt ist, wird keine Benutzeroberfläche angezeigt, aber der Platz auf der Seite ist weiterhin reserviert, wie durch **Breite** und **Höhe** angegeben. Dies ist nützlich, um das Seitenlayout beizubehalten, wenn **uiMode** geändert werden kann. Darüber hinaus ist der reservierte Speicherplatz transparent, sodass alle Elemente, die sich hinter dem Steuerelement befinden, sichtbar sind.

Wenn **uiMode** auf "full" oder "mini" festgelegt ist, zeigt Windows Media Player Transportsteuerelemente im Vollbildmodus an. Wenn **uiMode** auf "none" festgelegt ist, werden keine Steuerelemente im Vollbildmodus angezeigt.

Wenn das Fenster sichtbar ist und Audioinhalte wiedergegeben werden, wird die Visualisierung angezeigt, die zuletzt in Windows Media Player verwendet wurde.

Wenn **uiMode** in einem C++-Programm, das **IWMPRemoteMediaServices** implementiert, auf "custom" festgelegt ist, wird die von **IWMPRemoteMediaServices::GetCustomUIMode** angegebene Skindatei angezeigt.

Während der Vollbildwiedergabe blendet Windows Media Player den Mauszeiger aus, wenn **enableContextMenu** gleich false und **uiMode** gleich "none" ist.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein SELECT-HTML-Element erstellt, mit dem der Benutzer die Benutzeroberfläche für ein eingebettetes **Player-Objekt** ändern kann. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


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



Windows Media Player 10 Mobile: Diese Eigenschaft akzeptiert oder gibt nur Werte von "none" oder "full" zurück. Auf Smartphonegeräten werden nur der Wiedergabestatus und ein Zähler angezeigt, wenn *uiMode* auf "full" festgelegt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher. Windows Media Player Serie 9 oder höher für "unsichtbar" oder "benutzerdefiniert".<br/> |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                        |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMPRemoteMediaServices-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices)
</dt> <dt>

[**IWMPRemoteMediaServices::GetCustomUIMode**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getcustomuimode)
</dt> <dt>

[**Player-Objekt**](player-object.md)
</dt> </dl>

 

 





