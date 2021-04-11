---
description: IPv6-Link-Local-Adressierung in SOAP-Nachrichten stellt eine eindeutige Herausforderung dar, da IPv6-Link-Local-Adressen erfordern, dass eine Bereichs-ID sinnvoll ist, die Bereichs-ID jedoch nur für den lokalen Computer Bedeutung ist.
ms.assetid: 63495335-e447-4564-b669-0896c7aac63f
title: Verwenden von IPv6-Link-Local-Adressen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c89356042e8a71b0af19337b7013b8abd1e8a354
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130389"
---
# <a name="using-ipv6-link-local-addresses"></a>Verwenden von IPv6-Link-Local-Adressen

IPv6-Link-Local-Adressierung in SOAP-Nachrichten stellt eine eindeutige Herausforderung dar, da IPv6-Link-Local-Adressen erfordern, dass eine Bereichs-ID sinnvoll ist, die Bereichs-ID jedoch nur für den lokalen Computer Bedeutung ist. Alle Client-und Geräte Implementierungen müssen die Bereichs-ID entfernen, bevor Sie eine IPv6-Link-Local-Adresse in einer SOAP-Nachricht senden. Wenn eine IPv6-Link-Local-Adresse in einer Nachricht empfangen wird, muss außerdem die Schnittstelle bekannt sein, auf der die Nachricht empfangen wurde, damit die gesamte Verknüpfungs lokale Adresse mit der Bereichs-ID rekonstruiert werden kann.

 

 



