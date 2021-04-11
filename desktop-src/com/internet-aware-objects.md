---
title: Internet-Aware Objekte
description: Internet-Aware Objekte
ms.assetid: a8228431-5a07-4816-938d-c789ab6a8eaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 806b8887309760417247cb176c84cda1605bd5aa
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103949161"
---
# <a name="internet-aware-objects"></a>Internet-Aware Objekte

Es wurden bestimmte Kategorien identifiziert, um die Persistenz-Schnittstellen abzudecken. Diese wurden durch Definieren der Funktionsweise von Steuerelementen über das Internet identifiziert. Ein Container, der den vollständigen Bereich der Persistenz-Schnittstellen nicht unterstützt, sollte sicherstellen, dass er kein Steuerelement hostet, das eine Kombination von Schnittstellen erfordert, die es nicht unterstützt.

In den folgenden Tabellen wird die Bedeutung für verschiedene Kategorien sowohl als implementierte als auch als erforderliche Kategorien beschrieben.



| Erforderliche Kategorien                                                                                                                                                                                | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CATID \_ persiststomoniker, CATID \_ persiststostreaminit, CATID \_ persisitstostream, CATID \_ persiststostorage, CATID \_ persiststomemory, CATID \_ persiststofile, CATID \_ persiststopropertybag<br/> | Jede dieser Kategorien schließt sich gegenseitig aus und wird nur verwendet, wenn ein Objekt überhaupt nur einen Persistenzmechanismus unterstützt (also den gegenseitigen Ausschluss). Container, die den Persistenzmechanismus nicht unterstützen, der in einer dieser Kategorien beschrieben wird, sollten das Erstellen von Objekten von Klassen verhindern, die als markiert sind.<br/> |
| CATID "Requirements \_ sdatapathhost"<br/>                                                                                                                                                             | Das-Objekt erfordert die Möglichkeit, Daten in einem oder mehreren Pfaden zu speichern, und erfordert eine Container Beteiligung und erfordert daher Container Unterstützung für [**ibindhost**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775076(v=vs.85)).<br/>                                                                                                                                  |



 



| Implementierte Kategorien                                                                                                                                                                            | BESCHREIBUNG                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| CATID \_ persiststomoniker, CATID \_ persiststostreaminit, CATID \_ persiststostream, CATID \_ persiststostorage, CATID \_ persiststomemory, CATID \_ persiststofile, CATID \_ persiststopropertybag<br/> | Object unterstützt den entsprechenden ipersistent- \* Mechanismus für die Kategorie.<br/> |



 

In der folgenden Tabelle werden die genauen CATIDs bereitstellt, die den einzelnen Kategorien zugewiesen sind:



| Category                                | CATID                                           |
|-----------------------------------------|-------------------------------------------------|
| CATID "Requirements \_ sdatapathhost"<br/>  | 0un86a50-2baa-11CF-A229-00aa003d7352<br/> |
| CATID \_ persiststomoniker <br/>    | 0un86a51-2baa-11CF-A229-00aa003d7352<br/> |
| CATID \_ persiststostorage <br/>    | 0un86a52-2baa-11CF-A229-00aa003d7352<br/> |
| CATID \_ persiststostreaminit <br/> | 0un86a53-2baa-11CF-A229-00aa003d7352<br/> |
| CATID \_ persiststostream <br/>     | 0un86a54-2baa-11CF-A229-00aa003d7352<br/> |
| CATID \_ persiststomemory <br/>     | 0un86a55-2baa-11CF-A229-00aa003d7352<br/> |
| CATID \_ persiststofile <br/>       | 0un86a56-2baa-11CF-A229-00aa003d7352<br/> |
| CATID \_ persiststopropertybag<br/> | 0un86a57-2baa-11CF-A229-00aa003d7352<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Komponentenkategorien](component-categories.md)
</dt> </dl>

 

