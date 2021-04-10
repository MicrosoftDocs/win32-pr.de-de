---
title: TTM_TRACKACTIVATE Meldung (kommstrg. h)
description: Aktiviert oder deaktiviert eine nach Verfolgungs-QuickInfo.
ms.assetid: 6cf43377-a772-4749-81c4-a685998092e5
keywords:
- Windows-Steuerelemente für TTM_TRACKACTIVATE Meldung
topic_type:
- apiref
api_name:
- TTM_TRACKACTIVATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb3d0a6caf110045d694208c63aa81d63c265c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956714"
---
# <a name="ttm_trackactivate-message"></a>TTM \_ trackaktivierungs Meldung

Aktiviert oder deaktiviert eine nach Verfolgungs-QuickInfo.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Wert, der angibt, ob die Überwachung aktiviert oder deaktiviert wird. Die folgenden Werte sind möglich:



| Wert                                                                                                                                | Bedeutung                         |
|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>**Fall**</dt> </dl>    | Aktivieren Sie die Überwachung.<br/>   |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>**Alarm**</dt> </dl> | Deaktivieren Sie die Überwachung.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur, die das Tool identifiziert, für das diese Meldung gilt. Die **HWND** -und **UID** -Member identifizieren das Tool, und das **CBSIZE** -Element gibt die Größe der Struktur an. Alle anderen Member werden ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Nachricht wird nicht verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**TTM \_ trackposition**](ttm-trackposition.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Verwenden von Quick Infos](using-tooltip-contro.md)
</dt> </dl>

 

 





