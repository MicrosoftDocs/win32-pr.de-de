---
title: LVM_SETGROUPINFO Meldung (kommstrg. h)
description: Legt Gruppeninformationen fest.
ms.assetid: f79bd235-e2de-4055-be3e-76eb2744e1ee
keywords:
- Windows-Steuerelemente für LVM_SETGROUPINFO Meldung
topic_type:
- apiref
api_name:
- LVM_SETGROUPINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 688c5b56a57a579e5955fa62a9b44d88258b7afb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040098"
---
# <a name="lvm_setgroupinfo-message"></a>LVM- \_ setgroupinfo-Meldung

Legt Gruppeninformationen fest. Senden Sie diese Nachricht explizit oder mithilfe des [**ListView \_ setgroupinfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setgroupinfo) -Makros.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>ID, die die Gruppe angibt, deren Informationen festgelegt werden sollen.</dd> <dt>

*LPARAM* \[ in, out\]
</dt> <dd>Ein Zeiger auf eine [**orgroup**](windows/win32/api/commctrl/ns-commctrl-lvgroup) -Struktur, die die festzulegenden Informationen enthält.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die ID der Gruppe zurück, wenn erfolgreich, andernfalls-1.

## <a name="remarks"></a>Bemerkungen

Fügen Sie zum Ändern der Gruppen-ID einer vorhandenen Gruppe <b>LVGF_GROUPID</b> zu " <b>LVGROUP. Mask</b> " hinzu, und legen Sie " <b>LVGROUP. igroupid</b> " auf die neue ID fest. Der-Rückruf schlägt fehl, wenn " <b>LVGROUP. igroupid</b> " die ID einer vorhandenen Gruppe enthält.

Um andere Eigenschaften einer vorhandenen Gruppe zu aktualisieren (z. b. das Aktualisieren einer Ausrichtung des Kopf-oder Fußzeilen Texts für die Gruppe, die <b>ualign</b>), darf " <b>LVGROUP. Mask</b> " keine <b>LVGF_GROUPID</b>enthalten. andernfalls schlägt das Update fehl.

> [!Note]  
> Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





