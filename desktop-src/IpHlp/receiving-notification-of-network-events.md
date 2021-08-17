---
description: Verwenden Sie die folgenden Funktionen, um sicherzustellen, dass eine Anwendung Benachrichtigungen über bestimmte Netzwerkereignisse empfängt.
ms.assetid: e1ca5abf-83c2-44f0-8049-ddf1b81ef088
title: Empfangen von Benachrichtigungen über Netzwerkereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28225654bc7e4119f76eff21425e96dda83f628b88d16be9cdfc370d9fa63712
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146613"
---
# <a name="receiving-notification-of-network-events"></a>Empfangen von Benachrichtigungen über Netzwerkereignisse

Verwenden Sie die folgenden Funktionen, um sicherzustellen, dass eine Anwendung Benachrichtigungen über bestimmte Netzwerkereignisse empfängt.

Verwenden Sie die [**Funktion NotifyAddrChange,**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyaddrchange) um eine Benachrichtigung über änderungen anzufordern, die bei der Zuordnung zwischen IP-Adressen und Schnittstellen auf dem lokalen Computer auftreten.

Auf ähnliche Weise ermöglicht die [**Funktion NotifyRouteChange**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyroutechange) einer Anwendung, eine Benachrichtigung über änderungen anzufordern, die in der IP-Routingtabelle auftreten.

Die von diesen Funktionen bereitgestellten Benachrichtigungen geben nicht an, was sich geändert hat. sie geben einfach an, dass sich etwas geändert hat. Verwenden Sie andere IP-Hilfsfunktionen wie [**GetIPAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) und [**GetBestRoute,**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute)um die genaue Art der Änderung zu bestimmen.

 

 



