---
description: Nachverfolgen nicht zugewiesener Ressourcen
ms.assetid: ebaca876-5249-4b6b-b0d5-08f098e3f5f5
title: Nachverfolgen nicht zugewiesener Ressourcen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9c9f814e08798b4fbb0f160e0d0e0f8aabebba7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342607"
---
# <a name="tracking-non-allocated-resources"></a>Nachverfolgen nicht zugewiesener Ressourcen

Der Dispenser Manager kann eine Ressource, die nicht inventarisiert ist, basierend auf dem Wissen der Lebensdauer des Objekts nachverfolgen. Wenn eine nach verfolgte, nicht zugewiesene Ressource freigegeben wird, wird Sie zerstört und daher nicht an die Inventur zurückgegeben. Dieser Modus für Ressourcen, die für die Erstellung und Zerstörung kostengünstiger sind, ist nützlicher als die Speicherung im Inventar. Dieser Modus ist auch nützlich für die Verwaltung eines Speicher Verteilers oder für eine Ressource, die schwer zu inventarisieren ist, da zu viele verschiedene Typen vorhanden sind.

Im Modus "nur Nachverfolgung" erstellt ein Ressourcen Verteiler direkt eine angeforderte Ressource, anstatt den Dispenser-Manager aufzufordern, einen aus dem Inventar zuzuordnen. Bevor diese Ressource an die anfordernde Anwendungs Komponente zurückgegeben wird, weist der Ressourcen Verteiler dem Dispenser Manager an, die Ressource zu überprüfen. auf diese Weise wird sichergestellt, dass selbst dann, wenn die Komponente die Ressource nicht freigibt, der Dispenser-Manager dies tut, wenn die Lebensdauer der Komponente übersteigt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konzepte des com+-Ressourcen Verteilers](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



