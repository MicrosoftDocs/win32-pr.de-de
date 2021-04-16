---
description: Die phoneclose-Funktion schließt das angegebene Telefongerät.
ms.assetid: 7607d779-0715-48a3-a4f2-bcf07026d7c5
title: Schließen des Telefon Geräts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f137004e63b4b377e9ee88266d11f9c2b21d0af7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527233"
---
# <a name="closing-the-phone-device"></a>Schließen des Telefon Geräts

Die [**phoneclose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) -Funktion schließt das angegebene Telefongerät. Das Telefongerät kann auch zwangsweise geschlossen werden, nachdem der Benutzer die Konfiguration dieses Telefons oder seines Treibers geändert hat. Wenn der Benutzer möchte, dass die Konfigurationsänderungen sofort wirksam werden (im Gegensatz zu nach dem nächsten Neustart des Systems), und Sie sich auf die aktuelle Ansicht des Geräts (z. b. eine Änderung der Gerätefunktionen) auswirken, kann ein Dienstanbieter das Telefongerät schließen.

Diese Nachrichten können auch nicht angefordert werden, weil das Telefongerät auf andere Weise freigegeben wurde. Eine Anwendung sollte daher darauf vorbereitet sein, nicht angeforderte [**Telefon \_ Schließen**](phone-close.md) -Nachrichten zu verarbeiten. Zu dem Zeitpunkt, an dem das Telefongerät geschlossen wird, werden alle ausstehenden asynchronen Antworten in Bezug auf dieses Gerät unterdrückt.

 

 



