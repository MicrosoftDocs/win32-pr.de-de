---
title: CBEM_GETEDITCONTROL Nachricht (Commctrl.h)
description: Ruft das Handle für den Bearbeitungssteuerelementteil eines ComboBoxEx-Steuerelements ab. Ein ComboBoxEx-Steuerelement verwendet ein Bearbeitungsfeld, wenn es auf den \_ CBS-DROPDOWN-Stil festgelegt ist.
ms.assetid: def91949-cadc-4297-a504-0680d7d9b815
keywords:
- CBEM_GETEDITCONTROL Meldung Windows-Steuerelemente
topic_type:
- apiref
api_name:
- CBEM_GETEDITCONTROL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 885a90a1b37fab7cd8e4a492bd00ad349f96202e13ee25a404f7f4aa41f623e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118414070"
---
# <a name="cbem_geteditcontrol-message"></a>CBEM \_ GETEDITCONTROL-Nachricht

Ruft das Handle für den Bearbeitungssteuerelementteil eines ComboBoxEx-Steuerelements ab. Ein ComboBoxEx-Steuerelement verwendet ein Bearbeitungsfeld, wenn es auf den [**\_ CBS-DROPDOWN-Stil**](combo-box-styles.md) festgelegt ist.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle für das Bearbeitungssteuerelement im ComboBoxEx-Steuerelement zurück, wenn es den [**\_ CBS-DROPDOWN-Stil**](combo-box-styles.md) verwendet. Andernfalls gibt die Nachricht **NULL** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





