---
description: Mit dem COM+-Instrumentierungsdienst können Sie eigene COM+-Ereignisverwaltungs- und Protokollierungsprogramme erstellen, wenn Sie verschiedene Leistungsmetriken für Ihre COM+-Komponenten anzeigen möchten.
ms.assetid: 07f68734-a382-4fe5-86af-90805f61c68d
title: COM+-Instrumentierungskonzepte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 160a546c07ea4204f1f4da3ba4c56c76a6eed6b52a8d397d470d0bc34b76adc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118549506"
---
# <a name="com-instrumentation-concepts"></a>COM+-Instrumentierungskonzepte

Mit dem COM+-Instrumentierungsdienst können Sie eigene COM+-Ereignisverwaltungs- und Protokollierungsprogramme erstellen, wenn Sie verschiedene Leistungsmetriken für Ihre COM+-Komponenten anzeigen möchten. Die COM+-Instrumentierung kann auch verwendet werden, um benutzerdefinierte Ereignisse zu konfigurieren und COM+-Ereignisse in das Visual Studio Analyzer-Format (VSA) zu konvertieren, wenn Sie MTS-Pakete aktualisieren, die MTS-Ereignisse empfangen.

> [!Note]  
> Ab Windows Server 2003 verfügen nur Administratoren über Lesezugriffsberechtigungen für die Ablaufverfolgungsprotokolle für Systemereignisse.

 

Durch das Abonnieren der vom Systemereignisseherausgeber veröffentlichten Ereignisse [](com--instrumentation-interfaces.md) können Clients die COM+-Instrumentierungsschnittstellen implementieren, um Benachrichtigungen für eine Vielzahl von COM+-Leistungsmetriken zu empfangen, z. B. Informationen zu bestimmten COM+-Objekten, COM+-Anwendungen und COM+-Diensten. Die Metriken werden auf [](com--events.md)dem Client mithilfe des COM+-Ereignisdiensts veröffentlicht. Dabei handelt es sich um ein lose gekoppeltes Ereignissystem (Loosely Coupled Events, LCE), das Ereignisinformationen von verschiedenen Herausgebern in einem Ereignisspeicher im COM+-Katalog speichert.

> [!Note]  
> Die COM+-Instrumentierung garantiert nicht die Übermittlung eines Ereignisses.

 

Jede Metrik verfügt über einen Zeitstempel, der die Zeit angibt, zu der die Metrik generiert wurde, nicht die Zeit, zu der sie versendet oder empfangen wurde. Der Client kann den Zeitstempel korrelieren und die Kosten für die Ausführung einer COM+-Anwendung, die Kosten einer Transaktion, die in einer COM+-Anwendung ausgeführt wird, oder die Kosten eines Methodenaufrufs innerhalb einer COM+-Anwendung herausfinden.

Sie können auch den COM+-Instrumentierungsdienst verwenden, um nach den spezifischen Informationen zu Leistungsmetriken zu filtern, die Sie anzeigen möchten. Wenn Sie beispielsweise eine COM+-Instrumentierungsschnittstelle oder -Methode abonnieren, können Sie Eigenschaften für das Abonnement in der [**COMSVCSEVENTINFO-Struktur**](/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo) angeben, z. B. die Anwendungs-ID (**guidApp-Member)** oder die Prozess-ID (**dwPid-Member).**

Wenn die Anwendungs-ID angegeben ist, erhalten Sie nur die Metriken der angegebenen Anwendung. Wenn die Prozess-ID angegeben ist, erhalten Sie Metriken von der angegebenen Serveranwendung und bibliotheksanwendungen, die in diesem Prozess geladen werden. Der Benutzer kann sowohl die Anwendungs-ID als auch die Prozess-ID angeben, aber die Anwendungs-ID muss die der Serveranwendung sein, die im Prozess mit der angegebenen Prozess-ID ausgeführt wird. Wenn keines von beiden angegeben ist, empfängt der Benutzer Metriken von allen Server- und Bibliotheksanwendungen.

Die COM+-Instrumentierungsmetriken bieten genügend Informationen, damit die Überwachungsanwendung sie mit den Betriebssystemmetriken für Die Leistungsanalyse, Kapazitätsplanung und Modellierung und Vorhersage korrelieren kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM+-Instrumentierungsschnittstellen](com--instrumentation-interfaces.md)
</dt> </dl>

 

 



