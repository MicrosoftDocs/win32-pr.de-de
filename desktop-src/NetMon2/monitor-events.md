---
description: Monitore sind so konzipiert, dass sie Windows Management Instrumentation (WMI) verwenden, um Ereignisse auf lokalen oder Remotecomputern auszuleiten.
ms.assetid: b20746dd-d8d9-49b6-95b7-5151ee02901d
title: Überwachen von Ereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ebe76ddd8df02694f871899e0b172dda3529fc29c0e16b6b4a65e2ad15bd2ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995480"
---
# <a name="monitor-events"></a>Überwachen von Ereignissen

Monitore sind so konzipiert, dass [sie Windows Management Instrumentation](/windows/desktop/WmiSdk/wmi-start-page) (WMI) verwenden, um Ereignisse auf lokalen oder Remotecomputern auszuleiten.

> [!Note]  
> Da Monitore eine Echtzeiterfassung verwenden, können sie daten nur auf dem lokalen Computer erfassen. Dies ist eine Einschränkung der **IRTC-Schnittstelle** des Netzwerkpaketanbieters. Mithilfe von WMI-Ereignissen können die erfassten Daten jedoch lokal untersucht werden, während Ereignisse an lokale oder Remotecomputer gesendet werden können.

 

Monitore kommunizieren nicht direkt mit WMI. Der [*Monitor Control Service*](m.md) (MCSVC) stellt eine Schnittstelle (IMonitorEventer) bereit, mit der der Monitor eine Ereignisdatenstruktur abrufen und mit den relevanten Informationen füllen kann. [](imonitoreventer.md) McSVC kann dann die Ereignisdatenstruktur an WMI senden, wodurch wiederum das Ereignis ausgelöst wird.

 

 
