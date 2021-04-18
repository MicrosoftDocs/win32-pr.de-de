---
title: IMAPI-Schnittstellen
description: In den folgenden Tabellen werden die Schnittstellen, die C/C++-Entwickler verwendet haben, und das zugehörige Skript Objekt kurz beschrieben. Stellen Sie dem Objektnamen in der Tabelle den Namen \ 0034; IMAPI2. \ 0034; , um den Objektnamen vollständig zu qualifizieren, wenn das Objekt im Skript erstellt wird.
ms.assetid: dba81a45-34a8-4b49-9ccb-d61a7e7ee1f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bac989a9871b761a1f1700ec599cc51affd30b2e
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "106338645"
---
# <a name="imapi-interfaces"></a>IMAPI-Schnittstellen

In den folgenden Tabellen werden die Schnittstellen, die C/C++-Entwickler verwendet haben, und das zugehörige Skript Objekt kurz beschrieben. Stellen Sie dem Objektnamen in der Tabelle den Namen "IMAPI2" als Präfix voran. , um den Objektnamen vollständig zu qualifizieren, wenn das Objekt im Skript erstellt wird.

In der folgenden Tabelle sind die Schnittstellen, die Geräten zugeordnet sind, das Burn-Engine und das Format Writer und Radierer aufgeführt.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Schnittstelle</td>
<td>Object</td>
</tr>
<tr class="even">
<td>Low-Level-Burn-Engine.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-dwriteengine2events"><strong>DWriteEngine2Events</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2"><strong>IWriteEngine2</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2eventargs"><strong>IWriteEngine2EventArgs</strong></a></li>
</ul></td>
<td>MsftWriteEngine2</td>
</tr>
<tr class="odd">
<td>Hauptbildwriter.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2dataevents"><strong>DDiscFormat2DataEvents</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data"><strong>IDiscFormat2Data</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2dataeventargs"><strong>IDiscFormat2DataEventArgs</strong></a></li>
</ul></td>
<td>MsftDiscFormat2Data</td>
</tr>
<tr class="even">
<td>Datenträger.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2eraseevents"><strong>DDiscFormat2EraseEvents</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase"><strong>IDiscFormat2Erase</strong></a></li>
</ul></td>
<td>MsftDiscFormat2Erase</td>
</tr>
<tr class="odd">
<td>Rohbildwriter.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2rawcdevents"><strong>DDiscFormat2RawCDEvents</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd"><strong>IDiscFormat2RawCD</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcdeventargs"><strong>IDiscFormat2RawCDEventArgs</strong></a></li>
</ul></td>
<td>MsftDiscFormat2RawCD</td>
</tr>
<tr class="even">
<td>Track-at-Once-bildwriter.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2trackatonceevents"><strong>DDiscFormat2TrackAtOnceEvents</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce"><strong>IDiscFormat2TrackAtOnce</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonceeventargs"><strong>IDiscFormat2TrackAtOnceEventArgs</strong></a></li>
</ul></td>
<td>MsftDiscFormat2TrackAtOnce</td>
</tr>
<tr class="odd">
<td>Enumeration von Festplatten Geräten in der System Hardware Liste.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2"><strong>IDiscMaster2</strong></a></li>
</ul></td>
<td>MsftDiscMaster2</td>
</tr>
<tr class="even">
<td>Benachrichtigungs Delegat für das MsftDiscMaster2-Objekt.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscmaster2events"><strong>DDiscMaster2Events</strong></a></li>
</ul></td>
<td>DDiscMaster2Events</td>
</tr>
<tr class="odd">
<td>Einzelnes Aufzeichnungsgerät.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2"><strong>IDiscRecorder2</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2ex"><strong>IDiscRecorder2Ex</strong></a></li>
</ul></td>
<td>MsftDiscRecorder2</td>
</tr>
<tr class="even">
<td>Geräte Schreib Attribute, einschließlich Medientyp, Schreibgeschwindigkeit und Typ der Angular Velocity-Steuerelement.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-iwritespeeddescriptor"><strong>Iwrite-espeeddescriptor</strong></a></li>
</ul></td>
<td>Msftschreitespeeddescriptor</td>
</tr>
</tbody>
</table>



 

In der folgenden Tabelle sind die Dateisystem Schnittstellen aufgeführt.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Schnittstelle</td>
<td>Object</td>
</tr>
<tr class="even">
<td>Start Abbild Datenstrom und Eigenschaften für die Integration des Start baren Bilds in das Festplatten Abbild.
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ibootoptions"><strong>Ibootoptions</strong></a></li>
</ul></td>
<td>Bootoptions</td>
</tr>
<tr class="odd">
<td>Dateisystem Abbild und-Eigenschaften. Dieses Objekt enthält alle Spuren und Verweise auf das Startimage und das Ergebnisbild.
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageevents"><strong>Dfilesystemmageevents</strong></a></li>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageimportevents"><strong>Dfilesystemimageimportevents</strong></a></li>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage"><strong>Ifilesystemimage</strong></a></li>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2"><strong>IFileSystemImage2</strong></a></li>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage3"><strong>IFileSystemImage3</strong></a></li>
</ul></td>
<td>Cfilesystemimage</td>
</tr>
<tr class="even">
<td>Der Container des Datenstroms, der vom Dateisystem Objekt bereitgestellt wird.
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult"><strong>Ifilesystemimageresult</strong></a></li>
</ul></td>
<td>Filesystemimageresult</td>
</tr>
<tr class="odd">
<td>Verzeichnis Element im Dateisystem Abbild.
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem"><strong>Ifsidirectoriyitem</strong></a></li>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem2"><strong>IFsiDirectoryItem2</strong></a></li>
</ul></td>
<td>"F"</td>
</tr>
<tr class="even">
<td>Datei Element im Dateisystem Abbild.
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem"><strong>Ifsifleitem</strong></a></li>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem2"><strong>IFsiFileItem2</strong></a></li>
</ul></td>
<td>Fsifleitem</td>
</tr>
<tr class="odd">
<td>Schnittstelle, die Eigenschaften enthält, die für Datei-und Verzeichnis Elemente gemeinsam sind
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem"><strong>Ifsiitem</strong></a></li>
</ul></td>
<td>"F"</td>
</tr>
<tr class="even">
<td>Rohdaten-CD-Image Erstellung.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagecreator"><strong>Irawcdimagecreator</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagetrackinfo"><strong>Irawcdimagetrackinfo</strong></a></li>
</ul></td>
<td>Msctrawcdimagecreator</td>
</tr>
<tr class="odd">
<td>Objekt-Hilfsobjekt zum Verketten mehrerer Streams.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-istreamconcatenate"><strong>Istreamconcatenate</strong></a></li>
</ul></td>
<td>Msftstreamconcatenate</td>
</tr>
<tr class="even">
<td>Der überlappende Stream, der dem Festplatten Abbild hinzugefügt werden soll.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-istreaminterleave"><strong>Istreaminterleave</strong></a></li>
</ul></td>
<td>Msftstreaminterleave</td>
</tr>
<tr class="odd">
<td>Pseudo zufälliger generierter Stream.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-istreampseudorandombased"><strong>Istreampseudorandombased</strong></a></li>
</ul></td>
<td>MsftStreamPrgn001</td>
</tr>
<tr class="even">
<td>Das Skript Objekt <strong>msftstreamzero</strong> ist nicht als Schnittstelle implementiert.</td>
<td><a href="msftstreamzero.md"><strong>Msftstreamzero</strong></a></td>
</tr>
</tbody>
</table>



 

In der folgenden Tabelle sind hilfsschnittstellen aufgelistet.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Schnittstelle</td>
<td>Object</td>
</tr>
<tr class="even">
<td>Sammlung von sektorbereichen innerhalb eines Dateisystem Images.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrange"><strong>Iblockrange</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrangelist"><strong>Iblockrangelist</strong></a></li>
</ul></td>
<td>Kein entsprechendes Objekt</td>
</tr>
<tr class="odd">
<td>Unterstützung der Verbrauchs Überprüfung.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-iburnverification"><strong>Iburnverification</strong></a></li>
</ul></td>
<td>Kein entsprechendes Objekt</td>
</tr>
<tr class="even">
<td>Enumerator von "ssiitems" für C/C++-Anwendungen.
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumfsiitems"><strong>Ienumssiitems</strong></a></li>
</ul></td>
<td>Enummamaitems</td>
</tr>
<tr class="odd">
<td>Enumerator von progressitems für C/C++-Anwendungen.
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumprogressitems"><strong>Ienumprogressitems</strong></a></li>
</ul></td>
<td>Enumprogressitems</td>
</tr>
<tr class="even">
<td><ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsinamedstreams"><strong>Ifsinamedstreams</strong></a></li>
</ul></td>
<td>FsiFileItem2</td>
</tr>
<tr class="odd">
<td>Unterstützung der ISO-Abbild Überprüfung.
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iisoimagemanager"><strong>Iisoimagemanager</strong></a></li>
</ul></td>
<td>Kein entsprechendes Objekt</td>
</tr>
<tr class="even">
<td>Unterstützung mehrerer Sitzungen.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisession"><strong>Imultisession</strong></a></li>
</ul></td>
<td>Kein entsprechendes Objekt</td>
</tr>
<tr class="odd">
<td>Sequenzielle Unterstützung mehrerer Sitzungen.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential"><strong>Imultisessionsequential</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential2"><strong>IMultisessionSequential2</strong></a></li>
</ul></td>
<td>Msftmultisessionsequential</td>
</tr>
<tr class="even">
<td>Der Dateiname und die zugehörigen Blöcke im Ergebnisbild.
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem"><strong>Iprogressitem</strong></a></li>
</ul></td>
<td>Progressitem</td>
</tr>
<tr class="odd">
<td>Ergebnis Bildliste, aufgeschlüsselt nach Dateiname und zugeordneten Blöcken.
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitems"><strong>Iprogressitems</strong></a></li>
</ul></td>
<td>Progressitems</td>
</tr>
</tbody>
</table>



 

 

 




