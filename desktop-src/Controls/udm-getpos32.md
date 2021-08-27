---
title: UDM_GETPOS32 Nachricht (Commctrl.h)
description: Gibt die 32-Bit-Position eines Auf-Ab-Steuerelements zurück.
ms.assetid: 90feffbd-a472-446f-8a67-5da408cde002
keywords:
- UDM_GETPOS32 Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- UDM_GETPOS32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a11d043ca4f6b69a554b43d5abeaf35e4c2a2a6d72797e829900529df70b6c47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059790"
---
# <a name="udm_getpos32-message"></a>UDM \_ GETPOS32-Nachricht

Gibt die 32-Bit-Position eines Auf-Ab-Steuerelements zurück.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf einen **BOOL-Wert,** der auf 0 (null) festgelegt ist, wenn der Wert erfolgreich abgerufen wurde, oder auf einen Wert ungleich 0 (null), wenn ein Fehler auftritt. Wenn dieser Parameter auf **NULL** festgelegt ist, werden keine Fehler gemeldet.

Wenn **UDM \_ GETPOS32** in einer prozessübergreifenden Situation verwendet wird, muss dieser Parameter **NULL** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Position eines Auf-Ab-Steuerelements mit 32-Bit-Genauigkeit zurück. Anwendungen müssen den *lParam-Wert* überprüfen, um zu bestimmen, ob der Rückgabewert gültig ist.

## <a name="remarks"></a>Hinweise

Wenn diese Meldung verarbeitet wird, aktualisiert das Auf-Ab-Steuerelement seine aktuelle Position basierend auf der Beschriftung des Fensters "fenster". Es wird ein Fehler zurückgegeben, wenn kein Fenster vorhanden ist oder wenn die Beschriftung einen ungültigen oder außerhalb des Bereichs liegenden Wert angibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**UDM \_ GETPOS**](udm-getpos.md)
</dt> <dt>

[**UDM \_ SETPOS**](udm-setpos.md)
</dt> <dt>

[**UDM \_ SETPOS32**](udm-setpos32.md)
</dt> </dl>

 

 





