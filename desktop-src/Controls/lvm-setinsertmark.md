---
title: LVM_SETINSERTMARK Meldung (kommstrg. h)
description: Legt die Einfügemarke auf die definierte Position fest.
ms.assetid: 32cf5a11-918a-4dc4-bf10-88b3c26f26cc
keywords:
- Windows-Steuerelemente für LVM_SETINSERTMARK Meldung
topic_type:
- apiref
api_name:
- LVM_SETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dab80b1b73b620ce94b75aecab90f6bdd69bf228
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102883"
---
# <a name="lvm_setinsertmark-message"></a>LVM- \_ Nachricht

Legt die Einfügemarke auf die definierte Position fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Ein Zeiger auf eine <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">lvinsertmark</a> -Struktur, die angibt, wo die Einfügemarke festgelegt wird.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** . **False** wird zurückgegeben, wenn die Größe im **CBSIZE** -Member der [**lvinsertmark**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) -Struktur nicht der tatsächlichen Größe der Struktur entspricht oder wenn in der aktuellen Ansicht keine Einfügemarke angewendet wird.

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



 

 





