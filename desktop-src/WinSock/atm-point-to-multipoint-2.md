---
description: ATM fällt in die Kategorie der Stammdaten und der rooting-steuerungsflächen.
ms.assetid: 8e355efe-2903-49c1-a9b3-792b07bd2995
title: ATM Point to Multipoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba17616feadfe1c8bf87ee8468dd967af73452c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360040"
---
# <a name="atm-point-to-multipoint"></a>ATM Point to Multipoint

ATM fällt in die Kategorie der Stammdaten und der rooting-steuerungsflächen. Eine Anwendung, die als Stamm fungiert, erstellt c \_ -Stamm Sockets, und Gegenstücke, die auf Blattknoten ausgeführt werden, würden c- \_ Blatt Sockets verwenden. Die Stamm Anwendung verwendet [**wsajoinleaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) , um neue Blattknoten hinzuzufügen. Die entsprechenden Anwendungen auf den Blattknoten haben ihre c- \_ Blatt Sockets in den Abhör Modus festgelegt. **Wsajoinleaf** mit einem angegebenen c-Stamm- \_ Socket wird der Q. 2931 addparty-Nachricht zugeordnet. Der Blatt initiierte Join wird in ATM Uni 3,1 nicht unterstützt, wird jedoch in ATM-Uni 4,0 unterstützt. Daher wird **wsajoinleaf** mit einem \_ angegebenen c-Blatt Socket der entsprechenden ATM-Uni 4,0-Nachricht zugeordnet.

Es gibt weitere Überlegungen, die Sie bei der Point-to-Multipoint-Funktion von ATM berücksichtigen sollten:

-   Das Hinzufügen neuer Blätter zur ATM-Point-to-Multipoint-Sitzung ist nur Einladungs basiert. Die Root-Einladungen erhalten –, die bereits ihren [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) -Funktionsaufruf – haben, indem Sie die [**wsajoinleaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) -Funktion aufrufen.
-   Der Datenfluss in einer ATM-zu-Multipoint-Sitzung erfolgt nur von der Stamm-zu-Blätter-Sitzung. Blätter können nicht dieselbe Sitzung verwenden, um Informationen an den Stamm zu senden.
-   Pro ATM-Adapter ist nur ein Blatt zulässig.

 

 



