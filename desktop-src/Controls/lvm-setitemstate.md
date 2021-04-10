---
title: LVM_SETITEMSTATE Meldung (kommstrg. h)
description: Ändert den Zustand eines Elements in einem Listenansicht-Steuerelement. Sie können diese Nachricht explizit oder mithilfe des ListView-Objekts "" vom Typ "ListView" senden \_ .
ms.assetid: aecd14dd-cfd0-4c7c-bddc-f65022de68c9
keywords:
- Windows-Steuerelemente für LVM_SETITEMSTATE Meldung
topic_type:
- apiref
api_name:
- LVM_SETITEMSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2120d6d1d2cd3044368ebb343cdf0fe240d805c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103923"
---
# <a name="lvm_setitemstate-message"></a>LVM- \_ Nachricht

Ändert den Zustand eines Elements in einem Listenansicht-Steuerelement. Sie können diese Nachricht explizit oder mithilfe des ListView-Objekts "" vom Typ " [**ListView \_**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemstate) " senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Index des Listen Ansichts Elements. Wenn dieser Parameter-1 ist, wird die Zustandsänderung auf alle Elemente angewendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur. Der **statemask** -Member gibt an, welche Zustands Bits geändert werden sollen, und das **State** -Element enthält die neuen Werte für diese Bits. Die anderen Elemente werden ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn Sie diese Meldung explizit senden, wird **true** zurückgegeben, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Der Zustandswert eines Elements enthält einen Satz von Bitflags, die den Zustand des Elements angeben. Der Statuswert kann auch Bildlisten Indizes enthalten, die das Zustands Bild des Elements und das Überlagerungs Bild angeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





