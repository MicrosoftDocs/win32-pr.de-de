---
title: EM_EXSETSEL Meldung (RichEdit. h)
description: Wählt einen Bereich von Zeichen oder Component Object Model (com)-Objekten in einem Rich-Edit-Steuerelement von Microsoft aus.
ms.assetid: 85a0d1d4-1826-4ac5-b823-de81a051441d
keywords:
- Windows-Steuerelemente für EM_EXSETSEL Meldung
topic_type:
- apiref
api_name:
- EM_EXSETSEL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6939156fb1a8f35e03527e64a4c6f5185180668d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859018"
---
# <a name="em_exsetsel-message"></a>EM \_ Ex-tsel-Meldung

Wählt einen Bereich von Zeichen oder Component Object Model (com)-Objekten in einem Rich-Edit-Steuerelement von Microsoft aus.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. Er muss NULL sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Eine [**charrange**](/windows/desktop/api/Richedit/ns-richedit-charrange) -Struktur, die den Auswahlbereich angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist die Auswahl, die tatsächlich festgelegt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





