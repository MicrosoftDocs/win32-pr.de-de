---
title: UDM_GETPOS Meldung (Commctrl.h)
description: Ruft die aktuelle Position eines Auf-Ab-Steuerelements mit 16-Bit-Genauigkeit ab.
ms.assetid: 5f395de0-11b3-44f8-9bf4-42e27ce88a0c
keywords:
- UDM_GETPOS Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- UDM_GETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e92ca5fe5d902980560b6879ac7c345230056987308a1e390b0af351281eac62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059780"
---
# <a name="udm_getpos-message"></a>UDM \_ GETPOS-Nachricht

Ruft die aktuelle Position eines Auf-Ab-Steuerelements mit 16-Bit-Genauigkeit ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Erfolg wird [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) auf 0 (null) und [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) auf die aktuelle Position des Steuerelements festgelegt. Wenn ein Fehler auftritt, wird **HIWORD** auf einen Wert ungleich 0 (null) festgelegt.

## <a name="remarks"></a>Hinweise

Bei der Verarbeitung dieser Meldung aktualisiert das Auf-Ab-Steuerelement seine aktuelle Position basierend auf der Beschriftung des Fensters "fenster". Das Auf-Ab-Steuerelement gibt einen Fehler zurück, wenn kein Fenster vorhanden ist oder wenn die Beschriftung einen ungültigen oder außerhalb des Bereichs liegenden Wert angibt. Außerdem wird im HIWORD der Rückgabe ein Fehlerflag festgelegt, wenn das Steuerelement ohne den [**UDS \_ SETBUDDYINT-Stil**](up-down-control-styles.md) erstellt wird, obwohl es einen gültigen Positionswert im LOWORD der Rückgabe zurückgibt.

Wenn 32-Bit-Werte für ein Auf-Ab-Steuerelement mit [**UDM \_ SETRANGE32**](udm-setrange32.md)aktiviert wurden, gibt diese Meldung nur die unteren 16 Bits der Position zurück. Verwenden Sie [**UDM \_ GETPOS32,**](udm-getpos32.md)um die vollständige 32-Bit-Position abzurufen.

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

[**UDM \_ GETRANGE**](udm-getrange.md)
</dt> <dt>

[**UDM \_ GETRANGE32**](udm-getrange32.md)
</dt> <dt>

[**UDM \_ SETPOS**](udm-setpos.md)
</dt> <dt>

[**UDM \_ SETRANGE32**](udm-setrange32.md)
</dt> </dl>

 

