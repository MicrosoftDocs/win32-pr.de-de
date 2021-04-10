---
title: UDM_SETBASE Meldung (kommstrg. h)
description: Legt die Basis für ein auf-ab-Steuerelement fest. Der Basiswert bestimmt, ob das Buddy-Fenster Zahlen in Dezimal-oder hexadezimal Ziffern anzeigt. Hexadezimale Zahlen sind immer unsigniert, und Dezimalzahlen werden signiert.
ms.assetid: c76cdec1-e73b-4b4b-89be-9a00ff2ea172
keywords:
- Windows-Steuerelemente für UDM_SETBASE Meldung
topic_type:
- apiref
api_name:
- UDM_SETBASE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d6bcd7d6154b4ba732e5ffbbec889b326ec8176
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956792"
---
# <a name="udm_setbase-message"></a>UDM- \_ setbase-Nachricht

Legt die Basis für ein auf-ab-Steuerelement fest. Der Basiswert bestimmt, ob das Buddy-Fenster Zahlen in Dezimal-oder hexadezimal Ziffern anzeigt. Hexadezimale Zahlen sind immer unsigniert, und Dezimalzahlen werden signiert.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Neuer Basiswert für das Steuerelement. Dieser Parameter kann für "Decimal" oder "16" für hexadezimale 10 lauten.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist der vorherige Basiswert. Wenn eine ungültige Basis angegeben wird, ist der Rückgabewert 0 (null).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





