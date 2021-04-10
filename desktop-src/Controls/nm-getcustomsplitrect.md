---
title: NM_GETCUSTOMSPLITRECT Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Schaltflächen-Steuerelement an das übergeordnete Steuerelement gesendet, um Messungen für die beiden Rechtecke der unterteilten Schaltfläche Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: ce72778d-3cca-46a4-9d05-40954a18681d
keywords:
- Windows-Steuerelemente für NM_GETCUSTOMSPLITRECT Benachrichtigungs
topic_type:
- apiref
api_name:
- NM_GETCUSTOMSPLITRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97b839540da7e07069fdf56ed656ed8772d029eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102879"
---
# <a name="nm_getcustomsplitrect-notification-code"></a>NM \_ getcustomsplitrect-Benachrichtigungs Code

Wird von einem Schaltflächen-Steuerelement an das übergeordnete Steuerelement gesendet, um Messungen für die beiden Rechtecke der unterteilten Schaltfläche Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
NM_GETCUSTOMSPLITRECT
        
    nmCustomSplit = (NMCUSTOMSPLITRECTINFO *) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**nmcustomsplitrectinfo**](/windows/win32/api/commctrl/ns-commctrl-nmcustomsplitrectinfo) , um umschließende Rechtecke-Informationen zu erhalten. Die **nmcustomsplitrectinfo** -Struktur wird mit dem Benachrichtigungs Code als Anforderung gesendet, dass das übergeordnete Element Messungen für die Rechtecke der unterteilten Schaltfläche bereitstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt [**cdrf \_ skipdefault**](cdrf-constants.md) zurück, um das Schaltflächen-Steuerelement anzuweisen, die in der [**nmcustomsplitrectinfo**](/windows/win32/api/commctrl/ns-commctrl-nmcustomsplitrectinfo) -Struktur zurückgegebenen Werte zu verwenden; andernfalls wird [**cdrf \_ DODEFAULT**](cdrf-constants.md)zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Dieser Benachrichtigungs Code wird von einem Schaltflächen-Steuerelement gesendet, bevor es gezeichnet wird. Die Schaltfläche muss im Format " [**SB \_ SplitButton**](button-styles.md) " oder " [**SB \_ defsplitbutton**](button-styles.md)" lauten. Wenn die an das Steuerelement in *LPARAM* zurückgegebenen Rechtecke nicht gültig sind, werden Sie ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





