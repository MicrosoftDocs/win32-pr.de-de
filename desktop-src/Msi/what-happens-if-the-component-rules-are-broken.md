---
description: In bestimmten Fällen können Autoren entscheiden, dass Sie die Regeln zum Erstellen von Komponenten unterbrechen müssen, wie unter Organisieren von Anwendungen in Komponenten und Ändern des Komponenten Codes erläutert.
ms.assetid: 487b6a00-77eb-4c51-8e32-46bcd4493df8
title: Was geschieht, wenn die Komponenten Regeln beschädigt sind?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78f61a0a819856c5014aa70acfaeb46be5043e58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347660"
---
# <a name="what-happens-if-the-component-rules-are-broken"></a>Was geschieht, wenn die Komponenten Regeln beschädigt sind?

In bestimmten Fällen können Autoren entscheiden, dass Sie die Regeln zum Erstellen von Komponenten unterbrechen müssen, wie unter [Organisieren von Anwendungen in Komponenten](organizing-applications-into-components.md) und [Ändern des Komponenten Codes](changing-the-component-code.md)erläutert. Autoren müssen sich über die möglichen Konsequenzen im klaren sein, und es muss sichergestellt werden, dass Ihre Komponenten nie installiert werden, wo Sie andere Anwendungen oder Komponenten auf dem System des Benutzers beschädigen können.

In der folgenden Liste wird beschrieben, wie Autoren manchmal die empfohlenen Komponenten Regeln und die möglichen Konsequenzen unterbrechen.

Ein Autor fügt einer Komponente Ressourcen hinzu, ohne den Komponenten Code zu ändern.

-   Produkte, die mit der alten Komponente installiert wurden, haben keine Informationen zu den hinzugefügten Ressourcen in der Installations Datenbank.
-   Wenn ein neues Produkt mit den hinzugefügten Ressourcen und einem alten Produkt auf dem gleichen Computer installiert ist, können die Ressourcen zurückgelassen werden, wenn das neue Produkt zuerst deinstalliert wird.
-   Ein altes Produkt ohne die hinzugefügten Ressourcen kann die neuere Version der Komponente nicht reparieren. Durch die erneute Installation des alten Produkts werden die hinzugefügten Ressourcen nicht wieder hergestellt.

Ein Autor entfernt Ressourcen aus einer Komponente, ohne den Komponenten Code zu ändern.

-   Mit der neuen Komponente installierte Produkte verfügen über keine Informationen zu den entfernten Ressourcen in der Installations Datenbank.
-   Wenn sowohl ein altes Produkt mit den Ressourcen Informationen als auch ein neues Produkt auf demselben Computer installiert sind, können die Ressourcen zurückgelassen werden, wenn das alte Produkt zuerst deinstalliert wird.
-   Ein neues Produkt mit den entfernten Ressourcen kann die ältere Version des Produkts nicht reparieren. Wenn Sie das neue Produkt neu installieren, werden die entfernten Ressourcen nicht wieder hergestellt.

Ein Autor schließt eine Datei ein, die mit früheren Versionen nicht kompatibel ist, ohne den Komponenten Code zu ändern.

Wenn eine nicht kompatible Datei in einer Komponente enthalten ist, ohne den Komponenten Code zu ändern, bewirkt die [standardmäßige Datei Versions](default-file-versioning.md) Verwaltung, dass das Installationsprogramm die ursprüngliche Datei mit der neueren inkompatiblen Datei überschreibt. Dadurch können alte Produkte, die die ursprüngliche Datei benötigen, beschädigt werden. Dies kann auch verhindern, dass das Installationsprogramm das alte Produkt repariert, da die Version der Schlüssel Pfad Datei einer Komponente die Version der Komponente bestimmt. Wenn bereits eine neuere Version der Schlüssel Pfad Datei installiert ist, installiert das Installationsprogramm keine ältere Version der Komponente. Weitere Informationen finden Sie unter [Regeln für die Datei Versions](file-versioning-rules.md)Verwaltung. In diesem Fall muss das neue Produkt entfernt werden, bevor das alte Produkt neu installiert werden kann.

-   Die [standardmäßige Datei Versions](default-file-versioning.md) Verwaltung bewirkt, dass das Installationsprogramm die ursprüngliche Datei mit der neueren inkompatiblen Datei überschreibt.
-   Alte Produkte, die die ursprüngliche Datei benötigen, sind beschädigt.
-   Dies kann auch verhindern, dass das Installationsprogramm das alte Produkt repariert, da die Version der Schlüssel Pfad Datei einer Komponente die Version der Komponente bestimmt. Wenn bereits eine neuere Version der Schlüssel Pfad Datei installiert ist, installiert das Installationsprogramm nicht die ältere Version der Komponente. Weitere Informationen finden Sie unter [Regeln für die Datei Versions](file-versioning-rules.md)Verwaltung. In diesem Fall muss das neue Produkt entfernt werden, bevor das alte Produkt neu installiert werden kann.

Ein Autor enthält dieselbe Ressource in zwei unterschiedlichen Komponenten.

Wenn zwei Komponenten über eine Ressource mit dem gleichen Namen und Speicherort verfügen und beide Komponenten in demselben Ordner installiert sind, wird durch das Entfernen beider Komponenten die allgemeine Ressource entfernt, wodurch die verbleibende Komponente beschädigt wird.

-   Durch das Deinstallieren einer der beiden Komponenten wird die Ressource entfernt und die andere Komponente unterbrochen.
-   Der Mechanismus der Komponenten Verweis Zählung ist beschädigt.

 

 



