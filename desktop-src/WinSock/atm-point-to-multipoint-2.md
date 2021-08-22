---
description: Der Geldautomaten fällt in die Kategorie der Stammdaten und Steuerungsebenen mit Stamm.
ms.assetid: 8e355efe-2903-49c1-a9b3-792b07bd2995
title: Punkt-zu-Multipoint des Geldautomaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 198d8160fdb1e942cc581374af18ca57303726bdddd41142855d366e58dfbf68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119504460"
---
# <a name="atm-point-to-multipoint"></a>Punkt-zu-Multipoint des Geldautomaten

Der Geldautomaten fällt in die Kategorie der Stammdaten und Steuerungsebenen mit Stamm. Eine Anwendung, die als Stamm verwendet, würde C-Stammsockes erstellen, und Entsprechungen, die auf Blattknoten ausgeführt werden, würden \_ \_ C-Blattsockes verwenden. Die Stammanwendung verwendet [**WSAJoinLeaf,**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) um neue Blattknoten hinzuzufügen. Die entsprechenden Anwendungen auf den Blattknoten haben ihre \_ C-Blattsockes in den Lauschenmodus festgelegt. **WSAJoinLeaf mit** einem angegebenen c-Stammsocket wird \_ der Q.2931 ADDPARTY-Nachricht zugeordnet. Der vom Blatt initiierte Join wird in ATM UNI 3.1 nicht unterstützt, aber in ATM UNI 4.0. Daher **wird WSAJoinLeaf** mit einem angegebenen Blattsocket der entsprechenden \_ ATM UNI 4.0-Nachricht zugeordnet.

Bei Punkt-zu-Multipoint-Atm-Automaten sind weitere Überlegungen zu beachten:

-   Das Addition neuer Blätter zur Punkt-zu-Multipoint-Sitzung von ATM ist nur auf Einladungen basiert. Die Stammeinlädungen verlassen [](/windows/desktop/api/Winsock2/nf-winsock2-accept) , die bereits über ihren Accept-Funktionsaufruf verfügen, indem sie die [**WSAJoinLeaf-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) aufrufen.
-   Der Datenfluss in einer Punkt-zu-Multipoint-Atm-Sitzung wird nur von Stamm zu Blatt ausgeführt. leaves kann nicht dieselbe Sitzung verwenden, um Informationen an das Stammverzeichnis zu senden.
-   Pro ATM-Adapter ist nur ein Blatt zulässig.

 

 



