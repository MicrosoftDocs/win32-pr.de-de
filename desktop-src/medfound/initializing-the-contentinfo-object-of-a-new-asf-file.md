---
description: Initialisieren des ContentInfo-Objekts einer neuen ASF-Datei
ms.assetid: a4f6c90e-1b38-4c70-8bc5-e2e16af3d87a
title: Initialisieren des ContentInfo-Objekts einer neuen ASF-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf0180eb4e9369447355a9a4cd607f630bfb3664108ad77d6d008c281f92fdf1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114250"
---
# <a name="initializing-the-contentinfo-object-of-a-new-asf-file"></a>Initialisieren des ContentInfo-Objekts einer neuen ASF-Datei

Nach dem Erstellen eines leeren ContentInfo-Objekts durch Aufrufen der [**MFCreateASFContentInfo-Funktion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) muss die Anwendung [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) aufrufen, um das Codierungsprofil bereitzustellen. Informationen zum Erstellen eines Profils finden Sie unter [Erstellen eines ASF-Profils.](creating-an-asf-profile.md)

Bevor Informationen aus dem Profil gelesen werden können, muss die **SetProfile-Methode** das angegebene Profilobjekt überprüfen, indem sie die Streambezeichner oder Medientypen überprüft. Wenn das Profil die Überprüfung besteht, werden verschiedene Headerobjekte generiert, z. B. das Dateieigenschaftenobjekt, das Stream Bitrate Properties Object, das Stream Properties Object und das Mutual Exclusion Object.

**SetProfile** berechnet und legt empfohlene Werte für bestimmte Eigenschaften fest, z. B. den Prerollwert. Wenn dies noch nicht festgelegt ist, hängt der empfohlene Prärollwert in Millisekunden vom maximalen Pufferfenster des leaky-Buckets ab, der für die Streams im Profil angegeben ist. Auf ähnliche Weise werden auch die minimale und maximale Datenpaketgröße festgelegt. Die empfohlenen Werte können die Paketgrößen überschreiben, die im Profil über Attribute festgelegt werden.

Da die Datei gerade erstellt wird, wird sie als Broadcasttyp kategorisiert, der durch das Feld Flags des Dateieigenschaftenobjekts gekennzeichnet wird. Bestimmte unbekannte Werte, z. B. die Anzahl der Datenpakete, die Wiedergabedauer und die Sendedauer, werden auf 0 (null) festgelegt. Diese Werte werden durch **MF \_ PD \_ ASF \_ xxx-Attribute** dargestellt und müssen von der Anwendung aktualisiert werden, nachdem die Dateierstellung abgeschlossen ist.

Das angegebene Profilobjekt ersetzt alle vorhandenen Profile, die dem ContentInfo-Objekt zugeordnet sind, entfernt die Headerobjekte, auf die verwiesen wird, und setzt globale Dateieigenschaften wie Preroll und Datenpaketgröße zurück.

Die **SetProfile-Methode** erstellt auch das Datenobjekt, das das ASF-Datenobjekt darstellt. Wenn Sie ein ContentInfo-Objekt wiederverwenden, das Informationen zu Datenpaketen enthält, schlägt **SetProfile** fehl und gibt den MF E ALREADY INITIALIZED-Fehler zurück, der \_ \_ \_ angibt, dass es bereits einem vorhandenen ASF-Datenobjekt zugeordnet ist. Für ein neues ContentInfo-Objekt ist die Datenpaketanzahl standardmäßig auf 0 (null) und die Größe des Datenobjekts auf 50 Bytes festgelegt. Wenn Sie den Multiplexer zum Generieren von Datenpaketen verwenden, aktualisiert der Multiplexer das ContentInfo-Objekt, um neue Werte wie die Anzahl der Datenpakete widerzuspiegeln. Weitere Informationen zur Generierung von Datenpaketen finden Sie unter [Generieren neuer ASF-Datenpakete.](generating-new-asf-data-packets.md)

Nachdem alle Headerobjekte dem endgültigen ASF-Headerobjekt hinzugefügt wurden, kann die Gesamtheadergröße durch Aufrufen von [**IMFASFContentInfo::GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize)abgerufen werden. Diese Größe schließt die Anfängliche Größe des Datenobjekts ein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen von Eigenschaften im ContentInfo-Objekt](setting-properties-in-the-contentinfo-object.md)
</dt> <dt>

[Schreiben eines ASF-Headerobjekts für eine neue Datei](writing-an-asf-header-object-for-a-new-file.md)
</dt> </dl>

 

 



