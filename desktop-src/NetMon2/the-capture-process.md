---
description: Der Aufzeichnungsprozess ist für jede der vier NPP-Schnittstellen identisch.
ms.assetid: f778aba5-8f66-4fc9-830b-f830c364da56
title: Der Erfassungsprozess
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e0ca1987266b7e042713f1d1c292cf63d5e3ccf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104552348"
---
# <a name="the-capture-process"></a>Der Erfassungsprozess

Der Aufzeichnungsprozess ist für jede der vier NPP-Schnittstellen identisch. In jedem Fall umfasst der Prozess Folgendes:

-   Abrufen des zu verwendenden NPP-Schnittstellen Objekts
-   Herstellen einer Verbindung mit dem Netzwerk
-   Starten und anschließendes Beenden der [ *Erfassung*](c.md)
-   Trennen der Verbindung mit dem Netzwerk

> [!Note]  
> Wenn Sie das gewünschte Schnittstellen Objekt erhalten, stellen Sie sicher, dass Sie nur die in dieser Schnittstelle enthaltenen Methoden aufzurufen. Die folgende Abbildung zeigt, dass jede Schnittstelle ähnliche Methoden zum Erfassen von Netzwerkdaten bereitstellt. Ein Fehler wird zurückgegeben, wenn Sie mit einer Schnittstelle eine Verbindung mit dem Netzwerk herstellen und dann versuchen, eine Erfassung mithilfe der Methoden einer anderen Schnittstelle auszuführen.

 

Die folgenden Abbildungen zeigen zwei verschiedene Möglichkeiten, wie Sie eine Erfassung durchführen können. In der ersten Abbildung wird gezeigt, wie Sie eine oder mehrere sequenzielle Erfassungen ausführen, sodass Sie eine beliebige Anzahl von unabhängigen Erfassungen erstellen können.

![sequenzielle Erfassung](images/capt1.png)

Wie oben gezeigt, können Sie nach dem Herstellen einer Verbindung mit dem Netzwerk eine Erfassung beliebig oft starten und Abbrechen, eine neue Erfassung starten und jedes Mal neue Statistiken erstellen, wenn Sie die Erfassung neu starten. Bei einer verzögerten Erfassung mit der [**idelta-DC**](idelaydc.md) -Schnittstelle wird z. b. jedes Mal eine neue [*Erfassungs Datei*](c.md) erstellt, wenn Sie die Erfassung neu starten.

Beachten Sie jedoch, dass Sie jedes Mal, wenn Sie den Erfassungsprozess neu starten, die geeignete Configure-Methode zum Neukonfigurieren der Verbindung abrufen müssen. Für den ersten-Befehl zum Starten der Erfassung wird die Verbindung durch den-Befehl zum Herstellen einer Verbindung mit dem Netzwerk konfiguriert.

Die zweite Abbildung zeigt, wie Sie eine einzelne Erfassung ausführen können, indem Sie anhalten und neu starten.

![einzelne Erfassung durch anhalten und Neustarten](images/capt2.png)

In diesem Fall können Sie eine Erfassung beliebig oft anhalten und neu starten. Bei diesem Ansatz können Sie eine Erfassung ausführen, deren Daten (und die zugehörigen Statistiken) als einzelne Erfassung aufgezeichnet werden. Um z. b. eine verzögerte Erfassung mithilfe der [**idelta-DC**](idelaydc.md) -Schnittstelle auszuführen, werden alle erfassten Netzwerkinformationen in einer einzigen [*Erfassungs Datei*](c.md)gespeichert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**"Kreatenppinterface"**](createnppinterface.md)
</dt> <dt>

[**Idelta aydc:: Configure**](idelaydc-configure.md)
</dt> <dt>

[**Idelta aydc:: Connect**](idelaydc-connect.md)
</dt> <dt>

[**Idelta aydc::D isconnect**](idelaydc-disconnect.md)
</dt> <dt>

[**Idelta aydc::P ause**](idelaydc-pause.md)
</dt> <dt>

[**Idelta aydc:: Resume**](idelaydc-resume.md)
</dt> <dt>

[**Idelta aydc:: Start**](idelaydc-start.md)
</dt> <dt>

[**Idelta aydc:: Beendigung**](idelaydc-stop.md)
</dt> <dt>

[**IESP:: Configure**](iesp-configure.md)
</dt> <dt>

[**IESP:: Connect**](iesp-connect.md)
</dt> <dt>

[**IESP::D isconnect**](iesp-disconnect.md)
</dt> <dt>

[**IESP::P ause**](iesp-pause.md)
</dt> <dt>

[**IESP:: Resume**](iesp-resume.md)
</dt> <dt>

[**IESP:: Start**](iesp-start.md)
</dt> <dt>

[**IESP:: Beendigung**](iesp-stop.md)
</dt> <dt>

[**"Iran:: Configure"**](irtc-configure.md)
</dt> <dt>

[**Iran:: Connect**](irtc-connect.md)
</dt> <dt>

[**:D isconnect**](irtc-disconnect.md)
</dt> <dt>

[**Iran::P ause**](irtc-pause.md)
</dt> <dt>

[**Iran:: Resume**](irtc-resume.md)
</dt> <dt>

[**"Iran:: Start"**](irtc-start.md)
</dt> <dt>

[**Iran:: Beendigung**](irtc-stop.md)
</dt> <dt>

[**IStats:: Configure**](istats-configure.md)
</dt> <dt>

[**IStats:: Connect**](istats-connect.md)
</dt> <dt>

[**IStats::D isconnect**](istats-disconnect.md)
</dt> <dt>

[**IStats::P ause**](istats-pause.md)
</dt> <dt>

[**IStats:: Resume**](istats-resume.md)
</dt> <dt>

[**IStats:: Start**](istats-start.md)
</dt> <dt>

[**IStats:: Beendigung**](istats-stop.md)
</dt> </dl>

 

 



