---
description: Eine opportunistische Sperre (auch als "Oplock" bezeichnet) ist eine Sperre, die von einem Client in einer Datei, die sich auf einem Server befindet, platziert wird.
ms.assetid: b4c2f5f0-a29b-4598-a49b-da99e93d2991
title: Opportunistische Sperren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faec833caae05bff247a7a3655885b1a967f3435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752400"
---
# <a name="opportunistic-locks"></a>Opportunistische Sperren

Eine opportunistische Sperre (auch als "Oplock" bezeichnet) ist eine Sperre, die von einem Client in einer Datei, die sich auf einem Server befindet, platziert wird. In den meisten Fällen fordert ein Client eine opportunistische Sperre an, damit Daten lokal zwischengespeichert werden können, wodurch der Netzwerkverkehr reduziert und die offensichtliche Reaktionszeit verbessert wird. Opportunistische Sperren werden von netzwerkredirectors auf Clients mit Remote Servern sowie von Client Anwendungen auf lokalen Servern verwendet.

Opportunistische Sperren koordinieren das Zwischenspeichern von Daten und die Kohärenz zwischen Clients und Servern sowie zwischen mehreren Clients. Daten, die kohärent sind, sind Daten, die im gesamten Netzwerk identisch sind. Anders ausgedrückt: Wenn Daten kohärent sind, werden die Daten auf dem Server und allen Clients synchronisiert.

Opportunistische Sperren sind keine Befehle vom Client zum Server. Dabei handelt es sich um Anforderungen vom Client an den Server. Aus Sicht des Clients sind Sie opportunistisch. Das heißt, der Server gewährt solche Sperren, wenn andere Faktoren die Sperren ermöglichen.

Wenn eine lokale Anwendung den Zugriff auf eine Remote Datei anfordert, ist die Implementierung von opportunistischen Sperren für die Anwendung transparent. Der Netzwerkredirector und der Beteiligte Server öffnen und schließen die opportunistischen Sperren automatisch. Opportunistische Sperren können jedoch auch verwendet werden, wenn eine lokale Anwendung den Zugriff auf eine lokale Datei anfordert und der Zugriff durch andere Anwendungen und Prozesse delegiert werden muss, um eine Beschädigung der Datei zu verhindern. In diesem Fall fordert die lokale Anwendung direkt eine opportunistische Sperre aus dem lokalen Dateisystem an und speichert die Datei lokal zwischen. Wenn Sie auf diese Weise verwendet wird, ist die opportunistische Sperre tatsächlich ein Semaphor, das vom lokalen Server verwaltet wird. Sie wird hauptsächlich für die Datenkonsistenz in der Datei-und Datei Zugriffs Benachrichtigung verwendet.

Bevor Sie opportunistische Sperren in Ihrer Anwendung verwenden können, sollten Sie mit den Datei Zugriffs-und Freigabe Modi vertraut sein, die unter [Erstellen und Öffnen von Dateien](creating-and-opening-files.md)beschrieben werden.

Die maximale Anzahl von gleichzeitigen opportunistischen Sperren, die Sie erstellen können, ist nur durch die Menge des verfügbaren Arbeitsspeichers beschränkt.

Lokale Anwendungen sollten nicht versuchen, opportunistische Sperren von Remote Servern anzufordern. [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) wird ein Fehler zurückgegeben, wenn versucht wird, dies zu tun.

Opportunistische Sperren sind für Anwendungen sehr eingeschränkt. Der einzige praktische Verwendungszweck ist das Testen eines netzwerkredirectors oder eines Server opportunistischen Lock-Handlers. In der Regel implementieren Dateisysteme Unterstützung für opportunistische sperren. Anwendungen lassen die opportunistische Sperr Verwaltung in der Regel auf die Dateisystem Treiber aus. Jeder, der ein Dateisystem implementiert, sollte das [IFS-Kit (Installable File System)](https://www.microsoft.com/whdc/devtools/ifskit/default.mspx)verwenden. Jeder, der einen anderen Gerätetreiber als ein installier bares Dateisystem entwickelt, sollte das [Windows-Treiberkit (WDK)](https://www.microsoft.com/?ref=go)verwenden.

Opportunistische Sperren und die zugehörigen Vorgänge stellen eine übergeordnete Komponente des opportunistischen Sperr Teils des CIFS-Protokolls (Common Internet File System) dar, einem Internet Entwurf. Das CIFS-Protokoll ist eine erweiterte Version des SMB-Protokolls (Server Message Block). Weitere Informationen finden Sie unter [Übersicht über das Microsoft SMB-Protokoll und CIFS-Protokoll](microsoft-smb-protocol-and-cifs-protocol-overview.md). Der CIFS-Internet Entwurf identifiziert explizit, dass eine CIFS-Implementierung opportunistische Sperren implementieren kann, indem er sie ablehnt.

In den folgenden Themen werden opportunistische Sperren identifiziert.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                               | BESCHREIBUNG                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Lokales Caching](local-caching.md)<br/>                                                                       | Das *lokale Zwischenspeichern* von Daten ist eine Technik, mit der der Netzwerk Zugriff auf Datendateien beschleunigt werden kann. Dies umfasst das Zwischenspeichern von Daten auf Clients und nicht auf Servern, wenn dies möglich ist.<br/>                                                                                                                           |
| [Datenkohärenz](data-coherency.md)<br/>                                                                     | Wenn die Daten kohärent sind, werden die Daten auf dem Server und alle Clients synchronisiert. Eine Art von Softwaresystem, das Datenkonsistenz bereitstellt, ist ein Revisions Steuerungssystem (RCS).<br/>                                                                                                              |
| [Anfordern einer opportunistischen Sperre](how-to-request-an-opportunistic-lock.md)<br/>                         | Opportunistische Sperren werden angefordert, indem zuerst eine Datei mit Berechtigungen und Flags geöffnet wird, die für die Anwendung geeignet sind, die die Datei öffnet. Alle Dateien, für die opportunistische Sperren angefordert werden, müssen für einen überlappenden (asynchronen) Vorgang geöffnet werden.<br/>                                |
| [Server Antwort auf geöffnete Anforderungen für gesperrte Dateien](server-response-to-open-requests-on-locked-files.md)<br/> | Sie können die Auswirkung ihrer Anwendung auf andere Clients und deren Auswirkungen auf Ihre Anwendung minimieren, indem Sie so viele Freigabe Möglichkeiten wie möglich gewähren, die erforderliche Mindestzugriffsebene anfordern und die am wenigsten eindringliche opportunistische Sperre verwenden, die für Ihre Anwendung geeignet ist.<br/> |
| [Typen von opportunistischen Sperren](types-of-opportunistic-locks.md)<br/>                                         | Beschreibt die opportunistischen Sperren auf Ebene 1, Ebene 2, Batch und Filter.<br/>                                                                                                                                                                                                                     |
| [Unterbrechen opportunistischer Sperren](breaking-opportunistic-locks.md)<br/>                                         | Die Unterbrechung einer opportunistischen Sperre ist der Prozess der Herabwürdigung der Sperre, die ein Client in einer Datei hat, damit ein anderer Client die Datei mit oder ohne opportunistische Sperre öffnen kann.<br/>                                                                                                     |
| [Beispiele für die opportunistische Sperre](opportunistic-lock-examples.md)<br/>                                           | Diagramme von Netzwerkverkehrs Ansichten für eine opportunistische Sperre der Ebene 1, eine opportunistische Batch Sperre und eine opportunistische Filter-Sperre.<br/>                                                                                                                                                       |
| [Opportunistische Sperr Vorgänge](opportunistic-lock-operations.md)<br/>                                       | Wenn eine Anwendung opportunistische Sperren anfordert, müssen alle Dateien, für die Sie Sperren anfordert, für überlappende (asynchrone) Eingaben und Ausgaben geöffnet werden, indem [**die Funktion "**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) Funktion" mit dem überlappenden Flag für das **\_ Dateiflag \_** verwendet wird.<br/>                                   |



 

Weitere Informationen zu opportunistischen Sperren finden Sie im CIFS Internet Draft-Dokument. Alle Diskrepanzen zwischen diesem Thema und dem aktuellen CIFS-Internet Entwurf sollten zugunsten des CIFS-Internet Entwurfs gelöst werden.

 

