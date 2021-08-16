---
title: IAgentSpeechInputProperties
description: IAgentSpeechInputProperties
ms.assetid: 87bfc8c4-473b-4df9-becd-e90db12dae51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 660848eae85465ea322bcb08a218c6ee463eb384d3a4766cacf6a86038662386
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609330"
---
# <a name="iagentspeechinputproperties"></a>IAgentSpeechInputProperties

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

IAgentSpeechInputProperties bietet Zugriff auf die Vom Server verwalteten Spracheingabeeigenschaften. Die meisten Eigenschaften sind für Clientanwendungen schreibgeschützt, aber der Benutzer kann sie im Eigenschaftenblatt des Microsoft-Agents ändern. Der Microsoft Agent-Server gibt Nur Werte zurück, wenn eine kompatible Sprach-Engine installiert und aktiviert wurde. Beim Abfragen dieser Eigenschaften wird versucht, die Sprach-Engine zu starten.

**Methoden in Vtable-Reihenfolge**



| IAgentSpeechInputProperties-Methoden                                     | BESCHREIBUNG                                               |
|-------------------------------------------------------------------------|-----------------------------------------------------------|
| [**Getenabled**](iagentspeechinputproperties--getenabled.md)           | Gibt zurück, ob die Spracherkennungs-Engine aktiviert ist. |
| [**GetHotKey**](iagentspeechinputproperties--gethotkey.md)             | Gibt die aktuelle Schlüsselzuweisung des Lauschen-Schlüssels zurück.  |
| [**GetListeningTip**](iagentspeechinputproperties--getlisteningtip.md) | Gibt zurück, ob der Lauschende Tipp aktiviert ist.             |



 

[**Die Methoden GetInstalled,**](https://www.bing.com/search?q=**GetInstalled**) [**GetLCID,**](https://www.bing.com/search?q=**GetLCID**) [**GetEngine**](https://www.bing.com/search?q=**GetEngine**)und [**SetEngine**](https://www.bing.com/search?q=**SetEngine**) (unterstützt in früheren Versionen von Microsoft Agent) werden aus Gründen der Abwärtskompatibilität weiterhin unterstützt. Die Methoden sind jedoch nicht im Stub und geben keine nützlichen Werte zurück. Verwenden [**Sie GetSRModeID**](https://www.bing.com/search?q=**GetSRModeID**) und [**SetSRModeID**](https://www.bing.com/search?q=**SetSRModeID**) zum Abfragen und Festlegen der Spracherkennungs-Engine, die mit dem Zeichen verwendet werden soll. Beachten Sie, dass die Engine mit der aktuellen Spracheinstellung des Zeichens übereinstimmen muss.

 

 




