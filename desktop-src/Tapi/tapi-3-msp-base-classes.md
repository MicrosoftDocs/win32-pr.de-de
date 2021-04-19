---
description: In diesem Dokument werden das Design und die Verwendung der MSP-Basisklassen beschrieben. Die Verwendung dieser Klassen ist nicht erforderlich, aber die meisten Entwickler werden feststellen, dass Sie das Entwickeln eines DirectShow-basierten MSP für TAPI 3S New MSPi vereinfachen.
ms.assetid: 97597dcf-eb18-47aa-b0ed-a43286d5d134
title: TAPI 3-MSP-Basisklassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb7c7958847ef7bf699cfe4810f7133ef0b4bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373299"
---
# <a name="tapi-3-msp-base-classes"></a>TAPI 3-MSP-Basisklassen

In diesem Dokument werden das Design und die Verwendung der MSP-Basisklassen beschrieben. Die Verwendung dieser Klassen ist nicht erforderlich, aber die meisten Entwickler werden feststellen, dass Sie die Aufgabe der Entwicklung eines DirectShow-basierten MSP für die neue MSPi von TAPI 3 vereinfachen.

Quellcode für die MSP-Basisklassen finden Sie im Verzeichnis "Samples" des Platform Software Development Kit (SDK).

Es wird davon ausgegangen, dass Sie mit com, ATL, DirectShow und C++ vertraut sind. Der Reader muss auch das allgemeine Material in [über den Media Service Provider (MSP)](about-the-media-service-provider-msp-.md) und in der [Media Service Provider Interface (MSPi)](media-service-provider-interface-mspi-.md)kennen.

ATL 2,1 ist für Windows 2000 erforderlich. Ab Windows XP werden sowohl ATL 2,1 als auch 3,0 kompiliert.

MSP-Basisklassen Bibliotheken (verfügbar im SDK):

-   Mspbase. lib
-   Mspid. lib
-   "Ermbase. lib"
-   Tmuid. lib
    > [!Note]  
    > Es sollte dynamisch anstelle statischer Verknüpfungen verwendet werden.

     

MSP-Basisklassen Header Dateien (verfügbar im SDK):

-   Mspaddr. h
-   Mspbase. h
-   "Mspcall. h"
-   Msplog. h
-   Mspstraum. h
-   Mspterm. h
-   Mspthrd. h
-   Msptmac. h
-   Msptmvc. h
-   Msptrmvc. h
-   Msptrmac. h
-   Msptrmar. h
-   Msputils. h

Quelldateien der MSP-Basisklasse (in den SDK-Beispielen verfügbar):

-   Mspaddr. cpp
-   Mspcall. cpp
-   Msplog. cpp
-   Mspstraum. cpp
-   Mspterm. cpp
-   Mspthrd. cpp
-   Msptrmac. cpp
-   Msptrmar. cpp
-   Msptrmvc. cpp
-   Msputils. cpp

 

 



