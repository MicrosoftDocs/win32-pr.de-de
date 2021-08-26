---
title: TCM_SETITEMEXTRA Meldung (Commctrl.h)
description: Legt die Anzahl der Bytes pro Registerkarte fest, die für anwendungsdefinierte Daten in einem Registerkartensteuerelement reserviert sind. Sie können diese Nachricht explizit oder mithilfe des \_ TabCtrl-Makros SetItemExtra senden.
ms.assetid: 8315f1fd-8eca-48bd-bb4a-71b09e8aa2c4
keywords:
- TCM_SETITEMEXTRA Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TCM_SETITEMEXTRA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f92fb85f7133053392bee39119c91b55240f84f0a51c8acc7dc9c732b596526c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104760"
---
# <a name="tcm_setitemextra-message"></a>TCM \_ SETITEMEXTRA-Nachricht

Legt die Anzahl der Bytes pro Registerkarte fest, die für anwendungsdefinierte Daten in einem Registerkartensteuerelement reserviert sind. Sie können diese Nachricht explizit oder mithilfe des [**\_ TabCtrl-Makros SetItemExtra**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemextra) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Anzahl zusätzlicher Bytes.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

Standardmäßig beträgt die Anzahl zusätzlicher Bytes vier. Eine Anwendung, die die Anzahl zusätzlicher Bytes ändert, kann die [**TCITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-tcitema) nicht verwenden, um die von der Anwendung definierten Daten für eine Registerkarte abzurufen und festzulegen. Stattdessen müssen Sie eine neue Struktur definieren, die aus der [**TCITEMHEADER-Struktur**](/windows/win32/api/commctrl/ns-commctrl-tcitemheadera) gefolgt von anwendungsdefinierte Member besteht.

Eine Anwendung sollte die Anzahl zusätzlicher Bytes nur ändern, wenn ein Registerkartensteuerelement keine Registerkarten enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





