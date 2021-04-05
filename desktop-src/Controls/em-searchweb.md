---
title: EM_SEARCHWEB Meldung (kommstrg. h)
description: Öffnet den Browser und führt eine Websuche mit dem ausgewählten Text als Suchbegriff aus.
ms.assetid: 1b1ff5e7-e0b8-40c1-8b7e-7003e9ef959b
keywords:
- Windows-Steuerelemente für EM_SEARCHWEB Meldung
topic_type:
- apiref
api_name:
- EM_SEARCHWEB
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2e83c18db47d18648797ee3d58fe12567af941b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859129"
---
# <a name="em_searchweb-message"></a>EM \_ Searchweb-Nachricht

Öffnet den Browser und führt eine Websuche mit dem ausgewählten Text als Suchbegriff aus.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn das Feature "Web durchsuchen" mithilfe der Nachricht " [**EM \_ enablesearchweb**](em-enablesearchweb.md) " deaktiviert wird, hat diese Nachricht keine Auswirkung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10, 1809 \[ Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2019 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ enablesearchweb**](em-enablesearchweb.md)
</dt> </dl>

 

 





