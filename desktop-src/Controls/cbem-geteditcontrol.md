---
title: CBEM_GETEDITCONTROL Meldung (kommstrg. h)
description: Ruft das Handle für den Bearbeitungs Steuerelement Teil eines ComboBoxEx-Steuer Elements ab. Ein ComboBoxEx-Steuerelement verwendet ein Bearbeitungsfeld, wenn es auf den CBS- \_ Dropdown Stil festgelegt ist.
ms.assetid: def91949-cadc-4297-a504-0680d7d9b815
keywords:
- Windows-Steuerelemente für CBEM_GETEDITCONTROL Meldung
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
ms.openlocfilehash: 412d1183b29c8c89b5977d5f7f2a1b962d54dc01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105597"
---
# <a name="cbem_geteditcontrol-message"></a>CBEM \_ geteditcontrol-Meldung

Ruft das Handle für den Bearbeitungs Steuerelement Teil eines ComboBoxEx-Steuer Elements ab. Ein ComboBoxEx-Steuerelement verwendet ein Bearbeitungsfeld, wenn es auf den [**CBS- \_ Dropdown**](combo-box-styles.md) Stil festgelegt ist.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle für das Bearbeitungs Steuerelement im ComboBoxEx-Steuerelement zurück, wenn es die [**CBS- \_ Dropdown**](combo-box-styles.md) -Formatvorlage verwendet. Andernfalls gibt die Meldung **null** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





