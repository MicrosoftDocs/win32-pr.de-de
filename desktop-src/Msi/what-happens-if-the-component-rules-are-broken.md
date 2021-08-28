---
description: In bestimmten Fällen können Autoren entscheiden, dass sie die Regeln zum Erstellen von Komponenten wie unter Organisieren von Anwendungen in Komponenten und Ändern des Komponentencodes erläutert einhalten müssen.
ms.assetid: 487b6a00-77eb-4c51-8e32-46bcd4493df8
title: Was geschieht, wenn die Komponentenregeln verletzt werden?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3f830fa402da44be992d74adc957d88a19442dcbb51173a87e79fa2266552a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498766"
---
# <a name="what-happens-if-the-component-rules-are-broken"></a>Was geschieht, wenn die Komponentenregeln verletzt werden?

In bestimmten Fällen können Autoren entscheiden, dass sie die Regeln für das Erstellen von Komponenten wie unter [Organisieren](organizing-applications-into-components.md) von Anwendungen in Komponenten und Ändern des [Komponentencodes erläutert, nicht einhalten müssen.](changing-the-component-code.md) Autoren müssen sich der möglichen Konsequenzen bewusst sein und anderweitig garantieren, dass ihre Komponenten niemals installiert werden, wo sie andere Anwendungen oder Komponenten im System des Benutzers beschädigen können.

In der folgenden Liste werden Möglichkeiten beschrieben, wie Autoren manchmal die empfohlenen Komponentenregeln und die möglichen Konsequenzen brechen.

Ein Autor fügt einer Komponente Ressourcen hinzu, ohne den Komponentencode zu ändern.

-   Produkte, die mit der alten Komponente installiert werden, enthalten keine Informationen zu den hinzugefügten Ressourcen in ihrer Installationsdatenbank.
-   Wenn sowohl ein neues Produkt mit den hinzugefügten Ressourcen als auch ein altes Produkt auf demselben Computer installiert sind, können die Ressourcen zurückgelassen werden, wenn das neue Produkt zuerst deinstalliert wird.
-   Ein altes Produkt ohne die hinzugefügten Ressourcen kann die neuere Version der Komponente nicht reparieren. Durch die Neuinstallation des alten Produkts werden die hinzugefügten Ressourcen nicht wiederhergestellt.

Ein Autor entfernt Ressourcen aus einer Komponente, ohne den Komponentencode zu ändern.

-   Produkte, die mit der neuen Komponente installiert werden, enthalten keine Informationen zu den entfernten Ressourcen in ihrer Installationsdatenbank.
-   Wenn sowohl ein altes Produkt mit den Ressourceninformationen als auch ein neues Produkt auf demselben Computer installiert sind, können die Ressourcen zurückgelassen werden, wenn das alte Produkt zuerst deinstalliert wird.
-   Ein neues Produkt mit den entfernten Ressourcen kann die ältere Version des Produkts nicht reparieren. Durch die Neuinstallation des neuen Produkts werden die entfernten Ressourcen nicht wiederhergestellt.

Ein Autor enthält eine Datei, die nicht mit früheren Versionen kompatibel ist, ohne den Komponentencode zu ändern.

Wenn eine inkompatible Datei in einer Komponente enthalten [ist,](default-file-versioning.md) ohne den Komponentencode zu ändern, bewirkt die Standarddateiversionsierung, dass das Installationsprogramm die ursprüngliche Datei mit der neueren inkompatiblen Datei überschreibt. Dadurch können alte Produkte beschädigt werden, die die ursprüngliche Datei benötigen. Es kann auch verhindern, dass das Installationsprogramm das alte Produkt repariert, da die Version der Schlüsselpfaddatei einer Komponente die Version der Komponente bestimmt. Wenn bereits eine neuere Version der Schlüsselpfaddatei installiert ist, installiert das Installationsprogramm keine ältere Version der Komponente. Weitere Informationen finden Sie unter [Regeln für die Dateiversionsversion.](file-versioning-rules.md) In diesem Fall muss das neue Produkt entfernt werden, bevor das alte Produkt neu installiert werden kann.

-   [Die Standarddateiversionsierung](default-file-versioning.md) bewirkt, dass das Installationsprogramm die ursprüngliche Datei mit der neueren inkompatiblen Datei überschreibt.
-   Alte Produkte, die die ursprüngliche Datei benötigen, sind beschädigt.
-   Es kann auch verhindern, dass das Installationsprogramm das alte Produkt repariert, da die Version der Schlüsselpfaddatei einer Komponente die Version der Komponente bestimmt. Wenn bereits eine neuere Version der Schlüsselpfaddatei installiert ist, installiert das Installationsprogramm nicht die ältere Version der Komponente. Weitere Informationen finden Sie unter [Regeln für die Dateiversionsversion.](file-versioning-rules.md) In diesem Fall muss das neue Produkt entfernt werden, bevor das alte Produkt neu installiert werden kann.

Ein Autor schließt dieselbe Ressource in zwei verschiedene Komponenten ein.

Wenn zwei Komponenten über eine Ressource mit demselben Namen und Speicherort verfügen und beide Komponenten im gleichen Ordner installiert sind, entfernt das Entfernen einer der Komponenten die gemeinsame Ressource, wodurch die verbleibende Komponente beschädigt wird.

-   Durch das Deinstallieren einer komponente wird die Ressource entfernt und die andere Komponente unterbricht.
-   Der Mechanismus zum Zählen von Komponentenverweisen ist beschädigt.

 

 



