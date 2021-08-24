---
description: Ein Mediendienstanbieter muss eine Mindestteilmenge der MSPI-Schnittstellen ITMSPAddress ITTerminalSupport ITStreamControl und ITStream implementieren.
ms.assetid: 59560bdf-953e-48e8-b565-46c3e0123c7e
title: Schreiben eines Mediendienstanbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82f99cc8a52b7362caa01d9743fea7fc848faec2ae451b96ec916f4f3aa5c287
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739020"
---
# <a name="writing-a-media-service-provider"></a>Schreiben eines Mediendienstanbieters

Ein Mediendienstanbieter muss eine Mindestteilmenge von MSPI-Schnittstellen implementieren: [**ITMSPAddress,**](/windows/desktop/api/msp/nn-msp-itmspaddress) [**ITTerminalSupport,**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)und [**ITStream.**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) SubStream-Unterstützung ist optional. Darüber hinaus kann ein angegebener MSP zusätzliche Methoden implementieren, z. B. Steuerelemente, die für spezielle Hardware erforderlich sind.

Die folgenden Materialdokumente:

-   Die [TAPI 3 MSP-Basisklassen](tapi-3-msp-base-classes.md), bei denen es sich um eine Reihe von C++-Klassen handelt, die die Erstellung eines DirectShow-basierten MSP vereinfachen sollen. Die Basisklassen implementieren alle MSPI-Schnittstellen auf generische Weise. Verschiedene MSPs können MSP-spezifische Funktionen überschreiben und ihre eigenen Implementierungen bereitstellen.
-   Der [TAPI 3-Terminal-Manager,](tapi-3-terminal-manager.md)der Schnittstellen und Methoden bereitstellt, die von einem MSP zum Steuern von Terminals verwendet werden.
-   [Austauschbare Terminals,](writing-a-pluggable-terminal.md)die es einer Anwendung anstelle eines MSP ermöglichen, Terminals zu erstellen. Entwickler, die bereits Erfahrung mit dem Schreiben von Dienstanbietern haben, werden die primären Ersteller von austauschbaren Terminals sein. Die anfängliche Version, die für dieses Release implementiert wurde, ist auf Konferenzserveranwendungen ausgerichtet, die Multicastkonferenzen mit nicht Windows 2000 oder Nicht-Multicast zu TAPI 3 multi-party SDP/IP hinzufügen müssen.

 

 
