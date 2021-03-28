---
description: Mit einem übergeordneten Gerätekontext kann eine Anwendung die Zeit minimieren, die zum Einrichten des Clippingbereichs für ein Fenster erforderlich ist.
ms.assetid: 194d5add-d1a1-4c10-89ee-171ff008a7ab
title: Übergeordnete Geräte Kontexte anzeigen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e423ceaa65790df35fa55c8dda597cb1bb45019
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978441"
---
# <a name="parent-display-device-contexts"></a>Übergeordnete Geräte Kontexte anzeigen

Mit einem über *geordneten Gerätekontext* kann eine Anwendung die Zeit minimieren, die zum Einrichten des Clippingbereichs für ein Fenster erforderlich ist. Eine Anwendung verwendet in der Regel übergeordnete Geräte Kontexte, um das Zeichnen von Steuerungs Fenstern zu beschleunigen, ohne einen privaten oder Klassen Gerätekontext zu erfordern. Beispielsweise verwendet das System die übergeordneten Geräte Kontexte für die Schaltfläche Push-Schaltfläche und Bearbeitungs Steuerelemente. Übergeordnete Geräte Kontexte sind nur für die Verwendung mit untergeordneten Fenstern gedacht, niemals mit den Fenstern der obersten Ebene oder des Popup Fensters.

Eine Anwendung kann den CS- \_ parametrientdc-Stil angeben, um den Ausschneide Bereich des untergeordneten Fensters auf die des übergeordneten Fensters festzulegen, damit das untergeordnete Element in das übergeordnete Fenster gezeichnet werden kann. \_Durch die Angabe von CS-Parametern wird die Leistung einer Anwendung verbessert, da das System den sichtbaren Bereich nicht für jedes untergeordnete Fenster neu berechnen muss.

Vom übergeordneten Fenster festgelegte Attributwerte werden für das untergeordnete Fenster nicht beibehalten. Beispielsweise kann das übergeordnete Fenster den Pinsel nicht für seine untergeordneten Fenster festlegen. Die einzige Eigenschaft, die beibehalten wird, ist der Clippingbereich. Das Fenster muss seine eigene Ausgabe an die Begrenzungen des Fensters Ausschneiden. Da der Clippingbereich für den übergeordneten Gerätekontext mit dem übergeordneten Fenster identisch ist, kann das untergeordnete Fenster potenziell über das gesamte übergeordnete Fenster zeichnen, aber der übergeordnete Gerätekontext darf nicht auf diese Weise verwendet werden.

Das System ignoriert den CS- \_ Parser-Stil, wenn das übergeordnete Fenster einen privaten oder einen Klassen Gerätekontext verwendet, wenn das übergeordnete Fenster seine untergeordneten Fenster schneidet oder wenn das untergeordnete Fenster seine untergeordneten Fenster oder gleich geordneten Fenster schneidet.

 

 



