---
title: PGN_SCROLL Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster eines Pager-Steuerelements, dass im enthaltenen Fenster ein Bildlauf an steht. Diese Benachrichtigung wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 3d40e75e-c445-4885-b807-8cfcb92cb2d9
keywords:
- PGN_SCROLL Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- PGN_SCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 864903c73eeb611d1c748ec6a4d936192a1a27f22d3f37115af8879916286a8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830144"
---
# <a name="pgn_scroll-notification-code"></a>PGN \_ SCROLL-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster eines Pager-Steuerelements, dass im enthaltenen Fenster ein Bildlauf an steht. Diese Benachrichtigung wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
PGN_SCROLL

    lpnms = (LPNMPGSCROLL) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMPGSCROLL-Struktur,**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgscroll) die Informationen zum Benachrichtigungscode enthält und empfängt. Der **iDir-Member** dieser -Struktur gibt die Richtung des Bildlaufs an. Die **Elemente iXpos** und **iYpos** enthalten die horizontale und vertikale Position des enthaltenen Fensters vor dem Bildlauf. Das **iScroll-Member** enthält den standarden Deltawert für den Bildlauf. Sie können dieses Member bei Wunsch in einen anderen Bildlauf ändern.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





