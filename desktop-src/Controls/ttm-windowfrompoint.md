---
title: TTM_WINDOWFROMPOINT Meldung (kommstrg. h)
description: Ermöglicht es einer Unterklassen Prozedur, eine QuickInfo für ein anderes Fenster als das unter dem Mauszeiger anzuzeigen.
ms.assetid: f3bf6917-1745-4e4f-a9c1-8fe86b2b3906
keywords:
- Windows-Steuerelemente für TTM_WINDOWFROMPOINT Meldung
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
ms.openlocfilehash: 68679f6b6c2477a8279c22f11d0d300e44c8370d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742257"
---
# <a name="ttm_windowfrompoint-message"></a>TTM \_ WindowFromPoint-Meldung

Ermöglicht es einer Unterklassen Prozedur, eine QuickInfo für ein anderes Fenster als das unter dem Mauszeiger anzuzeigen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**Punkt**](/previous-versions//dd162805(v=vs.85)) Struktur, die den zu überprüfenden Punkt definiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist das Handle für das Fenster, das den Punkt enthält, oder **null** , wenn am angegebenen Punkt kein Fenster vorhanden ist.

## <a name="remarks"></a>Bemerkungen

Diese Nachricht soll von einer Anwendung verarbeitet werden, die eine QuickInfo Unterklassen unterteilt. Sie ist nicht für das Senden durch eine Anwendung vorgesehen. Eine QuickInfo sendet diese Nachricht an sich selbst, bevor Sie den Text für ein Fenster anzeigt. Durch Ändern der Koordinaten des durch *LPARAM* angegebenen Punkts kann die Unterklassen Prozedur bewirken, dass die QuickInfo Text für ein anderes Fenster als das unter dem Mauszeiger anzeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

