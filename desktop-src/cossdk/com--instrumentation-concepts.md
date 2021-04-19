---
description: Der com+-Instrumentations Dienst ermöglicht es Ihnen, ihre eigenen com+-ereignisverwaltungs-und Protokollierungs Programme zu erstellen, wenn Sie verschiedene Leistungsmetriken für Ihre COM+-Komponenten anzeigen möchten.
ms.assetid: 07f68734-a382-4fe5-86af-90805f61c68d
title: Com+-Instrumentations Konzepte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d86b5dbb7bb3f6db14d82220d88c58dbc0a8255
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346849"
---
# <a name="com-instrumentation-concepts"></a>Com+-Instrumentations Konzepte

Der com+-Instrumentations Dienst ermöglicht es Ihnen, ihre eigenen com+-ereignisverwaltungs-und Protokollierungs Programme zu erstellen, wenn Sie verschiedene Leistungsmetriken für Ihre COM+-Komponenten anzeigen möchten. Die com+-Instrumentation kann auch verwendet werden, um benutzerdefinierte Ereignisse zu konfigurieren und com+-Ereignisse in Visual Studio Analyzer Format (VSA) zu konvertieren, wenn Sie die MTS-Pakete aktualisieren, die MTS-Ereignisse empfangen.

> [!Note]  
> Ab Windows Server 2003 verfügen nur Administratoren über Lese Zugriffsberechtigungen für die Ablauf Verfolgungs Protokolle für Systemereignisse.

 

Durch Abonnieren der vom System Events Publisher veröffentlichten Ereignisse können Clients die [com+-Instrumentierungs Schnittstellen](com--instrumentation-interfaces.md) implementieren, um Benachrichtigungen für eine Reihe von com+-Leistungsmetriken zu erhalten, z. b. Informationen zu bestimmten COM+-Objekten, com+-Anwendungen und com+-Diensten. Die Metriken werden auf dem Client mit dem [com+](com--events.md)-Ereignis Dienst veröffentlicht, einem LCE-System (lose gekoppelte Ereignisse), das Ereignis Informationen von verschiedenen Verlegern in einem Ereignisspeicher im com+-Katalog speichert.

> [!Note]  
> Die com+-Instrumentation garantiert nicht die Übermittlung eines Ereignisses.

 

Jede Metrik verfügt über einen Zeitstempel, der die Uhrzeit angibt, zu der die Metrik generiert wurde, und nicht die Uhrzeit, zu der Sie gesendet oder empfangen wurde. Der Client kann den Zeitstempel korrelieren und die Kosten für die Ausführung einer COM+-Anwendung, die Kosten einer Transaktion, die in einer COM+-Anwendung ausgeführt wird, oder die Kosten eines Methoden Aufrufes in einer COM+-Anwendung ermitteln.

Sie können den com+-Instrumentations Dienst auch verwenden, um nach den spezifischen leistungsmetrikinformationen zu filtern, die Sie anzeigen möchten. Wenn Sie z. b. eine com+-Instrumentations Schnittstelle oder-Methode abonnieren, können Sie die Eigenschaften für das Abonnement in der [**comsvcereiginfo**](/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo) -Struktur angeben, z. b. die Anwendungs-ID (**guidapp** -Member) oder die Prozess-ID (**dwpid** -Member).

Wenn die Anwendungs-ID angegeben ist, erhalten Sie nur die Metriken aus der angegebenen Anwendung. Wenn die Prozess-ID angegeben ist, erhalten Sie Metriken von der angegebenen Serveranwendung und den Bibliotheksanwendungen, die in diesem Prozess geladen werden. Der Benutzer kann sowohl die Anwendungs-ID als auch die Prozess-ID angeben, aber die Anwendungs-ID muss die der Serveranwendung sein, die im Prozess mit der angegebenen Prozess-ID ausgeführt wird. Wenn keines von beiden angegeben ist, empfängt der Benutzer Metriken von allen Server-und Bibliotheksanwendungen.

Die com+-Instrumentierungs Metriken bieten genügend Informationen, damit die Überwachungsanwendung Sie mit den betriebssystemmetriken für Leistungsanalysen, Kapazitätsplanung und Modellierung und Vorhersage korrelieren kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Com+-Instrumentierungs Schnittstellen](com--instrumentation-interfaces.md)
</dt> </dl>

 

 



