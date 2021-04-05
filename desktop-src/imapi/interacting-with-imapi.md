---
title: Interagieren mit IMAPI
description: In den folgenden Schritten wird eine typische Interaktion zwischen einer Anwendung und IMAPI beschrieben.
ms.assetid: e57a86c4-7e27-40cf-a9c1-081b3f20d9d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e68bee24cfe0724ed14d439b0789f5023338853
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947787"
---
# <a name="interacting-with-imapi"></a>Interagieren mit IMAPI

In den folgenden Schritten wird eine typische Interaktion zwischen einer Anwendung und IMAPI beschrieben.

1.  Erstellen Sie eine Instanz von **msdiscmasterobj** (mithilfe von **cokreateinstance**, intelligenten Zeigern aus einem Import usw.), und fordern Sie die [**idiscmaster**](/windows/desktop/api/Imapi/nn-imapi-idiscmaster) -Schnittstelle an.
2.  Rufen Sie den Zugriff auf IMAPI durch Aufrufen von [**idiscmaster:: Open**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-open)ab. Wenn dieser Vorgang erfolgreich ist, verfügt die Anwendung über Vollzugriff auf alle in **msdiscmasterobj** implementierten Schnittstellen und Methoden.
3.  Rufen Sie den Enumerator für den discmaster Format mithilfe von [**enumdiscmasterformats**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-enumdiscmasterformats)ab. Listet die vom Disk-Master Objekt unterstützten Formate auf und wählt dann das aktive Format aus. Bei den vom Enumerator zurückgegebenen Formaten handelt es sich um die IIDs der Schnittstellen für [**ijolietdiscmaster**](/windows/desktop/api/Imapi/nn-imapi-ijolietdiscmaster) und [**iredbookdiscmaster**](/windows/desktop/api/Imapi/nn-imapi-iredbookdiscmaster).
4.  Rufen Sie den Disk Recorder-Enumerator mithilfe von " [**enumdiskrecorder**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-enumdiscrecorders)" ab. Auflisten Sie die Liste der unterstützten Festplatten Recorder (spezifisch für das aktive Format), und wählen Sie dann die aktive Aufzeichnung aus. Die [**idiscrecorder**](/windows/desktop/api/Imapi/nn-imapi-idiscrecorder) -Schnittstelle stellt ein physisches Gerät dar.
5.  Verwenden Sie [**idiscmaster::P rogressrat**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-progressadvise) zum Registrieren für Fortschritts Rückrufe.
6.  Verwenden Sie die-Schnittstelle für das ausgewählte Format, um Inhalt zu erstellen. Inhalts Builds werden inkrementell erstellt, sodass Titel oder Ordnerinhalte einem Teil Scheiben Stück für Stück hinzugefügt werden können. Das aufbauen dieses Inhalts wird als *Staging eines Bilds* bezeichnet. Der Inhalt des bereitgestellten Abbilds kann nicht inkrementell gelöscht werden. (Sie können keinen hinzugefügten Titel entfernen, aber es ist möglich, den Inhalt eines gestaffelten Bilds zu löschen, damit das Staging wieder gestartet werden kann. Verwenden Sie [**idiscmaster:: clearformatcontent**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-clearformatcontent) , um das Staging neu zu starten.

**Für Audiodaten:  **

1.  Verwenden Sie [**iredbookdiscmaster:: kreateaudiotrack**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-createaudiotrack) , um anzugeben, dass ein neuer Audiotitel auf der Festplatte gestartet wird.
2.  Verwenden Sie [**iredbookdiscmaster:: addaudiotrackblocks**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-addaudiotrackblocks) , um einer Spur rohaudiodaten hinzuzufügen. Die Anwendung kann [**getavailableaudiotrackblocks**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-getavailableaudiotrackblocks), [**gettotalaudioblocks**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-gettotalaudioblocks)und [**getusedaudioblocks**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-getusedaudioblocks) zum Abrufen statistischer Informationen verwenden.
3.  Verwenden Sie [**iredbookdiscmaster:: closeaudiotrack**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-closeaudiotrack) , um eine Audiospur zu schließen.
4.  Wiederholen Sie die Schritte 1-3, bis kein Speicherplatz mehr vorhanden ist oder alle Audiospuren geschrieben wurden.

**Für Daten:  **

1.  Verwenden Sie [**ijolietdiscmaster:: AddData**](/windows/desktop/api/Imapi/nf-imapi-ijolietdiscmaster-adddata) , um den Inhalt eines Ordners dem Image hinzuzufügen. Die Elemente in einem Ordner werden im Stammverzeichnis der Bilddatei abgelegt. Verwenden Sie [**gettotaldatablocks**](/windows/desktop/api/Imapi/nf-imapi-ijolietdiscmaster-gettotaldatablocks) und [**getuseddatablocks**](/windows/desktop/api/Imapi/nf-imapi-ijolietdiscmaster-getuseddatablocks) , um statistische Informationen abzurufen.
2.  Wiederholen Sie den obigen Schritt, bis Sie nicht mehr genügend Speicherplatz haben oder alle Daten hinzugefügt wurden.

**Für alle-CDs:  **

1.  Verwenden Sie [**idiscmaster:: recorddisk**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc) , um die Festplatte aufzuzeichnen.
2.  Schließen Sie die IMAPI-Sitzung mithilfe von [**idiscmaster:: Close**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-close). Durch das Schließen der Sitzung wird der Inhalt des Datenträger-Stash gelöscht.

 

 




