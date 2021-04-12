---
description: Das Installationsprogramm kann die Resilienz von Anwendungen erhöhen, indem beschädigte Komponenten automatisch neu installiert werden.
ms.assetid: aa565e34-f89d-4d26-945d-67b439586523
title: Suchen nach einer unterbrochenen Funktion oder Komponente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8398d084a543ee4c9491242faa287c60d83a5f7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216561"
---
# <a name="searching-for-a-broken-feature-or-component"></a>Suchen nach einer unterbrochenen Funktion oder Komponente

Das Installationsprogramm kann die [Resilienz](resiliency.md) von Anwendungen erhöhen, indem beschädigte Komponenten automatisch neu installiert werden. Insbesondere das Installationsprogramm installiert eine Komponente oder ein Feature neu, wenn es feststellt, dass die in der Spalte KEYPATH der [Komponenten Tabelle](component-table.md) angegebene Datei oder der Registrierungsschlüssel fehlt.

Wenn der KEYPATH der Komponente einer Funktion in der Quelle beschädigt ist, oder wenn bei der Erstellung des KEYPATH in der Datenbank ein Fehler auftritt, versucht das Installationsprogramm möglicherweise, ein Installationspaket zu öffnen und die Funktion bei jedem Aktivieren der Verknüpfung der Funktion erneut zu installieren.

Überprüfen Sie das Ereignisprotokoll auf zwei Einträge wie die folgende, um die Ursache für wiederholte Versuche zur erneuten Installation eines Features oder einer Anwendung zu ermitteln.

``` syntax
Detection of product 'MyProduct', feature 'MyFeature' failed during
 request for component 'MyComponent'
Detection of product 'MyProduct', feature 'MyFeature', component
 'MyComponent' failed
```

Die erste Meldung gibt an, welche Komponente im Paket des Produkts installiert wurde. Dies ist die Komponente, auf die in der Spalte Komponente der Verknüpfungs \_ [Tabelle](shortcut-table.md)verwiesen wird.

Die zweite Meldung gibt an, bei welcher Komponente eine Fehlererkennung auftritt. Dies ist die Komponente mit dem fehlenden oder beschädigten KEYPATH, der die Neuinstallation auslöst.

 

 



