---
description: Die folgende Abbildung zeigt die Beziehung zwischen Monitoren und anderen Komponenten der Netzwerkmonitor Architektur.
ms.assetid: cbd6116c-1a95-4ac4-bc79-632ebe198197
title: Monitor Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c1a36ef19933d888f27079d8d94ddba16bde79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104551686"
---
# <a name="monitor-architecture"></a>Monitor Architektur

Die folgende Abbildung zeigt die Beziehung zwischen [*Monitoren*](m.md) und anderen Komponenten der Netzwerkmonitor Architektur.

![Beziehung zwischen Monitoren und anderen Komponenten des Netzwerk Monitors](images/nmarch2.png)

Der Netzwerk Datenverkehr wird (als einzelne Frames) vom NDIS-Treiber gesammelt. Der Netzwerkmonitor Treiber (Nmnt.sys) leitet die Frames dann an einen Netzwerk Paketanbieter (NPP) weiter, der wiederum die Daten im Echtzeitmodus erfasst. Der npp ist eine Sammlung von COM-Schnittstellen, die zum Erfassen von Daten verwendet werden. In diesem Fall wird die Schnittstelle " [**untc**](irtc.md) " verwendet, um eine echt Zeiterfassung auszuführen.

> [!Note]  
> Der NPP wird für verzögerte und Echt Zeit Erfassungen verwendet. Bei verzögerten Erfassungen, die von Experten und Parser verwendet werden, wird die [**idelta-DC**](idelaydc.md) -Schnittstelle verwendet.

 

Der Monitor überprüft dann die erfassten Daten im Echtzeitmodus und erkennt bestimmte Netzwerkbedingungen und erzeugt Ereignisse nach Bedarf.

Drei weitere Komponenten werden von Überwachungsanwendungen verwendet: das Überwachungs Steuerungs Tool, der Überwachungs Steuerungs Dienst (Monitor Control Service, mcsvc) und die Ereignisanzeige:

-   Das Monitor Steuerungs Tool wird zum Verwalten von Monitor Anwendungen verwendet. Dies umfasst das Konfigurieren und Ausführen aller ihrer Monitor Anwendungen.
-   Der Überwachungs Steuerungs Dienst (Monitor Control Service, mcsvc) löst Ereignisse aus, stellt für die Ereignisanzeige einen Kommunikationslink zu WMI bereit und koordiniert die Verarbeitung von Monitor Vorgängen.
-   Die Ereignisanzeige zeigt die vom Monitor Steuerungs Dienst ausgelösten Ereignisse an.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Imonitor**](imonitor.md)
</dt> <dt>

[**Imonitoreventer Enter**](imonitoreventer.md)
</dt> <dt>

[**"Iran"**](irtc.md)
</dt> </dl>

 

 



