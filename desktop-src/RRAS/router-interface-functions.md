---
title: Routerschnittstellenfunktionen
description: Verwenden Sie die folgenden Funktionen, um Schnittstellen auf dem Router zu verwalten.
ms.assetid: e988753e-908a-4c42-aad3-dd9f641c90a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bcaaf257e31623036a075c21da66d4665b3afe7e821f8f246f6a225e02b8272
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117787836"
---
# <a name="router-interface-functions"></a>Routerschnittstellenfunktionen

Verwenden Sie die folgenden Funktionen, um Schnittstellen auf dem Router zu verwalten.



| Verwaltungsfunktion                                          | Konfigurationsfunktion                                             |
|------------------------------------------------------------------|--------------------------------------------------------------------|
| [**MprAdminInterfaceCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacecreate)       | [**MprConfigInterfaceCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacecreate)       |
| [**MprAdminInterfaceDelete**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacedelete)       | [**MprConfigInterfaceDelete**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacedelete)       |
| [**MprAdminInterfaceEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfaceenum)           | [**MprConfigInterfaceEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfaceenum)           |
| [**MprAdminInterfaceGetHandle**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacegethandle) | [**MprConfigInterfaceGetHandle**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacegethandle) |
| [**MprAdminInterfaceGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacegetinfo)     | [**MprConfigInterfaceGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacegetinfo)     |
| [**MprAdminInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacesetinfo)     | [**MprConfigInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacesetinfo)     |



 

Diese Funktionen wirken sich auf die Schnittstellen selbst aus, nicht auf Clients, die auf den Schnittstellen ausgeführt werden. Aus diesem Grund muss der Aufrufer für keine der Funktionen einen bestimmten Transport (IP oder IPX) angeben. Obwohl Clients (z. B. Routingprotokolle) bestimmten Transporten zugeordnet sind, ist dies bei den Schnittstellen selbst nicht der Fall.

Diese Funktionen werden direkt von DIM verarbeitet. Die Router-Manager werden nicht verwendet.

Die [**Funktionen MprAdminInterfaceCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacecreate) und [**MprAdminInterfaceDelete**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacedelete) können KEINE LAN-Schnittstellen erstellen oder löschen. Sie können nur Schnittstellen für die Wahl nach Bedarf erstellen oder löschen. Eine [**Liste der \_ \_ Schnittstellentypen**](/windows/desktop/api/Mprapi/ne-mprapi-router_interface_type) finden Sie unter ROUTER INTERFACE TYPE .

 

 




