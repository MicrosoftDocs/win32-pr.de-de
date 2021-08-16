---
title: Routerinformationsfunktionen
description: Verwenden Sie die folgenden Funktionen, um Routerinformationsheader und -blöcke zu bearbeiten. Ein Informationsheader besteht aus privaten Metadaten und Informationsblöcken. Informationsblöcke sind Arrays von Informationsstrukturen verschiedener Typen.
ms.assetid: e88720aa-080b-4d87-a442-1b436c256ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029b36ef862f11c58492fd8ec9c7c6f292797c2e35e75592f385e18d6d0e1a25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788015"
---
# <a name="router-information-functions"></a>Routerinformationsfunktionen

Verwenden Sie die folgenden Funktionen, um Routerinformationsheader und -blöcke zu bearbeiten. Ein Informationsheader besteht aus privaten Metadaten und Informationsblöcken. Informationsblöcke sind Arrays von [Informationsstrukturen](router-information-structures.md) verschiedener [Typen.](router-information-enumerations.md)

Die folgenden Funktionen bearbeiten Informationsheader:

-   [**MprInfoCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfocreate)
-   [**MprInfoDelete**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfodelete)
-   [**MprInfoDuplicate**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoduplicate)
-   [**MprInfoRemoveAll**](/windows/desktop/api/Mprapi/nf-mprapi-mprinforemoveall)

Die folgenden Funktionen bearbeiten Informationsblöcke innerhalb eines Informationsheaders:

-   [**MprInfoBlockAdd**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockadd)
-   [**MprInfoBlockFind**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockfind)
-   [**MprInfoBlockQuerySize**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockquerysize)
-   [**MprInfoBlockRemove**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockremove)
-   [**MprInfoBlockSet**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockset)

Viele der [Routerverwaltungs- und Konfigurationsfunktionen](understanding-mprinfo-functions-and-information-headers.md) verwenden Informationsheader.

 

 




