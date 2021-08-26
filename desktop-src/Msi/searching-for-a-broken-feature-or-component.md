---
description: Das Installationsprogramm kann die Anwendungsresilienz erhöhen, indem beschädigte Komponenten automatisch neu installiert werden.
ms.assetid: aa565e34-f89d-4d26-945d-67b439586523
title: Suchen nach einem fehlerhaften Feature oder einer fehlerhaften Komponente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fa17fc66fdf0bda0a04df9a5917d4e79671b32f453ead921d4f43f89bbd47dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041240"
---
# <a name="searching-for-a-broken-feature-or-component"></a>Suchen nach einem fehlerhaften Feature oder einer fehlerhaften Komponente

Das Installationsprogramm kann die [Anwendungsresilienz erhöhen,](resiliency.md) indem beschädigte Komponenten automatisch neu installiert werden. Insbesondere installiert das Installationsprogramm eine Komponente oder ein Feature neu, wenn es ermittelt, dass die Datei oder der Registrierungsschlüssel, die in der KeyPath -Spalte der [Component-Tabelle](component-table.md) angegeben ist, fehlt.

Wenn der KeyPath der Komponente eines Features in der Quelle beschädigt ist oder bei der Erstellung des KeyPath in der Datenbank ein Fehler auftritt, versucht das Installationsprogramm möglicherweise, ein Installationspaket zu öffnen und das Feature jedes Mal neu zu installieren, wenn die Verknüpfung des Features aktiviert wird.

Um die Ursache wiederholter Versuche zu ermitteln, ein Feature oder eine Anwendung neu zu installieren, überprüfen Sie das Ereignisprotokoll auf zwei Einträge wie die folgenden.

``` syntax
Detection of product 'MyProduct', feature 'MyFeature' failed during
 request for component 'MyComponent'
Detection of product 'MyProduct', feature 'MyFeature', component
 'MyComponent' failed
```

Die erste Meldung gibt an, welche Komponente im Paket des Produkts installiert wurde. Dies ist die Komponente, auf die in der Spalte Komponente \_ der [Verknüpfungstabelle verwiesen wird.](shortcut-table.md)

Die zweite Meldung gibt an, bei welcher Komponente die Erkennung fehlschlägt. Dies ist die Komponente mit dem fehlenden oder beschädigten KeyPath, der die Neuinstallation auslöst.

 

 



