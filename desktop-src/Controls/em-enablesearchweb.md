---
title: EM_ENABLESEARCHWEB Meldung (kommstrg. h)
description: Aktiviert oder deaktiviert das Feature "Internet durchsuchen" und den Kontextmenü Eintrag.
ms.assetid: 9393f03e-0719-458b-8122-616df738c417
keywords:
- Windows-Steuerelemente für EM_ENABLESEARCHWEB Meldung
topic_type:
- apiref
api_name:
- EM_ENABLESEARCHWEB
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdb2638476027f0a7fe2bb1a66a3a00a330e28c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956726"
---
# <a name="em_enablesearchweb-message"></a>EM \_ enablesearchweb-Meldung

Aktiviert oder deaktiviert das Feature "Internet durchsuchen" und den Kontextmenü Eintrag.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Wert **true** gibt an, dass das Feature "Web durchsuchen" aktiviert ist, und der Wert **false** gibt an, dass es deaktiviert ist.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn Sie "Internet durchsuchen" mit dieser Meldung deaktivieren, hat die Nachricht " [**EM \_ Searchweb**](em-searchweb.md) " keine Auswirkung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10, 1809 \[ Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2019 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**EM \_ Searchweb**](em-searchweb.md)
</dt> </dl>

 

 





