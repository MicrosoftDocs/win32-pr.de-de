---
title: RB_SETBANDINFO (Commctrl.h)
description: Legt Die Merkmale eines vorhandenen Bands in einem Rebar-Steuerelement fest.
ms.assetid: 00021c35-612d-4278-b10c-6e9f1f45a543
keywords:
- RB_SETBANDINFO von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- RB_SETBANDINFO
- RB_SETBANDINFOA
- RB_SETBANDINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aee89d91bc65556179d14c7e86a69a9e6399223f38bb1bcc44f746d7cd8f8a80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119798470"
---
# <a name="rb_setbandinfo-message"></a>RB \_ SETBANDINFO-Meldung

Legt Die Merkmale eines vorhandenen Bands in einem Rebar-Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nullbasierter Index des Bands, um die neuen Einstellungen zu erhalten.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**REBARBANDINFO-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) die das zu ändernde Band und die neuen Einstellungen definiert. Vor dem Senden dieser Nachricht müssen Sie den **cbSize-Member** dieser -Struktur auf die **sizeof-Struktur**(REBARBANDINFO) festlegen. Darüber hinaus müssen Sie den **cch-Member** der **REBARBANDINFO-Struktur** auf die Größe des **lpText-Puffers** festlegen, wenn RBBIM \_ TEXT angegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) oder andernfalls 0 (null) zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **RB \_ SETBANDINFOW** (Unicode) und **RB \_ SETBANDINFOA** (ANSI)<br/>             |



 

 





