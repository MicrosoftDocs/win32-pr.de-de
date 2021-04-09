---
description: Eine der ersten Aufgaben, die Sie für einen-Anbieter programmieren müssen, ist der Initialisierungs Prozess, der alle Aufgaben abdeckt, die der Anbieter ausführen muss, sodass er Informationen von WMI senden und empfangen, ein verwaltetes Objekt Steuern und andere Aufgaben ausführen kann.
ms.assetid: 3dc145b8-1ce4-4caa-b2ac-31a3681e76f1
ms.tgt_platform: multiple
title: Initialisieren eines Anbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f14a724d72d5e5c58eff30f2fa61da64d77a493f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868751"
---
# <a name="initializing-a-provider"></a>Initialisieren eines Anbieters

Eine der ersten Aufgaben, die Sie für einen-Anbieter programmieren müssen, ist der Initialisierungs Prozess, der alle Aufgaben abdeckt, die der Anbieter ausführen muss, sodass er Informationen von WMI senden und empfangen, ein verwaltetes Objekt Steuern und andere Aufgaben ausführen kann. Jeder Anbietertyp verfügt über einen anderen Satz von Aufgaben, den er ausführen muss und über einen begleitenden Satz eindeutiger Schnittstellen verfügt.

Allerdings initialisieren alle Anbieter über die [**iwbemproviderinit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) -Schnittstelle und informieren WMI über die [**iwbemproviderinitsink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinitsink) -Schnittstelle über Ihren Initialisierungs Status.

Im folgenden Verfahren wird beschrieben, wie ein Anbieter initialisiert wird.

**So initialisieren Sie einen Anbieter**

1.  Implementieren Sie [**iwbemproviderinit:: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) für Ihren Anbieter.

    Wenn WMI ermittelt, dass ein Client die Dienste eines Anbieters erfordert, lädt WMI den Anbieter durch Aufrufen der Methode [**iwbemproviderinit:: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) .

2.  Implementieren Sie alle Schnittstellen, die für Ihren Anbietertyp eindeutig sind.
3.  Informieren Sie WMI, dass Ihr Anbieter die Initialisierung abgeschlossen hat, indem Sie [**iwbemproviderinitsink:: SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus)aufrufen.

    Alle Implementierungen von [**iwbemproviderinit:: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) müssen [**iwbemproviderinitsink:: SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) aufrufen, um den Initialisierungs Status an WMI zu melden. Mit der **SetStatus** -Methode kann WMI ermitteln, ob ein Anbieter für den Empfang von Anforderungen bereit ist, und die Art der Anforderungen, die der Anbieter empfangen kann.

Im folgenden Verfahren wird beschrieben, wie eine erfolgreiche Initialisierung gemeldet wird.

**So melden Sie eine erfolgreiche Initialisierung**

-   Legen Sie den *istatus* -Parameter von [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) auf **WBEM \_ S \_ Initialized** fest.

    Durch das Zurückgeben von **WBEM S, das \_ \_ Initialisiert** wurde, gibt ein Anbieter eine Bereitschaft zum Verarbeiten von Anforderungen von Anwendungen, WMI und anderen Anbietern an. Nach \_ \_ dem Initialisieren von WBEM S ruft WMI die [**iwbemproviderinit:: QueryInterface**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) -Methode für den Anbieter auf. Diese Abfrage ruft einen Zeiger auf die primäre Schnittstelle des Anbieters ab.

Im folgenden Verfahren wird beschrieben, wie ein Fehler während der Initialisierung gemeldet wird.

**So melden Sie einen Fehler während der Initialisierung**

-   Fehler beim Festlegen des *istatus* -Parameters von [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) auf **WBEM \_ E \_**. WMI-Ansichts Anbieter, die **WBEM \_ E \_** zurückgeben, sind nicht funktionsfähig.

    WMI gibt den [**iwbemproviderinit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) -Zeiger entweder dann frei, nachdem WMI einen Zeiger auf die primäre Schnittstelle des Anbieters abgerufen hat oder wenn die Initialisierung fehlgeschlagen ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwickeln eines WMI-Anbieters](developing-a-wmi-provider.md)
</dt> <dt>

[Festlegen von namepace-Sicherheits Deskriptoren](setting-namespace-security-descriptors.md)
</dt> <dt>

[Sichern Ihres Anbieters](securing-your-provider.md)
</dt> </dl>

 

 



