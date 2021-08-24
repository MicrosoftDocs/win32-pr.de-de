---
title: Internet-Aware Objekte
description: Internet-Aware Objekte
ms.assetid: a8228431-5a07-4816-938d-c789ab6a8eaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 280141d4bc9cb1a6a6c685c4badde0b24609996683e73c74f69637440b39ef8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756150"
---
# <a name="internet-aware-objects"></a>Internet-Aware Objekte

Es gibt bestimmte Kategorien, die die Persistenzschnittstellen abdecken. diese wurden als Ergebnis der Definition der Funktionsweise von Steuerelementen im Internet identifiziert. Ein Container, der nicht den gesamten Bereich von Persistenzschnittstellen unterstützt, sollte sicherstellen, dass er kein Steuerelement hosten kann, das eine Kombination von Schnittstellen erfordert, die er nicht unterstützt.

In den folgenden Tabellen wird die Bedeutung verschiedener Kategorien als implementierte und erforderliche Kategorien beschrieben.



| Erforderliche Kategorien                                                                                                                                                                                | Beschreibung                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CATID \_ PersistsToMoniker, CATID \_ PersistsToStreamInit, CATID \_ PersisitsToStream, CATID \_ PersistsToStorage, CATID \_ PersistsToMemory, CATID \_ PersistsToFile, CATID \_ PersistsToPropertyBag<br/> | Jede dieser Kategorien schließen sich gegenseitig aus und wird nur verwendet, wenn ein Objekt überhaupt nur einen Persistenzmechanismus unterstützt (daher der gegenseitige Ausschluss). Container, die den von einer dieser Kategorien beschriebenen Persistenzmechanismus nicht unterstützen, sollten sich selbst daran hindern, Objekte von Klassen zu erstellen, die so markiert sind.<br/> |
| CATID \_ RequiresDataPathHost<br/>                                                                                                                                                             | Das -Objekt erfordert die Möglichkeit, Daten in einem oder mehrere Pfade zu speichern, und erfordert die Einbindung von Containern, daher ist Containerunterstützung für [**IBindHost erforderlich.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775076(v=vs.85))<br/>                                                                                                                                  |



 



| Implementierte Kategorien                                                                                                                                                                            | Beschreibung                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| CATID \_ PersistsToMoniker, CATID \_ PersistsToStreamInit, CATID \_ PersistsToStream, CATID \_ PersistsToStorage, CATID \_ PersistsToMemory, CATID \_ PersistsToFile, CATID \_ PersistsToPropertyBag<br/> | Das -Objekt unterstützt den entsprechenden \* IPersist-Mechanismus für die Kategorie.<br/> |



 

Die folgende Tabelle enthält die genauen CATIDs, die den einzelnen Kategorien zugewiesen sind:



| Kategorie                                | Catid                                           |
|-----------------------------------------|-------------------------------------------------|
| CATID \_ RequiresDataPathHost<br/>  | 0de86a50-2baa-11cf-a229-00aa003d7352<br/> |
| CATID \_ PersistsToMoniker <br/>    | 0de86a51-2baa-11cf-a229-00aa003d7352<br/> |
| CATID \_ PersistsToStorage <br/>    | 0de86a52-2baa-11cf-a229-00aa003d7352<br/> |
| CATID \_ PersistsToStreamInit <br/> | 0de86a53-2baa-11cf-a229-00aa003d7352<br/> |
| CATID \_ PersistsToStream <br/>     | 0de86a54-2baa-11cf-a229-00aa003d7352<br/> |
| CATID \_ PersistsToMemory <br/>     | 0de86a55-2baa-11cf-a229-00aa003d7352<br/> |
| CATID \_ PersistsToFile <br/>       | 0de86a56-2baa-11cf-a229-00aa003d7352<br/> |
| CATID \_ PersistsToPropertyBag<br/> | 0de86a57-2baa-11cf-a229-00aa003d7352<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Komponentenkategorien](component-categories.md)
</dt> </dl>

 

