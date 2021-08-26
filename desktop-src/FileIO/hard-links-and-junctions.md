---
description: Beschreibt harte Verknüpfungen und Verbindungen.
ms.assetid: f9e40a86-a4a6-4524-8045-312da72dc655
title: Hard Links and Junctions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 376ed8b3bbe163d2bad4b8c51715537e194633f02ec200ceb5df02df7d582ae3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107450"
---
# <a name="hard-links-and-junctions"></a>Hard Links and Junctions

Es gibt drei Arten von Dateilinks, die im NTFS-Dateisystem unterstützt werden: harte Verknüpfungen, Verbindungen und symbolische Verknüpfungen. Dieses Thema enthält eine Übersicht über harte Links und Verbindungen. Informationen zu symbolischen Verknüpfungen finden Sie unter [Erstellen symbolischer Verknüpfungen.](creating-symbolic-links.md)

## <a name="hard-links"></a>Feste Links

Ein *harter Link* ist die Dateisystemdarstellung einer Datei, mit der mehr als ein Pfad auf eine einzelne Datei auf demselben Volume verweist. Verwenden Sie die [**CreateHardLink-Funktion,**](/windows/desktop/api/WinBase/nf-winbase-createhardlinka) um einen hard-Link zu erstellen. Alle Änderungen an dieser Datei sind sofort für Anwendungen sichtbar, die über die hard-Links darauf zugreifen. Die Verzeichniseintragsgröße und die Attributinformationen werden jedoch nur für den Link aktualisiert, über den die Änderung vorgenommen wurde. Beachten Sie, dass die Attribute in der Datei in jedem hard-Link zu dieser Datei widergespiegelt werden und Änderungen an den Attributen dieser Datei an alle schwierigen Links verbreitet werden. Wenn Sie z. B. das READONLY-Attribut für einen hartverknüpften Link zurücksetzen, um diesen bestimmten hartverknüpften Link zu löschen, und es mehrere harte Links zur tatsächlichen Datei gibt, müssen Sie das READONLY-Bit für die Datei von einem der verbleibenden hartverknüpften Links zurücksetzen, um die Datei und alle verbleibenden feststehenden Links wieder in den READONLY-Zustand zu bringen.

In einem System, in dem C: und D: lokale Laufwerke sind und Z: ein Netzwerklaufwerk \\ \\ ist, das der Freigabe zugeordnet \\ ist, sind die folgenden Verweise als harte Verknüpfung zulässig:

-   C: \\ dira \\ethel.txt verknüpft mit C: \\ dirb \\ dirc \\lucy.txt
-   D: \\ dir1 \\tinker.txt zu D: \\ dir2 \\ dirx \\bell.txt
-   C: \\ diry \\ bob.bak verknüpft mit C: \\ dir2 \\mina.txt

Folgendes ist nicht der Folgende:

-   C: \\ dira verknüpft mit C: \\ dirb
-   C: \\ dira \\ethel.txt verknüpft mit D: \\ dirb \\lucy.txt
-   C: \\ dira \\ethel.txt verknüpft mit Z: \\ dirb \\lucy.txt

Verwenden Sie die [**DeleteFile-Funktion,**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) um einen hard-Link zu löschen. Sie können harte Links in beliebiger Reihenfolge löschen, unabhängig von der Reihenfolge, in der sie erstellt werden.

## <a name="junctions"></a>Verbindungen

Eine *Verbindung* (auch als *Softlink* bezeichnet) unterscheidet sich von einem hard-Link darin, dass es sich bei den Speicherobjekten, auf die es verweist, um separate Verzeichnisse handelt, und eine Verbindung kann Verzeichnisse verknüpfen, die sich auf verschiedenen lokalen Volumes auf demselben Computer befinden. Andernfalls funktionieren Verbindungen identisch mit harter Verknüpfung. Verbindungen werden über [Die Knoten](reparse-points.md)werden implementiert.

Unter der Annahme der gleichen Bedingungen im Abschnitt "HardLinks" sind die folgenden Verweise als Verbindungen zulässig:

-   C: \\ dira verknüpft mit C: \\ dirb \\ dirc
-   C: \\ dirx verknüpft mit D: \\ diry

Folgendes ist nicht der Folgende:

-   C: \\ dira \\one.txt verknüpft mit C: \\ dirb \\two.txt
-   C: \\ dir1 verknüpft mit Z: \\ dir2

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen symbolischer Verknüpfungen](creating-symbolic-links.md)
</dt> </dl>

 

 



