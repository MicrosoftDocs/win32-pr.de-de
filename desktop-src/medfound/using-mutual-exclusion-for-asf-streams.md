---
description: Verwenden des gegenseitigen Ausschlusses für ASF-Streams
ms.assetid: fdd31eac-1dd6-45f0-90fb-d5a74c85db2e
title: Verwenden des gegenseitigen Ausschlusses für ASF-Streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 411b5aa0638ab1c56298b93d01e8de99920abc6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348903"
---
# <a name="using-mutual-exclusion-for-asf-streams"></a>Verwenden des gegenseitigen Ausschlusses für ASF-Streams

Der ASF-Inhalt kann mehrere Datenströme enthalten, die sich gegenseitig ausschließen. Diese Streams können nicht gleichzeitig gelesen werden, aber nur einer davon wird gleichzeitig gelesen. Beispielsweise kann die Datei eine Reihe von Streams enthalten, die denselben Inhalt enthalten, der in einer anderen Bitrate codiert ist. Der verwendete Datenstrom wird von der Bandbreite bestimmt, die der Anwendung zur Verfügung steht, die den Inhalt streamt. Das gegenseitige ASF-Ausschluss Objekt, das Teil des Header Objekts ist, speichert Informationen über die Gruppe von sich gegenseitig ausschließenden Streams.

In Media Foundation ist das *gegenseitige Ausschluss* Objekt, das die [**imfassmutualexclusion**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion) -Schnittstelle verfügbar macht, für jedes gegenseitige ASF-Ausschluss Objekt vorhanden. Das Profil Objekt enthält Verweise auf alle Objekte des gegenseitigen Ausschlusses.

Das Objekt für den gegenseitigen Ausschluss speichert Informationen über die Gruppe von sich gegenseitig ausschließenden Streams als Datensätze. Ein gegenseitiges Ausschluss Objekt kann über mehrere Datensätze verfügen, die zum Erstellen komplexer Szenarien verwendet werden können. Jeder Datensatz enthält mindestens einen Datenstrom, der in einem anderen Datensatz, der vom gegenseitigen Ausschluss Objekt verwaltet wird, in Abhängigkeit vom Typ des gegenseitigen Ausschlusses, z. b. der Bitrate, nicht gleichzeitig vorhanden ist.

Ein häufiges Beispiel für den komplexen gegenseitigen Ausschluss ist eine Datei, die drei Audiostreams desselben Inhalts mit verschiedenen Bitraten in jeder der drei Sprachen enthält. Nur einer der neun Streams sollte gleichzeitig abgespielt werden, aber es gibt zwei Typen, mit denen Sie sich gegenseitig ausschließen: Sprache und Bitrate.

In diesem Beispiel werden den neun Streams die folgenden streamnummern zugewiesen:

<dl> 1-Sprache 1, Bitrate 1  
2-Sprache 1, Bitrate 2  
3-Sprache 1, Bitrate 3  
4-Sprache 2, Bitrate 1  
5-sprachige 2, Bitrate 2  
6-sprachige 2, Bitrate 3  
7-Sprache 3, Bitrate 1  
8-Sprache 3, Bitrate 2  
9-Sprache 3, Bitrate 3  
</dl>

Dieses Szenario kann mit den folgenden vier gegenseitigen Ausschluss Objekten implementiert werden:

-   Das erste gegenseitige Ausschluss Objekt umfasst Streams 1, 2 und 3, die sich gegen die Bitrate gegenseitig ausschließen. Jeder Stream verfügt über einen eigenen Datensatz.
-   Das zweite Objekt für den gegenseitigen Ausschluss schließt Streams 4, 5 und 6 ein, wobei sich die Bitrate gegenseitig ausschließt. Jeder Stream verfügt über einen eigenen Datensatz.
-   Das dritte gegenseitige Ausschluss Objekt umfasst 7, 8 und 9, wobei sich die Bitrate gegenseitig ausschließt. Jeder Stream verfügt über einen eigenen Datensatz.
-   Das vierte gegenseitige Ausschluss Objekt enthält drei Datensätze, die erste, einschließlich der Datenströme 1, 2 und 3. die zweite, einschließlich Streams 4, 5 und 6; und der dritte, einschließlich Streams 7, 8 und 9. Diese Datensätze schließen sich gegenseitig aus.

Beim Abspielen einer auf diese Weise erstellten Datei wählt die Streaminganwendung zuerst die Sprache aus, da Sie sich in der Mitte der Präsentation weniger wahrscheinlich ändert und dann eine Bitrate auswählt.

## <a name="mutual-exclusion-object-creation-and-configuration"></a>Erstellen und Konfigurieren von gegenseitigen Ausschluss Objekten

In der folgenden Liste wird der Prozess der Konfiguration eines gegenseitigen Ausschluss Objekts zusammengefasst:

1.  Erstellen Sie ein gegenseitiges Ausschluss Objekt.
2.  Legen Sie den Typ des gegenseitigen Ausschlusses fest.
3.  Konfigurieren Sie das gegenseitige Ausschluss Objekt, indem Sie Datensätze und die zugehörigen Streams hinzufügen.
4.  Fügen Sie dem Profil das gegenseitige Ausschluss Objekt hinzu.

So erstellen und konfigurieren Sie ein gegenseitiges Ausschluss Objekt

1.  Rufen Sie [**imfasfprofile:: kreatemutualexclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createmutualexclusion) auf, um ein leeres gegenseitiges Ausschluss Objekt zu erstellen.
2.  Rufen Sie [**imfasfmutualexclusion:: settype**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-settype) auf, um das Kriterium des sich gegenseitig exklusiven Streams festzulegen.

    Die Streams können sich gegen Sprache, Bitrate, Präsentation und benutzerdefinierte Kriterien gegenseitig ausschließen. Der Typ wird als GUID dargestellt. Eine Liste dieser Konstanten finden Sie unter [vom Typ "ASF gegenseitiger Ausschluss"-GUIDs](asf-mutual-exclusion-type-guids.md).

3.  Rufen Sie [**imfasfmutualexclusion:: addRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-addrecord) auf, um dem gegenseitigen Ausschluss Objekt einen Datensatz hinzuzufügen.

    Diese Methode fügt einen leeren Datensatz hinzu und weist ihm einen Daten Satz Index zu, beginnend mit 0 (null).

4.  Rufen Sie [**imfasfmutualexclusion:: addstreamforrecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-addstreamforrecord) auf, um die streamnummer dem durch den Daten Satz Index angegebenen Datensatz hinzuzufügen.

    Jeder Datensatz enthält mindestens einen Stream. Jeder Stream in einem Datensatz schließt sich gegenseitig von allen Streams in jedem anderen Datensatz aus. Rufen Sie zum Abrufen der Anzahl von Datenströmen in einem Datensatz [**imfasfmutualexclusion:: getstreamsforrecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-getstreamsforrecord) auf, indem Sie den Datensatz-Index angeben.

    Um einen Stream aus dem Datensatz zu entfernen, rufen Sie [**imfasfmutualexclusion:: removestreamfromrecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-removestreamfromrecord) auf, und geben Sie den Daten Satz Index und die Datenstrom Nummer an.

5.  Rufen Sie [**imfasfprofile:: addmutualexclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-addmutualexclusion) auf, um das konfigurierte Objekt für den gegenseitigen Ausschluss dem Profil hinzuzufügen.

## <a name="enumerating-mutual-exclusion-objects-in-a-profile"></a>Auflisten von gegenseitigen Ausschluss Objekten in einem Profil

Wenn [**imfasfprofile:: addmutualexclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-addmutualexclusion) erfolgreich ist, wird dem angegebenen Objekt ein Index zugewiesen, beginnend bei Null.

Rufen Sie zum Auflisten der einem Profil zugeordneten gegenseitigen Ausschluss Objekte [**imfasfprofile:: getmutualexclusioncount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getmutualexclusioncount) auf, und durchlaufen Sie die Liste durch Aufrufen von [**imfasfprofile:: getmutualexclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getmutualexclusion). Gegenseitige Ausschluss Indizes sind sequenziell und liegen zwischen 0 und einem kleiner als die Anzahl von Datenströmen, die von **getmutualexclusioncount** abgerufen werden.

Ein gegenseitiges Ausschluss Objekt wird durch Aufrufen von [**imfasfprofile:: removemutualexclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removemutualexclusion)aus dem Profil entfernt. Das Profil weist die gegenseitigen Ausschluss Indizes neu zu, sodass Sie sequenziell beginnen, beginnend mit 0 (null). Dies überschreibt zuvor gespeicherte Indizes, die nach dem Aufrufen dieser Methode nicht mehr gültig sind. Dadurch werden die zugehörigen Datensätze für den gegenseitigen Ausschluss Strom freigegeben

## <a name="removing-records-in-a-mutual-exclusion-object"></a>Entfernen von Datensätzen in einem gegenseitigen Ausschluss Objekt

Um einen Datensatz aus einem gegenseitigen Ausschluss Objekt zu entfernen, rufen Sie [**imfasfmutualexclusion:: removerecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-removerecord)auf. Wenn diese Methode erfolgreich ausgeführt wird, werden die restlichen Datensätze vom gegenseitigen Ausschluss Objekt so indiziert, dass Sie sequenziell beginnend mit NULL sind. Die Anwendung muss die Datensätze aufzählen, um den korrekten Index für jeden Datensatz sicherzustellen. Rufen Sie zu diesem Zweck [**imfasfmutualexclusion:: GetRecordCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-getrecordcount) auf, und durchlaufen Sie die Datensätze durch Aufrufen von [**imfasfmutualexclusion:: getstreamsforrecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-getstreamsforrecord).

Das Entfernen des Datensatzes mit dem höchsten Index hat keine Auswirkung auf die anderen Indizes.

## <a name="modifying-a-mutual-exclusion-object"></a>Ändern eines gegenseitigen Ausschluss Objekts

Um die Konfiguration des gegenseitigen Ausschluss Objekts im Profil zu ändern, muss die Anwendung das vorhandene gegenseitige Ausschluss Objekt durch ein anderes Objekt ersetzen, das die neuen Einstellungen enthält.

So ändern Sie die Konfiguration des gegenseitigen Ausschluss Objekts im Profil

1.  Listet die gegenseitigen Ausschluss Objekte im Profil auf, um das Objekt zu erhalten, das geändert werden muss.
2.  Rufen Sie [**imfasfmutualexclusion:: Clone**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-clone) auf, um das Objekt für den gegenseitigen Ausschluss zu klonen.

3.  Konfigurieren Sie das geklonte Objekt nach Bedarf.
4.  Rufen Sie [**imfasfprofile:: removemutualexclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removemutualexclusion) auf, um das alte gegenseitige Ausschluss Objekt aus dem Profil zu entfernen.

5.  Rufen Sie [**imfasfprofile:: addmutualexclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-addmutualexclusion) auf, um dem Profil das aktualisierte Objekt für den gegenseitigen Ausschluss hinzuzufügen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASF-Profil](asf-profile.md)
</dt> </dl>

 

 



