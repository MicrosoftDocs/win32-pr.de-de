---
description: Konfigurieren des ASF-Splitterobjekts
ms.assetid: 8e2ba659-e1f6-42be-afd6-21fc841dc8d3
title: Konfigurieren des ASF-Splitterobjekts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7068f2c869f6c73447b3341baee7221cdf8efbacec47ecdfa3a584bfb456f199
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606150"
---
# <a name="configuring-the-asf-splitter-object"></a>Konfigurieren des ASF-Splitterobjekts

Das *ASF-Splitterobjekt* ist ein WMContainer-Ebenenobjekt, das das ASF-Datenobjekt einer ASF-Datei (Advanced Systems Format) analysiert. Nachdem der Splitter erstellt und initialisiert wurde, um das ASF-Datenobjekt einer Mediendatei zu analysieren, muss der Splitter so konfiguriert werden, dass Stichproben für bestimmte Streams generiert werden. Rufen [**Sie IMFASFSplitter::SelectStreams auf,**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams) um die erforderlichen Streams auszuwählen.

Optional kann eine Anwendung sie auch so konfigurieren, dass Beispiele in umgekehrter Reihenfolge generiert oder Beispiele für geschützte Inhalte generiert werden. Rufen Sie ZUM Festlegen dieser Optionen [**IMFASFSplitter::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-setflags) auf, und übergeben Sie die erforderliche bitweise Kombination der unterstützten Flags. Vor dem Aufrufen dieser Methode muss der Client den [**IMFASFSplitter::Initialize-Aufruf erfolgreich**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) abschließen. Andernfalls **schlägt SetFlags** mit **MF \_ E NOT \_ \_ INITIALIZED-Fehlercode** fehl. Informationen zum Initialisieren des Splitters finden Sie unter [Erstellen des ASF-Splitterobjekts.](creating-the-asf-splitter-object.md)

Um zu überprüfen, ob dieses Flag derzeit für den Splitter festgelegt ist, rufen Sie [**IMFASFSplitter::GetFlags auf.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getflags)

## <a name="selecting-streams-for-parsing"></a>Auswählen Streams für die Analyse

Während des Initialisierungsprozesses über [**den IMFASFSplitter::Initialize-Aufruf**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) erkennt der Splitter die Anzahl der Streams und die Streambezeichner in der ASF-Datei. Standardmäßig werden vom Splitter keine Datenströme ausgewählt. Die Anwendung muss die Streams auswählen, indem [**sie IMFASFSplitter::SelectStreams aufruft.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams) Diese Methode verwendet ein Array von Streamnummern. Um die Streamnummer für einen Stream zu erhalten, rufen Sie [**IMFASFProfile::GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) im ASF-Profil auf, oder rufen Sie [**IMFASFProfile::GetStreamIdentifier**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getstreamidentifier) für den Streamdeskriptor auf. (Sie können sowohl das ASF-Profil als auch den Streamdeskriptor aus dem ContentInfo-Objekt abrufen.) Wenn der Client eine Datenstromnummer übergibt, die vom Splitter nicht erkannt wird, tritt ein **MF \_ E \_ INVALIDSTREAMNUMBER-Fehler** auf.

Durch [**das Aufrufen von SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams) werden die vorherigen Auswahlen nicht mehr ausgewählt. Ein Stream, der nicht im Array angegeben ist, ist nicht ausgewählt. Um eine Liste der aktuell ausgewählten Streams zu erhalten, rufen Sie [**IMFASFSplitter::GetSelectedStreams auf.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getselectedstreams) Diese Methode verwendet einen Zeiger auf ein Array, das von der -Methode mit den Streamnummern auffüllt wird. Wenn die Arraygröße kleiner als die Anzahl der ausgewählten Streams ist, schlägt die Methode mit dem **MF \_ E \_ BUFFERTOOSMALL-Fehler** fehl. In diesem Fall gibt die -Methode die Anzahl der ausgewählten Streams im *pwNumStreams-Parameter* zurück. Sie können diese Zahl dann verwenden, um ein Array der richtigen Größe zu zuordnen und die -Methode erneut aufrufen.

Beispielcode finden Sie unter "Select a Stream for Parsing" in [Tutorial: Reading an ASF File (Tutorial: Lesen einer ASF-Datei).](tutorial--reading-an-asf-file.md)

## <a name="reverse-playback-setting"></a>Einstellung für die umgekehrte Wiedergabe

Während des Initialisierungsprozesses des Splitters wird ermittelt, ob der ASF-Inhalt die umgekehrte Wiedergabe unterstützt. Wenn dies der Fall ist, kann der Splitter so konfiguriert werden, dass Stichproben in umgekehrter Reihenfolge generiert werden, indem das **Flag MFASF \_ SPLITTER REVERSE (MFASF-SPLITTER \_ REVERSE) konfiguriert** wird. Wenn der Inhalt keine umgekehrte Wiedergabe unterstützt, gibt [**IMFASFSplitter::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-setflags) **MF \_ E \_ INVALIDREQUEST** zurück, aber das Flag wird für den Splitter festgelegt.

Wenn der Splitter für die Analyse in umgekehrter Richtung konfiguriert ist, beginnt der Splitter immer mit der Analyse am Ende des Puffers, der das ASF-Datenobjekt enthält. Daher müssen für die umgekehrte Analyse der Datenoffset und die Länge der zu analysierenden Daten entsprechend festgelegt werden. Informationen zum Festlegen der richtigen Werte finden Sie unter [Generieren von Streambeispielen aus einem vorhandenen ASF-Datenobjekt.](generating-stream-samples-from-an-existing-asf-data-object.md)

## <a name="protected-content-setting"></a>Einstellung für geschützten Inhalt

Der Splitter kann so konfiguriert werden, dass er mit Verschlüsselungsinhalten auf Paketebene funktioniert, indem der **MFASF-SPLITTER \_ \_ WMDRM** über [**IMFASFSplitter::SetFlags festgelegt wird.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-setflags) Dadurch wird der Splitter angewiesen, Beispiele für Inhalte zu liefern, die durch Windows Media Digital Rights Management (DRM) geschützt sind. Wenn dieses Flag festgelegt ist, enthalten die vom Splitter generierten Beispiele Informationen, die zum Entschlüsseln von Mediendaten und Rekonstruieren der Frames erforderlich sind, z. B. das [**MFSampleExtension \_ PacketCrossOffsets-Attribut.**](mfsampleextension-packetcrossoffsets-attribute.md) Dieses Attribut ist ein Blob, das ein Array von **DWORD-s** enthält. Jedes **DWORD** stellt Ihnen die Nutzlastgrenzen für den Frame relativ zum Anfang des Frames zurEntlastung. Wenn dieses Attribut nicht vorhanden ist, ist der Frame in einer einzelnen Nutzlast enthalten. In der Regel enthalten die vom Splitter generierten Beispiele mehrere Medienpuffer. Die Anwendung kann alle Puffer in einen zusammenhängenden Puffer kopieren, indem [**sie DIEBSAMPLE::ConvertToContiguousBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer)aufruft. Der resultierende Puffer enthält den Frame, und der Attributwert enthält Offsets in diesem Puffer.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASF-Splitter](asf-splitter.md)
</dt> </dl>

 

 



