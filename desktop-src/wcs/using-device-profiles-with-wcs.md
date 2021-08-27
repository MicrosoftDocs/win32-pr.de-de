---
title: Verwenden von Geräteprofilen mit WCS
description: Geräteprofile sind ein grundlegendes Tool für die Farbverwaltung.
ms.assetid: 9ea420ad-dcf1-4ba9-b739-308be7a56a6c
keywords:
- Windows Farbsystem (WCS), Geräteprofile
- WCS (Windows Color System), Geräteprofile
- Bildfarbverwaltung, Geräteprofile
- Farbverwaltung, Geräteprofile
- Farben, Geräteprofile
- Windows Farbsystem (WCS), Profile
- WCS (Windows Color System), Profiles
- Bildfarbverwaltung,Profile
- Farbverwaltung,Profile
- Farben,Profile
- Geräteprofile
- Farbkonvertierung
- Gerätelinkprofile
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c8211ff883f8e30e7b67b0168e6da980744b252cbb1b89412fc834ac6370cca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090070"
---
# <a name="using-device-profiles-with-wcs"></a>Verwenden von Geräteprofilen mit WCS

Geräteprofile sind ein grundlegendes Tool für die Farbverwaltung. Ein [Geräteprofil](d.md) ist eine Datei, die Informationen zum Konvertieren von [](./g.md) Farben im Farbraum und der Farbpalette eines bestimmten Geräts in einen geräteunabhängigen Farbraum enthält. Der geräteunabhängige Farbraum, den ICM2 verwendet, wird als Profilverbindungsraum (PCS) bezeichnet. Ein Geräteprofil enthält auch Informationen zum Konvertieren von Farben aus dem PCS in den Farbraum und farbliche Gamut eines bestimmten Geräts.

Diese beiden Sätze von Konvertierungsinformationen werden für die [Farbkonvertierung und](c.md) Farbverwaltung verwendet. Beispielsweise kann ein Bild im Farbraum und farblichen Gamut einer Videoanzeige erstellt werden. Die Informationen in den Geräteprofildateien können verwendet werden, um eine Darstellung eines gedruckten Bilds anzuzeigen. Benutzer möchten häufig auf dem Bildschirm sehen, wie sich die Farben ändern, wenn ein Bild gedruckt wird. Dies wird als Proofing bezeichnet. Ein Bild kann durch Konvertieren der Farben aus der Quellfarbe Gamut (der Bildschirm) in [PCS-Farben](p.md) und anschließendes Konvertieren der Farben aus dem PCS in die Zielfarbe Gamut (drucker) dargestellt werden. Das resultierende Bild kann auf dem Bildschirm angezeigt werden, sodass der Benutzer sehen kann, wie das endgültige Bild aussieht, wenn es gedruckt wird.

Geräteprofile ermöglichen auch komplexere Verwendungsmöglichkeiten. Sie können z. B. verwendet werden, um eine Vorstellung davon zu erhalten, wie ein Bild, das auf einer Videoanzeige erstellt wird, aussehen würde, wenn es auf einem hochauflösenden Drucker gedruckt wird. Das Beispiel wird komplexer, wenn es nur einen Standarddrucker für den Nachweis gibt. ICM2 konvertiert das Bild aus dem [Gamut](./g.md) der Anzeige in den Gamut des Druckers " Printer". Von dort aus wird sie in den Gamut des Druckers konvertiert. Das resultierende Bild kann auf dem Drucker "Printer" gedruckt werden. Natürlich würde das Bild eine höhere Auflösung haben, wenn es auf dem Farblaserdrucker gedruckt wird. Die Farben des Aufdruckbilds, das auf dem Drucker "Drucker" gedruckt wird, würden jedoch mit den Farben übereinstimmen, die der Drucker drucken würde.

Die Konvertierungen aus einem Geräteprofil können in einer einzelnen Datei verkettet werden, die als *Gerätelinkprofil bezeichnet wird.* Wenn eine Reihe von Konvertierungen wiederholt verwendet wird, verkürzt das Erstellen eines Gerätelinkprofils für sie die Konvertierungszeit.

Geräteprofile selbst können verwaltet werden. Bei der Profilverwaltung werden Geräteinstanzen Farbprofile zu zuordnen. Jedem Farbausgabegerät kann ein oder mehrere Farbprofile zugeordnet sein. Hardwarehersteller und Drittanbieter, die Farbprofile bereitstellen, müssen die Profilverwaltung durchführen.

Profilsätze können von Geräten gemeinsam genutzt oder für bestimmte Geräte de dedicated sein. Angenommen, Sie verfügen über zwei Farbdrucker desselben Modells. Jeder Drucker erfordert, dass ihm eine Reihe von Farbprofilen zugeordnet ist. Der Satz von Farbprofilen für einen Drucker entspricht den verschiedenen Konfigurationen, die in diesem Modell möglich sind. Da beide Drucker das gleiche Modell verwenden, können sie einen Satz von Profilen gemeinsam nutzen. Alternativ können Sie jedem Drucker einen eigenen eigenen Profilsatz geben. Im letzteren Fall können die Farbprofile im Satz genau auf die individuelle Ausgabe des Druckers kalibriert werden, nicht nur auf die allgemeinen Ausgabemerkmale des Modells.

Es gibt drei verschiedene Klassen von PROFILEn für die Profilanzeige: Eingabeprofile, Anzeigeprofile und Ausgabeprofile. Eingabeprofile sind in der Regel einem Gerät zugeordnet, z. B. einem Scanner. Anzeigeprofile sind in der Regel einem Computermonitor zugeordnet. Ausgabeprofile sind häufig Druckern zugeordnet.

Die Spezifikation ermöglicht auch Geräteprofile, abstrakte Profile, Gerätelinkprofile, benannte Farbprofile und Farbraumprofile.

Ein Geräteprofil beschreibt den Farbraum eines bestimmten Geräts.

Ein abstraktes Profil stellt eine generische Methode für Benutzer dar, um durch Transformieren der Farbdaten innerhalb des PCS farbige Farbänderungen an Bildern oder Grafikobjekten vorzunehmen.

Wie bereits erwähnt, verkettet ein Gerätelinkprofil eine Reihe von Profilen zu einer Transformation.

Benannte Farbprofile können als gleichgeordnete Profile zu Geräteprofilen bezeichnet werden. Für ein bestimmtes Gerät gibt es mindestens ein Geräteprofil für die Verarbeitung von Prozessfarbkonvertierungen und mindestens ein benanntes Farbprofil für die Verarbeitung benannter Farben. Es gibt möglicherweise mehrere benannte Farbprofile, um verschiedene Verbrauchsmaterialien oder mehrere benannte Farbanbieter zu berücksichtigen.

Ein Farbraumprofil beschreibt einen geräteunabhängigen Farbraum.

In der folgenden Tabelle werden die verschiedenen Profiltypen zusammengefasst.



| Profiltyp        | Beschreibung                                                                                                                   |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------|
| Abstraktes Profil    | Ein Profil, das an die speziellen Einstellungen eines Benutzers angepasst wurde.                                                     |
| Farbraumprofil | Ein Profil, das einen geräteunabhängigen Farbraum beschreibt.                                                                    |
| Gerätelinkprofil | Eine Reihe von Profilen, die zu einem einzelnen Profil verkettet werden.                                                    |
| Geräteprofil      | Ein Profil, das den Farbraum eines bestimmten Geräts beschreibt.                                                              |
| Anzeigeprofil     | Eine Klasse oder Kategorie von Profilen, die einen beliebigen Profiltyp enthält, der einer Anzeige zugeordnet ist.                                  |
| Eingabeprofil       | Eine Klasse oder Kategorie von Profilen, die einen beliebigen Profiltyp enthält, der einem Eingabegerät zugeordnet ist, z. B. ein Scanner.          |
| Benanntes Farbprofil | Ein Profil für einen Farbraum, der aus benannten Farben besteht.                                                                    |
| Ausgabeprofile     | Eine Klasse oder Kategorie von Profilen, die einen beliebigen Profiltyp enthält, der einem Hardcopy-Ausgabegerät zugeordnet ist, z. B. einem Drucker. |



 

Farbtransformationen können mit mindestens einem Profil erstellt werden. Wenn eine Transformation mit nur einem Profil erstellt wird, muss es sich bei dem Profil um ein Gerätelinkprofil handelt. Eine Transformation kann auch zwei oder mehr Profile in einer Kette haben. Wenn dies der Fehler ist, kann es keine Gerätelinkprofile enthalten. Abstrakte Profile können sich nur in der Mitte der Kette finden. Das erste und das letzte Profil müssen Geräteprofile oder Farbraumprofile sein.

 

 