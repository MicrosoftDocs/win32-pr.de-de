---
title: TTM_WINDOWFROMPOINT Nachricht (Commctrl.h)
description: Ermöglicht einer Unterklassenprozedur, dass eine QuickInfo Text für ein anderes Fenster als das fenster unter dem Mauscursor anzeigt.
ms.assetid: f3bf6917-1745-4e4f-a9c1-8fe86b2b3906
keywords:
- TTM_WINDOWFROMPOINT Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TTM_WINDOWFROMPOINT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 572ce204fd9f0056ef77d62c7909a7281c478c38f6abeb95089ce86b0bdb1b8f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109540"
---
# <a name="ttm_windowfrompoint-message"></a>TTM \_ WINDOWFROMPOINT-Nachricht

Ermöglicht einer Unterklassenprozedur, dass eine QuickInfo Text für ein anderes Fenster als das fenster unter dem Mauscursor anzeigt.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**POINT-Struktur,**](/previous-versions//dd162805(v=vs.85)) die den zu überprüfenden Punkt definiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist das Handle für das Fenster, das den Punkt enthält, oder **NULL,** wenn am angegebenen Punkt kein Fenster vorhanden ist.

## <a name="remarks"></a>Hinweise

Diese Nachricht soll von einer Anwendung verarbeitet werden, die eine QuickInfo untergliedert. Sie ist nicht für das Senden durch eine Anwendung vorgesehen. Eine QuickInfo sendet diese Nachricht an sich selbst, bevor der Text für ein Fenster angezeigt wird. Durch Ändern der Koordinaten des durch *lParam* angegebenen Punkts kann die Unterklassenprozedur dazu führen, dass die QuickInfo Text für ein anderes Fenster als das fenster unter dem Mauszeiger anzeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

