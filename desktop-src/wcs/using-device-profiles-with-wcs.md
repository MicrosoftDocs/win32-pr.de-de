---
title: Verwenden von Geräteprofilen mit WCS
description: Geräteprofile sind ein einfaches Tool für die Farbverwaltung.
ms.assetid: 9ea420ad-dcf1-4ba9-b739-308be7a56a6c
keywords:
- Windows Color System (WCS), Geräteprofile
- WCS (Windows Color System), Geräteprofile
- Bild Farbverwaltung, Geräteprofile
- Farbverwaltung, Geräteprofile
- Farben, Geräteprofile
- Windows Color System (WCS), profile
- WCS (Windows Color System), profile
- Bildfarben Verwaltung, profile
- Farbverwaltung, profile
- Farben, profile
- Geräteprofile
- Farbkonvertierung
- Geräte Verknüpfungs profile
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cf58b46cbee67d437e7d6fe343c7f3a0fab451b
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106353277"
---
# <a name="using-device-profiles-with-wcs"></a>Verwenden von Geräteprofilen mit WCS

Geräteprofile sind ein einfaches Tool für die Farbverwaltung. Bei einem [Geräte Profil](d.md) handelt es sich um eine Datei, die Informationen darüber enthält, wie Farben im Farbraum und in der Farb [Palette](./g.md) eines bestimmten Geräts in einen geräteunabhängigen Farbraum konvertiert werden. Der von ICM2 verwendete geräteunabhängige Farbraum wird als Profil Verbindungsbereich (PCs) bezeichnet. Ein Geräte Profil enthält außerdem Informationen darüber, wie Farben von den PCs in den Farb Raum und die Farbpalette eines bestimmten Geräts konvertiert werden.

Diese zwei Sätze von Konvertierungs Informationen werden für die [Farbkonvertierung](c.md) und die Farbverwaltung verwendet. Beispielsweise kann ein Bild im Farbbereich und in der Farbpalette einer Videoanzeige erstellt werden. Die Informationen in den Geräte Profil Dateien können verwendet werden, um eine Darstellung eines gedruckten Bilds anzuzeigen. Benutzer möchten auf dem Bildschirm häufig sehen, wie sich Farben beim Drucken eines Bilds ändern. Dies wird als "Nachweis" bezeichnet. Ein Bild kann überprüft werden, indem die Farben von der Quell Farbpalette (dem Bildschirm) in [PCs](p.md) -Farben umgewandelt und dann von den PCs in das Ziel Farbfenster (der Drucker) umgewandelt werden. Das resultierende Bild kann auf dem Bildschirm angezeigt werden, sodass der Benutzer sehen kann, wie das endgültige Bild beim Drucken aussieht.

Geräteprofile ermöglichen auch komplexere Verwendungszwecke. Sie können z. b. verwendet werden, um eine Vorstellung davon zu erhalten, wie ein Bild, das auf einer Videoanzeige erstellt wird, beim Drucken auf einem Hochleistungs-Laserdrucker aussehen würde. Das Beispiel wird komplexer, wenn es nur einen Standard-Inkjet-Drucker gibt, auf dem der Nachweis erfolgt. ICM2 konvertiert das Bild [aus dem Spiel der Anzeige](./g.md) in die Palette des Inkjet-Druckers. Von dort aus wird Sie in den Farbskala des Laserdruckers konvertiert. Das resultierende Bild kann auf dem Inkjet-Drucker gedruckt werden. Natürlich wäre das Image bei der Ausgabe auf dem Color-Laser-Drucker eine höhere Auflösung. Die Farben des auf dem Inkjet-Drucker gedruckten Druck Abbilds entsprechen jedoch der Farbe, die der Laserdrucker drucken würde.

Die Konvertierungen von einem Geräte Profil können zusammen mit einer einzelnen Datei verkettet werden, die als *Geräte* Verknüpfungs Profil bezeichnet wird. Wenn wiederholt eine Reihe von Konvertierungen verwendet wird, verkürzt das Erstellen eines Geräte Verknüpfungs Profils für Sie die Konvertierungs Zeit.

Geräteprofile selbst können verwaltet werden. Die Profilverwaltung ist der Prozess der Zuordnung von Farbprofilen zu Geräte Instanzen. Jedem Farbausgabe Gerät kann ein Satz von mindestens einem Farbprofil zugeordnet sein. Hardware Hersteller und Drittanbieter, die Farbprofile bereitstellen, müssen die Profilverwaltung durchführen.

Profil Sätze können von Geräten gemeinsam genutzt werden, oder Sie können für bestimmte Geräte reserviert werden. Angenommen, Sie verfügen über zwei Farbdrucker desselben Modells. Jedem Drucker müsste ein Satz von Farbprofilen zugeordnet werden. Der Satz von Farbprofilen für einen Drucker entspricht den verschiedenen Konfigurationen, die in diesem Modell möglich sind. Beide Drucker haben das gleiche Modell und können einen Satz von Profilen freigeben. Die Alternative besteht darin, jedem Drucker einen eigenen, eindeutigen Profil Satz zuzuweisen. Im letzteren Fall können die Farbprofile im Satz genau auf die einzelne Ausgabe des Druckers, nicht nur auf die allgemeinen Ausgabe Merkmale des Modells, abgestimmt werden.

Es gibt drei verschiedene Klassen von ICC-Profilen: Eingabe Profile, Anzeige Profile und Ausgabeprofile. Eingabe Profile sind normalerweise einem Gerät zugeordnet, z. b. einem Scanner. Anzeige Profile sind in der Regel mit einem Computermonitor verknüpft. Ausgabeprofile sind häufig Druckern zugeordnet.

Die Spezifikation ermöglicht außerdem Geräte Profilen, abstrakte Profile, Geräte Verknüpfungs Profile, benannte Farbprofile und Farb Raum Profile.

Ein Geräte Profil beschreibt den Farbraum eines bestimmten Geräts.

Bei einem abstrakten Profil handelt es sich um eine generische Methode, mit der Benutzer subjektive Farbänderungen an Bildern oder Grafikobjekten vornehmen können, indem die Farbdaten innerhalb der PCs transformiert werden.

Wie bereits erwähnt, verkettet ein Geräte Verknüpfungs Profil eine Reihe von Profilen in eine Transformation.

Benannte Farbprofile können als gleich geordnete Profile für Geräteprofile betrachtet werden. Für ein bestimmtes Gerät gibt es mindestens ein Geräte Profil zum Verarbeiten von Prozess Farb Konvertierungen und mindestens ein benanntes Farbprofil, um benannte Farben zu behandeln. Möglicherweise gibt es mehrere benannte Farbprofile, die für unterschiedliche Verbrauchsmaterialien oder mehrere benannte Farbhersteller berücksichtigt werden müssen.

Ein Farb Raum Profil beschreibt einen geräteunabhängigen Farbraum.

In der folgenden Tabelle werden die verschiedenen Typen von Profilen zusammengefasst.



| Profiltyp        | BESCHREIBUNG                                                                                                                   |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------|
| Abstraktes Profil    | Ein Profil, das an die speziellen Einstellungen eines Benutzers angepasst wurde.                                                     |
| Farb Raum Profil | Ein Profil, das einen geräteunabhängigen Farbraum beschreibt.                                                                    |
| Geräte Verknüpfungs Profil | Eine Reihe von Profilen, die in einem einzelnen Profil verkettet werden.                                                    |
| Geräte Profil      | Ein Profil, in dem der Farbraum eines bestimmten Geräts beschrieben wird.                                                              |
| Profil anzeigen     | Eine Klasse oder Kategorie von Profilen, die jeden Typ von Profil enthält, der einer Anzeige zugeordnet ist.                                  |
| Eingabe Profil       | Eine Klasse oder Kategorie von Profilen, die einen beliebigen Typ von Profil enthält, der einem Eingabegerät zugeordnet ist, z. b. einem Scanner.          |
| Benanntes Farbprofil | Ein Profil für einen Farbraum, der aus benannten Farben besteht.                                                                    |
| Ausgabeprofile     | Eine Klasse oder Kategorie von Profilen, die einen beliebigen Typ von Profil enthält, der mit einem hart Kopier Ausgabegerät (z. b. einem Drucker) verknüpft ist. |



 

Farb Transformationen können mit einem oder mehreren Profilen erstellt werden. Wenn eine Transformation nur mit einem Profil erstellt wird, muss es sich bei dem Profil um ein Geräte Verknüpfungs Profil handeln. Eine Transformation kann auch über zwei oder mehr Profile in einer Kette verfügen. Wenn dies der Fall ist, kann er keine Geräte Verknüpfungs Profile enthalten. Abstrakte Profile können nur in der Mitte der Kette sein. Beim ersten und letzten Profil muss es sich um Geräteprofile oder Farb Raum profile handeln.

 

 