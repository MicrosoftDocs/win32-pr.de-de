---
title: Funktionen (Vergrößerungs-API)
description: Dieser Abschnitt enthält Referenzinformationen zu den Funktionen der Vergrößerungs-API.
ms.assetid: 82b7d82b-b8cd-4f80-ad30-f7db20c57742
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 4513258f5c4bbb1cafe9ef22b35a4708c63e1c45be353b55c8bda1e20c4fce4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644620"
---
# <a name="magnification-api-functions"></a>Funktionen der Vergrößerungs-API

Dieser Abschnitt enthält Referenzinformationen zu den Funktionen der Vergrößerungs-API.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | Beschreibung |
|:---|:---|
| [**MagGetColorEffect**](/windows/win32/api/Magnification/nf-magnification-maggetcoloreffect)<br/> | Ruft die Farbtransformationsmatrix für ein Bildschirmlupesteuerelement ab.<br/> |
| [**MagGetFullscreenColorEffect**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreencoloreffect)<br/>  |  Ruft die Farbtransformationsmatrix ab, die der Vollbildlupe zugeordnet ist.<br/> |
| [**MagGetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreentransform)<br/>  | Ruft die Vergrößerungseinstellungen für die Vollbildlupe ab.<br/>  |
| [***MagGetImageScalingCallback** _](/windows/win32/api/Magnification/nf-magnification-maggetimagescalingcallback)<br/>  | _*in Windows 7 und höher als veraltet gekennzeichnet**<br/>Ruft die registrierte Rückruffunktion ab, die eine benutzerdefinierte Transformation für die Bildskalierung implementiert. <br/> |
| [**MagGetInputTransform**](/windows/win32/api/Magnification/nf-magnification-maggetinputtransform)<br/>  | Ruft die aktuelle Eingabetransformation für Stift- und Toucheingaben ab, dargestellt als Quellrechteck und Zielrechteck.<br/>  |
| [**MagGetWindowFilterList**](/windows/win32/api/Magnification/nf-magnification-maggetwindowfilterlist)<br/>  | Ruft die Liste der Fenster ab, die vergrößert oder von der Vergrößerung ausgeschlossen werden.<br/>  |
| [**MagGetWindowSource**](/windows/win32/api/Magnification/nf-magnification-maggetwindowsource)<br/>  | Ruft das Rechteck des Bereichs ab, der vergrößert wird.<br/>  |
| [**MagGetWindowTransform**](/windows/win32/api/Magnification/nf-magnification-maggetwindowtransform)<br/>  | Ruft die Transformationsmatrix ab, die einem Bildschirmlupesteuerelement zugeordnet ist. <br/>  |
| [***MagImageScalingCallback** _](/windows/win32/api/Magnification/nc-magnification-magimagescalingcallback)<br/>  | _*in Windows 7 und höher als veraltet gekennzeichnet**<br/>Prototyp für eine Rückruffunktion, die eine benutzerdefinierte Transformation für die Bildskalierung implementiert.<br/>  |
| [**MagInitialize**](/windows/win32/api/Magnification/nf-magnification-maginitialize)<br/>  | Erstellt und initialisiert die Laufzeitobjekte der Bildschirmlupe. <br/>  |
| [**MagSetColorEffect**](/windows/win32/api/Magnification/nf-magnification-magsetcoloreffect)<br/>  | >Legt die Farbtransformationsmatrix für ein Bildschirmlupesteuerelement fest.<br/>  |
| [**MagSetFullscreenColorEffect**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreencoloreffect)<br/>  | Ändert die Farbtransformationsmatrix, die der Vollbildlupe zugeordnet ist.<br/>  |
| [**MagSetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform)<br/>  | Ändert die Vergrößerungseinstellungen für die Vollbildlupe.<br/>  |
| [***MagSetImageScalingCallback** _](/windows/win32/api/Magnification/nf-magnification-magsetimagescalingcallback)<br/>  | _*in Windows 7 und höher als veraltet gekennzeichnet**<br/>Legt die Rückruffunktion für die Filterung und Skalierung externer Bilder fest.<br/>  |
| [**MagSetInputTransform**](/windows/win32/api/Magnification/nf-magnification-magsetinputtransform)<br/>  | Legt die aktuelle aktive Eingabetransformation für Stift- und Toucheingaben fest, dargestellt als Quellrechteck und Zielrechteck.<br/>  |
| [**MagSetWindowFilterList**](/windows/win32/api/Magnification/nf-magnification-magsetwindowfilterlist)<br/>  | Legt die Liste der Fenster fest, die vergrößert werden sollen, oder die Liste der Fenster, die von der Vergrößerung ausgeschlossen werden sollen.<br/>  |
| [**MagSetWindowSource**](/windows/win32/api/Magnification/nf-magnification-magsetwindowsource)<br/>  | Legt das Quellrechteck für das Vergrößerungsfenster fest.<br/>  |
| [**MagSetWindowTransform**](/windows/win32/api/Magnification/nf-magnification-magsetwindowtransform)<br/>  | Legt die Transformationsmatrix für ein Bildschirmlupesteuerelement fest. <br/>  |
| [**MagShowSystemCursor**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor)<br/>  | Zeigt den Systemcursor an oder blendet den Cursor aus.<br/>  |
| [**MagUninitialize**](/windows/win32/api/Magnification/nf-magnification-maguninitialize)<br/>  | Zerstört die Bildschirmlupe-Laufzeitobjekte.<br/>  |

## <a name="related-topics"></a>Zugehörige Themen

[Referenz](entry-magapi-ref.md)
