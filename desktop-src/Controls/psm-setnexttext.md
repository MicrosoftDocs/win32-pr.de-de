---
title: PSM_SETNEXTTEXT (Prsht.h)
description: Legt den Text der Schaltfläche Weiter in einem Assistenten fest. Sie können diese Nachricht explizit oder mit dem PropSheet \_ SetNextText-Makro senden.
ms.assetid: 4608425e-1724-4d0b-b0f6-9fec147a85f6
keywords:
- PSM_SETNEXTTEXT von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- PSM_SETNEXTTEXT
- PSM_SETNEXTTEXTW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d177acb2f2c96e12f5dc4b460ee88149ad81f9b4f79cc3505f776d8f1f92551
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118410080"
---
# <a name="psm_setnexttext-message"></a>PSM \_ SETNEXTTEXT-Meldung

Legt den Text der Schaltfläche **Weiter** in einem Assistenten fest. Sie können diese Nachricht explizit oder mit dem [**PropSheet \_ SetNextText-Makro**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setnexttext) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf einen Puffer, der den Text enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein sinnvoller Rückgabewert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **PSM \_ SETNEXTTEXTW** (Unicode)<br/>                                         |



 

 





