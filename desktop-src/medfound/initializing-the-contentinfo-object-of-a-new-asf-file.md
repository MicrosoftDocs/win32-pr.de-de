---
description: Initialisieren des ContentInfo-Objekts einer neuen ASF-Datei
ms.assetid: a4f6c90e-1b38-4c70-8bc5-e2e16af3d87a
title: Initialisieren des ContentInfo-Objekts einer neuen ASF-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74826942700f4be8028075fcd9466414834eb8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343329"
---
# <a name="initializing-the-contentinfo-object-of-a-new-asf-file"></a>Initialisieren des ContentInfo-Objekts einer neuen ASF-Datei

Nachdem Sie ein leeres ContentInfo-Objekt durch Aufrufen der [**mfcreateasfcontentinfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) -Funktion erstellt haben, muss die Anwendung [**imfasfcontentinfo:: setprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) aufrufen, um das Codierungs Profil bereitzustellen. Weitere Informationen zum Erstellen eines Profils finden Sie unter [Erstellen eines ASF-Profils](creating-an-asf-profile.md).

Bevor Informationen aus dem Profil gelesen werden können, muss die **setprofile** -Methode das angegebene Profil Objekt durch Überprüfen der Datenstrom Bezeichner oder Medientypen überprüfen. Wenn das Profil die Überprüfung übergibt, werden verschiedene Header Objekte generiert, wie z. b. das Dateieigenschaften Objekt, das Eigenschaften Objekt der Stream-Bitrate, das Stream Properties-Objekt und das gegenseitige Ausschluss Objekt.

**Setprofile** berechnet und legt Empfohlene Werte für bestimmte Eigenschaften fest, z. b. den ein Vorlauf ausgeführt-Wert. Wenn dies nicht bereits festgelegt ist, hängt der empfohlene vorab Wert in Millisekunden vom maximalen Puffer Fenster des unzulässigen Bucket ab, der für die Streams im Profil angegeben ist. Entsprechend werden auch die minimalen und maximalen Datenpaket Größen festgelegt. Die empfohlenen Werte können die Paketgrößen überschreiben, die für das Profil über Attribute festgelegt werden.

Da die Datei gerade erstellt wird, wird die Datei als Broadcast-Typ kategorisiert, der durch das Flags-Feld des Dateieigenschaften Objekts gekennzeichnet ist. Bestimmte unbekannte Werte, wie z. b. die Anzahl von Datenpaketen, Wiedergabedauer und sende Dauer, werden auf 0 (null) festgelegt. Diese Werte werden durch die MF-,-ASF-Attribute **\_ \_ \_ xxx** -Attribute dargestellt und müssen von der Anwendung aktualisiert werden, nachdem die Dateierstellung fertiggestellt wurde.

Das angegebene Profil Objekt ersetzt alle vorhandenen Profile, die dem ContentInfo-Objekt zugeordnet sind, entfernt die Header Objekte, auf die verwiesen wird, und setzt globale Dateieigenschaften, z. b. vorab-und Datenpaket Größe, zurück.

Die **setprofile** -Methode erstellt außerdem das Datenobjekt, das das ASF-Datenobjekt darstellt. Wenn Sie ein ContentInfo-Objekt wieder verwenden, das Informationen zu beliebigen Datenpaketen enthält, schlägt **setprofile** fehl und gibt den \_ bereits initialisierten MF E-Fehler zurück, der \_ \_ anzeigt, dass er bereits einem vorhandenen ASF-Datenobjekt zugeordnet ist. Bei einem neuen ContentInfo-Objekt wird die Anzahl der Datenpakete standardmäßig auf 0 (null) festgelegt, und die Datenobjekt Größe ist auf 50 Bytes festgelegt. Wenn Sie den Multiplexer zum Generieren von Datenpaketen verwenden, aktualisiert der Multiplexer das ContentInfo-Objekt, um neue Werte wie die Anzahl der Datenpakete widerzuspiegeln. Weitere Informationen zur Generierung von Datenpaketen finden Sie unter [Generieren neuer ASF-Datenpakete](generating-new-asf-data-packets.md).

Nachdem alle Header Objekte zum endgültigen ASF-Header Objekt hinzugefügt wurden, kann die gesamte Header Größe durch den Aufruf von [**imfasfcontentinfo:: gedie adersize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize)abgerufen werden. Diese Größe schließt die anfängliche Größe des Datenobjekts ein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen von Eigenschaften im ContentInfo-Objekt](setting-properties-in-the-contentinfo-object.md)
</dt> <dt>

[Schreiben eines ASF-Header Objekts für eine neue Datei](writing-an-asf-header-object-for-a-new-file.md)
</dt> </dl>

 

 



