---
title: LVM_SETINSERTMARKCOLOR (Commctrl.h)
description: Legt die Farbe der Einfügemarke fest.
ms.assetid: dce2c266-672b-4682-ba23-51d9a8e1102b
keywords:
- LVM_SETINSERTMARKCOLOR von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- LVM_SETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 135275faa83f16956cfdeab90aaddded93caf2127f57c395a83deb4b29dd442a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919840"
---
# <a name="lvm_setinsertmarkcolor-message"></a>LVM \_ SETINSERTMARKCOLOR-Meldung

Legt die Farbe der Einfügemarke fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>**COLORREF-Struktur,** die die Farbe angibt, in der die Einfügemarke festgelegt werden soll.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **die COLORREF-Struktur** zurück, die auf die vorherige Farbe festgelegt ist.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Um diese Meldung zu verwenden, müssen Sie ein Manifest angeben, das Comclt32.dll 6.0 an. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen.](cookbook-overview.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





