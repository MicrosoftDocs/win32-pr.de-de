---
description: Ein TAPI 3-Mediendienstanbieter (Media Service Provider, MSP) ermöglicht einer Anwendung eine umfassende Kontrolle über die Medien für einen bestimmten Transportmechanismus.
ms.assetid: 2dd1268f-b31a-443b-a36b-05c1570e7a8a
title: Informationen zum Media Service Provider (MSP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f6113fa6c5fcceddaf379894d5680cbdccccec5be228041967dabb11fcc2caf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118872923"
---
# <a name="about-the-media-service-provider-msp"></a>Informationen zum Media Service Provider (MSP)

Ein TAPI 3-Mediendienstanbieter (Media Service Provider, MSP) ermöglicht einer Anwendung eine umfassende Kontrolle über die Medien für einen bestimmten Transportmechanismus. Ein MSP ist immer mit einem Telefoniedienstanbieter (Telefoniedienstanbieter, TSP) gekoppelt. Ebenso wie ein TSP eine Abstraktionsschicht für die Aufrufsteuerung ist, steuert der MSP Medien, ohne dass gerätespezifische Codierung erforderlich ist. Ein Beispiel für die MSP/TSP-Kommunikation finden Sie unter [Übersicht über TAPI-Dienstanbieter.](./tapi-service-provider-overview.md)

Ein MSP ermöglicht die Mediensteuerung durch die Verwendung spezieller Terminal-, Stream- und Substreamschnittstellen, die durch TAPI definiert werden. Das Diagramm unter About Call and Media Controls (Informationen zu [Anruf- und Mediensteuerelementen)](about-call-and-media-controls.md) veranschaulicht, wie diese Schnittstellen einer TAPI 3-Anwendung angezeigt werden.

Darüber hinaus kann ein MSP private [anbieterspezifische Schnittstellen](provider-specific-interfaces.md)implementieren, die TAPI auf die Standardobjekte aggregiert, die für eine Anwendung verfügbar gemacht werden. Beispielsweise implementiert der Microsoft IPConf MSP, der mit Microsoft Windows 2000 installiert wird, die [**ITParticipant-Schnittstelle,**](itparticipant.md) die Steuerelemente für einzelne Mitglieder einer Konferenz bereitstellt.

Im folgenden Thema werden kurz die MSPs beschrieben, die mit einem Microsoft-Betriebssystem installiert werden können. Ausführliche Informationen zur Konfiguration und Nutzung finden Sie im Resource Kit für die Zielplattform.

Zusätzliche Mediendienstanbieter von Drittanbietern können für bestimmte Protokolle oder für physische Geräte geschrieben werden. Die [Media Service Provider Interface (MSPI)](media-service-provider-interface-mspi-.md) beschreibt die Schnittstellen, die implementiert werden müssen, damit ein MSP mit den Komponenten von Microsoft Telefonie interagieren kann.

 

 
