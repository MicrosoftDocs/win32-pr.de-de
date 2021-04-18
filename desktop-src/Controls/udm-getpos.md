---
title: UDM_GETPOS Meldung (kommstrg. h)
description: Ruft die aktuelle Position eines auf-ab-Steuer Elements mit 16-Bit-Genauigkeit ab.
ms.assetid: 5f395de0-11b3-44f8-9bf4-42e27ce88a0c
keywords:
- Windows-Steuerelemente für UDM_GETPOS Meldung
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
ms.openlocfilehash: f8e78ad19289d85b93ebcb39a244a896ddb4f33f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339127"
---
# <a name="udm_getpos-message"></a>UDM- \_ GetPos-Nachricht

Ruft die aktuelle Position eines auf-ab-Steuer Elements mit 16-Bit-Genauigkeit ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei erfolgreicher Ausführung wird das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) auf 0 (null) festgelegt, und das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) wird auf die aktuelle Position des Steuer Elements festgelegt. Wenn ein Fehler auftritt, wird das **HIWORD** auf einen Wert ungleich 0 (null) festgelegt.

## <a name="remarks"></a>Bemerkungen

Bei der Verarbeitung dieser Nachricht aktualisiert das auf-ab-Steuerelement die aktuelle Position basierend auf der Beschriftung des Buddy-Fensters. Das auf-ab-Steuerelement gibt einen Fehler zurück, wenn kein Buddy-Fenster vorhanden ist oder wenn die Beschriftung einen ungültigen Wert oder einen Wert außerhalb des gültigen Bereichs angibt. Außerdem wird ein Fehlerflag im HIWORD der Rückgabe festgelegt, wenn das Steuerelement ohne den [**UDS- \_ setbuddyint**](up-down-control-styles.md) -Stil erstellt wird, obwohl es einen gültigen Positionswert im LoWord der Rückgabe zurückgibt.

Wenn 32-Bit-Werte für ein auf-ab-Steuerelement mit [**UDM- \_ SETRANGE32**](udm-setrange32.md)aktiviert wurden, gibt diese Meldung nur die unteren 16 Bits der Position zurück. Um die vollständige 32-Bit-Position abzurufen, verwenden Sie [**UDM \_ GETPOS32**](udm-getpos32.md).

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

[**UDM- \_ GetRange**](udm-getrange.md)
</dt> <dt>

[**UDM \_ GETRANGE32**](udm-getrange32.md)
</dt> <dt>

[**UDM- \_ SetPos**](udm-setpos.md)
</dt> <dt>

[**UDM \_ SETRANGE32**](udm-setrange32.md)
</dt> </dl>

 

