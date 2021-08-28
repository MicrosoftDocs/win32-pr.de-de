---
description: Die folgende Abbildung zeigt die Beziehung zwischen Monitoren und anderen Komponenten der Netzwerkmonitor-Architektur.
ms.assetid: cbd6116c-1a95-4ac4-bc79-632ebe198197
title: Überwachen der Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9cd0a099fc1474255b36f1f04d28899b25a527fee19ba1d29434b4692615ab8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119677125"
---
# <a name="monitor-architecture"></a>Überwachen der Architektur

Die folgende Abbildung zeigt die Beziehung zwischen [*Monitoren*](m.md) und anderen Komponenten der Netzwerkmonitor-Architektur.

![Beziehung zwischen Monitoren und anderen Komponenten des Netzwerkmonitors](images/nmarch2.png)

Der Netzwerkdatenverkehr wird (als einzelne Frames) vom NDIS-Treiber erfasst. Der Netzwerkmonitor-Treiber (Nmnt.sys) leitet die Frames dann an einen Netzwerkpaketanbieter (Network Packet Provider, NPP) weiter, der wiederum die Daten im Echtzeitmodus erfasst. Das NPP ist eine Sammlung von COM-Schnittstellen, die zum Erfassen von Daten verwendet werden. In diesem Fall wird die [**IRTC-Schnittstelle**](irtc.md) verwendet, um eine Echtzeiterfassung durchzuführen.

> [!Note]  
> Das NPP wird für verzögerte Erfassungen und Echtzeiterfassungen verwendet. Für verzögerte Erfassungen, die von Experten und Parsern verwendet werden, wird die [**IDelaydC-Schnittstelle**](idelaydc.md) verwendet.

 

Der Monitor untersucht dann die erfassten Daten im Echtzeitmodus, erkennt bestimmte Netzwerkbedingungen und generiert nach Bedarf Ereignisse.

Drei weitere Komponenten werden von Monitoranwendungen verwendet: das Monitor Control Tool, der Monitor Control Service (MCSVC) und die Ereignisanzeige:

-   Das Monitor Control Tool wird verwendet, um Ihre Überwachungsanwendungen zu verwalten. Dies umfasst das Konfigurieren und Ausführen aller Überwachungsanwendungen.
-   Der Monitor Control Service (MCSVC) löst Ereignisse aus, stellt einen Kommunikationslink zu WMI für die Ereignisanzeige bereit und koordiniert die Verarbeitung von Überwachungsvorgängen.
-   Der Ereignisanzeige zeigt die vom Überwachungssteuerungsdienst ausgelösten Ereignisse an.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Imonitor**](imonitor.md)
</dt> <dt>

[**IMonitorEventer**](imonitoreventer.md)
</dt> <dt>

[**IRTC**](irtc.md)
</dt> </dl>

 

 



