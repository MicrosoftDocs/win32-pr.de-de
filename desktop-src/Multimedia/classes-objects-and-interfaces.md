---
title: Klassen, Objekte und Schnittstellen
description: Klassen, Objekte und Schnittstellen
ms.assetid: 52e48402-32d5-46b0-8eb9-46432e59e36a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54008f316103a8a113e6702e4a4b1192bc0576f5a61fb28b38dbe2502bae881b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119786180"
---
# <a name="classes-objects-and-interfaces"></a>Klassen, Objekte und Schnittstellen

In der Programmiersprache C++ besteht eine *Klasse* aus *Eigenschaften* (oder Memberdaten) und *Methoden* (oder Memberfunktionen). Die Eigenschaften sind Datenelemente, z. B. in einer -Struktur enthaltene Elemente. Die Methoden werden für eine Vielzahl von Zwecken verwendet, z. B. Initialisierung, Zuweisung, Vorgänge und Datenzugriff. Sie verwenden eine Klassendeklaration auf die gleiche Weise wie eine Strukturdeklaration. Arbeitsspeicher wird einer Klasse zugeordnet, wenn Sie ein *Klassenobjekt* definieren. Jedes Klassenobjekt verfügt über einen Datenbereich für seine Eigenschaften und eine Tabelle mit Zeigern auf die unterstützten Methoden.

In OLE besteht ein Objekt wie in C++ aus Daten und Methoden. Ein OLE-Objekt befolgt jedoch strengere Regeln. Die Daten sind streng intern. Ein Objekt macht nur Schnittstellen verfügbar. Eine *Schnittstelle* ist ein Satz verwandter Methoden für ein Objekt. Jedes Objekt kann mehrere Schnittstellen unterstützen. Alle OLE-Schnittstellen unterstützen die [IUnknown-Schnittstelle.](/windows/win32/api/unknwn/nn-unknwn-iunknown)

 

 




