---
title: UDM_GETPOS32 Meldung (kommstrg. h)
description: Gibt die 32-Bit-Position eines auf-ab-Steuer Elements zurück.
ms.assetid: 90feffbd-a472-446f-8a67-5da408cde002
keywords:
- Windows-Steuerelemente für UDM_GETPOS32 Meldung
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
ms.openlocfilehash: 15f316b6833c67cd01d4e01910399a8730691f35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475726"
---
# <a name="udm_getpos32-message"></a>UDM \_ GETPOS32 Meldung

Gibt die 32-Bit-Position eines auf-ab-Steuer Elements zurück.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf einen **booleschen** Wert, der auf 0 (null) festgelegt wird, wenn der Wert erfolgreich abgerufen wird, oder ungleich NULL, wenn ein Fehler auftritt. Wenn dieser Parameter auf **null** festgelegt ist, werden keine Fehler gemeldet.

Wenn **UDM \_ GETPOS32** in einer prozessübergreifenden Situation verwendet wird, muss dieser Parameter **null** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Position eines auf-ab-Steuer Elements mit 32-Bit-Genauigkeit zurück. Anwendungen müssen den *LPARAM* -Wert überprüfen, um zu bestimmen, ob der Rückgabewert gültig ist.

## <a name="remarks"></a>Bemerkungen

Wenn diese Nachricht verarbeitet wird, aktualisiert das auf-ab-Steuerelement die aktuelle Position basierend auf der Beschriftung des Buddy-Fensters. Es wird ein Fehler zurückgegeben, wenn kein Buddy-Fenster vorhanden ist oder wenn die Beschriftung einen ungültigen Wert oder außerhalb des gültigen Bereichs angibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**UDM- \_ GetPos**](udm-getpos.md)
</dt> <dt>

[**UDM- \_ SetPos**](udm-setpos.md)
</dt> <dt>

[**UDM \_ SETPOS32**](udm-setpos32.md)
</dt> </dl>

 

 





