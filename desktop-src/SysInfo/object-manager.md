---
description: Ein Objekt besteht aus einem Standardheader und objektspezifischen Attributen. Da alle Objekte die gleiche Struktur aufweisen, gibt es einen einzelnen Objekt-Manager in Windows, der alle Objekte verwaltet.
ms.assetid: 104113f3-bfd1-4ff7-b92f-2f753c0f5185
title: Objekt-Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b87b239d685d53b29243212e06ba2fd5af20e1249794355ed2169278c7f46c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885348"
---
# <a name="object-manager"></a>Objekt-Manager

Ein Objekt besteht aus einem Standardheader und objektspezifischen Attributen. Da alle Objekte die gleiche Struktur aufweisen, gibt es einen einzelnen Objekt-Manager in Windows, der alle Objekte verwaltet.

Der Objektheader enthält Elemente wie den Objektnamen, sodass andere Prozesse anhand des Namens auf das Objekt verweisen können, und einen Sicherheitsdeskriptor, sodass der Objekt-Manager steuern kann, welche Prozesse auf die Systemressource zugreifen.

Der Objekt-Manager führt folgende Aufgaben aus:

-   Erstellen von Objekten
-   Überprüfen, ob ein Prozess das Recht hat, das Objekt zu verwenden
-   Erstellen von Objekthandles und Zurückgeben an den Aufrufer
-   Verwalten von Ressourcenkontingenten
-   Erstellen doppelter Handles
-   Schließen von Handles für Objekte

 

 



