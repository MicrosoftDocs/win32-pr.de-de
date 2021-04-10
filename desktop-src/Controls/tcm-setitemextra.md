---
title: TCM_SETITEMEXTRA Meldung (kommstrg. h)
description: Legt die Anzahl von Bytes pro Registerkarte fest, die für Anwendungs definierte Daten in einem Registerkarten-Steuerelement reserviert ist. Sie können diese Nachricht explizit oder mithilfe des tabctrl-Elements tabctrl/ \_ titemextra senden.
ms.assetid: 8315f1fd-8eca-48bd-bb4a-71b09e8aa2c4
keywords:
- Windows-Steuerelemente für TCM_SETITEMEXTRA Meldung
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
ms.openlocfilehash: 9dd6c7fdb47483ae0ddc841ae5f79b8f913e6a4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102855"
---
# <a name="tcm_setitemextra-message"></a>TCM- \_ Nachricht

Legt die Anzahl von Bytes pro Registerkarte fest, die für Anwendungs definierte Daten in einem Registerkarten-Steuerelement reserviert ist. Sie können diese Nachricht explizit oder mithilfe des [**tabctrl-Elements tabctrl/ \_ titemextra**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemextra) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Anzahl zusätzlicher bytes.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Standardmäßig beträgt die Anzahl zusätzlicher Bytes vier. Eine Anwendung, die die Anzahl zusätzlicher Bytes ändert, kann die [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) -Struktur nicht zum Abrufen und Festlegen der Anwendungs definierten Daten für eine Registerkarte verwenden. Stattdessen müssen Sie eine neue Struktur definieren, die aus der [**tcitemheader**](/windows/win32/api/commctrl/ns-commctrl-tcitemheadera) -Struktur gefolgt von Anwendungs definierten Membern besteht.

Eine Anwendung sollte nur die Anzahl zusätzlicher Bytes ändern, wenn ein Registerkarten-Steuerelement keine Registerkarten enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





