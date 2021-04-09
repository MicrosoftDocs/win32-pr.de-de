---
title: LVM_GETINSERTMARK Meldung (kommstrg. h)
description: Ruft die Position der Einfügemarke ab.
ms.assetid: ad00df4c-4b4b-48f1-8821-7849a216df2e
keywords:
- Windows-Steuerelemente für LVM_GETINSERTMARK Meldung
topic_type:
- apiref
api_name:
- LVM_GETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8cba96ae7d357e3e1f5a007fa41f6b7e9e3b64f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858784"
---
# <a name="lvm_getinsertmark-message"></a>LVM \_ getinsertmark-Nachricht

Ruft die Position der Einfügemarke ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Ein Zeiger auf eine <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">lvinsertmark</a> -Struktur, die die Position der Einfügemarke empfängt.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** . **False** wird zurückgegeben, wenn die Größe im **CBSIZE** -Member der [**lvinsertmark**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) -Struktur nicht der tatsächlichen Größe der Struktur entspricht.

## <a name="remarks"></a>Bemerkungen

Eine Einfügemarke kann nur angezeigt werden, wenn sich das Listenansicht-Steuerelement in der Symbol Ansicht, in der kleinen Symbol Ansicht oder in der Kachel Ansicht befindet und sich nicht im gruppenansichts Modus befindet.

> [!Note]  
> Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





