---
title: HKM_GETHOTKEY Meldung (kommstrg. h)
description: Ruft den Code des virtuellen Schlüssels und die Modifiziererflags eines Abkürzungs Schlüssels von einem Steuerelement für den Hot Key ab.
ms.assetid: 8b061411-604d-46ea-a082-3eca2d47d992
keywords:
- Windows-Steuerelemente für HKM_GETHOTKEY Meldung
topic_type:
- apiref
api_name:
- HKM_GETHOTKEY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16e23e02f32a4dd6f82f61fd735688353f48ec19
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476320"
---
# <a name="hkm_gethotkey-message"></a>HKM- \_ GetHotKey-Nachricht

Ruft den Code des virtuellen Schlüssels und die Modifiziererflags eines Abkürzungs Schlüssels von einem Steuerelement für den Hot Key ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Code und die Modifiziererflags des virtuellen Schlüssels zurück. Das [**lobyzeichen**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) von [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ist der virtuelle Schlüsselcode der "Hot"-Taste. Das [**Hibyte**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) des **loworts** ist der schlüsselmodifizierer, der die Schlüssel angibt, die eine Kombination aus der Tastenkombination definieren. Die Modifiziererflags können eine Kombination der folgenden Werte sein.



| Wert            | Bedeutung      |
|------------------|--------------|
| hotkeyf \_ alt     | ALT-TASTE      |
| hotkeyf- \_ Steuerelement | Steuerelement Taste  |
| hotkeyf \_ ext     | Erweiterter Schlüssel |
| hotkeyf- \_ Verschiebung   | Umschalttaste    |



 

## <a name="remarks"></a>Bemerkungen

Der 16-Bit-Wert, der von dieser Nachricht zurückgegeben wird, kann als *wParam* -Parameter in der [**WM \_ -**](/windows/desktop/inputdev/wm-sethotkey) Nachricht "*" verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

