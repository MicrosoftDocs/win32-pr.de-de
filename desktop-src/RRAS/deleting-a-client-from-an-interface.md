---
title: Löschen eines Clients aus einer Schnittstelle
description: Verwenden Sie zum Löschen eines Clients, z. b. eines Routing Protokolls, von einer bestimmten Schnittstelle entweder mpradmininterfacetransportgetinfo oder mprconfiginterfacetransportgetinfo, um alle Client Informationen für die Schnittstelle abzurufen.
ms.assetid: 22fd7233-a242-49c2-8c26-59b415c73af2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 585a37920b59f47a0c933427d7218d08a61bed9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947877"
---
# <a name="deleting-a-client-from-an-interface"></a>Löschen eines Clients aus einer Schnittstelle

Verwenden Sie zum Löschen eines Clients, z. b. eines Routing Protokolls, von einer bestimmten Schnittstelle entweder [**mpradmininterfacetransportgetinfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo) oder [**mprconfiginterfacetransportgetinfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportgetinfo) , um alle Client Informationen für die Schnittstelle abzurufen. Verwenden Sie [**mprinfoblockremove**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockremove) , um den Informationsblock für den zu löschenden Client zu entfernen. Fügen Sie dann mit [**mprinfoblockadd**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockadd) einen Block der Länge 0 (null) hinzu, um den Client zu löschen. Verwenden Sie zum Schluss [**mpradmininterfacetransportabfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) oder [**mprconfiginterfacetransportminfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportsetinfo) , um die Informationen entweder auf dem laufenden Router oder in der Registrierung wieder zu speichern.

Wenn der routermanager einen Schnittstellen Informationsblock der Länge 0 (null) für einen Client empfängt, weiß er, dass der Client aus der-Schnittstelle gelöscht wird. Der routermanager löscht den Client durch Aufrufen der Implementierung von " [**Delta Input Face**](/windows/desktop/api/Routprot/nc-routprot-pdelete_interface)" des Clients. Beachten Sie den wichtigen Unterschied zwischen dem Übergeben eines Informations Headers, der keinen Informationsblock für einen Client enthält, und dem Übergeben eines Informations Headers, der einen Informationsblock der Länge 0 (null) für den Client enthält. Im ersten Fall führt der routermanager keine Aktion in Bezug auf den Client aus. Im zweiten Fall löscht der routermanager den Client aus der-Schnittstelle.

 

 




