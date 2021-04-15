---
title: Klassen, Objekte und Schnittstellen
description: Klassen, Objekte und Schnittstellen
ms.assetid: 52e48402-32d5-46b0-8eb9-46432e59e36a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d4892a805c87122ff7fb6db80feb52a7dcd7625
ms.sourcegitcommit: 52d79b29f3b9933c8bef43207ff80c668a81cb73
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "104474614"
---
# <a name="classes-objects-and-interfaces"></a>Klassen, Objekte und Schnittstellen

In der Programmiersprache C++ besteht eine- *Klasse* aus *Eigenschaften* (oder Elementdaten) und *Methoden* (oder Element Funktionen). Die Eigenschaften sind Datenelemente, die in einer Struktur enthalten sind. Die Methoden werden für eine Vielzahl von Zwecken verwendet, wie z. b. Initialisierung, Zuweisung, Vorgänge und Datenzugriff. Eine Klassen Deklaration wird auf die gleiche Weise wie eine Struktur Deklaration verwendet. Arbeitsspeicher wird für eine Klasse zugewiesen, wenn Sie ein Klassen *Objekt* definieren. Jedes Klassenobjekt verfügt über einen Datenbereich für seine Eigenschaften und eine Tabelle mit Zeigern auf die unterstützten Methoden.

In OLE besteht ein Objekt aus Daten und Methoden, wie es in C++ der Fall ist. Ein OLE-Objekt befolgt jedoch strengere Regeln. Die Daten sind streng intern. Ein-Objekt macht nur Schnittstellen verfügbar. Eine *Schnittstelle* ist ein Satz verwandter Methoden für ein Objekt. Jedes-Objekt kann mehrere Schnittstellen unterstützen. Alle OLE-Schnittstellen unterstützen die [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.

 

 




