---
title: LVM_INSERTMARKHITTEST Meldung (kommstrg. h)
description: Ruft die Einfügemarke ab, die einem angegebenen Punkt am nächsten ist.
ms.assetid: 901bb770-a36d-4d9f-a53b-d497b4df39e5
keywords:
- Windows-Steuerelemente für LVM_INSERTMARKHITTEST Meldung
topic_type:
- apiref
api_name:
- LVM_INSERTMARKHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bdb82e924b4a5d74d152917f52c4039e0aca81b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105477"
---
# <a name="lvm_insertmarkhittest-message"></a>LVM \_ insertmarkhittest-Meldung

Ruft die Einfügemarke ab, die einem angegebenen Punkt am nächsten ist.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Zeiger auf eine **Punkt** Struktur, die die Treffer Test Koordinaten enthält.</dd> <dt>

*lParam* 
</dt> <dd>Ein Zeiger auf eine <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">lvinsertmark</a> -Struktur, die die Einfügemarke angibt, die den durch den *wParam* -Parameter definierten Koordinaten am nächsten liegt.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** . **False** wird zurückgegeben, wenn die Größe im **CBSIZE** -Member der [**lvinsertmark**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) -Struktur nicht der tatsächlichen Größe der Struktur entspricht oder wenn in der aktuellen Ansicht keine Einfügemarke angewendet wird.

## <a name="remarks"></a>Bemerkungen

Eine Einfügemarke kann nur angezeigt werden, wenn sich das Listenansicht-Steuerelement in der Symbol Ansicht, in der kleinen Symbol Ansicht oder in der Kachel Ansicht befindet und sich nicht im gruppenansichts Modus befindet.

Wenn für die Ansicht keine Einfügepunkte gelten, enthält die [**lvinsertmark**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) -Struktur im **iItem** -Member den Eintrag-1.

> [!Note]  
> Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





