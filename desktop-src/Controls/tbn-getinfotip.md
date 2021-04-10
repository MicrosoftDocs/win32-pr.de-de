---
title: TBN_GETINFOTIP Benachrichtigungs Code (kommctrl. h)
description: Ruft Infotipp-Informationen für ein Symbolleisten Element ab. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 877de60c-f6e1-440a-81f0-d66ab443c985
keywords:
- Windows-Steuerelemente für TBN_GETINFOTIP Benachrichtigungs
topic_type:
- apiref
api_name:
- TBN_GETINFOTIP
- TBN_GETINFOTIPA
- TBN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fda2c1b181ebea1840b153b8b2df8328b3f2cc8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040353"
---
# <a name="tbn_getinfotip-notification-code"></a>TBN- \_ getinfotip-Benachrichtigungs Code

Ruft Infotipp-Informationen für ein Symbolleisten Element ab. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
TBN_GETINFOTIP

    lptbgit = (LPNMTBGETINFOTIP) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**nmtbgetinfotip**](/windows/win32/api/commctrl/ns-commctrl-nmtbgetinfotipa) -Struktur, die Element Informationen enthält und Infotipp-Informationen empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird vom-Steuerelement ignoriert.

## <a name="remarks"></a>Bemerkungen

Die Infotipp-Unterstützung auf der Symbolleiste ermöglicht der Symbolleiste das Anzeigen von Quick Infos für Elemente, die so groß wie infotipsize-Zeichen sind. Wenn dieser Benachrichtigungs Code nicht verarbeitet wird, verwendet die Symbolleiste den Text des Elements für den infotip.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TBN \_ Getinfotipw** (Unicode) und **TBN \_ getinfotipa** (ANSI)<br/>             |



 

 





