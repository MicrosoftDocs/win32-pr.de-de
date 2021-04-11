---
title: LVM_GETGROUPINFO Meldung (kommstrg. h)
description: Ruft Gruppeninformationen ab.
ms.assetid: 72d84e0b-121e-473b-a34d-874234c598b6
keywords:
- Windows-Steuerelemente für LVM_GETGROUPINFO Meldung
topic_type:
- apiref
api_name:
- LVM_GETGROUPINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b55d5b1d781e7749df97bd0c9f7782f56545dbee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040441"
---
# <a name="lvm_getgroupinfo-message"></a>LVM \_ getgroupinfo-Meldung

Ruft Gruppeninformationen ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Eine ID, die die Gruppe angibt, deren Informationen abgerufen werden.</dd> <dt>

*lParam* 
</dt> <dd>Ein Zeiger auf eine <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**orgroup**</a> -Struktur, die die abgerufenen Informationen empfängt. Legen Sie den **CBSIZE** -Member dieser Struktur auf sizeof (LVGROUP) fest. </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die ID der Gruppe zurück, wenn erfolgreich, andernfalls-1.

## <a name="remarks"></a>Bemerkungen

Bevor Sie versuchen, die Kopfzeile für eine Gruppe abzurufen, stellen Sie zunächst sicher, dass die Gruppe nicht über den lbgs- \_ noheader-Stil verfügt.

> [!Note]  
> Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





