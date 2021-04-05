---
title: Grundlegendes zu mprinfo-Funktionen und Informations Headern
description: Die folgenden Funktionen erfordern, dass der Aufrufer eine Informationsstruktur oder einen Header als einen der Parameter übergibt.
ms.assetid: 389002c9-2d24-4b35-ab5b-801fe2091db9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 001c39bf28500d7261b3eb99abf0266470daf3d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947779"
---
# <a name="understanding-mprinfo-functions-and-information-headers"></a>Grundlegendes zu mprinfo-Funktionen und Informations Headern

Die folgenden Funktionen erfordern, dass der Aufrufer eine Informationsstruktur oder einen *Header* als einen der Parameter übergibt.



| Verwaltungsfunktion                                                        | Konfigurationsfunktion                                                           |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| Keine Verwaltungsfunktion                                                     | [**Mprconfigtransportcreate**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportcreate)                     |
| [**Mpradmintransporteintinfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportsetinfo)                   | [**Mprconfigtransporteintinfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportsetinfo)                   |
| [**Mpradmininterfacetransportabfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) | [**Mprconfiginterfacetransportantinfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportsetinfo) |
| [**Mpradmininterfacetransportadd**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportadd)         | [**Mprconfiginterfacetransportadd**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportadd)         |



 

Ebenso geben die folgenden Funktionen Informations Header zurück.



| Verwaltungsfunktion                                                        | Konfigurationsfunktion                                                           |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [**Mpradmintransportgetinfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportgetinfo)                   | [**Mprconfigtransportgetinfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportgetinfo)                   |
| [**Mpradmininterfacetransportgetinfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo) | [**Mprconfiginterfacetransportgetinfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportgetinfo) |



 

Für die Transportfunktionen enthält der Informations Header globale Informationen für den Transport. Der-Header enthält für die Client Funktionen (interfacetransport) spezifische Informationen für den Client (z. b. OSPF), der verwaltet wird.

Die Informations Header und ihre Inhalte sollten nur mithilfe der [mprinfo](router-information-functions.md) -Funktionen bearbeitet werden. Entwickler sollten nicht versuchen, den Inhalt der Informations Header direkt zu bearbeiten.

Die reinen Schnittstellen Funktionen, wie z. b. [**mpradmininterfakesetinfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacesetinfo) , erfordern nicht die Verwendung von mprinfo-Funktionen. Die Informationen, die mit diesen Funktionen übermittelt und zurückgegeben werden, sind immer in Form einer [**MPR- \_ Schnittstellen**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_0) Struktur.

 

 




