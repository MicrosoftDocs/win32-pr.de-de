---
title: Automatisieren der Wiedergabe
description: Automatisieren der Wiedergabe
ms.assetid: 3aa05a54-58d7-4d14-93ee-459aa860b20e
keywords:
- Mciwndcreate-Makro
- Mciwndplay-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6097d38b3d468b6de68ee7e11f98f530aff00d2b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714075"
---
# <a name="automating-playback"></a>Automatisieren der Wiedergabe

Sie können die Wiedergabe in der Anwendung automatisieren, indem Sie [**mciwndcreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) und das Makro mciwndplay zusammen mit dem [**mciwnddestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy) -Makro oder dem mciwndclose-Makro verwenden. [](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) [](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) Um die Wiedergabe zu automatisieren, geben Sie die Stile mciwndf \_ noplaybar und mciwndf \_ notifymode im Parameter **mciwndcreate * * * dwstyle* an. Geben Sie den mciwndf \_ -noplaybar-Stil zum Ausblenden der Symbolleiste und den mciwndf- \_ Stil "notifymode" an, um eine entsprechende Benachrichtigungs Meldung auszugeben, wenn das Gerät beendet wird.

Sie können das in **mciwndcreate** angegebene Gerät oder die Datei mit **mciwndplay** wiedergeben. Das mciwndplay-Makro beginnt mit der Wiedergabe des Inhalts von der aktuellen Wiedergabe Position bis zum Ende.

Sie können ein mciwnd-Fenster mit dem [**mciwnddestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy) -oder [**mciwndclose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) -Makro zerstören oder schließen. Das **mciwnddestroy** -Makro schließt das Gerät oder die Datei und zerstört das mciwnd-Fenster, indem das Handle ungültig wird. Wenn die Anwendung das mciwnd-Fenster wieder verwenden kann, verwenden Sie **mciwndclose** , um das Gerät zu schließen, ohne das Fenster zu zerstören.

Die Anwendung kann erkennen, wenn das Gerät beendet wird und das Fenster automatisch schließt. Geben Sie hierzu den mciwndf- \_ notifymode-Stil für den *dwstyle* -Parameter von [**mciwndcreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea)an. Dies bewirkt, dass das Gerät immer dann eine [**mciwndm- \_ Benachrichtigung**](mciwndm-notifymode.md) sendet, wenn der Modus geändert wird. Ihre Anwendung kann diese Nachricht abfangen, um zu bestimmen, ob das Gerät beendet wurde. Wenn die Wiedergabe des Geräts beendet wird, schließt die Anwendung das Fenster.

 

 




