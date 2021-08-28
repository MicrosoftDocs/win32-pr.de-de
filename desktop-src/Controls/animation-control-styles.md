---
title: Animationssteuerstile (CommCtrl.h)
description: In diesem Abschnitt werden die Fensterstile aufgeführt, die mit Animationssteuerelementen verwendet werden.
ms.assetid: ad4fc4fd-166d-4871-9f60-5133a48681aa
topic_type:
- apiref
api_name:
- ACS_AUTOPLAY
- ACS_CENTER
- ACS_TIMER
- ACS_TRANSPARENT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aff6116433533bdc79535be0e282cb81baa9368f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470622"
---
# <a name="animation-control-styles"></a>Animationssteuerstile

In diesem Abschnitt werden die Fensterstile aufgeführt, die mit Animationssteuerelementen verwendet werden.




| Konstante | BESCHREIBUNG | 
|----------|-------------|
| <span id="ACS_AUTOPLAY"></span><span id="acs_autoplay"></span><dl><dt><strong>ACS_AUTOPLAY</strong></dt></dl> | Startet die Wiedergabe der Animation, sobald der AVI-Clip geöffnet ist. <br /> | 
| <span id="ACS_CENTER"></span><span id="acs_center"></span><dl><dt><strong>ACS_CENTER</strong></dt></dl> | Centert die Animation im Fenster des Animationssteuer steuerelements. <br /> | 
| <span id="ACS_TIMER"></span><span id="acs_timer"></span><dl><dt><strong>ACS_TIMER</strong></dt></dl> | Standardmäßig erstellt das -Steuerelement einen Thread zum Wiedereinspielen des AVI-Clips. Wenn Sie dieses Flag festlegen, gibt das Steuerelement den Clip wieder, ohne einen Thread zu erstellen. Intern verwendet das Steuerelement einen Win32-Timer, um die Wiedergabe zu synchronisieren. <br /><strong>Comctl32.dll Version 6 und höher:</strong> Dieser Stil wird nicht unterstützt. Standardmäßig gibt das Steuerelement den AVI-Clip wieder, ohne einen Thread zu erstellen.<br /><blockquote>[!Note]<br />Comctl32.dll Version 6 ist nicht verteilbar. Um Version Comctl32.dll 6 zu verwenden, geben Sie sie in einem Manifest an. Weitere Informationen zu Manifesten finden Sie unter <a href="cookbook-overview.md">Aktivieren von visuellen Stilen.</a></blockquote><br /> | 
| <span id="ACS_TRANSPARENT"></span><span id="acs_transparent"></span><dl><dt><strong>ACS_TRANSPARENT</strong></dt></dl> | Ermöglicht es Ihnen, die Hintergrundfarbe einer Animation mit der des zugrunde liegenden Fensters zu übereinstimmen, wodurch ein "transparenter" Hintergrund erstellt wird. Das übergeordnete Element des Animationssteuer elements darf nicht über den WS_CLIPCHILDREN verfügen (siehe <a href="/windows/desktop/winmsg/window-styles">Fensterstile</a>). Das Steuerelement sendet eine <a href="wm-ctlcolorstatic.md"><strong>WM_CTLCOLORSTATIC</strong></a> nachricht an das übergeordnete Element. Verwenden <a href="/windows/desktop/api/wingdi/nf-wingdi-setbkcolor"><strong>Sie SetBkColor,</strong></a> um die Hintergrundfarbe für den Gerätekontext auf einen entsprechenden Wert zu setzen. Das Steuerelement interpretiert das obere linke Pixel des ersten Frames als Standardhintergrundfarbe der Animation. Alle Pixel mit dieser Farbe werden dem Wert neu zugeführt, den Sie als Reaktion auf die WM_CTLCOLORSTATIC. <br /> | 




## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



