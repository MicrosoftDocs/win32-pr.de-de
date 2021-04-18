---
description: Beschreibt feste Links und Verbindungen.
ms.assetid: f9e40a86-a4a6-4524-8045-312da72dc655
title: Feste Links und Verbindungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b8d1444db977dd95419e4cb004d2b3cb811da9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352532"
---
# <a name="hard-links-and-junctions"></a>Feste Links und Verbindungen

Es gibt drei Typen von Datei Verknüpfungen, die im NTFS-Dateisystem unterstützt werden: feste Links, Verbindungen und symbolische Verknüpfungen. Dieses Thema stellt eine Übersicht über feste Links und Verbindungen dar. Informationen zu symbolischen Verknüpfungen finden Sie unter [Erstellen von symbolischen Verknüpfungen](creating-symbolic-links.md).

## <a name="hard-links"></a>Feste Links

Ein fester *Link* ist die Dateisystem Darstellung einer Datei, durch die mehr als ein Pfad auf eine einzelne Datei auf demselben Volume verweist. Um einen festen Link zu erstellen, verwenden Sie die Funktion " [**kreatehardlink**](/windows/desktop/api/WinBase/nf-winbase-createhardlinka) ". Alle Änderungen an dieser Datei sind für Anwendungen, die über die darauf referendeten Hardlinks darauf zugreifen, sofort sichtbar. Die Verzeichniseintrags Größe und die Attributinformationen werden jedoch nur für den Link aktualisiert, über den die Änderung vorgenommen wurde. Beachten Sie, dass sich die Attribute für die Datei in jedem festen Link zu dieser Datei widerspiegeln, und dass Änderungen an den Attributen dieser Datei an alle festen Links weitergegeben werden. Wenn Sie z. b. das Attribut "schreibgeschützt" auf einem festen Link zurücksetzen, um diesen bestimmten festen Link zu löschen, und mehrere feste Links zur eigentlichen Datei vorhanden sind, müssen Sie das schreibgeschützte Bit in der Datei von einem der restlichen festen Links zurücksetzen, um die Datei und alle restlichen festen Links wieder in den schreibgeschützten Zustand zu bringen.

In einem System, in dem Z. b. "C:" und "D:" lokale Laufwerke sind und Z: ein Netzlaufwerk ist, \\ \\ das Fred-Freigabe zugeordnet ist \\ , sind die folgenden Verweise als hardlink zulässig:

-   C: \\ dira \\ethel.txt mit C: \\ dirb \\ Dirc verknüpft \\lucy.txt
-   D: \\ dir1 \\tinker.txt to d: \\ dir2 \\ DirX \\bell.txt
-   C: \\ DirY \\ Bob. bak, verknüpft mit C: \\ dir2 \\mina.txt

Folgendes ist nicht:

-   C: \\ dira mit c: \\ dirb verknüpft
-   C: \\ dira \\ethel.txt mit D: \\ dirb verknüpft \\lucy.txt
-   C: \\ dira \\ethel.txt mit Z: \\ dirb verknüpft \\lucy.txt

Verwenden Sie die [**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) -Funktion, um einen festen Link zu löschen. Sie können feste Verknüpfungen unabhängig von der Reihenfolge, in der Sie erstellt werden, in beliebiger Reihenfolge löschen.

## <a name="junctions"></a>Verbindungen

Eine *Verknüpfung (auch* als *Weiche Verknüpfung* bezeichnet) unterscheidet sich von einer festen Verknüpfung darin, dass es sich bei den Speicher Objekten, auf die verwiesen wird, um separate Verzeichnisse handelt, und eine Verknüpfung kann Verzeichnisse verknüpfen, die sich auf verschiedenen lokalen Volumes auf demselben Computer befinden. Andernfalls funktionieren die Verbindungen mit festen Links identisch. Verbindungen werden über Analyse [Punkte](reparse-points.md)implementiert.

Wenn Sie die gleichen Bedingungen im Abschnitt feste Links annehmen, sind die folgenden Verweise als Verbindungen zulässig:

-   C: \\ dira mit c: \\ dirb \\ Dirc verknüpft
-   C: \\ DirX verknüpft mit D: \\ DirY

Folgendes ist nicht:

-   C: \\ dira \\one.txt mit C: \\ dirb verknüpft \\two.txt
-   C: \\ dir1 verknüpft mit Z: \\ dir2

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von symbolischen Verknüpfungen](creating-symbolic-links.md)
</dt> </dl>

 

 



