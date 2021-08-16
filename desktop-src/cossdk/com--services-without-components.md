---
description: COM+-Dienste ohne Komponenten
ms.assetid: 5ef67411-334b-476e-b9b7-3677b24ab7df
title: COM+-Dienste ohne Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b395186875c37fb42e5011ee0486aa6de86ffe62b73c8ea1a54c09e82a27c588
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119638450"
---
# <a name="com-services-without-components"></a>COM+-Dienste ohne Komponenten

Mit COM+ 1.5 können Sie die von COM+ bereitgestellten Dienste verwenden, ohne eine Komponente erstellen zu müssen, die die Methoden enthält, die diese Dienste aufrufen. Dies ist für Entwickler von großem Vorteil, die normalerweise keine Komponenten verwenden, aber COM+-Dienste wie Transaktionen oder die COM+-Tracker verwenden möchten. Durch die Verwendung von COM+-Diensten ohne Komponenten können Entwickler den Mehraufwand beim Erstellen einer Komponente vermeiden, die nur für den Zugriff auf die com+-Dienste verwendet wird, die sie benötigen.

Beispielsweise waren Skriptumgebungen traditionell die größten Consumer von COM+-Diensten, konnten diese Dienste jedoch nie effizient verwenden, da die Dienste in einer COM+-Komponente gebündelt werden mussten. Durch diese Bündelungsanforderung erhöhten sich die Leistungskosten aufgrund der erhöhten Kommunikation und duplizierten Daten, die für die Interaktion der Skriptumgebung mit der Komponente erforderlich sind. Durch die Verwendung von Diensten ohne Komponenten werden diese Kosten minimiert.

Die in der folgenden Tabelle beschriebenen Themen enthalten Hintergrund- und Aufgabeninformationen zur Verwendung von COM+-Diensten ohne Komponenten. Dieses Feature richtet sich an fortgeschrittene Visual C++ Entwickler, die sich Sorgen um die Leistung machen.



| Thema                                                                                                 | BESCHREIBUNG                                                                                    |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [COM+-Dienste ohne Komponentenkonzepte](com--services-without-components-concepts.md)<br/> | Bietet eine Übersicht über die Verwendung von COM+-Diensten ohne Komponenten.<br/>                     |
| [COM+-Dienste ohne Komponententasks](com--services-without-components-tasks.md)<br/>       | Enthält Anweisungen für die Verwendung von COM+ zum Erstellen und Verwenden von Diensten ohne Komponenten.<br/> |



 

 

 




