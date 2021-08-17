---
description: Die meisten Namespaceerweiterungen sind eine Teilmenge des Shellnamespaces.
ms.assetid: 00b6b281-b157-4a61-9852-8aafd9ba68d3
title: Anzeigen einer Self-Contained Einer Namespaceerweiterung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00ea8ed12d4333ac2c4de7973410a822fefea827be769bbe7ccf754890712e3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968839"
---
# <a name="displaying-a-self-contained-view-of-a-namespace-extension"></a>Anzeigen einer Self-Contained Einer Namespaceerweiterung

Die meisten Namespaceerweiterungen sind eine Teilmenge des Shellnamespaces. Wenn Sie einen Verbindungspunkt erstellen, wie unter Angeben des Speicherorts einer [Namespaceerweiterung](nse-junction.md)beschrieben, ermöglicht der Windows-Explorer Benutzern das Navigieren zu und aus Ihrer Namespaceerweiterung wie in jedem anderen Ordner. Es ist jedoch auch möglich, Windows Explorer zu verwenden, um nur den Inhalt Ihrer Namespaceerweiterung anzuzeigen. Diese Anzeigeoption wird manchmal als *Stammansicht bezeichnet.* Obwohl sie nicht häufig verwendet werden, sind Stammansichten für einige Erweiterungstypen möglicherweise den normalen Ansichten vorzuziehen.

Mit einer Stammansicht wird eine neue Instanz von Windows Explorer erstellt, die den Inhalt der Erweiterung als separaten Namespace anzeigt. Die Strukturansicht einer Stammansicht zeigt nur die Ordner an, die Teil der Erweiterung sind. Benutzer können nicht von einer Stammansicht zu anderen Teilen des Shellnamespace navigieren.

Erweiterungen werden für Stammansichten auf die gleiche Weise implementiert wie für normale Ansichten. Der einzige Unterschied besteht in der Anzeige des Inhalts der Erweiterung durch Windows Explorer. Es ist sogar möglich, normale Ansichten und Stammansichten derselben Erweiterung zu haben.

Um eine Ansicht einer Erweiterung zu öffnen, müssen Sie eine Instanz von Explorer.exe mit einem /root-Flag starten. Abhängig von der Art Ihrer Erweiterung gibt es verschiedene Möglichkeiten, eine Ansicht mit Stamm zu starten.

-   [Verwenden eines Verbindungspunkts zum Öffnen einer Ansicht mit Stamm](how-to-use-a-junction-point-to-open-a-rooted-view.md)
-   [Verwenden einer Verknüpfungsdatei zum Öffnen einer Ansicht mit Stamm](how-to-use-a-shortcut-file-to-open-a-rooted-view.md)
-   [Anzeigen einer Stammansicht einer Datei](how-to-display-a-rooted-view-of-a-file.md)

 

 



