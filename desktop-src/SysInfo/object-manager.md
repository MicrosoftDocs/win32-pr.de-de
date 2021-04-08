---
description: Ein-Objekt besteht aus einem Standard Header und Objekt spezifischen Attributen. Da alle Objekte dieselbe Struktur aufweisen, gibt es einen einzelnen Objekt-Manager in Windows, der alle Objekte verwaltet.
ms.assetid: 104113f3-bfd1-4ff7-b92f-2f753c0f5185
title: Objekt-Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3a74581650828a77c6423825d3c557a13075a89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960243"
---
# <a name="object-manager"></a>Objekt-Manager

Ein-Objekt besteht aus einem Standard Header und Objekt spezifischen Attributen. Da alle Objekte dieselbe Struktur aufweisen, gibt es einen einzelnen Objekt-Manager in Windows, der alle Objekte verwaltet.

Der Objekt Header enthält Elemente, wie z. b. den Objektnamen, sodass andere Prozesse anhand des Namens und einer Sicherheits Beschreibung auf das Objekt verweisen können, sodass der Objekt-Manager steuern kann, welche Prozesse auf die System Ressource zugreifen.

Die Aufgaben, die der Objekt-Manager ausführt, umfassen Folgendes:

-   Erstellen von Objekten
-   Überprüfen, ob ein Prozess über das Recht zur Verwendung des Objekts verfügt
-   Erstellen von Objekt Handles und Zurückgeben dieser Objekte an den Aufrufer
-   Verwalten von Ressourcen Kontingente
-   Erstellen von doppelten Handles
-   Schließen von Handles in Objekte

 

 



