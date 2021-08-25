---
title: LVM_SETVIEW (Commctrl.h)
description: Legt die Ansicht eines Listenansicht-Steuerelements fest.
ms.assetid: e6d3f16d-52ea-4863-a6c9-9a085d5f794a
keywords:
- LVM_SETVIEW meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- LVM_SETVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd8d07b636a14624632d0e41ebcf6db66f420b9df4f8ca852e55ab2f3e1578e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119656200"
---
# <a name="lvm_setview-message"></a>LVM \_ SETVIEW-Meldung

Legt die Ansicht eines Listenansicht-Steuerelements fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>**DWORD,** das die Sicht angibt.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 1 zurück, wenn erfolgreich, andernfalls -1. Beispielsweise wird -1 zurückgegeben, wenn die Sicht ungültig ist.

## <a name="remarks"></a>Hinweise

Im Folgenden finden Sie die Werte für Sichten.

-   \_ \_ LV-ANSICHTSDETAILS
-   SYMBOL \_ FÜR \_ LV-ANSICHT
-   LV \_ VIEW \_ LIST
-   LV \_ VIEW \_ SMALLICON
-   KACHEL "LV \_ \_ VIEW"

> [!Note]  
> Um diese Meldung zu verwenden, müssen Sie ein Manifest angeben, das Comctl32.dll 6.0 an. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen.](cookbook-overview.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





