---
description: Ein Medien Dienstanbieter muss eine minimale Teilmenge von MSPi-Schnittstellen implementieren, itmspaddress itterminalsupport itstreamcontrol und itstream.
ms.assetid: 59560bdf-953e-48e8-b565-46c3e0123c7e
title: Schreiben eines Media Service-Anbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 782dddb9a87725bde7c104d459b71204a04de018
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351168"
---
# <a name="writing-a-media-service-provider"></a>Schreiben eines Media Service-Anbieters

Ein Medien Dienstanbieter muss eine minimale Teilmenge von MSPi-Schnittstellen implementieren: [**itmspaddress**](/windows/desktop/api/msp/nn-msp-itmspaddress), [**itterminalsupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport), [**itstreamcontrol**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)und [**itstream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream). Die Unterstützung von Substreams ist optional. Darüber hinaus kann ein bestimmtes MSP zusätzliche Methoden implementieren, z. b. Steuerelemente, die für spezialisierte Hardware erforderlich sind.

Die folgenden Material Dokumente:

-   Die [TAPI 3-MSP-Basisklassen](tapi-3-msp-base-classes.md), bei denen es sich um eine Reihe von C++-Klassen handelt, die die Aufgabe der Einrichtung eines DirectShow-basierten MSP vereinfachen. Die Basisklassen implementieren alle MSPi-Schnittstellen auf generische Weise. Verschiedene MSPs können MSP-spezifische Funktionen überschreiben und ihre eigenen Implementierungen bereitstellen.
-   Der [TAPI 3-Terminal-Manager](tapi-3-terminal-manager.md), der Schnittstellen und Methoden bereitstellt, die von einem MSP zum Steuern von Terminals verwendet werden.
-   [Austauschbare Terminals](writing-a-pluggable-terminal.md), mit denen eine Anwendung anstelle eines MSP Terminals erstellen kann. Entwickler, die bereits Erfahrung mit dem Schreiben von Dienstanbietern haben, sind die Haupt Ersteller von austauschbaren Terminals. Die für diese Version implementierte anfängliche Version richtet sich an Konferenz Server Anwendungen, die nicht-Windows 2000-oder nicht-Multicast-Clients zu TAPI 3 Multi-Party-SDP/IP-Multicast Konferenzen hinzufügen müssen.

 

 
