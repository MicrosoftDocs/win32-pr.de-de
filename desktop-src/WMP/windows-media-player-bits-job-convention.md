---
title: Windows Media Player Bits-Auftrags Konvention
description: Windows Media Player können digitale Medienelemente automatisch herunterladen und der Bibliothek hinzufügen, wenn Sie Background Intelligent Transfer Service (Bits) verwenden.
ms.assetid: 643faba7-9af2-4292-8d92-e321d7690a5b
keywords:
- Windows Media Player Online Stores, Background Intelligent Transfer Service (Bits)
- Online Stores, Background Intelligent Transfer Service (Bits)
- Typ 2 Online Stores, Background Intelligent Transfer Service (Bits)
- Intelligenter Hintergrundübertragungsdienst (Background Intelligent Transfer Service, BITS)
- Bits (Background Intelligent Transfer Service)
- Windows Media Player Online Stores, Bits-Auftrags Konvention
- Online Stores, Bits-Auftrags Konvention
- Typ 2 Online Stores, Bits-Auftrags Konvention
- Bits-Auftrags Konvention
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85278593ce151f46370ca491ccac8e1645f9bb70
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104209321"
---
# <a name="windows-media-player-bits-job-convention"></a>Windows Media Player Bits-Auftrags Konvention

Windows Media Player können digitale Medienelemente automatisch herunterladen und der Bibliothek hinzufügen, wenn Sie [Background Intelligent Transfer Service (Bits)](/windows/desktop/Bits/background-intelligent-transfer-service-portal)verwenden. Um dieses Feature nutzen zu können, müssen Sie den Auftrag der Bits-Übertragungs Warteschlange hinzufügen und **ibackgroundcopyjob:: setDescription** aufrufen, indem Sie eine Beschreibungs Zeichenfolge mit dem richtigen Format angeben.

> [!Note]  
> In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

## <a name="syntax"></a>Syntax

``` syntax
::WMP_JOB:1:serviceId:Provider:AlbumArtist:AlbumTitle:TrackNumber:Title:Duration:Rating
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="serviceId"></span><span id="serviceid"></span><span id="SERVICEID"></span>*serviceId*
</dt> <dd>

Ein zufällig generierter 32-Bit-Wert, der von Windows Media Player verwendet wird, um den Dienst zu identifizieren.

</dd> <dt>

<span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>*Ab*
</dt> <dd>

Der Anbietername. Dieser Wert muss mit einem gültigen Namen für den Onlinespeicher Schlüssel identisch sein.

</dd> <dt>

<span id="AlbumArtist"></span><span id="albumartist"></span><span id="ALBUMARTIST"></span>*Albumartist*
</dt> <dd>

Der Name des primären Künstlers für das Album.

</dd> <dt>

<span id="AlbumTitle"></span><span id="albumtitle"></span><span id="ALBUMTITLE"></span>*Albumtitle*
</dt> <dd>

Der Titel des Albums.

</dd> <dt>

<span id="TrackNumber"></span><span id="tracknumber"></span><span id="TRACKNUMBER"></span>*Tracknumber*
</dt> <dd>

Die CD-Nachverfolgung.

</dd> <dt>

<span id="Title"></span><span id="title"></span><span id="TITLE"></span>*Tel*
</dt> <dd>

Der Titel des Inhalts.

</dd> <dt>

<span id="Duration"></span><span id="duration"></span><span id="DURATION"></span>*Auf*
</dt> <dd>

Die Dauer des Inhalts.

</dd> <dt>

<span id="Rating"></span><span id="rating"></span><span id="RATING"></span>*Leistung*
</dt> <dd>

Die Bewertung für den Inhalt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Windows Media Player 10 oder höher Bits zum Herunterladen von Inhalten verwendet, listet es die Aufträge in der Übertragungs Warteschlange auf und überprüft die Beschreibungs Zeichenfolge für jeden Auftrag. Wenn die Beschreibungs Zeichenfolge mit der erwarteten Konvention übereinstimmt, lädt Windows Media Player den Inhalt herunter.

Sie müssen für jeden Bits-Auftrag nur eine digitale Mediendatei hinzufügen, die heruntergeladen werden soll.

Nachdem Sie einen BITS-Auftrag mithilfe dieser Konvention gestartet haben, müssen Sie Windows Media Player den Auftrag Fertigstellen lassen. Windows Media Player entfernt auch den Auftrag aus der Bits-Warteschlange, verschiebt die heruntergeladene Datei an den Speicherort, an dem die aufgeladene Musik gespeichert wird, und fügt die heruntergeladene Datei der Bibliothek hinzu.

Der *serviceid-* Parameter muss einen 32-Bit-Wert ungleich 0 (null) enthalten. Es wird empfohlen, dass Sie die Funktion " [**cryptgenrandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) " verwenden, um diesen Wert zu erstellen.

Der Dateiname, den Sie mit dem *localname* -Parameter von **ibackgroundcopyjob:: AddFile** angeben, muss die Dateinamenerweiterung. WMA,. WMV,. MP3 oder. ASF aufweisen.

Die übrigen Parameter sind so konzipiert, dass Sie Metadatenwerte enthalten, die sich auf den Inhalt beziehen Sie können diese Werte von der Webseite für den Online Shop abrufen, indem Sie die Datei " **Downloader. getiteminfo**" verwenden. Sie können die korrekte Download Auflistung abrufen, indem Sie **Downloadmanager. getdownloadcollection** aufrufen und *serviceid* als *CollectionId* -Parameter bereitstellen.

Windows Media Player überprüft die Bits-Warteschlange in regelmäßigen Abständen, während der Spieler ausgeführt wird. Um sicherzustellen, dass Windows Media Player die Bits-Warteschlange auf Download Aufträge überprüft, sollten Sie einen Wert im folgenden Registrierungs Unterschlüssel erstellen:

**HKEY \_ Current \_ User \\ Software \\ Microsoft \\ Media Player \\ Services**

Der Wert sollte wie folgt erstellt werden.



| Name                | type      | BESCHREIBUNG                                                                                                                                                                                                          |
|---------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Aktuerfrischendes Download** | **DWORD** | Gibt an, ob Windows Media Player die Bits-Warteschlange auf Download Aufträge prüfen soll. Wenn der Wert 0 (null) ist, wird der Spieler die Bits-Warteschlange nicht untersuchen. Der Player muss die Warteschlange untersuchen, wenn der Wert ungleich 0 (null) ist. |



 

Mit der folgenden alternativen Syntax können Sie BITS-Aufträge hinzufügen, die von Windows Media Player nicht ausgeführt werden, für die jedoch lediglich Statusinformationen angezeigt werden:

``` syntax
::WMP_STATUS:1:serviceId:Provider:AlbumArtist:AlbumTitle:TrackNumber:Title:Duration:Rating
```

Wenn Sie die obige Syntax verwenden, müssen Sie Code schreiben, um den Bits-Download abzuschließen, den Inhalt auf dem Computer des Benutzers zu organisieren und den Inhalt bei Bedarf der Bibliothek hinzuzufügen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Cryptgenrandom verwendet](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom)
</dt> <dt>

[**Download Element. getiteminfo**](downloaditem-getiteminfo.md)
</dt> <dt>

[**Download Manager. getdownloadcollection**](downloadmanager-getdownloadcollection.md)
</dt> <dt>

[**Referenz für Typ 2-Onlineshops**](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 