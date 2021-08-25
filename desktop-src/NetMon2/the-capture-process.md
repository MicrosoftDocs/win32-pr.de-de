---
description: Der Erfassungsprozess ist für jede der vier NPP-Schnittstellen identisch.
ms.assetid: f778aba5-8f66-4fc9-830b-f830c364da56
title: Der Erfassungsprozess
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51a6d82d721f0f85c6b1ab279d556aaad866f70fde7c8e422995cba5be513d8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889588"
---
# <a name="the-capture-process"></a>Der Erfassungsprozess

Der Erfassungsprozess ist für jede der vier NPP-Schnittstellen identisch. In jedem Fall umfasst der Prozess Folgendes:

-   Abrufen des zu verwendende NPP-Schnittstellenobjekts
-   Herstellen einer Verbindung mit dem Netzwerk
-   Starten und anschließendes Beenden der [ *Erfassung*](c.md)
-   Trennen der Verbindung mit dem Netzwerk

> [!Note]  
> Wenn Sie das gewünschte Schnittstellenobjekt abrufen, stellen Sie sicher, dass Sie nur die Methoden aufrufen, die in dieser Schnittstelle enthalten sind. Die folgende Abbildung zeigt, dass jede Schnittstelle ähnliche Methoden zum Erfassen von Netzwerkdaten bereitstellt. Ein Fehler wird zurückgegeben, wenn Sie eine Verbindung mit dem Netzwerk über eine Schnittstelle herstellen und dann versuchen, eine Erfassung mithilfe der Methoden einer anderen Schnittstelle auszuführen.

 

Die folgenden Abbildungen zeigen zwei verschiedene Möglichkeiten zum Ausführen einer Erfassung. Die erste Abbildung zeigt, wie Sie eine oder mehrere sequenzielle Erfassungen ausführen, sodass Sie eine beliebige Anzahl unabhängiger Erfassungen erstellen können.

![Sequenzielle Erfassung](images/capt1.png)

Wie oben gezeigt, können Sie nach dem Herstellen einer Verbindung mit dem Netzwerk eine Erfassung beliebig oft starten und beenden, eine neue Erfassung starten und bei jedem Neustart der Erfassung neue Statistiken generieren. Für eine verzögerte Erfassung mithilfe der [**IDelaydC-Schnittstelle**](idelaydc.md) wird beispielsweise bei jedem Neustart der Erfassung eine neue [*Erfassungsdatei*](c.md) erstellt.

Beachten Sie jedoch auch, dass Sie bei jedem Neustart des Erfassungsprozesses die entsprechende Konfigurationsmethode aufrufen müssen, um die Verbindung neu zu konfigurieren. Damit der erste Aufruf die Erfassung startet, wird die Verbindung durch den Aufruf konfiguriert, um eine Verbindung mit dem Netzwerk herzustellen.

Die zweite Abbildung zeigt, wie Sie eine einzelne Erfassung durch Anhalten und Neustarten ausführen können.

![Einzelne Erfassung durch Anhalten und Neustarten](images/capt2.png)

In diesem Fall können Sie eine Erfassung beliebig oft anhalten und neu starten. Mit diesem Ansatz können Sie eine Erfassung ausführen, deren Daten (und die zugehörigen Statistiken) als einzelne Erfassung aufgezeichnet werden. Wenn Sie beispielsweise eine verzögerte Erfassung mithilfe der [**IDelaydC-Schnittstelle**](idelaydc.md) durchführen möchten, werden alle erfassten Netzwerkinformationen in einer einzigen [*Erfassungsdatei*](c.md)gespeichert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**CreateNPPInterface**](createnppinterface.md)
</dt> <dt>

[**IDelaydC::Configure**](idelaydc-configure.md)
</dt> <dt>

[**IDelaydC::Verbinden**](idelaydc-connect.md)
</dt> <dt>

[**IDelaydC::D isconnect**](idelaydc-disconnect.md)
</dt> <dt>

[**IDelaydC::P ause**](idelaydc-pause.md)
</dt> <dt>

[**IDelaydC::Resume**](idelaydc-resume.md)
</dt> <dt>

[**IDelaydC::Start**](idelaydc-start.md)
</dt> <dt>

[**IDelaydC::Stop**](idelaydc-stop.md)
</dt> <dt>

[**IESP::Configure**](iesp-configure.md)
</dt> <dt>

[**IESP::Verbinden**](iesp-connect.md)
</dt> <dt>

[**IESP::D isconnect**](iesp-disconnect.md)
</dt> <dt>

[**IESP::P ause**](iesp-pause.md)
</dt> <dt>

[**IESP::Resume**](iesp-resume.md)
</dt> <dt>

[**IESP::Start**](iesp-start.md)
</dt> <dt>

[**IESP::Stop**](iesp-stop.md)
</dt> <dt>

[**IRTC::Configure**](irtc-configure.md)
</dt> <dt>

[**IRTC::Verbinden**](irtc-connect.md)
</dt> <dt>

[**IRTC::D isconnect**](irtc-disconnect.md)
</dt> <dt>

[**IRTC::P ause**](irtc-pause.md)
</dt> <dt>

[**IRTC::Resume**](irtc-resume.md)
</dt> <dt>

[**IRTC::Start**](irtc-start.md)
</dt> <dt>

[**IRTC::Stop**](irtc-stop.md)
</dt> <dt>

[**IStats::Configure**](istats-configure.md)
</dt> <dt>

[**IStats::Verbinden**](istats-connect.md)
</dt> <dt>

[**IStats::D isconnect**](istats-disconnect.md)
</dt> <dt>

[**IStats::P ause**](istats-pause.md)
</dt> <dt>

[**IStats::Resume**](istats-resume.md)
</dt> <dt>

[**IStats::Start**](istats-start.md)
</dt> <dt>

[**IStats::Stop**](istats-stop.md)
</dt> </dl>

 

 



