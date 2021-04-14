---
description: Monitore wurden für die Verwendung von Windows-Verwaltungsinstrumentation (WMI) zum Auslösen von Ereignissen auf lokalen Computern oder Remote Computern konzipiert.
ms.assetid: b20746dd-d8d9-49b6-95b7-5151ee02901d
title: Überwachen von Ereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d98241081d8a59c33ab173447eaedd903e72eb09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485147"
---
# <a name="monitor-events"></a>Überwachen von Ereignissen

Monitore wurden für die Verwendung von [Windows-Verwaltungsinstrumentation](/windows/desktop/WmiSdk/wmi-start-page) (WMI) zum Auslösen von Ereignissen auf lokalen Computern oder Remote Computern konzipiert.

> [!Note]  
> Da Monitore eine echt Zeiterfassung verwenden, können Sie nur Daten auf dem lokalen Computer erfassen. Dies ist eine Einschränkung der **untc** -Schnittstelle des Netzwerk Paket Anbieters. Mithilfe von WMI-Ereignissen können die erfassten Daten jedoch lokal überprüft werden, während Ereignisse an lokale oder Remote Computer gesendet werden können.

 

Monitore kommunizieren nicht direkt mit WMI. Der [*Überwachungs Steuerungs Dienst (Monitor Control Service*](m.md) , mcsvc) stellt eine Schnittstelle (" [imonitoreventer Enter Enter Enter Enter Enter Enter Enter Enter Enter Enter Enter Enter Enter Enter Enter Enter Enter](imonitoreventer.md))" bereit, mit der der Monitor eine Ereignisdaten Struktur Die mcsvc kann dann die Ereignisdaten Struktur an WMI senden, wodurch wiederum das Ereignis ausgelöst wird.

 

 
