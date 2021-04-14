---
title: PSM_GETTABCONTROL Meldung (prsht. h)
description: Ruft das Handle für das Registerkarten-Steuerelement eines Eigenschaften Blatts ab. Sie können diese Nachricht explizit oder mithilfe des propsheet \_ gettabcontrol-Makros senden.
ms.assetid: 5ddea541-c8e0-4357-b08e-3b5e64be377f
keywords:
- Windows-Steuerelemente für PSM_GETTABCONTROL Meldung
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
ms.openlocfilehash: ab296159cac4dbfb4ef894d90d31bcd74d6ca2e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518527"
---
# <a name="psm_gettabcontrol-message"></a>PSM \_ gettabcontrol-Meldung

Ruft das Handle für das Registerkarten-Steuerelement eines Eigenschaften Blatts ab. Sie können diese Nachricht explizit oder mithilfe des [**propsheet \_ gettabcontrol**](/windows/desktop/api/Prsht/nf-prsht-propsheet_gettabcontrol) -Makros senden.

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

Gibt das Handle für das Registerkarten-Steuerelement zurück.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Diese Meldung wird nicht unterstützt, wenn der Aero Wizard Style ([**PSH \_ aerowizard**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) verwendet wird.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





