---
title: Ereignisse (Windows-Remoteverwaltung)
description: Der Ereignis Sammler Dienst verwendet das WS-Management-Protokoll, um Ereignisse von Remote Computern zu erfassen.
ms.assetid: 5c8e0559-c576-4ac6-b636-c4a6fc399c9f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 06f96877904a5e76ea61a6b2f636e962e4dbd9b9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391364"
---
# <a name="events-windows-remote-management"></a>Ereignisse (Windows-Remoteverwaltung)

Der Ereignis Sammler Dienst verwendet das WS-Management-Protokoll, um Ereignisse von Remote Computern zu erfassen. Mit dem Event Collector-Dienst können Sie Abonnements für Windows-Ereignisse auf Remote Computern und von Baseboard-Verwaltungs Controllern (BMCs) generierten Hardware Ereignissen erstellen. BMCs müssen das WS-Management-Protokoll unterstützen.

Wenn Sie ein Abonnement erstellen, werden die Ereignisse an den Computer weitergeleitet, auf dem das Abonnement erstellt wurde. Sie werden in der Ereignisanzeige angezeigt.

Hardware Ereignisse, die von der Intelligent Platform Management Interface (IPMI) auf Windows-basierten Computern generiert werden, werden lokal mithilfe des IPMI-Treibers gesammelt und im Hardware Ereignisprotokoll gespeichert. Anschließend können Sie wie andere Ereignisse des Windows-Betriebssystems weitergeleitet werden.

Mit dem Befehlszeilen Tool Wecutil.exe können Sie Abonnements erstellen. Weitere Informationen zur Verwendung dieses Tools erhalten Sie, wenn Sie an einer Eingabeaufforderung **wecutil/?** eingeben. Weitere Informationen zum Event Collector-Dienst finden Sie unter [Windows-Ereignis](/windows/desktop/WEC/windows-event-collector)Sammlung.

> [!Note]  
> Windows-Remoteverwaltung-APIs erfordern, dass alle IPv6-Adressen in eckige Klammern eingeschlossen sind.

 

> [!Caution]
>
> Wenn Sie vom Collector initiierte Abonnements verwenden, begrenzen Sie die Anzahl der Remote Computer auf 500, und isolieren Sie den [Windows-Ereignis](/windows/desktop/WEC/windows-event-collector) Sammlungs Dienst (Wecsvc) in einem separaten Host Prozess.
>
> Ein Verbindungsfehler enthält einen Thread, bis ein Timeout eintritt. Eine große Anzahl von gleichzeitigen Verbindungsfehlern kann die Auslastung des Thread Pools verursachen und den Server als nicht reagierend Renten.

 

 

 
