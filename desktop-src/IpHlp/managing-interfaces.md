---
description: Das IP-Hilf hilft Ihnen bei der Verwaltung von Netzwerkschnittstellen. Es gibt eine 1:1-Entsprechung zwischen den Schnittstellen und Adaptern auf einem bestimmten Computer. Eine Schnittstelle ist eine Abstraktion auf IP-Ebene, während ein Adapter eine Abstraktion auf Datenlinkebene ist.
ms.assetid: 598bbe67-30df-4c02-8f30-2ccf15b5c494
title: Verwalten von Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bb46ecba6f1c5780960f6d8e363db9ec04d0cc3611da1caf023ec95bf5a99a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146693"
---
# <a name="managing-interfaces"></a>Verwalten von Schnittstellen

Das IP-Hilf hilft Ihnen bei der Verwaltung von Netzwerkschnittstellen. Es gibt eine 1:1-Entsprechung zwischen den Schnittstellen und Adaptern auf einem bestimmten Computer. Eine Schnittstelle ist eine Abstraktion auf IP-Ebene, während ein Adapter eine Abstraktion auf Datenlinkebene ist.

Verwenden Sie die in den folgenden Abschnitten beschriebenen Funktionen, um Schnittstellen auf dem lokalen Computer zu verwalten.

Die [**GetNumberOfInterfaces-Funktion**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnumberofinterfaces) gibt die Anzahl der Schnittstellen auf dem lokalen Computer zurück.

Die [**GetInterfaceInfo-Funktion**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) gibt eine Tabelle zurück, die die Namen und entsprechenden Indizes für die Schnittstellen auf dem lokalen Computer enthält. Codebeispiele für **GetInterfaceInfo** finden Sie unter [Verwalten von Schnittstellen mit GetInterfaceInfo.](managing-interfaces-using-getinterfaceinfo.md)

Die [**GetFriendlyIfIndex-Funktion**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getfriendlyifindex) verwendet einen Schnittstellenindex und gibt einen abwärtskompatiblen Schnittstellenindex zurück, d.h. einen Index, der nur die unteren 24 Bits verwendet. Diese Art von Index wird manchmal als "benutzerfreundlicher" Schnittstellenindex bezeichnet.

Die [**GetIfEntry-Funktion**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getifentry) gibt eine [**\_ MIB-IFROW-Struktur**](/windows/win32/api/ifmib/ns-ifmib-mib_ifrow) zurück, die Informationen zu einer bestimmten Schnittstelle auf dem lokalen Computer enthält. Für diese Funktion muss der Aufrufer den Index der Schnittstelle bereitstellen.

Die [**GetIfTable-Funktion**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getiftable) gibt eine Tabelle mit [**MIB \_ IFROW-Einträgen**](/windows/win32/api/ifmib/ns-ifmib-mib_ifrow) zurück, eine für jede Schnittstelle auf dem Computer.

Verwenden Sie die [**SetIfEntry-Funktion,**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setifentry) um die Konfiguration einer bestimmten Schnittstelle zu ändern.

 

 
