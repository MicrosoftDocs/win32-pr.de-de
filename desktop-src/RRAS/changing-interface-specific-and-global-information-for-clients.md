---
title: Ändern von Interface-Specific und globalen Informationen für Clients
description: Verwenden Sie zum Ändern der Schnittstellen Informationen für einen bestimmten Client (z. b. NAT) zuerst die entsprechende \ 0034; GetInfo \ 0034; Funktion zum Abrufen der aktuellen Informationen.
ms.assetid: 208e356b-328e-416d-881c-732fed460ebf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e5c8f2ef3c37d75db1cc7686a67108530b16b28
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947716"
---
# <a name="changing-interface-specific-and-global-information-for-clients"></a>Ändern von Interface-Specific und globalen Informationen für Clients

Zum Ändern der Schnittstellen Informationen für einen bestimmten Client (z. b. NAT) verwenden Sie zunächst die entsprechende Funktion "GetInfo", um die aktuellen Informationen abzurufen. Wenn der Router ausgeführt wird, verwenden Sie [**mpradmininterfacetransportgetinfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo). Wenn der Router nicht ausgeführt wird, verwenden Sie [**mprconfiginterfacetransportgetinfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportgetinfo). Dieser Befehl ruft die Informationen für alle Clients ab, die auf der angegebenen Schnittstelle ausgeführt werden. Wenn beispielsweise OSPF und RIP an einer bestimmten Schnittstelle ausgeführt werden, ruft dieser Befehl die Schnittstellen Informationen für beide ab. Verwenden Sie die Funktion [**mprinfoblockfind**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockfind) , um den Informationsblock zu finden, der dem zu ändernden Client entspricht. Verwenden Sie dann die [**mprinfoblockset**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockset) -Funktion, um die Änderungen auszuführen. Verwenden Sie schließlich [**mpradmininterfacetransportabfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) oder [**mprconfiginterfacesetinfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacesetinfo) , um die Änderungen an dem ausgelaufenden Router oder der Routerkonfiguration in der Registrierung vorzunehmen.

Globale Client Informationen sind Informationen, die nicht spezifisch für bestimmte Schnittstellen sind, auf denen der Client ausgeführt wird. Verwenden Sie ein ähnliches Verfahren, um globale Informationen für einen bestimmten Client zu ändern. Rufen Sie zuerst die globalen Informationen für alle Clients mithilfe von [**mpradmintransportgetinfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportgetinfo) oder [**mprconfigtransportgetinfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportgetinfo)ab. Verwenden Sie dann die mprinfo-Funktionen, um die Informationen zu ändern. Verwenden Sie abschließend die Funktionen [**mpradmintransportsettinfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportsetinfo) oder [**mprconfigtransportabfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportsetinfo) , um die geänderten Informationen wieder auf dem laufenden Router oder in der Registrierung zu speichern.

Aufrufe der vorangehenden Verwaltungsfunktionen durchlaufen den Dynamic Interface Manager (Dim) und übersetzen schließlich Aufrufe vom routermanager zu den Clients selbst. Alle Clients, unabhängig davon, ob Sie Routing Protokolle sind oder nicht, müssen der im Abschnitt [Router Protocol Interface](about-routing-protocol-interface.md)beschriebenen Schnittstelle entsprechen. Im Rahmen dieser Schnittstelle muss das Routing Protokoll die folgenden Funktionen unterstützen (u.a.):

-   [**GetGlobalInfo**](/windows/desktop/api/Routprot/nc-routprot-pget_global_info)
-   [**Setglobalinfo**](/windows/desktop/api/Routprot/nc-routprot-pset_global_info)
-   [**Getinterfacetten Info**](/windows/desktop/api/Routprot/nc-routprot-pget_interface_info)
-   [**Setinterfacetten Info**](/windows/desktop/api/Routprot/nc-routprot-pset_interface_info)

Der routermanager Ruft die [**getinterfaceinfo**](/windows/desktop/api/Routprot/nc-routprot-pget_interface_info) -Funktionen für jeden der Clients auf, um die Informationen zu erfassen, die von einem Aufruf an [**mpradmininterfacetransportgetinfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo)zurückgegeben werden. Ebenso, wenn der routermanager aktualisierte Informationen über den [**mpradmininterfacetransportsetinfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) -Aufruf empfängt, verwendet er die [**setinterfaceinfo**](/windows/desktop/api/Routprot/nc-routprot-pset_interface_info) -Funktionen, um die Schnittstellen Informationen für die einzelnen Clients zu aktualisieren.

 

 




