---
title: NM_CUSTOMDRAW (Schaltfläche)-Benachrichtigungs Code (kommstrg. h)
description: Benachrichtigt das übergeordnete Fenster eines Schaltflächen-Steuer Elements über benutzerdefinierte Zeichnungsvorgänge auf der Schaltfläche. Das Schaltflächen-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs \_ Meldung.
ms.assetid: cabe5515-ba64-4c53-8746-7a0559df8989
keywords:
- NM_CUSTOMDRAW-Schaltfläche (Schaltfläche) Windows-Steuerelemente
topic_type:
- apiref
api_name:
- NM_CUSTOMDRAW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab3cc4eb73c3a0185131bb6ef2198458888ec89d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479425"
---
# <a name="nm_customdraw-button-notification-code"></a>NM \_ (Schaltfläche)-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines Schaltflächen-Steuer Elements über benutzerdefinierte Zeichnungsvorgänge auf der Schaltfläche.

Das Schaltflächen-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs Meldung. [**\_**](wm-notify.md)


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**nmcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) -Struktur, die Informationen über den Zeichnungs Vorgang enthält. Der **dwitemspec** -Member dieser Struktur enthält den Index des Elements, das gezeichnet wird, und der **litemlparam** -Member dieser Struktur enthält den *LPARAM*-Wert des Elements.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Wert, den die Anwendung zurückgeben kann, hängt von der aktuellen Zeichnungsphase ab. Der **dwdrawstage** -Member der zugeordneten [**nmcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) -Struktur enthält einen Wert, der die Zeichnungsphase angibt. Sie müssen einen der folgenden Werte zurückgeben.



| Rückgabecode                                                                                          | Beschreibung                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**cdrf \_ notifyposterase**</dt> </dl> | Das-Steuerelement benachrichtigt das übergeordnete Element nach dem Löschen eines Elements. Dies kann nur verwendet werden, wenn **dwdrawstage** auf CDDs \_ preerase fest.<br/>                                  |
| <dl> <dt>**cdrf \_ notifypostpaint**</dt> </dl> | Das-Steuerelement benachrichtigt das übergeordnete Element, nachdem ein Element gezeichnet wurde. Dies kann nur verwendet werden, wenn **dwdrawstage** auf CDDs \_ PrePaint fest.<br/>                                 |
| <dl> <dt>**cdrf \_ skipdefault**</dt> </dl>     | Die Anwendung hat das Element manuell gezeichnet. Das-Steuerelement zeichnet das Element nicht. Dies kann verwendet werden, wenn **dwdrawstage** auf CDDs \_ preerase oder CDDs \_ PrePaint fest.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Wenn das Schaltflächen-Steuerelement als "Besitzer zeichnen" gekennzeichnet ist \_ , wird der "nm \_ customdraw"-Benachrichtigungs Code nicht gesendet.

Weitere Informationen finden [Sie unter Verwenden von benutzerdefiniertem zeichnen](custom-draw.md) .

> [!Note]  
> Zur Verwendung dieses Benachrichtigungs Codes müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Kommctrl. h (Include Windows. h)</dt> </dl> |



 

 





