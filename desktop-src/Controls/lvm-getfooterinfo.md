---
title: LVM_GETFOOTERINFO Meldung (kommstrg. h)
description: Ruft Informationen über die Fußzeile eines Listenansicht-Steuer Elements ab. Senden Sie diese Nachricht explizit oder mithilfe des ListView \_ getfooterinfo-Makros.
ms.assetid: 5734e151-50c0-46df-8f2c-220c4910a590
keywords:
- Windows-Steuerelemente für LVM_GETFOOTERINFO Meldung
topic_type:
- apiref
api_name:
- LVM_GETFOOTERINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 718e6c165985981190b5a1d4c52e851d1a2d504d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949425"
---
# <a name="lvm_getfooterinfo-message"></a>LVM- \_ getfooterinfo-Meldung

Ruft Informationen über die Fußzeile eines Listenansicht-Steuer Elements ab. Senden Sie diese Nachricht explizit oder mithilfe des [**ListView \_ getfooterinfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooterinfo) -Makros.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet. Muss den Wert 0 (null) haben.

</dd> <dt>

*LPARAM* \[ in, out\]
</dt> <dd>

Ein Zeiger auf eine " [**lvfooterinfo**](/windows/win32/api/commctrl/ns-commctrl-lvfooterinfo) "-Struktur, die Informationen abhängig vom Wert des **Masken** Elements empfangen soll. Der Aufrufprozess ist dafür verantwortlich, diese Struktur zuzuordnen und das **Masken** Element festzulegen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





