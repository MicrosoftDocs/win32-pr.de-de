---
description: Ein Monitor ist eine Dll (Dynamic Link Library), die Echtzeiterfassungen des Netzwerkdatenverkehrs untersucht.
ms.assetid: 96d04352-5f1c-4964-94d2-692c6b642cb8
title: Monitore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29adc2e3abaa165903b78ac10683f76ce07719b7513cd25b8b4a7ca4377bb6c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364633"
---
# <a name="monitors"></a>Monitore

Ein Monitor ist eine Dll (Dynamic Link Library), die Echtzeiterfassungen des Netzwerkdatenverkehrs untersucht. Er sucht nach vordefinierten Bedingungen und generiert dann Ereignisse, wenn diese Bedingungen erkannt werden. Beispielsweise kann ein Ereignis ausgelöst werden, wenn ein Netzwerkeinbruch versucht wird, wenn eine nicht autorisierte Arbeitsstation IP-Adressen aushing oder wenn ein Router ausfällt.

> [!Note]  
> Wenn Sie detaillierte Analysen von Netzwerkdaten durchführen müssen, die eine [](e.md) Analyse nach der Erfassung erfordern, müssen Sie Experten- und [*Parseranwendungen*](p.md) verwenden.

 

Der [*Monitor Control Service*](m.md) (MCSVC) stellt das Framework für die Verwaltung Ihrer Monitore zur Verfügung. Sie stellt Funktionen zum Laden der Monitor-DLLs und eine Kommunikationsschnittstelle für das Monitor control Tool bereit, damit Sie mehrere Instanzen Ihrer Monitore erstellen, konfigurieren, starten, beenden und deaktivieren können.

Monitore werden in zwei Ausführungsthreads ausgeführt. McSVC stellt den ersten Thread zur direkten Steuerung des Monitors zur Anwendung. Der zweite Thread wird vom Netzwerkpaketanbieter (Network [*Packet Provider,*](n.md) NPP) bereitgestellt, der eine Möglichkeit bietet, die erfassten Netzwerkdaten, Statistiken und den Status der Erfassung vom NPP zurück an den Monitor zu übergeben.

Für jede NPP-Laufzeitschnittstelle, die zum Erfassen von Daten verwendet wird, kann mehr als eine Instanz desselben Monitors vorhanden sein.

 

 



