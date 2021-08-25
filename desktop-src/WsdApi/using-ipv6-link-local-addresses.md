---
description: Die lokale Adressierung von IPv6-Links in SOAP-Nachrichten stellt eine besondere Herausforderung dar, da lokale IPv6-Linkadressen eine Bereichs-ID erfordern, um aussagekräftig zu sein, aber die Bereichs-ID hat nur eine Bedeutung für den lokalen Computer.
ms.assetid: 63495335-e447-4564-b669-0896c7aac63f
title: Verwenden von lokalen IPv6-Linkadressen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e10c1719e4e6d374e7afd859b80cd1bc14c4c841cb7dceee149f14d0acb777f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897160"
---
# <a name="using-ipv6-link-local-addresses"></a>Verwenden von lokalen IPv6-Linkadressen

Die lokale Adressierung von IPv6-Links in SOAP-Nachrichten stellt eine besondere Herausforderung dar, da lokale IPv6-Linkadressen eine Bereichs-ID erfordern, um aussagekräftig zu sein, aber die Bereichs-ID hat nur eine Bedeutung für den lokalen Computer. Alle Client- und Geräteimplementierungen müssen die Bereichs-ID entfernen, bevor eine lokale IPv6-Linkadresse in einer SOAP-Nachricht gesendet wird. Wenn außerdem eine lokale IPv6-Linkadresse in einer Nachricht empfangen wird, muss die Schnittstelle, auf der die Nachricht empfangen wurde, bekannt sein, damit die vollständige lokale Linkadresse mit Bereichs-ID rekonstruiert werden kann.

 

 



