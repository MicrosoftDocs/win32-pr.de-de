---
title: RB_GETBANDINFO Meldung (kommstrg. h)
description: Ruft Informationen zu einem angegebenen Band in einem Grund leisten-Steuerelement ab.
ms.assetid: c2a76c91-7d44-4278-823d-bd263520e7a8
keywords:
- Windows-Steuerelemente für RB_GETBANDINFO Meldung
topic_type:
- apiref
api_name:
- RB_GETBANDINFO
- RB_GETBANDINFOA
- RB_GETBANDINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b87715cf61b4eb2726eab83d500330721f41719f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104792"
---
# <a name="rb_getbandinfo-message"></a>RB \_ GetBandInfo-Meldung

Ruft Informationen zu einem angegebenen Band in einem Grund leisten-Steuerelement ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der null basierte Index des Bands, für das die Informationen abgerufen werden.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) -Struktur, die die angeforderten Bandinformationen empfängt. Vor dem Senden dieser Nachricht müssen Sie das **CBSIZE** -Element dieser Struktur auf die Größe der **REBARBANDINFO** -Struktur festlegen und das **fmask** -Element auf die Elemente festlegen, die Sie abrufen möchten. Außerdem müssen Sie den **CCH** -Member der **REBARBANDINFO** -Struktur auf die Größe des **lpText** -Puffers festlegen, wenn rbbim- \_ Text angegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **RB \_ Getbandinfow** (Unicode) und **RB \_ getbandinfoa** (ANSI)<br/>             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**RB \_ SetBandInfo**](rb-setbandinfo.md)
</dt> </dl>

 

 





