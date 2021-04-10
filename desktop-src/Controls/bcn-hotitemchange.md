---
title: BCN_HOTITEMCHANGE Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt den Besitzer des Button-Steuer Elements, dass die Maus in den Client Bereich des Schaltflächen-Steuer Elements wechselt oder diesen verlässt. Das Schaltflächen-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs \_ Meldung.
ms.assetid: 92882e21-b69d-4326-94e9-ae69a0d00a83
keywords:
- Windows-Steuerelemente für BCN_HOTITEMCHANGE Benachrichtigungs
topic_type:
- apiref
api_name:
- BCN_HOTITEMCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67ba6a7e64e95b45d0883b5adf34b384bccac8c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040448"
---
# <a name="bcn_hotitemchange-notification-code"></a>BCN-Warnungs \_ Änderungs Benachrichtigungs Code

Benachrichtigt den Besitzer des Button-Steuer Elements, dass die Maus in den Client Bereich des Schaltflächen-Steuer Elements wechselt oder diesen verlässt. Das Schaltflächen-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs Meldung. [**\_**](wm-notify.md)


```C++
BCN_HOTITEMCHANGE

    pnmbchotitem = (NMBCHOTITEM*) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**nmbchotitem**](/windows/win32/api/commctrl/ns-commctrl-nmbchotitem) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Zur Verwendung dieses Benachrichtigungs Codes müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





