---
title: LVM_GETEMPTYTEXT Meldung (kommstrg. h)
description: Ruft den Text ab, der für die Anzeige bestimmt ist, wenn das Listenansicht-Steuerelement leer erscheint. Senden Sie diese Nachricht explizit oder mithilfe des ListView \_ getemptytext-Makros.
ms.assetid: aa6cb0ae-0c6c-42b7-80c5-c086c9579c81
keywords:
- Windows-Steuerelemente für LVM_GETEMPTYTEXT Meldung
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
ms.openlocfilehash: 7549081ef7f158a6a6a061bcee9669ea62d52f68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475168"
---
# <a name="lvm_getemptytext-message"></a>LVM- \_ getemptytext-Nachricht

Ruft den Text ab, der für die Anzeige bestimmt ist, wenn das Listenansicht-Steuerelement leer erscheint. Senden Sie diese Nachricht explizit oder mithilfe des [**ListView \_ getemptytext**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getemptytext) -Makros.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Die Größe des Puffers, auf den *LPARAM* zeigt, einschließlich des abschließenden **null**-Werte.

</dd> <dt>

*LPARAM* \[ in, out\]
</dt> <dd>

Ein Zeiger auf einen null-terminierten Unicode-Puffer der Größe, der von *wParam* angegeben wird, um den Text zu empfangen. Der Aufrufer ist für die Zuordnung des Puffers verantwortlich.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





