---
title: CCM_GETVERSION Meldung (kommstrg. h)
description: Ruft die Versionsnummer für ein Steuerelement ab, das von der aktuellen ccm-setVersion-Nachricht festgelegt wird \_ .
ms.assetid: c4b401d7-bba0-430c-b368-c363d49b3411
keywords:
- Windows-Steuerelemente für CCM_GETVERSION Meldung
topic_type:
- apiref
api_name:
- CCM_GETVERSION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bd302774f8821b51a4abaf72bccc403e7302e6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104511"
---
# <a name="ccm_getversion-message"></a>CCM- \_ GetVersion-Meldung

Ruft die Versionsnummer für ein Steuerelement ab, das von der aktuellen [**ccm- \_ setVersion**](ccm-setversion.md) -Nachricht festgelegt wird.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Versionsnummer zurück, die von der aktuellen [**ccm- \_ setVersion**](ccm-setversion.md) -Nachricht festgelegt wurde. Wenn eine solche Nachricht nicht gesendet wurde, wird NULL zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Diese Meldung gibt die dll-Version nicht zurück. Eine Erläuterung der Verwendung von [**dllgetversion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) zum Abrufen der aktuellen dll-Version finden Sie unter [Shell-Versionen](common-control-versions.md) .

> [!Note]  
> Die Versionsnummer wird für ein Steuerelement als Steuerelement festgelegt und ist möglicherweise nicht für alle Steuerelemente identisch.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

