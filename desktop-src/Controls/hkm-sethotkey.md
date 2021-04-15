---
title: HKM_SETHOTKEY Meldung (kommstrg. h)
description: Legt die Tastenkombination für ein Hot Key-Steuerelement fest.
ms.assetid: 372a7b2f-d9d5-43a8-9c06-730f2f5dc56e
keywords:
- Windows-Steuerelemente für HKM_SETHOTKEY Meldung
topic_type:
- apiref
api_name:
- HKM_SETHOTKEY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3672136c44c0268e218e7f87cbbeb3373b76b39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517651"
---
# <a name="hkm_sethotkey-message"></a>HKM-Nachricht für " \_ abkthotkey"

Legt die Tastenkombination für ein Hot Key-Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das [**lobyzeichen**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) von [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ist der virtuelle Schlüsselcode der "Hot"-Taste. Das [**Hibyte**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) des **loworts** ist der schlüsselmodifizierer, der die Schlüssel angibt, die eine Kombination aus der Tastenkombination definieren. Eine Liste der modifiziererflagwerte finden Sie in der Beschreibung der [**HKM \_ GetHotKey**](hkm-gethotkey.md) -Nachricht.

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es wird immer NULL zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

