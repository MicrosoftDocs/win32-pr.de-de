---
title: Einführung für Benutzer des SDK für den Windows Media-Format
description: Einführung für Benutzer des SDK für den Windows Media-Format
ms.assetid: 21f06c43-213e-4fbf-a33a-c1890b4b40ce
keywords:
- Windows Media-Format-SDK, erweiterte DRM-Client-APIs
- Windows Media-Format-SDK, erweiterte Client-APIs
- Windows Media-Format-SDK, erweiterte APIs
- SDK für Windows Media-Format, APIs
- Windows Media-Format-SDK, Digital Rights Management (DRM)
- Digital Rights Management (DRM), erweiterte Client-APIs
- DRM (Digital Rights Management), erweiterte Client-APIs
- Digital Rights Management (DRM), erweiterte APIs
- DRM (Digital Rights Management), erweiterte APIs
- Digital Rights Management (DRM), APIs
- DRM (Digital Rights Management), APIs
- Erweiterte APIs für den DRM-Client, Informationen zu
- Erweiterte Client-APIs, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 538978305e4df952ed97e063b3512ce9fd5cfc34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388354"
---
# <a name="introduction-for-users-of-the-windows-media-format-sdk"></a>Einführung für Benutzer des SDK für den Windows Media-Format

Ein Großteil der Funktionen, die von den erweiterten APIs des Windows Media DRM-Clients bereitgestellt werden, ist identisch mit der Funktionalität, die von den Objekten des Windows Media Format SDK bereitgestellt wird. Das Windows Media-Format-SDK stellt Entwicklern die Objekte zur Verfügung, die zum Erstellen, zugreifen auf und Bearbeiten von Mediendateien benötigt werden, die die Dateistruktur von Advanced Systems Format (ASF) verwenden. Da Windows Media DRM zum Schutz von ASF-Dateien vorgesehen ist, waren Client seitige DRM-Funktionen im Windows Media-Format-SDK enthalten.

Die erweiterten APIs des Windows Media DRM-Clients werden in Verbindung mit der Microsoft-Plattform der nächsten Generation (Digital Media), dem Microsoft Media Foundation SDK, veröffentlicht. In Media Foundation werden die Funktionen von ASF enthalten sein, die einige der Features des Windows Media SDK überlappen. Da jetzt zwei Microsoft SDKs zur Bearbeitung von ASF-Dateien vorhanden sind, wird die Client seitige DRM-Funktionalität vom Windows Media-Format-SDK in die erweiterten APIs des Windows Media DRM-Clients aufgeteilt. Auf diese APIs kann von Benutzern des Windows Media-Format-SDK und des Media Foundation SDK zugegriffen werden. Derzeit sind diese APIs als Teil des Windows Media Format SDK-Installationspakets enthalten und werden als Teil des SDK für den Windows Media-Format dokumentiert. Die erweiterten APIs des Windows Media DRM-Clients werden jedoch in ihrer eigenen Bibliothek implementiert und verfügen über eine eigene Header Datei. Nach der Installation des Windows Media Format SDK können diese APIs einzeln verwendet werden, ohne dass Windows Media Format SDK-Header oder-Bibliotheken in Ihre Anwendung eingeschlossen werden.

Wenn Sie Anwendungen entwickeln, die das SDK für den Windows Media-Format verwenden, müssen Sie entscheiden, ob die von SDK bereitgestellte DRM-Funktionalität verwendet oder die erweiterten APIs des Windows Media DRM-Clients verwendet werden sollen. Obwohl viele der Features dieser beiden sdker sehr ähnlich sind, bieten die erweiterten APIs für den Windows Media DRM-Client die folgenden Features, die für Benutzer der älteren DRM-Routinen nicht verfügbar sind:

-   Möglichkeit zum Importieren von Inhalten, die von einem Drittanbieter-Rechte Verwaltungssystem geschützt werden.
-   Möglichkeit zum Exportieren von Inhalten, die von Windows Media DRM geschützt sind, in ein Rights Management-System von Drittanbietern.
-   Direkte Enumeration von Lizenzen im Lizenz Speicher.
-   Einfache, aggregierte Rechte Abfragen basierend auf der Schlüssel-ID (es ist nicht erforderlich, die Mediendatei zu laden).
-   Möglichkeit zum Erneuern von widerrufenen Komponenten mithilfe der Standard Media Foundation-Schnittstelle **imfcontentenabler**.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zu den erweiterten APIs für den Windows Media DRM-Client**](about-the-windows-media-drm-client-extended-apis.md)
</dt> </dl>

 

 




