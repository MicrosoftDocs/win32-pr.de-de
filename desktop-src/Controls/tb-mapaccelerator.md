---
title: TB_MAPACCELERATOR (Commctrl.h)
description: Bestimmt die ID der Schaltfläche, die dem angegebenen Zugriffstastenzeichen entspricht.
ms.assetid: 724b593d-39af-4301-b721-0332844677b1
keywords:
- TB_MAPACCELERATOR meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- TB_MAPACCELERATOR
- TB_MAPACCELERATORA
- TB_MAPACCELERATORW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f905ccf5ea01e3c06cb87a160a44598c2c4a7790c972f4ee83b245e3ed5c0111
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168084"
---
# <a name="tb_mapaccelerator-message"></a>TB \_ MAPACCELERATOR-Meldung

Bestimmt die ID der Schaltfläche, die dem angegebenen Zugriffstastenzeichen entspricht.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ In\]
</dt> <dd>

Das Zugriffstastenzeichen.

</dd> <dt>

*lParam* \[ out\]
</dt> <dd>

Zeiger auf einen **UINT.** Bei erfolgreicher Rückgabe enthält dieser Parameter die ID der Schaltfläche, die *wParam als* Beschleunigerzeichen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert ungleich 0 (null) zurück, wenn eine der Schaltflächen *wParam* als Beschleunigerzeichen hat, andernfalls 0 (null).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TB \_ MAPACCELERATORW** (Unicode) und **TB \_ MAPACCELERATORA** (ANSI)<br/>       |



 

 





