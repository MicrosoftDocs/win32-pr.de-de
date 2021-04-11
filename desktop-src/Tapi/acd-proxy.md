---
description: Bei einem Server für die automatische Aufruf Verteilung handelt es sich um eine Kombination aus Hardware und Software, mit der eingehende Aufrufe von Agents oder ausgehende Aufrufe an Zeilen klassifiziert, in die Warteschlange eingereiht und verteilt werden.
ms.assetid: 29fb0bd7-0ca9-4490-82d2-39550f00a97b
title: ACD-Proxy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c345fbcac3ac3471098e964336a0c3135fd1f582
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960239"
---
# <a name="acd-proxy"></a>ACD-Proxy

Bei einem Server für die automatische Aufruf Verteilung handelt es sich um eine Kombination aus Hardware und Software, mit der eingehende Aufrufe von Agents oder ausgehende Aufrufe an Zeilen klassifiziert, in die Warteschlange eingereiht und verteilt werden.

Bei der Server-ACD-Anwendung handelt es sich um eine TAPI-Proxy Anwendung, die für maximale Effizienz auf demselben Server wie der Telefoniedienstanbieter (TSP) ausgeführt werden soll. Bei einem herkömmlichen ACD-Switch würde die Proxy Anwendung eine Schnittstelle zur internen ACD des Switchs machen und ihren Vorgang verfügbar machen. Eine softwarebasierte oder "virtuelle" ACD-Proxy Anwendung ist vollständig für die Nachverfolgung von aufrufen, Warteschlangen, Gruppen und Agents zuständig und verwendet die Standard-TAPI-Schnittstellen, um die Wechsel Hardware zu steuern. Agent-Client Anwendungen werden in der Regel auf den Arbeitsstationen des einzelnen Agents ausgeführt und verwenden den TAPI-Remote Dienstanbieter für die Kommunikation mit dem tapisrv auf dem Server Computer und somit die Proxy Anwendung.

Die Klassifizierung eingehender Aufrufe ist so konzipiert, dass Sie einen Aufruf an einen Agent erhält, der ihn effektiv verarbeiten kann. Die Klassifizierung kann auf der Anzahl der wählenden, eines IVR-Systems (Interactive Voice Recognition) oder anderer Kriterien basieren. TAPI verwendet das Konzept einer [ACD-Gruppe](about-call-center-controls.md) , um diesen Vorgang darzustellen.

Warteschlangen sind eine ordnungsgemäße und erwartete Methode für Callcenter, um große Lade Zeiträume zu bewältigen. Eine Warteschlange ist normalerweise einer ACD-Gruppe zugeordnet, kann aber erstellt werden, um ausgehende Zeilen oder eingehende Aufrufe zu verarbeiten, die auf eine IVR-Anwendung warten. Weitere Informationen finden Sie unter [Warteschlangen](about-call-center-controls.md) .

Die Aufrufe der Verteilung an Agents oder Gruppen von Agents sind möglicherweise einheitlich, basieren jedoch in der Regel auf Daten wie z. b. den Informationen zum Telefon, der agentverfügbarkeit und der Fähigkeit Der TAPI- [Agent-Handler](about-call-center-controls.md) bietet Zugriff auf Informationen wie die agentverfügbarkeit und Adressen für die Übertragung von Aufrufen an Agents.

Zusätzlich zur einfachen aufrufsverteilung bietet ein ACD-System die Verwaltung und Berichterstattung zur Systemleistung. Statistiken, die in Warteschlangen, Gruppen und Agents gesammelt werden, werden verwendet, um die Leistung des Systems zu verfeinern und zu verbessern. Sie werden in der Regel als Grundlage für die agentvergütung verwendet.

 

 



