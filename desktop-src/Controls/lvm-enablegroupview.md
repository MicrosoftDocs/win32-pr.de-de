---
title: LVM_ENABLEGROUPVIEW Meldung (kommstrg. h)
description: Aktiviert oder deaktiviert, ob die Elemente in einem Listenansicht-Steuerelement als Gruppe angezeigt werden.
ms.assetid: 783a5e23-d1cb-4523-a6d2-b2cf93fa7f62
keywords:
- Windows-Steuerelemente für LVM_ENABLEGROUPVIEW Meldung
topic_type:
- apiref
api_name:
- LVM_ENABLEGROUPVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1d546e1236fa4f0800c0353810beb5b427ba4fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040112"
---
# <a name="lvm_enablegroupview-message"></a>LVM \_ enablegroupview-Nachricht

Aktiviert oder deaktiviert, ob die Elemente in einem Listenansicht-Steuerelement als Gruppe angezeigt werden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Ein **boolescher** Wert, der angibt, ob ein Listenansicht-Steuerelement zum Gruppieren der angezeigten Elemente aktiviert werden soll. Verwenden Sie **true** , um die Gruppierung zu aktivieren. **false** , um Sie zu deaktivieren </dd> <dt>

*lParam* 
</dt> <dd>Muss **null** sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden Werte zurück.



| Rückgabecode                                                                       | Beschreibung                                                                                  |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**0**</dt> </dl>  | Die Möglichkeit zum Anzeigen von Listen Ansichts Elementen als Gruppe ist bereits aktiviert oder deaktiviert.<br/> |
| <dl> <dt>**1**</dt> </dl>  | Der Zustand des Steuer Elements wurde erfolgreich geändert.<br/>                                |
| <dl> <dt>**-1**</dt> </dl> | Fehler beim Vorgang.<br/>                                                             |



 

## <a name="remarks"></a>Bemerkungen

**LVM \_ Enablegroupview** wird unter dem [**LVS-Besitzer \_ Daten**](list-view-window-styles.md) Stil nicht unterstützt.

> [!Note]  
> Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





