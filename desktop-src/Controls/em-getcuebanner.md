---
title: EM_GETCUEBANNER-Nachricht (Commctrl.h)
description: Ruft den Text ab, der als Texthinweis oder Tipp in einem Bearbeitungssteuerelement angezeigt wird.
ms.assetid: 311b783a-cd78-440f-bfc2-f5108ae7d1f8
keywords:
- EM_GETCUEBANNER Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- EM_GETCUEBANNER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e5a47811adcd13c0f2531bd645a9ea607dd68c4dd2c1154f226a54cf108b291
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019718"
---
# <a name="em_getcuebanner-message"></a>EM \_ GETCUEBANNER-Nachricht

Ruft den Text ab, der als Texthinweis oder Tipp in einem Bearbeitungssteuerelement angezeigt wird.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ In\]
</dt> <dd>

Ein Zeiger auf einen Unicode-Puffer, der den Als Text cue festgelegten Text empfängt. Der Aufrufer ist für die Zuweisung des Puffers verantwortlich.

</dd> <dt>

*lParam* \[ In\]
</dt> <dd>

Die Größe des Puffers, auf den *wParam* in **WCHARs** zeigt, einschließlich des abschließenden **NULL-Werts.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

> [!Note]  
> Um diese Meldung verwenden zu können, müssen Sie ein Manifest angeben, das Comclt32.dll Version 6.0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen.](cookbook-overview.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Bearbeiten \_ von GetCueBannerText**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getcuebannertext)
</dt> </dl>

 

 





