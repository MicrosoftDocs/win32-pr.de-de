---
title: Bildschirmlupestile
description: In diesem Thema werden die Stile beschrieben, die mit dem Bildschirmlupesteuerelement verwendet werden.
ms.assetid: B3C575AC-B8D3-40CF-AF09-BAC73E6C7B45
topic_type:
- apiref
api_name:
- MS_CLIPAROUNDCURSOR
- MS_INVERTCOLORS
- MS_SHOWMAGNIFIEDCURSOR
api_location:
- Magnification.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: ef65f736b50210ed52c542375aa340d5bd85ae38265a71858d82e069d830aa62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052578"
---
# <a name="magnifier-styles"></a>Bildschirmlupestile

In diesem Thema werden die Stile beschrieben, die mit dem Bildschirmlupesteuerelement verwendet werden. Verwenden Sie zum Erstellen eines Bildschirmlupesteuerelements die [**CreateWindowEx-Funktion,**](/windows/win32/api/winuser/nf-winuser-createwindowexa) und geben Sie die WC_MAGNIFIER-Fensterklasse zusammen mit einer Kombination der folgenden Bildschirmlupe an.

| Anforderung | Wert |
|:---|:---|
| MS_CLIPAROUNDCURSOR 0x0002L | Klammern sie den Bereich des Bildschirmlupefensters, das den Systemcursor umgibt. Mit diesem Stil kann der Benutzer Bildschirminhalte anzeigen, die sich hinter dem Bildschirmlupefenster befindet. |
| MS_INVERTCOLORS 0x0004L | Zeigt den vergrößerten Bildschirminhalt mit invertierten Farben an. |
| MS_SHOWMAGNIFIEDCURSOR 0x0001L | Zeigt den vergrößerten Systemcursor zusammen mit dem vergrößerten Bildschirminhalt an. |

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Vergrößerung.h</dt> </dl> |

## <a name="see-also"></a>Siehe auch

[Konstanten](entry-magapi-constants.md)
