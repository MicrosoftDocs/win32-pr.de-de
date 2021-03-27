---
description: In den folgenden Themen wird beschrieben, wie die ETW-API für die Ereignis Ablauf Verfolgung verwendet wird.
ms.assetid: 7362874a-8206-4973-bb79-a9eaff55feb4
title: Verwenden der Ereignis Ablauf Verfolgung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5141c19838796c0ec29f9eb20add689d56b97757
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214865"
---
# <a name="using-event-tracing"></a>Verwenden der Ereignis Ablauf Verfolgung

In den folgenden Themen wird beschrieben, wie die ETW-API für die Ereignis Ablauf Verfolgung verwendet wird.



| Thema                                                                          | BESCHREIBUNG                                                                                                             |
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [Steuern von Ereignis Ablauf Verfolgungs Sitzungen](controlling-event-tracing-sessions.md)   | Beschreibt, wie Ereignis Ablauf Verfolgungs Sitzungen verwaltet werden.                                                                         |
| [Bereitstellen von Ereignissen](providing-events.md)                                       | Beschreibt, wie ein Ereignis Ablauf Verfolgungs Anbieter registriert und instrumentiert wird.                                                       |
| [Verarbeiten von Ereignissen](consuming-events.md)                                       | Beschreibt, wie Rückruf Funktionen implementiert werden, die zum Verarbeiten und Verarbeiten von Ereignissen aus einer Ablauf Verfolgungs Protokolldatei oder in Echtzeit verwendet werden. |
| [Windows-Ablaufverfolgungs-Präprozessor](windows-software-trace-preprocessor.md) | Bietet einen effizienten Mechanismus zum Protokollieren und Verarbeiten von Ereignissen, die während der Ausführung einer Anwendung oder eines Treibers auftreten.  |



 

Schließen Sie die Header Datei "wmistr. h" ein, bevor Sie die Header Datei "evntrace. h" einschließen.

 

 



