---
title: LVM_GETOUTLINECOLOR Meldung (kommstrg. h)
description: Ruft die Farbe des Rahmens eines Listenansicht-Steuer Elements ab, wenn der \_ \_ Erweiterte Fenster Stil LVS Ex borderselect festgelegt ist.
ms.assetid: cc9d69d1-1470-4eaa-8d54-e31b796cf685
keywords:
- Windows-Steuerelemente für LVM_GETOUTLINECOLOR Meldung
topic_type:
- apiref
api_name:
- LVM_GETOUTLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 489f21f2f6d4dcca2c79d92a13a85d7718a85693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859155"
---
# <a name="lvm_getoutlinecolor-message"></a>LVM \_ getoutlinecolor-Meldung

Ruft die Farbe des Rahmens eines Listenansicht-Steuer Elements ab, wenn der erweiterte Fenster Stil [**LVS \_ Ex \_ borderselect**](extended-list-view-styles.md) festgelegt ist.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt eine **COLORREF** -Struktur zurück, die die Farbe des Rahmens eines Listenansicht-Steuer Elements enthält.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





