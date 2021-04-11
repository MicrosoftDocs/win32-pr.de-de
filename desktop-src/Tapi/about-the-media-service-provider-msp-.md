---
description: Ein TAPI 3-Medien Dienstanbieter (MSP) ermöglicht einer Anwendung eine beträchtliche Kontrolle über die Medien für einen bestimmten Transportmechanismus.
ms.assetid: 2dd1268f-b31a-443b-a36b-05c1570e7a8a
title: Informationen zum Media Service Provider (MSP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ef4d19a2f01c047d5fc2afd4a0323d7908fcac
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104132153"
---
# <a name="about-the-media-service-provider-msp"></a>Informationen zum Media Service Provider (MSP)

Ein TAPI 3-Medien Dienstanbieter (MSP) ermöglicht einer Anwendung eine beträchtliche Kontrolle über die Medien für einen bestimmten Transportmechanismus. Ein MSP ist immer mit einem Telefoniedienstanbieter (TSP) gekoppelt. Ebenso wie ein TSP eine Abstraktionsschicht für die aufrufssteuerung ist, steuert der MSP Medien, ohne dass gerätespezifische Codierungen erforderlich sind. Ein Beispiel für die MSP/TSP-Kommunikation finden Sie unter [Übersicht über den TAPI-Dienstanbieter](./tapi-service-provider-overview.md).

Ein MSP ermöglicht die Mediensteuerung durch die Verwendung von speziellen Terminal-, Datenstrom-und substreamschnittstellen, die von TAPI definiert werden. Das Diagramm in [Informationen über die Aufrufe und mediensteuer Elemente](about-call-and-media-controls.md) veranschaulicht, wie diese Schnittstellen für eine TAPI 3-Anwendung angezeigt werden.

Außerdem kann ein MSP private [anbieterspezifische Schnittstellen](provider-specific-interfaces.md)implementieren, die TAPI auf den Standardobjekten aggregiert, die für eine Anwendung verfügbar gemacht werden. Beispielsweise implementiert das Microsoft ipconf msp, das mit Microsoft Windows 2000 installiert wird, die [**itteilnehmer**](itparticipant.md) -Schnittstelle, die Steuerelemente für einzelne Mitglieder einer Konferenz bereitstellt.

Im folgenden Thema werden die MSPs kurz beschrieben, die möglicherweise mit einem Microsoft-Betriebssystem installiert werden. Ausführliche Informationen zur Konfiguration und Verwendung finden Sie im Ressourcenkit für die Zielplattform.

Zusätzliche Medien Dienstanbieter von Drittanbietern können für bestimmte Protokolle oder für physische Geräte geschrieben werden. Die [Media Service Provider Interface (MSPi)](media-service-provider-interface-mspi-.md) beschreibt die Schnittstellen, die implementiert werden müssen, damit ein MSP mit den Komponenten von Microsoft Telefonie interagieren kann.

 

 
