---
title: TTM_GETTEXT Nachricht (Commctrl.h)
description: Ruft die Informationen ab, die ein QuickInfo-Steuerelement über ein Tool verwaltet.
ms.assetid: f2afa706-4209-4761-a981-df3d5b938c88
keywords:
- TTM_GETTEXT Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TTM_GETTEXT
- TTM_GETTEXTA
- TTM_GETTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9efe79105c705eba3dd25c124cf17ff0e4773618608bc7ef86ebbf3d0d9f715e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967890"
---
# <a name="ttm_gettext-message"></a>TTM \_ GETTEXT-Nachricht

Ruft die Informationen ab, die ein QuickInfo-Steuerelement über ein Tool verwaltet.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Die Anzahl der **TCHARs**, einschließlich des abschließenden NULL-Werts, der in den Puffer kopiert werden soll, auf den  **lpszText** zeigt. </dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**TOOLINFO-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) Legen Sie den **cbSize-Member** dieser -Struktur auf fest, `sizeof(TOOLINFO)` bevor Sie diese Nachricht senden. Legen Sie die **Member hwnd** und **uId** fest, um das Tool zu identifizieren, für das Informationen abgerufen werden sollen. Ordnen Sie einen Puffer der größe zu, die von *wParam* angegeben wird. Legen Sie den **lpszText-Member** so fest, dass er auf den Puffer verweist, um den Tooltext zu empfangen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TTM \_ GETTEXTW** (Unicode) und **TTM \_ GETTEXTA** (ANSI)<br/>                   |



 

 





