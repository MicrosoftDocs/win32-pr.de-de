---
title: IMAPI-Schnittstellen
description: In den folgenden Tabellen werden die Schnittstellen, die C/C++-Entwickler verwenden, und das zugehörige Skriptobjekt identifiziert und kurz beschrieben. Stellen Sie dem Objektnamen in der Tabelle das Präfix \ 0034;IMAPI2 voran. \ 0034; , um den Objektnamen beim Erstellen des Objekts im Skript vollständig zu qualifizieren.
ms.assetid: dba81a45-34a8-4b49-9ccb-d61a7e7ee1f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c093acd587f975859d68fda23f6c1f169d969a78
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466176"
---
# <a name="imapi-interfaces"></a>IMAPI-Schnittstellen

In den folgenden Tabellen werden die Schnittstellen, die C/C++-Entwickler verwenden, und das zugehörige Skriptobjekt identifiziert und kurz beschrieben. Stellen Sie dem Objektnamen in der Tabelle das Präfix "IMAPI2" voran. , um den Objektnamen beim Erstellen des Objekts im Skript vollständig zu qualifizieren.

In der folgenden Tabelle sind die Schnittstellen aufgeführt, die Geräten, der Burn-Engine und dem Formatwriter und Radierer zugeordnet sind.




| | | Schnittstellen-| Objekt | | Low-Level-Burn-Engine.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-dwriteengine2events"><strong>DWriteEngine2Events</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2"><strong>IWriteEngine2</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2eventargs"><strong>IWriteEngine2EventArgs</strong></a></li></ul> | MsftWriteEngine2 | | Hauptimagewriter.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2dataevents"><strong>DDiscFormat2DataEvents</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data"><strong>IDiscFormat2Data</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2dataeventargs"><strong>IDiscFormat2DataEventArgs</strong></a></li></ul> | MsftDiscFormat2Data | | Datenträgerradierer.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2eraseevents"><strong>DDiscFormat2EraseEvents</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase"><strong>IDiscFormat2Erase</strong></a></li></ul> | MsftDiscFormat2Erase | | Raw Image Writer.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2rawcdevents"><strong>DDiscFormat2RawCDEvents</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd"><strong>IDiscFormat2RawCD</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcdeventargs"><strong>IDiscFormat2RawCDEventArgs</strong></a></li></ul> | MsftDiscFormat2RawCD | | Track-At-Once-Imagewriter.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2trackatonceevents"><strong>DDiscFormat2TrackAtOnceEvents</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce"><strong>IDiscFormat2TrackAtOnce</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonceeventargs"><strong>IDiscFormat2TrackAtOnceEventArgs</strong></a></li></ul> | MsftDiscFormat2TrackAtOnce | | Enumeration von Datenträgergeräten in der Systemhardwareliste.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2"><strong>IDiscMaster2</strong></a></li></ul> | MsftDiscMaster2-| | Benachrichtigungsdelegat für das MsftDiscMaster2-Objekt.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscmaster2events"><strong>DDiscMaster2Events</strong></a></li></ul> | DDiscMaster2Events | | Einzelnes Aufzeichnungsgerät.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2"><strong>IDiscRecorder2</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2ex"><strong>IDiscRecorder2Ex</strong></a></li></ul> | MsftDiscRecorder2 | | Geräte, die Attribute schreiben, einschließlich Medientyp, Schreibgeschwindigkeit und Typ der Angular-Geschwindigkeitssteuerung.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-iwritespeeddescriptor"><strong>IWriteSpeedDescriptor</strong></a></li></ul> | MsftWriteSpeedDescriptor | 




 

In der folgenden Tabelle sind die Dateisystemschnittstellen aufgeführt.




| | | Schnittstellen-| Objekt | | Startimagestream und Eigenschaften für die Integration des startbaren Images in das Datenträgerimage.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ibootoptions"><strong>IBootOptions</strong></a></li></ul> | BootOptions | | Dateisystemimage und -eigenschaften. Dieses Objekt enthält alle Spuren und Verweise auf das Startabbild und das Ergebnisimage.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageevents"><strong>DFileSystemImageEvents</strong></a></li><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageimportevents"><strong>DFileSystemImageImportEvents</strong></a></li><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage"><strong>IFileSystemImage</strong></a></li><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2"><strong>IFileSystemImage2</strong></a></li><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage3"><strong>IFileSystemImage3</strong></a></li></ul> | CFileSystemImage | | Container des vom Dateisystemobjekt bereitgestellten Datenstroms.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult"><strong>IFileSystemImageResult</strong></a></li></ul> | FileSystemImageResult-| | Verzeichniselement im Dateisystemimage.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem"><strong>IFsiDirectoryItem</strong></a></li><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem2"><strong>IFsiDirectoryItem2</strong></a></li></ul> | FsiDirectoryItem | | Dateielement im Dateisystemimage.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem"><strong>IFsiFileItem</strong></a></li><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem2"><strong>IFsiFileItem2</strong></a></li></ul> | FsiFileItem | | Schnittstelle, die Eigenschaften enthält, die sowohl Datei- als auch Verzeichniselementen gemeinsam sind.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem"><strong>IFsiItem</strong></a></li></ul> | FsiItem | | Erstellung von RAW-CD-Images.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagecreator"><strong>IRawCDImageCreator</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagetrackinfo"><strong>IRawCDImageTrackInfo</strong></a></li></ul> | MsftRawCDImageCreator | | Streamobjekthilfsobjekt zum Verketten mehrerer Streams.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-istreamconcatenate"><strong>IStreamConcatenate</strong></a></li></ul> | MsftStreamConcatenate | | Verschachtelter Stream, der dem Datenträgerimage hinzugefügt werden soll.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-istreaminterleave"><strong>IStreamInterleave</strong></a></li></ul> | MsftStreamInterleave | | Pseudozufallsbasierter generierter Stream.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-istreampseudorandombased"><strong>IStreamPseudoRandomBased</strong></a></li></ul> | MsftStreamPrgn001 | | Das <strong>MsftStreamZero-Skriptobjekt</strong> ist nicht als Schnittstelle implementiert. | <a href="msftstreamzero.md"><strong>MsftStreamZero</strong></a> | 




 

In der folgenden Tabelle sind Hilfschnittstellen aufgeführt.




| | | Schnittstellen-| Objekt | | Sammlung von Sektorbereichen innerhalb eines Dateisystemimages.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrange"><strong>IBlockRange</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrangelist"><strong>IBlockRangeList</strong></a></li></ul> | Kein entsprechendes Objekt | | Burn-Überprüfungsunterstützung.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-iburnverification"><strong>I Auslassungserteilung</strong></a></li></ul> | Kein entsprechendes Objekt | | Enumerator von FsiItems für C/C++-Anwendungen.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumfsiitems"><strong>IEnumFsiItems</strong></a></li></ul> | EnumFsiItems | | Enumerator von ProgressItems für C/C++-Anwendungen.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumprogressitems"><strong>IEnumProgressItems</strong></a></li></ul> | EnumProgressItems | | <ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsinamedstreams"><strong>IFsiNamedStreams</strong></a></li></ul> | FsiFileItem2 | | Unterstützung der ISO-Imageüberprüfung.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iisoimagemanager"><strong>IIsoImageManager</strong></a></li></ul> | Kein entsprechendes Objekt | | Unterstützung mehrerer Sitzungen.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisession"><strong>IMultisession</strong></a></li></ul> | Kein entsprechendes Objekt | | Unterstützung mehrerer sequenzieller Sitzungen.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential"><strong>IMultisessionSequential</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential2"><strong>IMultisessionSequential2</strong></a></li></ul> | MsftMultisessionSequential | | Dateiname und zugeordnete Blöcke im Ergebnisbild.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem"><strong>IProgressItem</strong></a></li></ul> | ProgressItem | | Auflistung der Ergebnisbilder, aufgeschlüsselt nach Dateinamen und zugeordneten Blöcken.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitems"><strong>IProgressItems</strong></a></li></ul> | ProgressItems | 




 

 

 




