---
title: EM_GETWORDWRAPMODE Meldung (RichEdit. h)
description: Ruft die aktuellen Zeilenumbruch-und Wort Umbruch Optionen für das Rich-Edit-Steuerelement ab.
ms.assetid: a87d80d6-2e9e-40ba-9348-a1cc1ef8ec10
keywords:
- Windows-Steuerelemente für EM_GETWORDWRAPMODE Meldung
topic_type:
- apiref
api_name:
- EM_GETWORDWRAPMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efc8a2b6d17623964eb0d3714c1c099f47fc788a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475567"
---
# <a name="em_getwordwrapmode-message"></a>EM \_ getwordwrapmode-Meldung

Ruft die aktuellen Zeilenumbruch-und Wort Umbruch Optionen für das Rich-Edit-Steuerelement ab.

> [!Note]  
> Diese Meldung wird nur in asiatischen Sprachversionen von Microsoft Rich Edit 1,0 unterstützt. Sie wird in höheren Versionen der Rich-Edit-Version nicht unterstützt.

 

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

Die Meldung gibt die aktuellen Optionen für Zeilenumbruch und Wort Umbruch zurück.

## <a name="remarks"></a>Bemerkungen

Diese Nachricht darf nicht von der Anwendungs definierten Prozedur für das Wort Umbruch gesendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





