---
title: Verwenden von Teredo mit IP-Hilfsprogramm
description: Die IP-hilfsprogrammapi (Internet Protocol Helper) wird von einer Anwendung verwendet, um wichtige Informationen zur Netzwerkkonfiguration des lokalen Computers zu erfassen und bereitzustellen.
ms.assetid: 67dbe639-aff5-4628-9471-63f50504962d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e5936ce9987262fe24cfd6cf718a426b6123b89
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728480"
---
# <a name="using-teredo-with-ip-helper"></a>Verwenden von Teredo mit IP-Hilfsprogramm

Die IP Helper-API ( [Internet Protocol Helper](/windows/desktop/IpHlp/about-ip-helper) ) wird von einer Anwendung verwendet, um wichtige Informationen zur Netzwerkkonfiguration des lokalen Computers zu sammeln und bereitzustellen. Wenn Sie auf der Windows Vista-Plattform arbeiten, beinhalten diese Informationen den dynamischen UDP-Port, der der Teredo-Schnittstelle zugewiesen ist, sowie Änderungen, die möglicherweise am vorgesehenen Port vorgenommen werden

Die folgenden Funktionen werden von der IP Helper-API verwendet, um die Verwendung der Teredo-Schnittstelle zu vereinfachen:

-   [**Getteredoport**](/windows/desktop/api/netioapi/nf-netioapi-getteredoport)
-   [**Notifyteredoportchange**](/windows/desktop/api/netioapi/nf-netioapi-notifyteredoportchange)
-   [**Notifystableunicastipadresssstable**](/windows/desktop/api/netioapi/nf-netioapi-notifystableunicastipaddresstable)

 

 