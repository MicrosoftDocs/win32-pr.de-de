---
description: Das Microsoft Windows-Betriebssystem bietet Unterstützung für eine Vielzahl von Hardwaregeräten und Netzwerkzeitprotokollen mithilfe der Zeitanbieterarchitektur.
ms.assetid: a7575373-eeda-4f2a-85e5-d1b50994e7ae
title: Zeitanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67f2073e94bdf893793b4ae1df2974226aa197de4ff429be9ce8f2a2e4b5f597
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117957904"
---
# <a name="time-provider"></a>Zeitanbieter

Das Microsoft Windows-Betriebssystem bietet Unterstützung für eine Vielzahl von Hardwaregeräten und Netzwerkzeitprotokollen mithilfe der *Zeitanbieterarchitektur.* Eingabezeitanbieter rufen genaue Zeitstempel von der Hardware oder dem Netzwerk ab, und Ausgabezeitanbieter stellen anderen Clients im Netzwerk Zeitstempel zur Verfügung.

Zeitanbieter werden vom *Zeitanbieter-Manager verwaltet.* Sie ist für das Laden, Starten und Beenden von Zeitanbietern verantwortlich, wie vom Dienststeuerungs-Manager geleitet. Diese Schnittstelle erleichtert das Schreiben eines Zeitanbieters als das Schreiben eines vollständigen Diensts.

-   [Erstellen eines Zeitanbieters](creating-a-time-provider.md)
-   [Registrieren eines Zeitanbieters](registering-a-time-provider.md)
-   [Beispielzeitanbieter](sample-time-provider.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Zeitdienst](https://www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/security/ws03mngd/26_s3wts.mspx)
</dt> </dl>

 

 



