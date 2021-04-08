---
title: NM_RDBLCLK (Listenansicht) Benachrichtigungs Code (kommstrg. h)
description: Wird von einem Listenansicht-Steuerelement gesendet, wenn der Benutzer auf ein Element mit der rechten Maustaste doppelklickt. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: ebbb127f-07bd-48e0-bf38-7bbda5802f70
keywords:
- NM_RDBLCLK (Listenansicht) Windows-Steuerelemente für Benachrichtigungs Code
topic_type:
- apiref
api_name:
- NM_RDBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41832b228fe40b212c0aba809b15022c6f7b39ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957256"
---
# <a name="nm_rdblclk-list-view-notification-code"></a>NM \_ rdblclk (Listenansicht) Benachrichtigungs Code

Wird von einem Listenansicht-Steuerelement gesendet, wenn der Benutzer auf ein Element mit der rechten Maustaste doppelklickt. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
NM_RDBLCLK

    lpnmitem = (LPNMITEMACTIVATE) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

[Version 4,71](common-control-versions.md). Zeiger auf eine [**nmitemaktivierungs**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält. Die Member **iItem**, **iSubItem** und **ptaction** dieser Struktur enthalten Informationen über das Element.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Benachrichtigung wird nicht verwendet.

## <a name="remarks"></a>Bemerkungen

Das **iItem** -Member von *LPARAM* ist nur gültig, wenn auf das Symbol oder die erste Spalten Bezeichnung geklickt wurde. Wenn Sie bestimmen möchten, welches Element ausgewählt wird, wenn ein Klick an einer anderen Stelle in einer Zeile erfolgt, senden Sie eine [**LVM \_ subitemhittest**](lvm-subitemhittest.md) -Nachricht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





