---
description: Das IP-Hilfsfunktionen bietet Funktionen zum Verwalten von Netzwerkadaptern. Es gibt eine 1:1-Entsprechung zwischen den Schnittstellen und Adaptern auf einem bestimmten Computer. Eine Schnittstelle ist eine Abstraktion auf IP-Ebene, während ein Adapter eine Abstraktion auf Datenlinkebene ist.
ms.assetid: fbb32941-2add-4f74-90c4-1dc1bfebd64c
title: Verwalten von Netzwerkadaptern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1e1fd02426b27e3c07d4634edbe0215efa1c5c25c7a9c3abde32e991f766daf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078260"
---
# <a name="managing-network-adapters"></a>Verwalten von Netzwerkadaptern

Das IP-Hilfsfunktionen bietet Funktionen zum Verwalten von Netzwerkadaptern. Es gibt eine 1:1-Entsprechung zwischen den Schnittstellen und Adaptern auf einem bestimmten Computer. Eine Schnittstelle ist eine Abstraktion auf IP-Ebene, während ein Adapter eine Abstraktion auf Datenlinkebene ist.

Verwenden Sie die in den folgenden Absätzen beschriebenen Funktionen, um Informationen zu den Netzwerkadaptern auf dem lokalen Computer abzurufen.

Die [**GetAdaptersInfo-Funktion**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) gibt ein Array von [**IP ADAPTER \_ \_ INFO-Strukturen**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) zurück, eine für jeden Adapter auf dem lokalen Computer. Die [**GetPerAdapterInfo-Funktion**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getperadapterinfo) gibt zusätzliche Informationen zu einem bestimmten Adapter zurück. Die **GetPerAdapterInfo-Funktion** erfordert, dass der Aufrufer den Index des Adapters angibt. Um den Adapterindex aus dem Adapternamen abzurufen, verwenden Sie die [**GetAdapterIndex-Funktion.**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadapterindex)

Einige Anwendungen verwenden Adapter, die Datagramme empfangen, aber nicht übertragen können. Verwenden Sie die [**GetUniDirectionalAdapterInfo-Funktion,**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getunidirectionaladapterinfo) um Informationen zu diesen Adaptern abzurufen.

Mit [**der GetAdaptersAddresses-Funktion**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersaddresses) können Sie die IP-Adressen abrufen, die einem bestimmten Adapter zugeordnet sind. Diese Funktion unterstützt sowohl IPv4- als auch IPv6-Adressierung.

-   Codebeispiele für [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) finden Sie unter [Managing Network Adapters Using GetAdaptersInfo ( Verwalten von Netzwerkadaptern mit GetAdaptersInfo).](managing-network-adapters-using-getadaptersinfo.md)

 

 



