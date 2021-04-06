---
title: Routerinformationsfunktionen
description: Verwenden Sie die folgenden Funktionen, um die Header und Blöcke der Routerinformationen zu bearbeiten. Ein Informations Header besteht aus privaten metadatendaten und Informations Blöcken. Informationsblöcke sind Arrays von Informationsstrukturen verschiedener Typen.
ms.assetid: e88720aa-080b-4d87-a442-1b436c256ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f694d2dcd140d8af8950fa7a2a4ae5049a679ff8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036231"
---
# <a name="router-information-functions"></a>Routerinformationsfunktionen

Verwenden Sie die folgenden Funktionen, um die Header und Blöcke der Routerinformationen zu bearbeiten. Ein Informations Header besteht aus privaten metadatendaten und Informations Blöcken. Informationsblöcke sind Arrays von [Informationsstrukturen](router-information-structures.md) verschiedener [Typen](router-information-enumerations.md).

Die folgenden Funktionen bearbeiten Informations Header:

-   [**Mprinfocreate**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfocreate)
-   [**Mprinfodelete**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfodelete)
-   [**Mprinfoduplicate**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoduplicate)
-   [**Mprinforemoveall**](/windows/desktop/api/Mprapi/nf-mprapi-mprinforemoveall)

Die folgenden Funktionen bearbeiten Informationsblöcke innerhalb eines Informations Headers:

-   [**Mprinfoblockadd**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockadd)
-   [**Mprinfoblockfind**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockfind)
-   [**Mprinfoblockquerysize**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockquerysize)
-   [**Mprinfoblockremove**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockremove)
-   [**Mprinfoblockset**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockset)

Viele der [routerverwaltungs-und Konfigurationsfunktionen](understanding-mprinfo-functions-and-information-headers.md) verwenden Informations Header.

 

 




