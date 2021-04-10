---
title: EM_GETAUTOURLDETECT Meldung (RichEdit. h)
description: Gibt an, ob die automatische URL-Erkennung im Rich Edit-Steuerelement aktiviert ist.
ms.assetid: f723f15c-bf8f-41ab-aef0-bd8f2c0b9e5d
keywords:
- Windows-Steuerelemente für EM_GETAUTOURLDETECT Meldung
topic_type:
- apiref
api_name:
- EM_GETAUTOURLDETECT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e68e4f2991c5f8780cb587594289674e07ec992
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040693"
---
# <a name="em_getautourldetect-message"></a>EM \_ GETAUTOURLDETECT Meldung

Gibt an, ob die automatische URL-Erkennung im Rich Edit-Steuerelement aktiviert ist.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die automatische URL-Erkennung aktiv ist, ist der Rückgabewert 1.

Wenn die automatische URL-Erkennung inaktiv ist, ist der Rückgabewert 0.

## <a name="remarks"></a>Bemerkungen

Wenn die automatische URL-Erkennung eingeschaltet ist, überprüft Microsoft Rich Edit den typisierten Text ständig auf eine gültige URL. Bei der umfassenden Bearbeitung werden URLs erkannt, die mit den folgenden Präfixen beginnen:

-   http:
-   file:
-   mailto:
-   FTP
-   http
-   Gopher
-   NNTP-
-   Prospero:
-   Telnet
-   News
-   Wais:
-   positiv

Rich Edit erkennt auch Standard Pfadnamen, die mit beginnen \\ \\ . Wenn Rich Edit eine URL verwendet, ändert Sie die Textfarbe der URL, unterstreicht den Text und benachrichtigt den Client über den [ \_ Link "en](en-link.md)".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Link "en" \_](en-link.md)
</dt> </dl>

 

 





