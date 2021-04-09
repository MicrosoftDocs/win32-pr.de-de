---
description: Bei einem Monitor handelt es sich um eine DLL (Dynamic Link Library), die echt Zeiterfassung von Netzwerk Datenverkehr untersucht.
ms.assetid: 96d04352-5f1c-4964-94d2-692c6b642cb8
title: Monitore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76ed9ad355ab02b5e130b896efd6654df81e492e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959016"
---
# <a name="monitors"></a>Monitore

Bei einem Monitor handelt es sich um eine DLL (Dynamic Link Library), die echt Zeiterfassung von Netzwerk Datenverkehr untersucht. Er sucht nach vordefinierten Bedingungen und generiert dann Ereignisse, wenn diese Bedingungen erkannt werden. Beispielsweise kann ein Ereignis ausgelöst werden, wenn versucht wird, einen Netzwerk Umbruch auszuführen, wenn eine nicht autorisierte Arbeitsstation IP-Adressen ausgibt oder wenn ein Router ausfällt.

> [!Note]  
> Wenn Sie detaillierte Analysen der Netzwerkdaten durchführen müssen, die eine nach Erfassungs Analyse erfordern, müssen Sie [*Experten*](e.md) -und [*Parser*](p.md) -Anwendungen verwenden.

 

Der [*Überwachungs Steuerungs Dienst (Monitor Control Service*](m.md) , mcsvc) stellt das Framework zum Verwalten Ihrer Monitore bereit. Es stellt Funktionen zum Laden der Monitor-DLLs und eine Kommunikationsschnittstelle zum Monitor-Steuerungs Tool bereit, sodass Sie mehrere Instanzen Ihrer Monitore erstellen, konfigurieren, starten, Abbrechen und deaktivieren können.

Monitore werden in zwei Ausführungs Threads ausgeführt. Mcsvc stellt den ersten Thread bereit, der die direkte Steuerung des Monitors ermöglicht. Der zweite Thread wird vom [*Netzwerk Paketanbieter*](n.md) (NPP) bereitgestellt, der eine Möglichkeit bietet, die erfassten Netzwerkdaten, Statistiken und den Status der Erfassung von der NPP zurück an den Monitor zu übergeben.

Es können mehr als eine Instanz desselben Monitors für jede Lauf Zeit-NPP-Schnittstelle vorhanden sein, die zum Erfassen von Daten verwendet wird.

 

 



