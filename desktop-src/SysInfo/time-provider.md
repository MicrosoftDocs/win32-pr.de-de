---
description: Das Microsoft Windows-Betriebssystem bietet Unterstützung für eine Vielzahl von Hardware Geräten und Netzwerk Zeit Protokollen mithilfe der Zeit Anbieter Architektur.
ms.assetid: a7575373-eeda-4f2a-85e5-d1b50994e7ae
title: Zeit Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c844e2c4d0d49e87e978a47621338b167c4f5a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867380"
---
# <a name="time-provider"></a>Zeit Anbieter

Das Microsoft Windows-Betriebssystem bietet Unterstützung für eine Vielzahl von Hardware Geräten und Netzwerk Zeit Protokollen mithilfe der *Zeit Anbieter* Architektur. Eingabe Zeit Anbieter rufen genaue Zeitstempel von der Hardware oder dem Netzwerk ab, und Ausgabezeit Anbieter stellen Zeitstempel für andere Clients im Netzwerk bereit.

Zeit Anbieter werden vom *Zeit Anbieter-Manager* verwaltet. Er ist verantwortlich für das Laden, starten und Beenden von Zeit Anbietern, die vom Dienststeuerungs-Manager gesteuert werden. Diese Schnittstelle vereinfacht das Schreiben eines Zeit Anbieters, als ein vollständiger Dienst zu schreiben.

-   [Erstellen eines Zeit Anbieters](creating-a-time-provider.md)
-   [Registrieren eines Zeit Anbieters](registering-a-time-provider.md)
-   [Beispiel Zeit Anbieter](sample-time-provider.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Zeitdienst](https://www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/security/ws03mngd/26_s3wts.mspx)
</dt> </dl>

 

 



