---
description: Verwenden des gegenseitigen Ausschlusses für ASF-Streams
ms.assetid: fdd31eac-1dd6-45f0-90fb-d5a74c85db2e
title: Verwenden des gegenseitigen Ausschlusses für ASF-Streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40c7fd104659064952803c16f572ee1e55dee0508144474e89ee7c0f362315c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034564"
---
# <a name="using-mutual-exclusion-for-asf-streams"></a>Verwenden des gegenseitigen Ausschlusses für ASF-Streams

ASF-Inhalte können mehrere Streams enthalten, die sich gegenseitig ausschließen. Diese Datenströme können nicht gleichzeitig gelesen werden, aber nur einer von ihnen wird gleichzeitig gelesen. Beispielsweise kann die Datei eine Reihe von Datenströmen enthalten, die denselben Inhalt enthalten, der mit einer anderen Bitrate codiert ist. Der verwendete Datenstrom wird durch die Bandbreite bestimmt, die der Anwendung zur Verfügung steht, die den Inhalt streamt. Das ASF-Objekt für gegenseitigen Ausschluss, das Teil des Headerobjekts ist, speichert Informationen über die Gruppe der sich gegenseitig ausschließenden Datenströme.

In Media Foundation ist das Objekt für *gegenseitigen Ausschluss,* das die [**IMFASFMutualExclusion-Schnittstelle**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion) verfügbar macht, für jedes ASF-Objekt für gegenseitigen Ausschluss vorhanden. Das Profilobjekt enthält Einen Verweis auf alle objekte für gegenseitigen Ausschluss.

Das Objekt für gegenseitigen Ausschluss speichert Informationen über die Gruppe der sich gegenseitig ausschließenden Datenströme als Datensätze. Ein objekt für gegenseitigen Ausschluss kann über mehrere Datensätze verfügen, die zum Erstellen komplexer Szenarien verwendet werden können. Jeder Datensatz enthält einen oder mehrere Datenströme, die nicht gleichzeitig mit Streams in einem anderen Datensatz vorhanden sein können, die vom objekt für gegenseitigen Ausschluss verwaltet werden, je nach Art des gegenseitigen Ausschlusses, z. B. Bitrate.

Ein häufiges Beispiel für einen komplexen gegenseitigen Ausschluss ist eine Datei, die drei Audiostreams desselben Inhalts mit verschiedenen Bitraten in jeder von drei Sprachen enthält. Nur einer der neun Streams sollte gleichzeitig wiedergegeben werden, aber es gibt zwei Typen, durch die sie sich gegenseitig ausschließen: Sprache und Bitrate.

In diesem Beispiel werden den neun Streams die folgenden Datenstromnummern zugewiesen:

<dl> 1 – Sprache 1, Bitrate 1  
2 – Sprache 1, Bitrate 2  
3 – Sprache 1, Bitrate 3  
4– Sprache 2, Bitrate 1  
5 – Sprache 2, Bitrate 2  
6 – Sprache 2, Bitrate 3  
7 – Sprache 3, Bitrate 1  
8 – Sprache 3, Bitrate 2  
9 – Sprache 3, Bitrate 3  
</dl>

Dieses Szenario kann mithilfe der folgenden vier objekte für gegenseitigen Ausschluss implementiert werden:

-   Das erste objekt für gegenseitigen Ausschluss umfasst die Streams 1, 2 und 3, die sich durch die Bitrate gegenseitig ausschließen. Jeder Stream verfügt über einen eigenen Datensatz.
-   Das zweite objekt für gegenseitigen Ausschluss umfasst die Streams 4, 5 und 6, die sich durch die Bitrate gegenseitig ausschließen. Jeder Stream verfügt über einen eigenen Datensatz.
-   Das dritte objekt für gegenseitigen Ausschluss umfasst 7, 8 und 9, das sich durch die Bitrate gegenseitig ausschließt. Jeder Stream verfügt über einen eigenen Datensatz.
-   Das vierte objekt für gegenseitigen Ausschluss enthält drei Datensätze, die erste einschließlich der Streams 1, 2 und 3. die zweite einschließlich der Streams 4, 5 und 6; und das dritte einschließlich der Streams 7, 8 und 9. Diese Datensätze schließen sich nach Sprache gegenseitig aus.

Beim Wiedergeben einer auf diese Weise erstellten Datei wählt die Streaminganwendung zuerst die Sprache aus, da die Wahrscheinlichkeit geringer ist, dass sie sich in der Mitte der Präsentation ändert, und wählt dann eine Bitrate aus.

## <a name="mutual-exclusion-object-creation-and-configuration"></a>Objekterstellung und -konfiguration für gegenseitigen Ausschluss

In der folgenden Liste wird der Prozess der Konfiguration eines gegenseitigen Ausschlussobjekts zusammengefasst:

1.  Erstellen Sie ein objekt für gegenseitigen Ausschluss.
2.  Legen Sie den Typ des gegenseitigen Ausschlusses fest.
3.  Konfigurieren Sie das Objekt für gegenseitigen Ausschluss, indem Sie Datensätze und die zugeordneten Streams hinzufügen.
4.  Fügen Sie dem Profil das Objekt für gegenseitigen Ausschluss hinzu.

So erstellen und konfigurieren Sie ein objekt für gegenseitigen Ausschluss

1.  Rufen Sie [**IMFASFProfile::CreateMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createmutualexclusion) auf, um ein leeres objekt für gegenseitigen Ausschluss zu erstellen.
2.  Rufen Sie [**IMFASFMutualExclusion::SetType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-settype) auf, um das Kriterium des sich gegenseitig ausschließenden Streams festzulegen.

    Die Streams können sich durch Sprache, Bitrate, Darstellung und benutzerdefinierte Kriterien gegenseitig ausschließen. Der Typ wird als GUID dargestellt. Eine Liste dieser Konstanten finden Sie unter [ASF Mutual Exclusion Type GUIDs](asf-mutual-exclusion-type-guids.md).

3.  Rufen Sie [**IMFASFMutualExclusion::AddRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-addrecord) auf, um dem objekt für gegenseitigen Ausschluss einen Datensatz hinzuzufügen.

    Diese Methode fügt einen leeren Datensatz hinzu und weist ihm einen Datensatzindex zu, der mit 0 beginnt.

4.  Rufen Sie [**IMFASFMutualExclusion::AddStreamForRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-addstreamforrecord) auf, um dem vom Datensatzindex angegebenen Datensatz die Streamnummer hinzuzufügen.

    Jeder Datensatz enthält mindestens einen Datenstrom. Jeder Datenstrom in einem Datensatz schließen sich gegenseitig von allen Datenströmen in jedem anderen Datensatz aus. Um die Anzahl der Streams in einem Datensatz abzurufen, rufen Sie [**IMFASFMutualExclusion::GetStreamsForRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-getstreamsforrecord) auf, indem Sie den Datensatzindex angeben.

    Um einen Datenstrom aus dem Datensatz zu entfernen, rufen Sie [**IMFASFMutualExclusion::RemoveStreamFromRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-removestreamfromrecord) auf, und geben Sie den Datensatzindex und die Streamnummer an.

5.  Rufen Sie [**IMFASFProfile::AddMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-addmutualexclusion) auf, um dem Profil das konfigurierte Objekt für gegenseitigen Ausschluss hinzuzufügen.

## <a name="enumerating-mutual-exclusion-objects-in-a-profile"></a>Aufzählen gegenseitiger Ausschlussobjekte in einem Profil

Wenn [**IMFASFProfile::AddMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-addmutualexclusion) erfolgreich ist, wird dem angegebenen Objekt ein Index zugewiesen, beginnend bei 0 (null).

Um die einem Profil zugeordneten gegenseitigen Ausschlussobjekte aufzulisten, rufen [**Sie IMFASFProfile::GetMutualExclusionCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getmutualexclusioncount) auf und durchlaufen die Liste, indem Sie [**IMFASFProfile::GetMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getmutualexclusion)aufrufen. Indizes für gegenseitigen Ausschluss sind sequenziell und liegen zwischen 0 und 1 kleiner als die Anzahl von Datenströmen, die von **GetMutualExclusionCount** abgerufen werden.

Ein objekt für gegenseitigen Ausschluss wird durch Aufrufen von [**IMFASFProfile::RemoveMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removemutualexclusion)aus dem Profil entfernt. Das Profil weist die gegenseitigen Ausschlussindizes neu zu, sodass sie sequenziell mit 0 beginnen. Dadurch werden zuvor gespeicherte Indizes überschrieben, die nach dem Aufruf dieser Methode nicht mehr gültig sind. Dadurch werden die zugeordneten Datensätze des gegenseitigen Ausschlussdatenstroms veröffentlicht.

## <a name="removing-records-in-a-mutual-exclusion-object"></a>Entfernen von Datensätzen in einem objekt für gegenseitigen Ausschluss

Um einen Datensatz aus einem gegenseitigen Ausschlussobjekt zu entfernen, rufen Sie [**IMFASFMutualExclusion::RemoveRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-removerecord)auf. Wenn diese Methode erfolgreich ist, indiziert das objekt für gegenseitigen Ausschluss die verbleibenden Datensätze, sodass sie sequenziell mit 0 beginnen. Die Anwendung sollte die Datensätze auflisten, um den richtigen Index für jeden Datensatz sicherzustellen. Rufen Sie hierzu [**IMFASFMutualExclusion::GetRecordCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-getrecordcount) auf, und durchlaufen Sie die Datensätze, indem [**Sie IMFASFMutualExclusion::GetStreamsForRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-getstreamsforrecord)aufrufen.

Das Entfernen des Datensatzes mit dem höchsten Index hat keine Auswirkungen auf die anderen Indizes.

## <a name="modifying-a-mutual-exclusion-object"></a>Ändern eines gegenseitigen Ausschlussobjekts

Um die Konfiguration des objekts für gegenseitigen Ausschluss im Profil zu ändern, muss die Anwendung das vorhandene objekt für gegenseitigen Ausschluss durch ein anderes Objekt ersetzen, das die neuen Einstellungen enthält.

So ändern Sie die Konfiguration des objekts für gegenseitigen Ausschluss im Profil

1.  Aufzählen der objekte für gegenseitigen Ausschluss im Profil, um das objekt abzurufen, das geändert werden muss.
2.  Rufen Sie [**IMFASFMutualExclusion::Clone**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-clone) auf, um das gegenseitige Ausschlussobjekt zu klonen.

3.  Konfigurieren Sie das geklonte Objekt nach Bedarf.
4.  Rufen Sie [**IMFASFProfile::RemoveMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removemutualexclusion) auf, um das alte gegenseitige Ausschlussobjekt aus dem Profil zu entfernen.

5.  Rufen Sie [**IMFASFProfile::AddMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-addmutualexclusion) auf, um dem Profil das aktualisierte Objekt für gegenseitigen Ausschluss hinzuzufügen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASF-Profil](asf-profile.md)
</dt> </dl>

 

 



