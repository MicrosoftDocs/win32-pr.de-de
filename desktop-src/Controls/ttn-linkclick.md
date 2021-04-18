---
title: TTN_LINKCLICK Benachrichtigungs Code (kommctrl. h)
description: Wird gesendet, wenn auf einen Textlink in einer QuickInfo-Sprechblase geklickt wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: d3e76431-5b5f-4d67-8528-db21fd939917
keywords:
- Windows-Steuerelemente für TTN_LINKCLICK Benachrichtigungs
topic_type:
- apiref
api_name:
- TTN_LINKCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c90be24910c2739b4495b651abf97156342d955b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344681"
---
# <a name="ttn_linkclick-notification-code"></a>TTN- \_ linkclick-Benachrichtigungs Code

Wird gesendet, wenn auf einen Textlink in einer QuickInfo-Sprechblase geklickt wird. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
TTN_LINKCLICK
```



## <a name="parameters"></a>Parameter

Dieser Benachrichtigungs Code weist keine Parameter auf.

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird nicht verwendet.

## <a name="remarks"></a>Bemerkungen

Im folgenden finden Sie ein Beispiel für den Fall, dass diese Benachrichtigung gesendet wird. Angenommen, die QuickInfo-QuickInfo enthält den folgenden Text: "This is a <A>Link</A>". Wenn auf "Link" geklickt wird, sendet das ToolTip-Steuerelement einen TTN- \_ linkclick-Benachrichtigungs Code.

> [!Note]  
> Zur Verwendung dieses Benachrichtigungs Codes müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





