---
description: Zum Generieren eines Mergemoduls müssen Sie ein Software Tool abrufen, mit dem eine MSM-Datei bearbeitet werden kann.
ms.assetid: bc14d36a-b299-4c61-ade2-43fad142d21d
title: Abrufen von mergemodulauthoring-Tools
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dac673c7cfa191cecb1b576e1b17f2f4a7a1f4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356562"
---
# <a name="obtaining-merge-module-authoring-tools"></a>Abrufen von mergemodulauthoring-Tools

Zum Generieren eines Mergemoduls müssen Sie ein Software Tool abrufen, mit dem eine MSM-Datei bearbeitet werden kann. Da es sich bei einer MSM-Datei im Grunde um eine vereinfachte MSI-Datei handelt, können Sie möglicherweise dieselben Tools verwenden, die auch zum Erstellen einer Installations Datenbank verwendet wurden. Beispielsweise Orca.exe die Anwendung mit dem Windows Installer SDK bereitgestellt.

Eine Alternative besteht darin, eines der Installer-Paket Erstellungs Tools zu erwerben, die von unabhängigen Softwareanbietern zur Verfügung gestellt werden können. Es gibt mehrere Tools von Drittanbietern, die für die Erstellung von Mergemodulen verwendet werden können. Wenn Sie sich für die Verwendung eines Drittanbieter Tools entscheiden, sollten Sie sicherstellen, dass Mergemodule generiert werden, die mit dem in diesem Dokument beschriebenen Standard übereinstimmen. Insbesondere sollten Sie feststellen, dass die Bearbeitungs Tools für das Mergemodul keines der folgenden Aktionen durchgeführt haben.

-   Dem Mergemodul wurden überflüssige Tabellen hinzugefügt, auf die in der [Tabelle "moduleignoretable](moduleignoretable-table.md)" nicht verwiesen wird.

    Löschen Sie diese Tabellen, oder fügen Sie Sie der Tabelle moduleignoretable hinzu.

-   Dem Mergemodul wurde eine unnötige [TextStyle-Tabelle](textstyle-table.md) hinzugefügt.

    Wenn das Mergemodul über keine Benutzeroberfläche verfügt (was in der Regel nicht der Fall ist), können Sie diese Tabelle gefahrlos löschen.

-   Der [Verzeichnis Tabelle](directory-table.md)wurden unnötige Einträge hinzugefügt.

    Entfernen Sie unnötige Einträge aus der Verzeichnis Tabelle.

-   Linke Informationen aus der Validierungs Tabelle des Mergemoduls \_ .

    Dadurch wird die mergemodulvalidierung verhindert. Fügen Sie eine komplette \_ Validierungs Tabelle hinzu.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von Benutzeroberflächen in Mergemodulen](authoring-user-interfaces-in-merge-modules.md)
</dt> <dt>

[Erstellen von mergemodulverzeichnistabellen](authoring-merge-module-directory-tables.md)
</dt> <dt>

[Validieren von Mergemodulen](validating-merge-modules.md)
</dt> </dl>

 

 



