---
title: LVM_SETOUTLINECOLOR Meldung (kommstrg. h)
description: Legt die Farbe des Rahmens eines Listenansicht-Steuer Elements fest, wenn der \_ \_ Erweiterte Fenster Stil LVS Ex borderselect festgelegt ist.
ms.assetid: c2b606fa-8d47-4192-94b7-d01c3cfdc514
keywords:
- Windows-Steuerelemente für LVM_SETOUTLINECOLOR Meldung
topic_type:
- apiref
api_name:
- LVM_SETOUTLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 776cb13479e4d091d394941844691c117a4ebbef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858653"
---
# <a name="lvm_setoutlinecolor-message"></a>LVM- \_ setoutlinecolor-Meldung

Legt die Farbe des Rahmens eines Listenansicht-Steuer Elements fest, wenn der erweiterte Fenster Stil [**LVS \_ Ex \_ borderselect**](extended-list-view-styles.md) festgelegt ist.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>**COLORREF** -Struktur, die die Farbe zum Festlegen des Rahmens angibt.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt eine **COLORREF** -Struktur zurück, die die Kontur Farbe enthält.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





