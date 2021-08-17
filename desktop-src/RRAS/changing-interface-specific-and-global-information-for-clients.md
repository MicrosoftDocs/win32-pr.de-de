---
title: Ändern Interface-Specific und globalen Informationen für Clients
description: Um die Schnittstelleninformationen für einen bestimmten Client zu ändern, z. B. NAT, verwenden Sie zuerst den entsprechenden \0034; GetInfo \ 0034; -Funktion, um die aktuellen Informationen abzurufen.
ms.assetid: 208e356b-328e-416d-881c-732fed460ebf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcea02c6d70e7d7e2da53926854879f1ca5b76526a83185b786b0074b8098434
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791753"
---
# <a name="changing-interface-specific-and-global-information-for-clients"></a>Ändern Interface-Specific und globalen Informationen für Clients

Um die Schnittstelleninformationen für einen bestimmten Client zu ändern, z. B. NAT, verwenden Sie zuerst die entsprechende "GetInfo"-Funktion, um die aktuellen Informationen abzurufen. Wenn der Router ausgeführt wird, verwenden Sie [**MprAdminInterfaceTransportGetInfo.**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo) Wenn der Router nicht ausgeführt wird, verwenden Sie [**mprConfigInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportgetinfo). Dieser Aufruf ruft die Informationen für alle Clients ab, die auf der angegebenen Schnittstelle ausgeführt werden. Wenn beispielsweise sowohl OSPF als auch RIP auf einer bestimmten Schnittstelle ausgeführt werden, ruft dieser Aufruf die Schnittstelleninformationen für beide ab. Verwenden Sie die [**MprInfoBlockFind-Funktion,**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockfind) um den Informationsblock zu finden, der dem Client entspricht, den Sie ändern möchten. Verwenden Sie dann die [**MprInfoBlockSet-Funktion,**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockset) um die Änderungen durchzuführen. Verwenden Sie abschließend [**MprAdminInterfaceTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) oder [**MprConfigInterfaceSetInfo,**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacesetinfo) um die Änderungen am ausgeführten Router oder an der Routerkonfiguration in der Registrierung vorzunehmen.

Globale Clientinformationen sind Informationen, die nicht spezifisch für eine bestimmte Schnittstelle sind, auf der der Client ausgeführt wird. Verwenden Sie ein ähnliches Verfahren, um globale Informationen für einen bestimmten Client zu ändern. Rufen Sie zunächst die globalen Informationen für alle Clients mit [**mprAdminTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportgetinfo) oder [**MprConfigTransportGetInfo ab.**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportgetinfo) Verwenden Sie dann die MprInfo-Funktionen, um die Informationen zu ändern. Verwenden Sie abschließend die [**Funktionen MprAdminTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportsetinfo) oder [**MprConfigTransportSetInfo,**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportsetinfo) um die geänderten Informationen entweder auf dem ausgeführten Router oder in der Registrierung zu speichern.

Aufrufe der oben genannten Verwaltungsfunktionen werden über den Dynamic Interface Manager (DIM) übertragen und werden schließlich in Aufrufe vom Router-Manager an die Clients selbst übersetzt. Alle Clients, unabhängig davon, ob es sich um Routingprotokolle handelt, müssen der im Abschnitt [Router Protocol Interface beschriebenen Schnittstelle entsprechen.](about-routing-protocol-interface.md) Im Rahmen dieser Schnittstelle muss das Routingprotokoll u. a. die folgenden Funktionen unterstützen:

-   [**GetGlobalInfo**](/windows/desktop/api/Routprot/nc-routprot-pget_global_info)
-   [**SetGlobalInfo**](/windows/desktop/api/Routprot/nc-routprot-pset_global_info)
-   [**GetInterfaceInfo**](/windows/desktop/api/Routprot/nc-routprot-pget_interface_info)
-   [**SetInterfaceInfo**](/windows/desktop/api/Routprot/nc-routprot-pset_interface_info)

Der Router-Manager ruft die [**GetInterfaceInfo-Funktionen**](/windows/desktop/api/Routprot/nc-routprot-pget_interface_info) für jeden der Clients auf, um die Informationen zu sammeln, die von einem Aufruf von [**MprAdminInterfaceTransportGetInfo zurückgegeben werden.**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo) Wenn der Router-Manager aktualisierte Informationen über den [**MprAdminInterfaceTransportSetInfo-Aufruf**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) empfängt, verwendet er entsprechend die [**SetInterfaceInfo-Funktionen,**](/windows/desktop/api/Routprot/nc-routprot-pset_interface_info) um die Schnittstelleninformationen für jeden der Clients zu aktualisieren.

 

 




