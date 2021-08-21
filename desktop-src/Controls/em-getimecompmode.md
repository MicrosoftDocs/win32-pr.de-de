---
title: EM_GETIMECOMPMODE Nachricht (Richedit.h)
description: Ruft den aktuellen IME-Modus (Input Method Editor) für ein Rich-Edit-Steuerelement ab.
ms.assetid: dac96833-4c3d-4da7-9ea4-52204434ec10
keywords:
- EM_GETIMECOMPMODE Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 53b9c0242872446c22034502d92af00ead7289fc68b4d5a66d79c3ef68be5eaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019548"
---
# <a name="em_getimecompmode-message"></a>EM \_ GETIMECOMPMODE-Nachricht

Ruft den aktuellen IME-Modus (Input Method Editor) für ein Rich-Edit-Steuerelement ab.

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
| <dl> <dt>**\_ICM NOTOPEN**</dt> </dl>     | IME ist nicht geöffnet.<br/>  |
| <dl> <dt>**\_ICM LEVEL3**</dt> </dl>      | True-Inlinemodus.<br/> |
| <dl> <dt>**\_ICM LEVEL2**</dt> </dl>      | 2\. Ebene.<br/>          |
| <dl> <dt>**\_ICM LEVEL2 \_ 5**</dt> </dl>   | Ebene 2.5<br/>         |
| <dl> <dt>**\_ICM \_LEVEL2-SUI**</dt> </dl> | Spezielle Benutzeroberfläche.<br/>       |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



 

 





