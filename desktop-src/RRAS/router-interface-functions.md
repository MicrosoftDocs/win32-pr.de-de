---
title: Funktionen der Routerschnittstelle
description: Verwenden Sie die folgenden Funktionen, um Schnittstellen auf dem Router zu verwalten.
ms.assetid: e988753e-908a-4c42-aad3-dd9f641c90a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3a5318eedfbc3a04c13549012fda3bd4d93b4d9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309156"
---
# <a name="router-interface-functions"></a>Funktionen der Routerschnittstelle

Verwenden Sie die folgenden Funktionen, um Schnittstellen auf dem Router zu verwalten.



| Verwaltungsfunktion                                          | Konfigurationsfunktion                                             |
|------------------------------------------------------------------|--------------------------------------------------------------------|
| [**Mpradmininterfakecreate**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacecreate)       | [**Mprconfiginterfaecreate**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacecreate)       |
| [**Mpradmininterfacedelete**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacedelete)       | [**Mprconfiginterfacedelete**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacedelete)       |
| [**Mpradmininterfaceerum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfaceenum)           | [**Mprconfiginterfacereum**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfaceenum)           |
| [**Mpradmininterfacegethandle**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacegethandle) | [**Mprconfiginterfacegethandle**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacegethandle) |
| [**Mpradmininterfacegetinfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacegetinfo)     | [**Mprconfiginterfacegetinfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacegetinfo)     |
| [**Mpradmininterfakesetinfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacesetinfo)     | [**Mprconfiginterfakesetinfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacesetinfo)     |



 

Diese Funktionen wirken sich auf die Schnittstellen selbst aus, nicht auf Clients, die auf den Schnittstellen Aus diesem Grund erfordert keine der Funktionen, dass der Aufrufer einen bestimmten Transport (IP oder IPX) angibt. Obwohl Clients (z. b. Routing Protokolle) bestimmten Transporten zugeordnet sind, sind die Schnittstellen nicht selbst.

Diese Funktionen werden direkt von Dim verarbeitet. Die Router-Manager werden nicht verwendet.

Die [**mpradmininterfacecreate**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacecreate) -und [**mpradmininterfacedelete**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacedelete) -Funktionen können keine LAN-Schnittstellen erstellen oder löschen. Sie können nur Schnittstellen mit Bedarf erstellen oder löschen. Eine Liste der Schnittstellentypen finden Sie unter [**Router \_ Interface \_ Type**](/windows/desktop/api/Mprapi/ne-mprapi-router_interface_type) .

 

 




