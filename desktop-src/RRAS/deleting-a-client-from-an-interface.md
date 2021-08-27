---
title: Löschen eines Clients aus einer Schnittstelle
description: Verwenden Sie zum Löschen eines Clients, z. B. eines Routingprotokolls, von einer bestimmten Schnittstelle mprAdminInterfaceTransportGetInfo oder MprConfigInterfaceTransportGetInfo, um alle Clientinformationen für die Schnittstelle abzurufen.
ms.assetid: 22fd7233-a242-49c2-8c26-59b415c73af2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2e5b93e062f5971f6e43ad1d7c08f7a0c2ef3bff72e66849815a053b342b13b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127890"
---
# <a name="deleting-a-client-from-an-interface"></a>Löschen eines Clients aus einer Schnittstelle

Verwenden Sie zum Löschen eines Clients, z. B. eines Routingprotokolls, von einer bestimmten Schnittstelle [**mprAdminInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo) oder [**MprConfigInterfaceTransportGetInfo,**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportgetinfo) um alle Clientinformationen für die Schnittstelle abzurufen. Verwenden [**Sie MprInfoBlockRemove,**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockremove) um den Informationsblock für den zu löschenden Client zu entfernen. Verwenden Sie [**dann MprInfoBlockAdd,**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockadd) um einen Block der Länge 0 (null) für den zu löschenden Client hinzuzufügen. Verwenden Sie abschließend [**MprAdminInterfaceTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) oder [**MprConfigInterfaceTransportSetInfo,**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportsetinfo) um die Informationen entweder auf dem ausgeführten Router oder in der Registrierung zu speichern.

Wenn der Router-Manager einen Schnittstelleninformationsblock der Länge 0 (null) für einen Client empfängt, weiß er, diesen Client von der Schnittstelle zu löschen. Der Router-Manager löscht den Client, indem er die Implementierung von [**DeleteInterface des Clients aufruft.**](/windows/desktop/api/Routprot/nc-routprot-pdelete_interface) Beachten Sie den wichtigen Unterschied zwischen der Übergabe eines Informationsheaders, der keinen Informationsblock für einen Client enthält, und der Übergabe eines Informationsheaders, der einen Informationsblock der Länge 0 (null) für den Client enthält. Im ersten Fall führt der Router-Manager keine Maßnahmen in Bezug auf den Client aus. Im zweiten Fall löscht der Router-Manager den Client von der Schnittstelle.

 

 




