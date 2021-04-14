---
title: Bildschirm Stile
description: In diesem Thema werden die Stile beschrieben, die mit dem Bildschirm Steuerelement verwendet werden.
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
ms.openlocfilehash: 212e079a59db9a85b6d232d1c11ac9f46eceb314
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391929"
---
# <a name="magnifier-styles"></a>Bildschirm Stile

In diesem Thema werden die Stile beschrieben, die mit dem Bildschirm Steuerelement verwendet werden. Um ein Bildschirm Steuerelement zu erstellen, verwenden Sie die Funktion "die Funktion" ", und geben [**Sie die WC_MAGNIFIER**](/windows/win32/api/winuser/nf-winuser-createwindowexa) Window-Klasse zusammen mit einer Kombination der folgenden Bildschirm Stile an.

| Anforderung | Wert |
|:---|:---|
| MS_CLIPAROUNDCURSOR 0x0002l | Schneidet den Bereich des Vergrößerungs Fensters ab, der den System Cursor umgibt. Dieser Stil ermöglicht dem Benutzer das Anzeigen von Bildschirminhalt, der sich hinter dem Fenster "Bildschirmlupe" befindet. |
| MS_INVERTCOLORS 0x0004l | Zeigt den vergrößerten Bildschirminhalt mithilfe von umgekehrten Farben an. |
| MS_SHOWMAGNIFIEDCURSOR 0x0001l | Zeigt den vergrößerten System Cursor zusammen mit den vergrößerten Bildschirm Inhalten an. |

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Vergrößerung. h</dt> </dl> |

## <a name="see-also"></a>Siehe auch

[Konstanten](entry-magapi-constants.md)
