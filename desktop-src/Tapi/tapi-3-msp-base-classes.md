---
description: In diesem Dokument werden der Entwurf und die Verwendung der MSP-Basisklassen beschrieben. Die Verwendung dieser Klassen ist nicht erforderlich, aber die meisten Entwickler werden feststellen, dass sie die Aufgabe vereinfachen, einen DirectShow-basierten MSP für neue MSPI von TAPI 3s zu erstellen.
ms.assetid: 97597dcf-eb18-47aa-b0ed-a43286d5d134
title: TAPI 3 MSP-Basisklassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee34d4f9f67618c3637bfaff149773ab7b0de4b93f33c8bca8e5eb892527735e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012340"
---
# <a name="tapi-3-msp-base-classes"></a>TAPI 3 MSP-Basisklassen

In diesem Dokument werden der Entwurf und die Verwendung der MSP-Basisklassen beschrieben. Die Verwendung dieser Klassen ist nicht erforderlich, aber die meisten Entwickler werden feststellen, dass sie die Aufgabe vereinfachen, einen DirectShow-basierten MSP für den neuen MSPI von TAPI 3 zu erstellen.

Den Quellcode für die MSP-Basisklassen finden Sie im Verzeichnis Samples des Platform Software Development Kit (SDK).

Es wird vorausgesetzt, dass Sie mit COM, ATL, DirectShow und C++ vertraut sind. Der Leser muss auch das allgemeine Material in [About the Media Service Provider (MSP)](about-the-media-service-provider-msp-.md) und in Media Service Provider Interface [(MSPI) kennen.](media-service-provider-interface-mspi-.md)

ATL 2.1 ist für Windows 2000 erforderlich. Ab Windows XP werden sowohl ATL 2.1 als auch 3.0 kompiliert.

MSP-Basisklassenbibliotheken (im SDK verfügbar):

-   Mspbase.lib
-   Mspid.lib
-   Strmbase.lib
-   Tmuid.lib
    > [!Note]  
    > Es sollte eine dynamische anstelle einer statischen Verknüpfung verwendet werden.

     

Headerdateien der MSP-Basisklasse (im SDK verfügbar):

-   Mspaddr.h
-   Mspbase.h
-   Mspcall.h
-   Msplog.h
-   Mspstrm.h
-   Mspterm.h
-   Mspthrd.h
-   Msptmac.h
-   Msptmvc.h
-   Msptrmvc.h
-   Msptrmac.h
-   Msptrmar.h
-   Msputils.h

Quelldateien der MSP-Basisklasse (in den SDK-Beispielen verfügbar):

-   Mspaddr.cpp
-   Mspcall.cpp
-   Msplog.cpp
-   Mspstrm.cpp
-   Mspterm.cpp
-   Mspthrd.cpp
-   Msptrmac.cpp
-   Msptrmar.cpp
-   Msptrmvc.cpp
-   Msputils.cpp

 

 



