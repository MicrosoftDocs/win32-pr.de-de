---
title: Automatisieren der Wiedergabe
description: Automatisieren der Wiedergabe
ms.assetid: 3aa05a54-58d7-4d14-93ee-459aa860b20e
keywords:
- MCIWndCreate-Makro
- MCIWndPlay-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad1c05041bade08f47505a2cf1207739777c5af825ea9f5f300b343b87efe3c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691970"
---
# <a name="automating-playback"></a>Automatisieren der Wiedergabe

Sie können die Wiedergabe in Ihrer Anwendung automatisieren, indem Sie [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) und das [**MCIWndPlay-Makro**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) zusammen mit dem [**Makro MCIWndDestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy) oder [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) verwenden. Um die Wiedergabe zu automatisieren, geben Sie die Stile MCIWNDF \_ NOPLAYBAR und MCIWNDF NOTIFYMODE im \_ Parameter **MCIWndCreate**_dwStyle_ an. Geben Sie den MCIWNDF NOPLAYBAR-Stil an, um die Symbolleiste auszublenden, und den \_ MCIWNDF NOTIFYMODE-Stil, um eine entsprechende Benachrichtigung auszustellen, wenn das Gerät die Wiedergabe \_ beendet.

Sie können das in **MCIWndCreate** angegebene Gerät oder die Datei mithilfe von **MCIWndPlay wieder geben.** Das MCIWndPlay-Makro beginnt mit der Wiedergabe des Inhalts von seiner aktuellen Wiedergabeposition bis zum Ende.

Sie können ein MCIWnd-Fenster mithilfe des Makros [**MCIWndDestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy) oder [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) zerstören oder schließen. Das **MCIWndDestroy-Makro** schließt das Gerät oder die Datei und zerstört das MCIWnd-Fenster, indem es sein Handle ungültig macht. Wenn Ihre Anwendung das MCIWnd-Fenster wiederverwenden kann, verwenden Sie **MCIWndClose,** um das Gerät zu schließen, ohne das Fenster zu zerstören.

Ihre Anwendung kann erkennen, wann das Gerät die Wiedergabe beendet, und das Fenster automatisch schließen. Geben Sie hierzu den MCIWNDF NOTIFYMODE-Stil für \_ den *dwStyle-Parameter* von [**MCIWndCreate an.**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) Dies bewirkt, dass das Gerät immer dann [**eine MCIWNDM \_ NOTIFYMODE-Nachricht**](mciwndm-notifymode.md) sendet, wenn es den Modus ändert. Ihre Anwendung kann diese Nachricht abfangen, um zu ermitteln, ob die Wiedergabe des Geräts beendet wurde. Wenn das Gerät die Wiedergabe beendet, schließt die Anwendung das Fenster.

 

 




