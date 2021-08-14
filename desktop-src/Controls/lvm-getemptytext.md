---
title: LVM_GETEMPTYTEXT Meldung (Commctrl.h)
description: Ruft den Text ab, der angezeigt werden soll, wenn das Listenansichtssteuerelement leer angezeigt wird. Senden Sie diese Nachricht explizit oder mithilfe des ListView \_ GetEmptyText-Makros.
ms.assetid: aa6cb0ae-0c6c-42b7-80c5-c086c9579c81
keywords:
- LVM_GETEMPTYTEXT Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- LVM_GETEMPTYTEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9dd1dc1df7b0a558adda37938849b5383bbfee304d807a22a329e4f7301889b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411469"
---
# <a name="lvm_getemptytext-message"></a>LVM \_ GETEMPTYTEXT-Nachricht

Ruft den Text ab, der angezeigt werden soll, wenn das Listenansichtssteuerelement leer angezeigt wird. Senden Sie diese Nachricht explizit oder mithilfe des [**ListView \_ GetEmptyText-Makros.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getemptytext)

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ In\]
</dt> <dd>

Die Größe des Puffers, auf den *lParam* zeigt, einschließlich des abschließenden **NULL-Werts.**

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Ein Zeiger auf einen mit NULL endenden Unicode-Puffer der Größe, der von *wParam* angegeben wird, um den Text zu empfangen. Der Aufrufer ist für die Zuweisung des Puffers verantwortlich.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





