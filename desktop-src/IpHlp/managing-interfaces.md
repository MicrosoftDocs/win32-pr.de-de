---
description: IP Helper erweitert ihre Fähigkeiten zum Verwalten von Netzwerkschnittstellen. Zwischen den Schnittstellen und Adaptern eines bestimmten Computers besteht eine eins-zu-eins-Entsprechung. Eine Schnittstelle ist eine Abstraktion auf IP-Ebene, während ein Adapter eine Abstraktion auf DataLink-Ebene ist.
ms.assetid: 598bbe67-30df-4c02-8f30-2ccf15b5c494
title: Verwalten von Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 024d79d46ec1ba7606cbc7e79b4312432984239a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215919"
---
# <a name="managing-interfaces"></a>Verwalten von Schnittstellen

IP Helper erweitert ihre Fähigkeiten zum Verwalten von Netzwerkschnittstellen. Zwischen den Schnittstellen und Adaptern eines bestimmten Computers besteht eine eins-zu-eins-Entsprechung. Eine Schnittstelle ist eine Abstraktion auf IP-Ebene, während ein Adapter eine Abstraktion auf DataLink-Ebene ist.

Verwenden Sie die Funktionen, die in den folgenden Abschnitten beschrieben werden, um Schnittstellen auf dem lokalen Computer zu verwalten.

Die [**getnumofinterfaces**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnumberofinterfaces) -Funktion gibt die Anzahl der Schnittstellen auf dem lokalen Computer zurück.

Die [**getinterfakeinfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) -Funktion gibt eine Tabelle zurück, die die Namen und die entsprechenden Indizes für die Schnittstellen auf dem lokalen Computer enthält. Codebeispiele, die **getinterfacetten Info** betreffen, finden [Sie unter Verwalten von Schnittstellen mithilfe von getinterfacetten](managing-interfaces-using-getinterfaceinfo.md)Info.

Die [**getfriendlyifindex**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getfriendlyifindex) -Funktion nimmt einen Schnittstellen Index an und gibt einen abwärts kompatiblen Schnittstellen Index zurück, d. h. einen, der nur die unteren 24 Bits verwendet. Dieser Indextyp wird manchmal als "benutzerfreundlicher" Schnittstellen Index bezeichnet.

Die [**getif Entry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getifentry) -Funktion gibt eine [**MIB- \_ ifrow**](/windows/win32/api/ifmib/ns-ifmib-mib_ifrow) -Struktur zurück, die Informationen zu einer bestimmten Schnittstelle auf dem lokalen Computer enthält. Diese Funktion erfordert, dass der Aufrufer den Index der-Schnittstelle bereitstellt.

Die [**getiftable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getiftable) -Funktion gibt eine Tabelle mit [**MIB \_ ifrow**](/windows/win32/api/ifmib/ns-ifmib-mib_ifrow) -Einträgen zurück, eine für jede Schnittstelle auf dem Computer.

Verwenden Sie [**die Funktion "**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setifentry) -Funktion", um die Konfiguration einer bestimmten Schnittstelle zu ändern.

 

 
