---
description: Verwenden Sie die folgenden Funktionen, um sicherzustellen, dass eine Anwendung Benachrichtigungen über bestimmte Netzwerkereignisse empfängt.
ms.assetid: e1ca5abf-83c2-44f0-8049-ddf1b81ef088
title: Empfangen von Benachrichtigungen über Netzwerkereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecb9840f7ddf4adbfaae5775de337da81a3e7670
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345085"
---
# <a name="receiving-notification-of-network-events"></a>Empfangen von Benachrichtigungen über Netzwerkereignisse

Verwenden Sie die folgenden Funktionen, um sicherzustellen, dass eine Anwendung Benachrichtigungen über bestimmte Netzwerkereignisse empfängt.

Verwenden Sie die [**notifyaddrchange**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyaddrchange) -Funktion, um eine Benachrichtigung über jede Änderung anzufordern, die bei der Zuordnung zwischen IP-Adressen und Schnittstellen auf dem lokalen Computer auftritt.

Ebenso ermöglicht die [**notifyroutechange**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyroutechange) -Funktion einer Anwendung, eine Benachrichtigung über jede Änderung anzufordern, die in der IP-Routing Tabelle auftritt.

Die von diesen Funktionen bereitgestellten Benachrichtigungen geben nicht an, was geändert wurde. Sie geben einfach an, dass sich etwas geändert hat. Verwenden Sie andere IP-Hilfsfunktionen, wie z. b. [**getipaddrtable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) und [**getbestroute**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute), um die genaue Natur der Änderung zu ermitteln.

 

 



