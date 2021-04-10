---
title: LVM_SETTILEINFO Meldung (kommstrg. h)
description: Legt Informationen für eine vorhandene Kachel eines Listenansicht-Steuer Elements fest.
ms.assetid: 345e8f16-9a6c-44e3-a262-d5d3be4d33ef
keywords:
- Windows-Steuerelemente für LVM_SETTILEINFO Meldung
topic_type:
- apiref
api_name:
- LVM_SETTILEINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 489e163955b8f9cbf99ad25357b5be5a5d5981fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103354"
---
# <a name="lvm_settileinfo-message"></a>LVM- \_ settileinfo-Nachricht

Legt Informationen für eine vorhandene Kachel eines Listenansicht-Steuer Elements fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Zeiger auf eine <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileinfo">**lvtileinfo**</a> -Struktur, die die festzulegenden Informationen enthält.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

**LVM \_ Settileingefo** wird unter dem [**LVS-Besitzer \_ Daten**](list-view-window-styles.md) Stil nicht unterstützt.

> [!Note]  
> Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





