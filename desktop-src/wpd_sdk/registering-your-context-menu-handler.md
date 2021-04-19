---
description: Registrieren Ihres Kontextmenü Handlers
ms.assetid: 0023004b-b6b3-486a-8b8c-8e63c5731206
title: Registrieren Ihres Kontextmenü Handlers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aafd2798683b4bc291653bca34996f143fc36842
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348713"
---
# <a name="registering-your-context-menu-handler"></a>Registrieren Ihres Kontextmenü Handlers

Damit der Kontextmenü Handler vom WPD-Namespace erkannt werden kann, müssen Sie ihn ordnungsgemäß in der Windows-Registrierung registrieren. Die Registrierungseinträge für einen WPD-Kontextmenü Handler ähneln denen für die Shell, aber Sie werden als spezielle Dateitypen registriert. WPD-Kontextmenü Handler werden gemäß dem Inhaltstyp, den Sie darstellen, registriert. Im folgenden finden Sie eine Beispiel Registrierungs Struktur für einen WPD-Kontextmenü Handler:


```C++
HKEY_CLASSES_ROOT
 \-- WPDContextMenu.Image
      \-- shellex
           \-- ContextMenuHandlers
                \-- ShImageViewer (Default)  REG_SZ {E847DA7C-1D6A-45F6-B725-CB260C236066}

```



Im obigen Beispiel wird die Shell Image Viewer mit dem WPD-Namespace registriert. Wenn ein Benutzer mit der rechten Maustaste auf den Inhalt eines Geräts über die Windows Vista-Shell klickt oder darauf klickt, wird dieser Kontextmenü Handler aufgerufen. Der WPD-Namespace verwendet den WPD- \_ \_ Inhaltstyp, um zu bestimmen, welche Kontextmenü Handler geladen werden sollen. Wenn der WPD- \_ \_ Inhaltstyp mit dem WPD-Inhaltstyp \_ \_ \_ nicht angegeben, dem WPD- \_ \_ Inhaltstyp \_ generic \_ File oder dem WPD- \_ \_ Inhaltstyp \_ Programm übereinstimmt, versucht der WPD-Namespace, die beste Übereinstimmung basierend auf der Erweiterung der ausgewählten Datei zu finden. Wenn weder die Dateierweiterung noch der Inhaltstyp eine sinnvolle Klassifizierung bereitstellt, lädt der WPD-Namespace die Kontextmenü Handler unter dem Registrierungsschlüssel " **wpdcontextmenu. Generic** ". In der folgenden Tabelle sind alle Datei Klassen aufgelistet, die für einen Kontextmenü Handler verfügbar sind, und welche Inhaltstypen und Dateierweiterungen Sie darstellen:



| Registrierungsschlüssel                           | WPD-Inhaltstyp                                                                                               | Dateierweiterung                                                                                           |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| **Wpdcontextmenu. Device**              | Durch die Registrierung unter diesem Schlüssel wird der Kontextmenü Handler auf Geräteebene aktiviert. (Klicken Sie mit der rechten Maustaste auf ein Gerät.)   | (Nicht zutreffend)                                                                                                    |
| **Wpdcontextmenu. Storage**             | Wenn Sie unter diesem Schlüssel registrieren, wird der Kontextmenü Handler auf der Speicher Ebene aktiviert. (Klicken Sie mit der rechten Maustaste auf einen Speicher.) | (Nicht zutreffend)                                                                                                    |
| **Wpdcontextmenu. Folder**              | Ordner für WPD- \_ \_ Inhaltstyp \_                                                                                     | (Nicht zutreffend)                                                                                                    |
| **Wpdcontextmenu. Image**               | Bild für WPD- \_ \_ Inhaltstyp \_                                                                                      | BMP <br/> .gif <br/> .png <br/> .jpg <br/> JPE <br/> JPEG <br/>   |
| **Wpdcontextmenu. Audiodatei**               | WPD \_ \_ -Inhaltstyp \_ Audiodatei                                                                                      | AIFF <br/> .mp3 <br/> WAV <br/> .wma <br/>                                     |
| **Wpdcontextmenu. Video**               | Video zum WPD- \_ \_ Inhaltstyp \_                                                                                      | .asf<br/> AVI <br/> . DVR-MS <br/> . MPEG <br/> .mpg <br/> .wmv <br/> |
| **Wpdcontextmenu. Wiedergabeliste**<br/> | WPD \_ - \_ Inhaltstyp \_ Wiedergabeliste                                                                                   | WPL <br/> .m3u <br/> . mpl <br/> .asx <br/> . pls <br/>                     |
| **WPDContextMenu.Doc-übergeordneten**            | Dokument für WPD- \_ \_ Inhaltstyp \_                                                                                   | .doc <br/> .txt <br/> .rtf <br/> .xls <br/> .ppt <br/>                     |
| **Wpdcontextmenu. Contact**<br/>  | Kontakt zum WPD- \_ \_ Inhaltstyp \_                                                                                    | Keine                                                                                                     |
| **WPDContextMenu.Email**               | e-Mail zum WPD \_ \_ -Inhaltstyp \_                                                                                      | Keine                                                                                                     |
| **Wpdcontextmenu. Termin**         | WPD \_ - \_ Inhaltstyp \_ Termin                                                                                | Keine                                                                                                     |
| **Wpdcontextmenu. Task**                | WPD \_ - \_ Inhaltstyp \_ Aufgabe                                                                                       | Keine                                                                                                     |
| **Wpdcontextmenu. Memo**                | WPD \_ - \_ Inhaltstyp \_ Memo                                                                                       | Keine                                                                                                     |
| **Wpdcontextmenu. imagealbum**          | Bild-Album für WPD- \_ \_ Inhaltstyp \_ \_                                                                               | Keine                                                                                                     |
| **Wpdcontextmenu. Audioalbum**          | Audioalbum für WPD \_ \_ -Inhaltstyp \_ \_                                                                               | Keine                                                                                                     |
| **Wpdcontextmenu. Videoalbum**          | Video zum WPD- \_ \_ Inhaltstyp \_ \_                                                                               | Keine                                                                                                     |
| **Wpdcontextmenu. mixedalbum**          | WPD \_ - \_ Inhaltstyp \_ gemischtes \_ Inhalts \_ Album                                                                      | Keine                                                                                                     |
| **Wpdcontextmenu. Generic**             | WPD \_ - \_ Inhaltstyp \_ nicht angegeben                                                                                | Alle anderen Dateierweiterungen                                                                                |



 

 

 




