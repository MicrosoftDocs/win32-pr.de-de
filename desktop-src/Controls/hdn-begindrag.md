---
title: HDN_BEGINDRAG Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Header-Steuerelement gesendet, wenn ein Zieh Vorgang für eines der Elemente begonnen hat. Dieser Benachrichtigungs Code wird nur von Header Steuerelementen gesendet, die auf den HDS DragDrop-Stil festgelegt sind \_ . Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 3dfb7a7c-d783-48e0-ba92-8144104f163a
keywords:
- Windows-Steuerelemente für HDN_BEGINDRAG Benachrichtigungs
topic_type:
- apiref
api_name:
- HDN_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed6b4af8e662a8a9891e9a81535de987337567f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040540"
---
# <a name="hdn_begindrag-notification-code"></a>\_Benachrichtigungs Code für Hdn BeginDrag

Wird von einem Header-Steuerelement gesendet, wenn ein Zieh Vorgang für eines der Elemente begonnen hat. Dieser Benachrichtigungs Code wird nur von Header Steuerelementen gesendet, die auf den [**HDS \_ DragDrop**](header-control-styles.md) -Stil festgelegt sind. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
HDN_BEGINDRAG

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) -Struktur, die Informationen über das Header Element enthält, das gezogen wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Um dem Header Steuerelement das automatische Verwalten von Drag & Drop-Vorgängen zu ermöglichen, wird **false** zurückgegeben. Wenn der Besitzer des Steuer Elements die Neuanordnung per Drag & Drop manuell ausführt, wird **true** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Ein Header Steuerelement verwendet standardmäßig die automatische Verwaltung der Drag & Drop-Neuanordnung. Wenn " **true** " zurückgegeben wird, um die externe (manuelle) Drag & Drop-Verwaltung anzugeben, kann der Besitzer des Steuer Elements benutzerdefinierte Dienste als Teil des Drag & Drop-Prozesses bereitstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





