---
title: LVM_CANCELEDITLABEL Meldung (Commctrl.h)
description: Bricht einen Bearbeitungsvorgang für Elementtext ab.
ms.assetid: 73e9c922-3223-4c49-a33c-df7c09443ccc
keywords:
- LVM_CANCELEDITLABEL Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- LVM_CANCELEDITLABEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da0b105c1082457c2cafd14e7a36361100f8e82197db7e5d76ae51447f945897
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698800"
---
# <a name="lvm_canceleditlabel-message"></a>LVM \_ CANCELEDITLABEL-Nachricht

Bricht einen Bearbeitungsvorgang für Elementtext ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="remarks"></a>Hinweise

> [!Note]  
> Um diese Meldung verwenden zu können, müssen Sie ein Manifest angeben, das Comclt32.dll Version 6.0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen.](cookbook-overview.md)

 

Diese Meldung bewirkt, dass eine [LVN \_ ENDLABELEDIT-Benachrichtigung](lvn-endlabeledit.md) gesendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





