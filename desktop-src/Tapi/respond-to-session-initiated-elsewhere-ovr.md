---
description: Wenn eine neue Kommunikationssitzung eintrifft, werden TAPI-Anwendungen, die ein Interesse an der Adresse und dem Medientyp registriert haben, eine Ereignis Benachrichtigung gesendet.
ms.assetid: 6074619c-6aa0-4b03-9208-10268682e704
title: Reagieren auf die an anderer Stelle initiierte Sitzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e25651b58f8841ac4de9bf14f4d139161c1359
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366267"
---
# <a name="respond-to-session-initiated-elsewhere"></a>Reagieren auf die an anderer Stelle initiierte Sitzung

Wenn eine neue Kommunikationssitzung eintrifft, werden TAPI-Anwendungen, die ein Interesse an der [Adresse](address-ovr.md) und dem [Medientyp](media-type-ovr.md) registriert haben, eine [Ereignis Benachrichtigung](event-notification.md)gesendet. Nur eine Anwendung erhält Besitz [Rechte](privilege-ovr.md) für die Sitzung. Diese Anwendung kann die Sitzung nicht ablehnen.

Der erste Ansichts Zustand einer eingehenden Sitzung ist "Angebot". Während sich der-Befehl im Angebots Zustand befindet, kann eine Anwendung Informationen wie den bearermodus und den Abruf Grund abrufen, wenn die Dienstanbieter diese Informationen bereitgestellt haben und verfügbar sind. Einige Aufruf Informationen sind möglicherweise nicht sofort verfügbar, z. b. die Aufruferkennung.

Es gibt sechs einfache Antworten auf eine angebotene Sitzung: " [Answer](answer-ovr.md)", " [Accept](accept-ovr.md)", " [Übergabe](handoffs-ovr.md)", " [Drop](drop-ovr.md)", " [Forward](forward-ovr.md)" und " [Redirect](redirect-ovr.md) Abhängig vom Dienstanbieter ist der vollständige Satz dieser Vorgänge möglicherweise nicht verfügbar.

 

 



