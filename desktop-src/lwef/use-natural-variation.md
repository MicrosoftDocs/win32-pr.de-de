---
title: Verwenden natürlicher Variationen
description: Verwenden natürlicher Variationen
ms.assetid: 5d5750e4-cf30-43dc-9419-7e6bbdb9aa5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6259730599966205f4751c4ada9b8ef361cedf6d1a1a59dd1ce7d67aaf0fb448
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474508"
---
# <a name="use-natural-variation"></a>Verwenden natürlicher Variationen

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

Die Konsistenz der Darstellung in der herkömmlichen Oberfläche Ihrer Anwendung, z. B. Menüs und Dialogfelder, macht die Schnittstelle zwar vorhersagbarer, variiert jedoch die Animation und gesprochene Ausgabe in der Benutzeroberfläche des Zeichens. Das entsprechende Variieren der Antworten des Zeichens bietet eine natürlichere Schnittstelle. Wenn ein Zeichen den Benutzer immer genau auf die gleiche Weise adressiert; Wenn der Benutzer z. B. immer die gleichen Wörter sagt, ist es wahrscheinlich, dass er das Zeichen als "verwaist", "desinteressiert" oder sogar "unerschädigend" betrachtet. Bei der menschlichen Kommunikation kommt es selten zu einer präzisen Wiederholung. Auch wenn wir etwas in einer ähnlichen Situation wiederholen, können wir Formulierungen, Gesten oder Gesichtsausdrücke ändern.

Microsoft Agent ermöglicht es Ihnen, in einer Variation für ein Zeichen zu erstellen. Beim Definieren der Animationen eines Zeichens können Sie Verzweigungswahrscheinlichkeiten für jeden Animationsframe verwenden, um eine Animation zu ändern, wenn sie abspielt. Sie können jedem Zustand auch mehrere Animationen zuweisen. Microsoft Agent wählt bei jedem Initiieren eines Zustands nach dem Zufallsprinzip eine der zugewiesenen Animationen aus. Für die Sprachausgabe können Sie auch vertikale Balkenzeichen in Ihren Ausgabetext eingeben, um den gesprochenen Text automatisch zu variieren. Microsoft Agent wählt beispielsweise nach dem Zufallsprinzip eine der folgenden Anweisungen aus, wenn dieser Text als Teil der [**Speak-Methode verarbeitet**](speak-method.md) wird:

"Das kann ich sagen. \| Das kann ich sagen. \| Ich kann etwas anderes sagen."

 

 




