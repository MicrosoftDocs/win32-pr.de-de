---
description: Registrieren des Eigenschaften Blatt Handlers
ms.assetid: 6621529c-717b-4f36-8d9e-769d6b720b8a
title: Registrieren des Eigenschaften Blatt Handlers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6a59a03ebd13f5a541674012da7b07045e0a510
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358575"
---
# <a name="registering-your-property-sheet-handler"></a>Registrieren des Eigenschaften Blatt Handlers

Damit der Eigenschaften Blatt Handler vom WPD-Namespace erkannt werden kann, müssen Sie ihn ordnungsgemäß in der Windows-Registrierung registrieren. Die Registrierungseinträge für einen WPD-Eigenschaften Blatt Handler ähneln denen für die Shell, aber Sie werden als spezielle Dateitypen registriert. WPD-Eigenschaften Blatt Handler werden gemäß dem Inhaltstyp, den Sie darstellen, registriert. Im folgenden finden Sie eine Beispiel Registrierungs Struktur für einen WPD-Kontextmenü Handler:


```C++
HKEY_CLASSES_ROOT
 \-- WPDPropSheet.Image
      \-- shellex
           \-- PropertySheetHandlers
                \-- MyHandler (Default)  REG_SZ {0000000-0000-0000-0000-000000000000}

```



Im obigen Beispiel wird ein benutzerdefinierter Handler beim WPD-Namespace registriert. Wenn ein Benutzer mit der rechten Maustaste auf eine Bilddatei auf einem Gerät über die Windows-Shell klickt und Eigenschaften auswählt, wird dieser **Eigenschaften** Blatt Handler aufgerufen. Der WPD-Namespace verwendet den WPD- \_ \_ Inhaltstyp, um zu bestimmen, welche Eigenschaften Blatt Handler geladen werden sollen. Wenn der Inhaltstyp keine nützliche Klassifizierung bietet, lädt der Namespace die Eigenschaften Blatt Handler unter dem Registrierungsschlüssel " **wpdpropsheet. Generic** ". In der folgenden Tabelle sind alle Datei Klassen aufgelistet, die für einen Kontextmenü Handler verfügbar sind, und welche Inhaltstypen und Dateierweiterungen Sie darstellen.



| Registrierungsschlüssel                   | WPD-Inhaltstyp                                                                                                               |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| **Wpdcontextmenu. Device**      | Durch die Registrierung unter diesem Schlüssel wird der Kontextmenü Handler auf Geräteebene aktiviert. (Klicken Sie mit der rechten Maustaste auf ein Gerät.)                   |
| **Wpdcontextmenu. Storage**     | Wenn Sie unter diesem Schlüssel registrieren, wird der Kontextmenü Handler auf der Speicher Ebene aktiviert. (Klicken Sie mit der rechten Maustaste auf einen Speicher.)                 |
| **Wpdcontextmenu. Folder**      | Ordner für WPD- \_ \_ Inhaltstyp \_                                                                                                     |
| **Wpdcontextmenu. Image**       | Bild für WPD- \_ \_ Inhaltstyp \_                                                                                                      |
| **Wpdcontextmenu. Audiodatei**       | WPD \_ \_ -Inhaltstyp \_ Audiodatei                                                                                                      |
| **Wpdcontextmenu. Video**       | Video zum WPD- \_ \_ Inhaltstyp \_                                                                                                      |
| **Wpdcontextmenu. Wiedergabeliste**    | WPD \_ - \_ Inhaltstyp \_ Wiedergabeliste                                                                                                   |
| **WPDContextMenu.Doc-übergeordneten**    | Dokument für WPD- \_ \_ Inhaltstyp \_                                                                                                   |
| **Wpdcontextmenu. Contact**     | Kontakt zum WPD- \_ \_ Inhaltstyp \_                                                                                                    |
| **WPDContextMenu.Email**       | e-Mail zum WPD \_ \_ -Inhaltstyp \_                                                                                                      |
| **Wpdcontextmenu. Termin** | WPD \_ - \_ Inhaltstyp \_ Termin                                                                                                |
| **Wpdcontextmenu. Task**        | WPD \_ - \_ Inhaltstyp \_ Aufgabe                                                                                                       |
| **Wpdcontextmenu. Memo**        | WPD \_ - \_ Inhaltstyp \_ Memo                                                                                                       |
| **Wpdcontextmenu. imagealbum**  | Bild-Album für WPD- \_ \_ Inhaltstyp \_ \_                                                                                               |
| **Wpdcontextmenu. Audioalbum**  | Audioalbum für WPD \_ \_ -Inhaltstyp \_ \_                                                                                               |
| **Wpdcontextmenu. Videoalbum**  | Video zum WPD- \_ \_ Inhaltstyp \_ \_                                                                                               |
| **Wpdcontextmenu. mixedalbum**  | WPD \_ - \_ Inhaltstyp \_ gemischtes \_ Inhalts \_ Album                                                                                      |
| **Wpdcontextmenu. Generic**     | WPD \_ - \_ Inhaltstyp \_ nicht angegeben<br/> generische Datei für WPD- \_ \_ Inhaltstyp \_ \_<br/> WPD \_ - \_ Inhaltstyp \_ Programm<br/> |



 

 

 




