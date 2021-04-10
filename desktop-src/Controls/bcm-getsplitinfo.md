---
title: BCM_GETSPLITINFO Meldung (kommstrg. h)
description: Ruft Informationen für ein unterteilte Schaltflächen Steuerelement ab. Senden Sie diese Nachricht explizit oder mithilfe des Schaltflächen \_ getsplitinfo-Makros.
ms.assetid: d608440d-b8d8-4e32-9128-08b7566b185c
keywords:
- Windows-Steuerelemente für BCM_GETSPLITINFO Meldung
topic_type:
- apiref
api_name:
- BCM_GETSPLITINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 162c5522fcb432e3d512f688ae24aa12d4d0d8e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956544"
---
# <a name="bcm_getsplitinfo-message"></a>BCM \_ getsplitinfo-Meldung

Ruft Informationen für ein unterteilte Schaltflächen Steuerelement ab. Senden Sie diese Nachricht explizit oder mithilfe des [**Schaltflächen \_ getsplitinfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_getsplitinfo) -Makros.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*LPARAM* \[ in, out\]
</dt> <dd>

Ein Zeiger auf eine [**\_ splitinfo**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) -Struktur der Schaltfläche, um Informationen über die Schaltfläche zu erhalten. Der Aufrufer ist dafür verantwortlich, den Arbeitsspeicher für die Struktur zuzuordnen. Legen Sie den **Mask** -Member dieser Struktur fest, um zu bestimmen, welche Informationen empfangen werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Meldung nur mit den Schaltflächen Stilen [**\_ SplitButton**](button-styles.md) und [**SB \_ defsplitbutton**](button-styles.md) .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[Schaltflächenstile](button-styles.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Schaltflächentypen](button-types-and-styles.md)
</dt> </dl>

 

 





