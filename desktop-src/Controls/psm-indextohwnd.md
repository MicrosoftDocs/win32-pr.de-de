---
title: PSM_INDEXTOHWND Meldung (prsht. h)
description: Nimmt den Index einer Eigenschaften Blattseite an und gibt das Fenster Handle zurück. Sie können diese Nachricht explizit senden oder das propsheet- \_ indexdehwnd-Makro verwenden.
ms.assetid: 93b46b4c-47f9-4ce8-8797-f3d4bd5248e9
keywords:
- Windows-Steuerelemente für PSM_INDEXTOHWND Meldung
topic_type:
- apiref
api_name:
- PSM_INDEXTOHWND
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 788b1dd0e7312f301051d9a57fcdec43f3f2f72a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105261"
---
# <a name="psm_indextohwnd-message"></a>PSM- \_ Indexdienst-Nachricht

Nimmt den Index einer Eigenschaften Blattseite an und gibt das Fenster Handle zurück. Sie können diese Nachricht explizit senden oder das [**propsheet- \_ indexdehwnd**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextohwnd) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der null basierte Index der Seite.

</dd> <dt>

*lParam* 
</dt> <dd>

Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle für das Fenster der Eigenschaften Blattseite zurück, das bei erfolgreicher Ausführung von *wParam* angegeben wurde. Andernfalls wird 0 (null) zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





