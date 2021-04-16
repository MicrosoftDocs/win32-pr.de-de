---
title: EM_GETIMECOMPMODE Meldung (RichEdit. h)
description: Ruft den aktuellen IME-Modus (Eingabemethoden-Editor) für ein Rich-Edit-Steuerelement ab.
ms.assetid: dac96833-4c3d-4da7-9ea4-52204434ec10
keywords:
- Windows-Steuerelemente für EM_GETIMECOMPMODE Meldung
topic_type:
- apiref
api_name:
- EM_GETIMECOMPMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1feb2f5f31831e0e292bf002f24ca4978f25753a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477913"
---
# <a name="em_getimecompmode-message"></a>EM \_ getimecompmode-Meldung

Ruft den aktuellen IME-Modus (Eingabemethoden-Editor) für ein Rich-Edit-Steuerelement ab.

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

Der Rückgabewert ist einer der folgenden Werte.



| Rückgabecode                                                                                     | Beschreibung                  |
|-------------------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**ICM \_ notopen**</dt> </dl>     | IME ist nicht geöffnet.<br/>  |
| <dl> <dt>**ICM \_ LEVEL3**</dt> </dl>      | True Inline Modus.<br/> |
| <dl> <dt>**ICM \_ Level2**</dt> </dl>      | Ebene 2.<br/>          |
| <dl> <dt>**ICM \_ Level2 \_ 5**</dt> </dl>   | Ebene 2,5<br/>         |
| <dl> <dt>**ICM \_ Level2 \_ SUI**</dt> </dl> | Spezielle Benutzeroberfläche.<br/>       |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





