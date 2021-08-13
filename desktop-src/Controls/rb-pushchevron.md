---
title: RB_PUSHCHEVRON (Commctrl.h)
description: Wird an ein Rebar-Steuerelement gesendet, um ein Chevron programmgesteuert zu pushen.
ms.assetid: 00a8ce10-1fb2-488a-a6f9-1814f73f82bd
keywords:
- RB_PUSHCHEVRON meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- RB_PUSHCHEVRON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2d095cd824970b7ea90541420274b204a1e2f63ce6e1218e62221741f572feb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434970"
---
# <a name="rb_pushchevron-message"></a>RB \_ PUSHCHEVRON-Nachricht

Wird an ein Rebar-Steuerelement gesendet, um ein Chevron programmgesteuert zu pushen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nullbasierter Index des Bands, dessen Chevron pusht werden soll.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein von der Anwendung definierter 32-Bit-Wert. Sie wird als **lParamNM-Mitglied** der [**NMREBARCHEVRON-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) die mit der [RBN-CHEVRONPUSHED-Benachrichtigung \_](rbn-chevronpushed.md) übergeben wird, an die Anwendung übergeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Meldung wird nicht verwendet.

## <a name="remarks"></a>Hinweise

Wenn diese Meldung gesendet wird, sendet das Leistensteuerelement der Anwendung einen [ \_ RBN-CHEVRONPUSHED-Benachrichtigungscode](rbn-chevronpushed.md) und fordert sie auf, das Chevronmenü anzuzeigen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





