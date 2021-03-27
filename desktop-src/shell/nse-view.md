---
description: Die meisten Namespace Erweiterungen sind eine Teilmenge des Shell-Namespace.
ms.assetid: 00b6b281-b157-4a61-9852-8aafd9ba68d3
title: Anzeigen einer Self-Contained Ansicht einer Namespace Erweiterung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b6f8555cfb8cdac6248c5ea1c70ce8af29bfd16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980008"
---
# <a name="displaying-a-self-contained-view-of-a-namespace-extension"></a>Anzeigen einer Self-Contained Ansicht einer Namespace Erweiterung

Die meisten Namespace Erweiterungen sind eine Teilmenge des Shell-Namespace. Wenn Sie einen Verknüpfungs Punkt erstellen, wie unter [angeben des Speicher Orts einer Namespace Erweiterung](nse-junction.md)beschrieben, können Benutzer mithilfe von Windows-Explorer genau wie bei jedem anderen Ordner zu ihrer Namespace Erweiterung navigieren. Es ist jedoch auch möglich, Windows-Explorer zu verwenden, um nur den Inhalt der Namespace Erweiterung anzuzeigen. Diese Anzeigeoption wird manchmal als Stamm *Ansicht* bezeichnet. Auch wenn es nicht häufig verwendet wird, können rootansichten normalen Ansichten für einige Erweiterungs Typen vorzuziehen sein.

Mit einer Ansicht im Stammverzeichnis wird eine neue Instanz von Windows Explorer erstellt, in der der Inhalt der Erweiterung als separater Namespace angezeigt wird. Die Strukturansicht einer Stamm Ansicht zeigt nur die Ordner an, die Teil der Erweiterung sind. Benutzer können nicht von einer rootansicht zu anderen Teilen des Shell-Namespace navigieren.

Erweiterungen werden auf die gleiche Weise für rootansichten implementiert wie für normale Ansichten. Der einzige Unterschied besteht darin, wie der Inhalt der Erweiterung von Windows-Explorer angezeigt wird. Es ist sogar möglich, die Ansichten "Normal" und "Rooting" der gleichen Erweiterung zu haben.

Wenn Sie eine Ansicht einer Erweiterung öffnen möchten, müssen Sie eine Instanz von Explorer.exe mit einem/root-Flag starten. Es gibt verschiedene Möglichkeiten zum Starten einer Ansicht mit Rootzugriff, abhängig von der Art der Erweiterung.

-   [Verwenden eines Verknüpfungs Punkts zum Öffnen einer rootansicht](how-to-use-a-junction-point-to-open-a-rooted-view.md)
-   [Verwenden einer Verknüpfungs Datei zum Öffnen einer rootansicht](how-to-use-a-shortcut-file-to-open-a-rooted-view.md)
-   [Anzeigen einer rootansicht einer Datei](how-to-display-a-rooted-view-of-a-file.md)

 

 



