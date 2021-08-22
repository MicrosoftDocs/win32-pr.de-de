---
title: CCM_GETVERSION Meldung (Commctrl.h)
description: Ruft die Versionsnummer für ein Steuerelement ab, das durch die letzte CCM \_ SETVERSION-Nachricht festgelegt wurde.
ms.assetid: c4b401d7-bba0-430c-b368-c363d49b3411
keywords:
- CCM_GETVERSION Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: fb1ad49ebb00d5d57555bb07be1bcf78ab97115ada43e18a7f81cda93e29fa1a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119320260"
---
# <a name="ccm_getversion-message"></a>CCM \_ GETVERSION-Nachricht

Ruft die Versionsnummer für ein Steuerelement ab, das durch die letzte [**CCM \_ SETVERSION-Nachricht**](ccm-setversion.md) festgelegt wurde.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Versionsnummer zurück, die von der neuesten [**CCM \_ SETVERSION-Nachricht**](ccm-setversion.md) festgelegt wurde. Wenn keine solche Nachricht gesendet wurde, wird 0 (null) zurückgegeben.

## <a name="remarks"></a>Hinweise

Diese Meldung gibt die DLL-Version nicht zurück. Unter [Shellversionen](common-control-versions.md) erfahren Sie, wie [**Sie dllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) zum Abrufen der aktuellen DLL-Version verwenden.

> [!Note]  
> Die Versionsnummer wird auf Steuerelementbasis festgelegt und ist möglicherweise nicht für alle Steuerelemente identisch.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

