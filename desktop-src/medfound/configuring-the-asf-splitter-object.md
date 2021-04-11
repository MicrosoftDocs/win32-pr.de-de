---
description: Konfigurieren des ASF-Splitter Objekts
ms.assetid: 8e2ba659-e1f6-42be-afd6-21fc841dc8d3
title: Konfigurieren des ASF-Splitter Objekts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14f27885e602dd52012808d330d997f9b7a7e983
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127957"
---
# <a name="configuring-the-asf-splitter-object"></a>Konfigurieren des ASF-Splitter Objekts

Das ASF- *Splitter* Objekt ist ein wmcontainer-Ebenenobjekt, das das ASF-Datenobjekt einer ASF-Datei (Advanced Systems Format) analysiert. Nachdem der Splitter erstellt und initialisiert wurde, um das ASF-Datenobjekt einer Mediendatei zu analysieren, muss der Splitter so konfiguriert werden, dass er Beispiele für bestimmte Streams generiert. Greifen Sie auf [**imfasfsplitter:: selectstreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams) zu, um die erforderlichen Streams auszuwählen.

Optional kann eine Anwendung Sie auch so konfigurieren, dass Beispiele in umgekehrter Reihenfolge generiert oder Beispiele für geschützte Inhalte generiert werden. Um diese Optionen festzulegen, müssen Sie [**imfasfsplitter:: setFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-setflags) aufrufen und die erforderliche bitweise Kombination der unterstützten Flags übergeben. Vor dem Aufrufen dieser Methode muss der Client den [**imfasfsplitter:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) -Aufruf erfolgreich abschließen. Andernfalls schlägt " **setFlags** " mit dem Fehlercode " **MF \_ E \_ Not \_ Initialized** " fehl. Weitere Informationen zum Initialisieren des Splitters finden Sie unter [Erstellen des ASF-Splitter Objekts](creating-the-asf-splitter-object.md).

Um zu überprüfen, ob dieses Flag momentan für den Splitter festgelegt ist, müssen Sie [**imfasfsplitter:: GetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getflags)aufrufen.

## <a name="selecting-streams-for-parsing"></a>Auswählen von Streams für die Verarbeitung

Während des Initialisierungs Vorgangs durch den [**imfasfsplitter:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) -Befehl erkennt der Splitter die Anzahl der Streams und die Datenstrom Bezeichner in der ASF-Datei. Standardmäßig werden keine Streams vom Splitter ausgewählt. Die Anwendung muss die Streams durch Aufrufen von [**imfasfsplitter:: selectstreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams)auswählen. Diese Methode nimmt ein Array von streamnummern an. Um die streamnummer für einen Stream abzurufen, müssen Sie [**imfasfprofile:: GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) im ASF-Profil aufrufen oder [**imfstreamdescriptor:: getstreamidentifier**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getstreamidentifier) für den Datenstrom Deskriptor aufrufen. (Sie können sowohl das ASF-Profil als auch den Datenstrom Deskriptor aus dem ContentInfo-Objekt abrufen.) Wenn der Client eine streamnummer übergibt, die nicht vom Splitter erkannt wird, schlägt er mit einem Fehler in der **MF- \_ E \_ invalidstreamnumber** fehl.

Durch das Aufrufen von [**selectstreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams) wird die vorherige Auswahl gelöscht. Jeder Datenstrom, der nicht im-Array angegeben ist, ist nicht ausgewählt. Zum Abrufen einer Liste von Datenströmen, die derzeit ausgewählt sind, müssen Sie [**imfasfsplitter:: getselectedstreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getselectedstreams)aufrufen. Diese Methode nimmt einen Zeiger auf ein Array, das die-Methode mit den streamnummern füllt. Wenn die Array Größe kleiner ist als die Anzahl der ausgewählten Streams, schlägt die Methode mit dem Fehler " **MF \_ E \_ buffertoosmall** " fehl. In diesem Fall gibt die-Methode die Anzahl der ausgewählten Streams im *pwnumstreams* -Parameter zurück. Anschließend können Sie diese Zahl verwenden, um ein Array der richtigen Größe zuzuweisen und die Methode erneut aufzurufen.

Beispielcode finden Sie unter "Auswählen eines Datenstroms zum Auswerten" in [Tutorial: Lesen einer ASF-Datei](tutorial--reading-an-asf-file.md).

## <a name="reverse-playback-setting"></a>Umgekehrte Wiedergabe Einstellung

Während der Initialisierung des Splitters wird ermittelt, ob der ASF-Inhalt die umgekehrte Wiedergabe unterstützt. Wenn dies der Fall ist, kann der Splitter so konfiguriert werden, dass er Beispiele in umgekehrter Reihenfolge generiert, indem das Flag " **mfasf- \_ Splitter \_ umkehren** " Wenn der Inhalt die umgekehrte Wiedergabe nicht unterstützt, gibt [**imfasssplitter:: setFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-setflags) **MF \_ E \_ invalidrequest** zurück, aber das Flag wird für den Splitter festgelegt.

Wenn der Splitter zum Analysieren in umgekehrter Richtung konfiguriert ist, beginnt der Splitter stets mit der Analyse am Ende des Puffers, der das ASF-Datenobjekt enthält. Daher muss für die umgekehrte Analyse des Daten Offsets und die Länge der zu testenden Daten entsprechend festgelegt werden. Weitere Informationen zum Festlegen der korrekten Werte finden Sie unter [Erstellen von streambeispielen aus einem vorhandenen ASF-Datenobjekt](generating-stream-samples-from-an-existing-asf-data-object.md).

## <a name="protected-content-setting"></a>Einstellung geschützter Inhalt

Der Splitter kann so konfiguriert werden, dass er mit Verschlüsselungs Inhalt auf Paketebene arbeitet, indem er die **mfasf- \_ Splitter- \_ WMDRM** über [**imfasfsplitter:: setFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-setflags)festlegt. Dies weist den Splitter an, Beispiele für Inhalte bereitzustellen, die von Windows Media Digital Rights Management (DRM) geschützt werden. Wenn dieses Flag festgelegt ist, enthalten die von dem Splitter generierten Beispiele Informationen, die zum Entschlüsseln von Mediendaten und zum Rekonstruieren der Frames, wie z. b. das [**mfsampleextension \_ packetcrossoffsets**](mfsampleextension-packetcrossoffsets-attribute.md) -Attribut, erforderlich sind. Dieses Attribut ist ein BLOB, das ein Array von **DWORD** s enthält. Jedes **DWORD** stellt die Nutz Last Begrenzungen für den Frame relativ zum Anfang des Frames bereit. Wenn dieses Attribut nicht vorhanden ist, ist der Frame in einer einzelnen Nutzlast enthalten. Die vom Splitter generierten Beispiele enthalten in der Regel mehrere Medien Puffer. die Anwendung kann alle Puffer durch Aufrufen von [**imfsample:: converttocontiguousbuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer)in einen zusammenhängenden Puffer kopieren. Der resultierende Puffer enthält den Frame, und der Attribut Wert enthält Offsets in diesem Puffer.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASF-Splitter](asf-splitter.md)
</dt> </dl>

 

 



