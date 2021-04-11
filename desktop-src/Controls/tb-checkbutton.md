---
title: TB_CHECKBUTTON Meldung (kommstrg. h)
description: Überprüft oder überprüft eine angegebene Schaltfläche in einer Symbolleiste.
ms.assetid: e67734a9-851c-41ab-8ad7-15d434f58e5a
keywords:
- Windows-Steuerelemente für TB_CHECKBUTTON Meldung
topic_type:
- apiref
api_name:
- TB_CHECKBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7734b37da44db38d9ca09b34ad9e666cc90eb5b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104041014"
---
# <a name="tb_checkbutton-message"></a>TB \_ checkbutton-Meldung

Überprüft oder überprüft eine angegebene Schaltfläche in einer Symbolleiste.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Befehls Bezeichner der zu Überprüfung enden Schaltfläche.

</dd> <dt>

*lParam* 
</dt> <dd>

Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ist ein **boolescher** Wert, der angibt, ob die angegebene Schaltfläche überprüft oder nicht überprüft werden soll. **True** gibt an, dass die Überprüfung hinzugefügt wird. Wenn der Wert **false** ist, wird die Überprüfung entfernt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Wenn eine Schaltfläche aktiviert ist, wird Sie im gedrückten Zustand angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

