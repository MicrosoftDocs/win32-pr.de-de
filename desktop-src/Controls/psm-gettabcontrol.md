---
title: PSM_GETTABCONTROL-Nachricht (Prsht.h)
description: Ruft das Handle für das Registerkartensteuerelement eines Eigenschaftenblatts ab. Sie können diese Nachricht explizit oder mithilfe des \_ PropSheet-Makros GetTabControl senden.
ms.assetid: 5ddea541-c8e0-4357-b08e-3b5e64be377f
keywords:
- PSM_GETTABCONTROL Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- PSM_GETTABCONTROL
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b0e26c9489dc839383552b407a16313c94e1fc3b070d93f1d59ddaf0310134d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169660"
---
# <a name="psm_gettabcontrol-message"></a>PSM \_ GETTABCONTROL-Nachricht

Ruft das Handle für das Registerkartensteuerelement eines Eigenschaftenblatts ab. Sie können diese Nachricht explizit oder mithilfe des [**\_ PropSheet-Makros GetTabControl**](/windows/desktop/api/Prsht/nf-prsht-propsheet_gettabcontrol) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle an das Registerkartensteuerelement zurück.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Diese Meldung wird nicht unterstützt, wenn Sie den Stil des Assistenten Für Dies verwenden [**\_ (PSH-DIALOGFELDWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





