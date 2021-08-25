---
title: LVM_GETVIEW (Commctrl.h)
description: Ruft die aktuelle Ansicht eines Listenansicht-Steuerelements ab.
ms.assetid: dd63e726-3a7f-40e7-8d46-4680816c02a3
keywords:
- LVM_GETVIEW meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- LVM_GETVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 431b0a7b3fba9a45370c372347285489a56082c4a04396c273a45c4da41b05b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915510"
---
# <a name="lvm_getview-message"></a>LVM \_ GETVIEW-Nachricht

Ruft die aktuelle Ansicht eines Listenansicht-Steuerelements ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ein **DWORD zurück,** das die aktuelle Ansicht angibt.

## <a name="remarks"></a>Hinweise

Im Folgenden finden Sie die Werte für Sichten.

-   \_ \_ LV-ANSICHTSDETAILS
-   SYMBOL \_ FÜR \_ LV-ANSICHT
-   LV \_ VIEW \_ LIST
-   LV \_ VIEW \_ SMALLICON
-   KACHEL "LV \_ \_ VIEW"

> [!Note]  
> Um diese Meldung zu verwenden, müssen Sie ein Manifest angeben, das Comclt32.dll 6.0 an. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen.](cookbook-overview.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





