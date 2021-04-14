---
title: RB_PUSHCHEVRON Meldung (kommstrg. h)
description: Wird an ein Grund leisten-Steuerelement gesendet, um ein Chevron Programm gesteuert zu pushen.
ms.assetid: 00a8ce10-1fb2-488a-a6f9-1814f73f82bd
keywords:
- Windows-Steuerelemente für RB_PUSHCHEVRON Meldung
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
ms.openlocfilehash: e09e558d5574d4fd28cf01e9794657556dda4ae8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518275"
---
# <a name="rb_pushchevron-message"></a>RB \_ pushchevron-Nachricht

Wird an ein Grund leisten-Steuerelement gesendet, um ein Chevron Programm gesteuert zu pushen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

NULL basierter Index des Bands, dessen Chevron per pushübertragung durchgesetzt werden soll.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein von der Anwendung definierter 32-Bit-Wert. Sie wird an die Anwendung als **lparamnm** -Member der [**nmrebarchevron**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) -Struktur zurückgegeben, die mit der [RBN- \_ chevronpushbenachrichtigung](rbn-chevronpushed.md) übergeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Nachricht wird nicht verwendet.

## <a name="remarks"></a>Bemerkungen

Wenn diese Nachricht gesendet wird, sendet das Grund leisten-Steuerelement der Anwendung einen [RBN- \_ chevronpushbenachrichtigungscode](rbn-chevronpushed.md) , der Sie auffordert, das Chevron-Menü anzuzeigen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





