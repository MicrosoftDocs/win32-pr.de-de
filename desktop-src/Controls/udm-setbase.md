---
title: UDM_SETBASE (Commctrl.h)
description: Legt die Radixbasis für ein Auf-Ab-Steuerelement fest. Der Basiswert bestimmt, ob im Fenster "Fenster" Zahlen in Dezimal- oder Hexadezimalziffern angezeigt werden. Hexadezimalzahlen sind immer ohne Vorzeichen, und Dezimalzahlen werden signiert.
ms.assetid: c76cdec1-e73b-4b4b-89be-9a00ff2ea172
keywords:
- UDM_SETBASE meldungssteuerelemente Windows
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
ms.openlocfilehash: 0f9fd3750a70e676c3e9f32efe9ff0bfd9b300b812d09f4a04c34e4a90f36933
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118669078"
---
# <a name="udm_setbase-message"></a>UDM \_ SETBASE-Nachricht

Legt die Radixbasis für ein Auf-Ab-Steuerelement fest. Der Basiswert bestimmt, ob im Fenster "Fenster" Zahlen in Dezimal- oder Hexadezimalziffern angezeigt werden. Hexadezimalzahlen sind immer ohne Vorzeichen, und Dezimalzahlen werden signiert.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Neuer Basiswert für das Steuerelement. Dieser Parameter kann 10 für decimal oder 16 für hexadezimal sein.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist der vorherige Basiswert. Wenn eine ungültige Basis angegeben wird, ist der Rückgabewert 0 (null).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





