---
title: Binden von ACF-Attributen
description: Geben Sie an, wie der Client eine Verbindung mit dem Server für Remoteprozeduraufrufe mit den in der folgenden Tabelle aufgeführten Attributen herstellt.
ms.assetid: 2a9fdd2f-c646-4ccd-bfa8-66fe973ef911
keywords:
- ACF MIDL , Attribute, Bindung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c32b4d53cea81ed2a69a702a1a58942834a538ffbef75cb11315dd792882bf89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118385226"
---
# <a name="binding-acf-attributes"></a>Binden von ACF-Attributen

Geben Sie an, wie der Client eine Verbindung mit dem Server für Remoteprozeduraufrufe mit den in der folgenden Tabelle aufgeführten Attributen herstellt.



| attribute                                                          | Verbrauch                                                                                                                                                                                                              |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Asynchrone**](async.md)                                             | Definiert ein Handle, das es dem Aufrufer ermöglicht, einen asynchronen Aufruf auszuführen und sofort zurückzugeben, ohne auf Ergebnisse zu warten, und synchronisiert dann mit der aufgerufenen Funktion erneut, um Daten nach Abschluss des Aufrufs zu empfangen. |
| [**Automatisches \_ Handle**](auto-handle.md)                                | Weist MIDL an, dass der Stubcode die Bindung automatisch steuern soll. Dies ist die Standardeinstellung, wenn Sie kein Bindungshandle angeben.                                                                                    |
| [**context \_ handle \_ noserialize**](context-handle-noserialize.md) | Garantiert, dass ein Kontexthandle unabhängig vom Standardverhalten der Anwendung nie serialisiert wird.                                                                                                       |
| [**\_Kontexthandle \_ serialisieren**](context-handle-serialize.md)     | Garantiert, dass ein Kontexthandle unabhängig vom Standardverhalten der Anwendung immer serialisiert wird.                                                                                                       |
| [**Explizites \_ Handle**](explicit-handle.md)                        | Ermöglicht der Clientanwendung die Steuerung der Bindung mit einem expliziten Parameter in jeder Prozedur.                                                                                                                      |
| [**Implizites \_ Handle**](implicit-handle.md)                        | Gibt ein Handle für Prozeduren an, die keinen expliziten Handleparameter aufweisen. Die Clientanwendung steuert weiterhin die Bindung.                                                                                |
| [**Striktes \_ \_ Kontexthandle**](strict-context-handle.md)           | Garantiert, dass die Methoden in der -Schnittstelle nur Kontexthandles akzeptieren, die von einer Methode dieser Schnittstelle erstellt wurden.                                                                                     |



 

 

 




