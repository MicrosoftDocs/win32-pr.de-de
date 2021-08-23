---
title: Interagieren mit IMAPI
description: Die folgenden Schritte beschreiben eine typische Interaktion zwischen einer Anwendung und IMAPI.
ms.assetid: e57a86c4-7e27-40cf-a9c1-081b3f20d9d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab97d1a9d76d1e82dab64fb777ef5207d3d47560b2a889981c698ab78e3622b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726990"
---
# <a name="interacting-with-imapi"></a>Interagieren mit IMAPI

Die folgenden Schritte beschreiben eine typische Interaktion zwischen einer Anwendung und IMAPI.

1.  Erstellen Sie eine Instanz von **MSDiscMasterObj** (mithilfe von **CoCreateInstance,** intelligenten Zeigern aus einem Import und so weiter), und fordern Sie die [**IDiscMaster-Schnittstelle**](/windows/desktop/api/Imapi/nn-imapi-idiscmaster) an.
2.  Rufen Sie [**IDiscMaster::Open**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-open)auf, um Zugriff auf IMAPI zu erhalten. Wenn dieser Aufruf erfolgreich ist, hat die Anwendung Vollzugriff auf alle Schnittstellen und Methoden, die in **MSDiscMasterObj implementiert sind.**
3.  Rufen Sie den Datenträgermasterformat-Enumerator [**mithilfe von EnumDiscMasterFormats ab.**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-enumdiscmasterformats) Enumerieren Sie den Satz von Formaten, die das Datenträgermasterobjekt unterstützt, und wählen Sie dann das aktive Format aus. Die vom Enumerator zurückgegebenen Formate sind die IIDs der Schnittstellen für [**IJolietDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-ijolietdiscmaster) und [**IRedbookDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-iredbookdiscmaster).
4.  Rufen Sie den Datenträgeraufzeichnungs-Enumerator [**mithilfe von EnumDiscRecorders ab.**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-enumdiscrecorders) Listen Sie die Liste der unterstützten Datenträgeraufzeichnungen auf (spezifisch für das aktive Format), und wählen Sie dann die aktive Aufzeichnung aus. Die [**IDiscRecorder-Schnittstelle**](/windows/desktop/api/Imapi/nn-imapi-idiscrecorder) stellt ein physisches Gerät dar.
5.  Verwenden [**Sie IDiscMaster::P rogressAdvise,**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-progressadvise) um sich für Statusrückrufe zu registrieren.
6.  Verwenden Sie die -Schnittstelle für das ausgewählte Format, um Inhalt zu erstellen. Der Inhalt wird inkrementell erstellt, sodass Titel oder Ordnerinhalte einem Datenträger stückweise hinzugefügt werden können. Das Erstellen dieses Inhalts wird als Staging *eines Images bezeichnet.* Der Inhalt des gestagten Bilds kann nicht inkrementell gelöscht werden (Sie können eine hinzugefügte Spur nicht entfernen), aber es ist möglich, den Inhalt eines gestagten Bilds zu löschen, damit das Staging erneut gestartet werden kann. Verwenden [**Sie IDiscMaster::ClearFormatContent,**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-clearformatcontent) um das Staging neu zu starten.

**Für Audio: **

1.  Verwenden [**Sie IRedbookDiscMaster::CreateAudioTrack,**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-createaudiotrack) um anzugeben, dass eine neue Audiospur auf dem Datenträger gestartet wird.
2.  Verwenden [**Sie IRedbookDiscMaster::AddAudioTrackBlocks,**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-addaudiotrackblocks) um unformatierte Audiodaten zu einer Spur hinzuzufügen. Die Anwendung kann [**GetAvailableAudioTrackBlocks,**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-getavailableaudiotrackblocks) [**GetTotalAudioBlocks**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-gettotalaudioblocks)und [**GetUsedAudioBlocks**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-getusedaudioblocks) verwenden, um statistische Informationen abzurufen.
3.  Verwenden [**Sie IRedbookDiscMaster::CloseAudioTrack,**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-closeaudiotrack) um eine Audiospur zu schließen.
4.  Wiederholen Sie die Schritte 1 bis 3, bis kein Speicherplatz mehr zur Verfügung steht oder alle Audiospuren geschrieben wurden.

**Für Daten: **

1.  Verwenden [**Sie IJolietDiscMaster::AddData,**](/windows/desktop/api/Imapi/nf-imapi-ijolietdiscmaster-adddata) um dem Bild den Inhalt eines Ordners hinzuzufügen. Die Elemente in einem Ordner werden im Stammverzeichnis der Imagedatei platziert. Verwenden [**Sie GetTotalDataBlocks**](/windows/desktop/api/Imapi/nf-imapi-ijolietdiscmaster-gettotaldatablocks) und [**GetUsedDataBlocks,**](/windows/desktop/api/Imapi/nf-imapi-ijolietdiscmaster-getuseddatablocks) um statistische Informationen abzurufen.
2.  Wiederholen Sie den obigen Schritt, bis nicht mehr Speicherplatz zur Verfügung steht oder alle Daten hinzugefügt wurden.

**Für alle Datenträger: **

1.  Verwenden [**Sie IDiscMaster::RecordDisc,**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc) um den Datenträger aufzeichnen.
2.  Schließen Sie die IMAPI-Sitzung [**mithilfe von IDiscMaster::Close**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-close). Wenn Sie die Sitzung schließen, wird der Inhalt des Datenträgerstashs gelöscht.

 

 




