---
title: TTM_GETTEXT Meldung (kommstrg. h)
description: Ruft die Informationen ab, die ein QuickInfo-Steuerelement zu einem Tool beibehält.
ms.assetid: f2afa706-4209-4761-a981-df3d5b938c88
keywords:
- Windows-Steuerelemente für TTM_GETTEXT Meldung
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
ms.openlocfilehash: f774671d34f89306593d23481fa917190ae69aaa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337515"
---
# <a name="ttm_gettext-message"></a>TTM \_ gettext-Nachricht

Ruft die Informationen ab, die ein QuickInfo-Steuerelement zu einem Tool beibehält.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Die Anzahl der **tchars**, einschließlich des abschließenden **null**-Werts, der in den Puffer kopiert werden soll, auf den von **lpszText** verwiesen wird. </dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur. Legen Sie den **CBSIZE** -Member dieser-Struktur auf fest, `sizeof(TOOLINFO)` bevor Sie diese Nachricht senden. Legen Sie die **HWND** -und **UID** -Member fest, um das Tool zu identifizieren, für das Informationen abgerufen werden sollen. Zuordnen eines Puffer der Größe, die von *wParam* angegeben wird. Legen Sie fest, dass der **lpszText** -Member auf den Puffer verweist, um den tooltext zu empfangen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TTM \_ Gettextw** (Unicode) und **TTM \_ gettexta** (ANSI)<br/>                   |



 

 





