---
description: IP-Hilfsprogramm bietet Funktionen zum Verwalten von Netzwerkadaptern. Zwischen den Schnittstellen und Adaptern eines bestimmten Computers besteht eine eins-zu-eins-Entsprechung. Eine Schnittstelle ist eine Abstraktion auf IP-Ebene, während ein Adapter eine Abstraktion auf DataLink-Ebene ist.
ms.assetid: fbb32941-2add-4f74-90c4-1dc1bfebd64c
title: Verwalten von Netzwerkadaptern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaa8f42cf1499ee7873d13334d0edbc9f954794f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525892"
---
# <a name="managing-network-adapters"></a>Verwalten von Netzwerkadaptern

IP-Hilfsprogramm bietet Funktionen zum Verwalten von Netzwerkadaptern. Zwischen den Schnittstellen und Adaptern eines bestimmten Computers besteht eine eins-zu-eins-Entsprechung. Eine Schnittstelle ist eine Abstraktion auf IP-Ebene, während ein Adapter eine Abstraktion auf DataLink-Ebene ist.

Verwenden Sie die Funktionen, die in den folgenden Abschnitten beschrieben werden, um Informationen zu den Netzwerkadaptern auf dem lokalen Computer abzurufen.

Die [**getadaptersinfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) -Funktion gibt ein Array von [**IP- \_ Adapter \_ Informations**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) Strukturen zurück, eines für jeden Adapter auf dem lokalen Computer. Die [**getperadapterinfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getperadapterinfo) -Funktion gibt zusätzliche Informationen zu einem bestimmten Adapter zurück. Die **getperadapterinfo** -Funktion erfordert, dass der Aufrufer den Index des Adapters angibt. Verwenden Sie die [**GetAdapterIndex**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadapterindex) -Funktion, um den Adapter Index aus dem Adapter Namen abzurufen.

Einige Anwendungen verwenden Adapter, die Datagramme empfangen, jedoch nicht übertragen können. Zum Abrufen von Informationen zu diesen Adaptern verwenden Sie die [**getunidirectionaladapterinfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getunidirectionaladapterinfo) -Funktion.

Mit der Funktion " [**getadaptersadressen**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersaddresses) " können Sie die einem bestimmten Adapter zugeordneten IP-Adressen abrufen. Diese Funktion unterstützt sowohl IPv4-als auch IPv6-Adressierung.

-   Codebeispiele, die [**getadaptersinfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) betreffen, finden [Sie unter Verwalten von Netzwerkadaptern mithilfe von getadaptersinfo](managing-network-adapters-using-getadaptersinfo.md).

 

 



