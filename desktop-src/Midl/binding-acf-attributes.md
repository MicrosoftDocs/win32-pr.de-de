---
title: Binden von ACF-Attributen
description: Geben Sie an, wie der Client für Remote Prozedur Aufrufe mit den in der folgenden Tabelle aufgeführten Attributen eine Verbindung mit dem Server herstellt.
ms.assetid: 2a9fdd2f-c646-4ccd-bfa8-66fe973ef911
keywords:
- ACF-Mittell, Attribute, Bindung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2a2e9ac9ada0ee33c4930005add6a1ca031ee5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037360"
---
# <a name="binding-acf-attributes"></a>Binden von ACF-Attributen

Geben Sie an, wie der Client für Remote Prozedur Aufrufe mit den in der folgenden Tabelle aufgeführten Attributen eine Verbindung mit dem Server herstellt.



| Attribut                                                          | Verbrauch                                                                                                                                                                                                              |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**async**](async.md)                                             | Definiert ein Handle, das dem Aufrufer das Ausführen eines asynchronen Aufrufs ermöglicht und sofort zurückgegeben wird, ohne auf Ergebnisse zu warten |
| [**Automatisches \_ handle**](auto-handle.md)                                | Weist die-Klasse an, den Stub-Code das automatische Steuern der Bindung zu ermöglichen. Dies ist die Standardeinstellung, wenn Sie kein Bindungs Handle angeben.                                                                                    |
| [**Kontext \_ handle \_ noserialize**](context-handle-noserialize.md) | Gewährleistet, dass ein Kontext Handle unabhängig vom Standardverhalten der Anwendung niemals serialisiert wird.                                                                                                       |
| [**Kontext \_ handle- \_ Serialisierung**](context-handle-serialize.md)     | Gewährleistet, dass ein Kontext Handle unabhängig vom Standardverhalten der Anwendung immer serialisiert wird                                                                                                       |
| [**explizites \_ handle**](explicit-handle.md)                        | Ermöglicht es der Client Anwendung, die Bindung mit einem expliziten Parameter in den einzelnen Prozeduren zu steuern.                                                                                                                      |
| [**implizites \_ handle**](implicit-handle.md)                        | Gibt ein Handle für Prozeduren an, die keinen expliziten handle-Parameter aufweisen. Die Client Anwendung steuert die Bindung weiterhin.                                                                                |
| [**Strict- \_ Kontext \_ handle**](strict-context-handle.md)           | Gewährleistet, dass die Methoden in der-Schnittstelle nur Kontext Handles akzeptieren, die von einer-Methode dieser Schnittstelle erstellt wurden.                                                                                     |



 

 

 




