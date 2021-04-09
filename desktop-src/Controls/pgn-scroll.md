---
title: PGN_SCROLL Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Pager-Steuer Elements, dass für das enthaltene Fenster ein Rollup durchgeführt wird. Diese Benachrichtigung wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 3d40e75e-c445-4885-b807-8cfcb92cb2d9
keywords:
- Windows-Steuerelemente für PGN_SCROLL Benachrichtigungs
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
ms.openlocfilehash: 62bc964b1a820fb0d5cd341e8909f36d5f6312ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103471"
---
# <a name="pgn_scroll-notification-code"></a>PGN- \_ scrollbenachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines Pager-Steuer Elements, dass für das enthaltene Fenster ein Rollup durchgeführt wird. Diese Benachrichtigung wird in Form einer WM-Benachrichtigungs Meldung gesendet. [**\_**](wm-notify.md)


```C++
PGN_SCROLL

    lpnms = (LPNMPGSCROLL) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**nmpgscroll**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgscroll) -Struktur, die Informationen über den Benachrichtigungs Code enthält und empfängt. Der **Idir** -Member dieser Struktur gibt die Richtung des Bildlaufs an. Die Elemente **IXPOS** und **iypos** enthalten die horizontale und vertikale Position des enthaltenen Fensters vor dem Bildlauf. Der **iscroll** -Member enthält den Standardwert für das Schiebe Delta. Wenn gewünscht, können Sie diesen Member in einen anderen Bild Lauf Betrag ändern.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





