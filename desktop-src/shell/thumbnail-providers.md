---
description: Windows Vista nutzt Datei spezifische Miniaturbilder besser als frühere Versionen von Windows.
title: Miniatur Ansichts Handler
ms.topic: article
ms.date: 07/02/2018
ms.assetid: ed9e17bb-aa28-4f8c-8b5a-9b57cab1c438
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d81accf59401a46dd6b5611e15a67eeec68d5d82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217685"
---
# <a name="thumbnail-handlers"></a>Miniatur Ansichts Handler

Windows Vista nutzt Datei spezifische Miniaturbilder besser als frühere Versionen von Windows. Windows Vista verwendet diese in allen Ansichten, in Dialogfeldern und für jeden Dateityp, der Sie bereitstellt. Andere Anwendungen können auch die Miniaturansicht nutzen. Die Miniaturansicht wurde ebenfalls geändert. Nun ist ein kontinuierliches Spektrum von Benutzer auswählbaren Größen verfügbar, und nicht die diskreten Größen wie Symbole und Miniaturansichten, die in Windows XP bereitgestellt werden.

> [!Note]  
> Diese Miniaturansichten werden möglicherweise als Live-Symbole bezeichnet.

 

Miniaturansichten der 32-Bit-Auflösung und so groß wie 256 x 256 Pixel werden häufig in der Windows Vista-Benutzeroberfläche verwendet. Besitzer des Datei Formats sollten darauf vorbereitet sein, die Miniaturansichten in dieser Größe anzuzeigen. Sie sollten außerdem nicht statische Bilder für Ihre Miniaturansichten bereitstellen, die den Inhalt der jeweiligen Datei widerspiegeln. Beispielsweise sollte die Miniaturansicht einer Textdatei eine Miniaturversion des Dokuments, einschließlich des Texts, anzeigen.

Die [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) -Schnittstelle wurde eingeführt, um das Bereitstellen einer Miniaturansicht zu vereinfachen und einfacher als in der Vergangenheit, wenn stattdessen [**iextractimage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) verwendet worden wäre. Beachten Sie, dass vorhandener Code, der **iextractimage** verwendet, weiterhin unter Windows Vista gültig ist. **Iextractimage** wird jedoch im **Detail** Bereich nicht unterstützt.

In diesem Thema wird Folgendes erörtert:

-   [Miniatur Ansichts Prozesse](#thumbnail-processes)
-   [Miniatur Ansichts Cache und Größenanpassung](#thumbnail-cache-and-sizing)
-   [Miniaturansichten Überlagerungen](#thumbnail-overlays)
-   [Miniatur Ansichts Zusatzelemente](#thumbnail-adornments)
-   [Registrieren des Miniatur Ansichts Handlers](#registering-your-thumbnail-handler)
-   [Zugehörige Themen](#related-topics)

## <a name="thumbnail-processes"></a>Miniatur Ansichts Prozesse

Handler, einschließlich Miniatur Ansichts Handler, werden standardmäßig in einem separaten Prozess ausgeführt. Sie können erzwingen, dass der Handler Prozess seitig ausgeführt wird, indem Sie einen **null** -Wert als Bindungs Kontext in einem Aufrufen von [**IShellItem:: bindtohandler**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler) übergeben, wie hier gezeigt:


```
IShellItem::BindToHandler(NULL, BHID_ThumbnailHandler,..)
```



Sie können auch die Ausführung des Out-of-Process-Vorgangs deaktivieren, indem Sie den Eintrag disableprocessisolations in der Registrierung festlegen, wie in diesem Beispiel gezeigt. Der Klassen Bezeichner (CLSID) {E357FCCD-A995-4576-B01F-234630154E96} ist die CLSID für [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) -Implementierungen.

```
HKEY_CLASSES_ROOT
   CLSID
      {E357FCCD-A995-4576-B01F-234630154E96}
         DisableProcessIsolation = 1
```

## <a name="thumbnail-cache-and-sizing"></a>Miniatur Ansichts Cache und Größenanpassung

Wenn eine Miniaturansicht erforderlich ist, prüft Windows zuerst den Miniatur Ansichts Cache auf das Bild. Der Miniatur Ansichts Extraktor wird aufgerufen, wenn das Bild nicht im Cache gefunden wurde. Sie wird auch aufgerufen, wenn der Zeitpunkt der letzten Änderung des Bilds später ist als der der Kopie im Cache.

Die Miniaturbilder in diesem Cache werden in einem Satz diskreter Größen gespeichert. Alle Größen werden in Pixel angegeben.

-   32 x 32
-   96 x 96
-   256x256
-   1024 x 1024

> [!Note]  
> Diese Werte können geändert werden. Sie sollten nicht davon ausgehen, dass eine bestimmte Größe immer verwendet wird.

 

Wenn ein Bild nicht quadratisch ist, sollten Sie es nicht selbst auffüllen. Windows ist dafür verantwortlich, das ursprüngliche Seitenverhältnis zu berücksichtigen und das Bild auf eine quadratische Größe aufzusetzen.

Wenn ein Image einer bestimmten Größe angefordert wird, ruft Windows Vista immer das nächste größte Bild ab und skaliert es auf die angeforderte Größe, sofern keine genaue Entsprechung gefunden wird. Ein Bild wird nie in der Größe zentral hochskaliert, wie es in früheren Versionen von Windows der Fall war.

In der folgenden Tabelle sind einige Beispiele für die Beziehung zwischen angeforderter Größe und verfügbarer Größe angegeben.



| Maximale Image Größe, die Sie bereitstellen | Vom Extraktor angeforderte Größe | Sie stellen                                 |
|--------------------------------|---------------------------------|---------------------------------------------|
| 156 x 120                        | 256x256                         | 156x120 (nicht auffüllen, Seitenverhältnis beibehalten) |
| 2048x1024                      | 256x256                         | Größe 256x128 (nicht auffüllen, Seitenverhältnis beibehalten) |



 

Sie können einen Umstellungs Punkt als Teil des Programm-ID-Eintrags der zugeordneten app in der Registrierung deklarieren. Unter dieser Größe werden keine Miniaturansichten verwendet.

```
HKEY_CLASSES_ROOT
   .{ProgId}
      ThumbnailCutoff
```

Der thumbnailcuumff-Eintrag ist einer dieser reg \_ DWORD-Werte.

| Wert | Umstellungs | Hohe dpi-Zeichen |
|-------|--------|-------------------|
| 0     | 32 x 32  | Ja               |
| 1     | 16 x 16  | Ja               |
| 2     | 48x48  | Ja               |
| 3     | 16 x 16  | Ja               |


Die Unterscheidung nach "High dots per inch" (dpi) bedeutet, dass die Pixel Dimensionen der Miniaturansicht automatisch für den größeren dpi-Wert angepasst werden. Beispielsweise wäre ein 32 x 32-Bild bei 96 dpi ein 40 x 40-Bild bei 120 dpi.

Wenn der thumbnailcuumff-Eintrag nicht angegeben wird, ist der Standardwert für "20x20" (nicht dpi-sensibel).

## <a name="thumbnail-overlays"></a>Miniaturansichten Überlagerungen

Miniaturansichten, ein kleines Bild, das in der unteren rechten Ecke der Miniaturansicht angezeigt wird, bieten Entwicklern die Möglichkeit, Marken Identifizierung auf Ihre Miniaturansichten anzuwenden. Überlagerungen werden in der Registrierung als Teil des Programm-ID-Eintrags der zugeordneten App deklariert, wie hier gezeigt:

```
HKEY_CLASSES_ROOT
   .{ProgId}
      TypeOverlay
```

Der typeoverlay-Eintrag enthält einen REG SZ-Wert, der \_ wie folgt interpretiert wird:

-   Wenn es sich bei dem Wert um einen Ressourcen Verweis (eine in die DLL eingebettete **ICO** -Datei) wie handelt `ISVComponent.dll,-155` , wird dieses Bild als Überlagerung für Dateien mit dieser Dateinamenerweiterung verwendet. Beachten Sie, dass in diesem Beispiel **155** die Ressourcen-ID ist, und wenn die dll in einem Standardpfad (z. **b. C:/Windows/System32**) nicht vorhanden ist, ist anstelle des DLL-namens der vollständige Pfad erforderlich.
-   Wenn der Wert eine leere Zeichenfolge ist, wird kein Overlay auf das Bild angewendet.
-   Wenn der Wert nicht vorhanden ist, wird das Standard Symbol der zugeordneten Anwendung verwendet.

Überlagerungen für Ihre Miniaturansichten sollten nur über diesen Mechanismus bereitgestellt und von Windows angewendet werden. Wenden Sie keine Überlagerungen selbst an.

## <a name="thumbnail-adornments"></a>Miniatur Ansichts Zusatzelemente

Zusatzelemente, wie z. b. Schlag Schatten, werden auf Miniaturansichten basierend auf dem aktuell ausgewählten Design des Benutzers angewendet. Zusatzelemente werden von Windows bereitgestellt. Erstellen Sie diese nicht selbst. Windows könnte das Aussehen bestimmter Zusatzelemente jederzeit ändern. Wenn Sie also eine eigene Ausgabe bereitgestellt haben, würden Sie mit dem System nicht synchron sein. Ihre Miniaturansichten können nach unten oder außerhalb des Orts angezeigt werden.

Potenzielle Zusatzelemente werden in der Registrierung als Teil des Programm-ID-Eintrags der zugeordneten App deklariert, wie hier gezeigt:

```
HKEY_CLASSES_ROOT
   .{ProgId}
      Treatment
```

Der Behandlungs Eintrag enthält einen der folgenden reg \_ DWORD-Werte:



| Wert | Bedeutung         |
|-------|-----------------|
| 0     | Kein Zusatzelement    |
| 1     | Schatten     |
| 2     | Fotorahmen    |
| 3     | Video Sprockets |


Standardmäßig wird ein Schlag Schatten auf Bilder angewendet.

## <a name="registering-your-thumbnail-handler"></a>Registrieren des Miniatur Ansichts Handlers

Die Registrierung eines Miniatur Ansichts Handlers basiert auf standardmäßigen Dateizuordnungen.

Die GUID für die Miniatur Ansichts Handler-Shellerweiterung ist `E357FCCD-A995-4576-B01F-234630154E96` .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider)
</dt> <dt>

[Entwickeln von Miniatur Ansichts Handlern](building-thumbnail-providers.md)
</dt> <dt>

[Richtlinien für Miniaturansichten](thumbnail-provider-guidelines.md)
</dt> </dl>

 

 



