---
title: PSM_INDEXTOHWND (Prsht.h)
description: Verwendet den Index einer Eigenschaftenblattseite und gibt dessen Fensterhandpunkt zurück. Sie können diese Nachricht explizit senden oder das PropSheet \_ IndexToHwnd-Makro verwenden.
ms.assetid: 93b46b4c-47f9-4ce8-8797-f3d4bd5248e9
keywords:
- PSM_INDEXTOHWND meldungssteuerelemente Windows
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
ms.openlocfilehash: ff0c170d1a9ce1586adbfc49c6e265002f9b638a8fc01766ab0a98db66044d58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078844"
---
# <a name="psm_indextohwnd-message"></a>PSM \_ INDEXTOHWND-Nachricht

Verwendet den Index einer Eigenschaftenblattseite und gibt dessen Fensterhandpunkt zurück. Sie können diese Nachricht explizit senden oder das [**PropSheet \_ IndexToHwnd-Makro**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextohwnd) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nullbasierter Index der Seite.

</dd> <dt>

*lParam* 
</dt> <dd>

Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle an das Fenster der Eigenschaftenblattseite zurück, das *von wParam bei Erfolg* angegeben wird. Andernfalls wird 0 (null) zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





