---
description: Registrieren des Kontextmenühandlers
ms.assetid: 0023004b-b6b3-486a-8b8c-8e63c5731206
title: Registrieren des Kontextmenühandlers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 027e01d4b3bc58727579b77345d3f1b8eed668e5b858e49eb4859a40db9ad2d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083544"
---
# <a name="registering-your-context-menu-handler"></a>Registrieren des Kontextmenühandlers

Damit Ihr Kontextmenühandler vom WPD-Namespace erkannt wird, müssen Sie ihn ordnungsgemäß in der Windows registrieren. Die Registrierungseinträge für einen WPD-Kontextmenühandler ähneln denen für die Shell, werden jedoch als spezielle Dateitypen registriert. WPD-Kontextmenühandler werden entsprechend dem Inhaltstyp registriert, den sie darstellen. Im Folgenden finden Sie eine Beispielregistrierungsstruktur für einen WPD-Kontextmenühandler:


```C++
HKEY_CLASSES_ROOT
 \-- WPDContextMenu.Image
      \-- shellex
           \-- ContextMenuHandlers
                \-- ShImageViewer (Default)  REG_SZ {E847DA7C-1D6A-45F6-B725-CB260C236066}

```



Im obigen Beispiel wird der Shellbild-Viewer beim WPD-Namespace registriert. Wenn ein Benutzer über die Vista Windows-Shell mit der rechten Maustaste auf inhalte eines Geräts klickt oder darauf doppelklickt, ruft er diesen Kontextmenühandler auf. Der WPD-Namespace verwendet WPD \_ CONTENT \_ TYPE, um zu bestimmen, welche Kontextmenühandler geladen werden. Wenn WPD CONTENT TYPE gleich \_ \_ WPD \_ CONTENT TYPE \_ \_ UNSPECIFIED, WPD CONTENT TYPE GENERIC FILE oder \_ \_ WPD CONTENT TYPE PROGRAM \_ ist, \_ \_ \_ versucht der \_ WPD-Namespace, die beste Übereinstimmung basierend auf der Erweiterung der ausgewählten Datei zu finden. Wenn weder die Dateierweiterung noch der Inhaltstyp eine nützliche Klassifizierung bietet, werden die Kontextmenühandler vom WPD-Namespace unter dem **Registrierungsschlüssel WPDContextMenu.Generic** geladen. In der folgenden Tabelle sind alle Dateiklassen aufgeführt, die für einen Kontextmenühandler verfügbar sind und welche Inhaltstypen und Dateierweiterungen sie darstellen:



| Registrierungsschlüssel                           | WPD-Inhaltstyp                                                                                               | Dateierweiterung                                                                                           |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| **WPDContextMenu.Device**              | Die Registrierung unter diesem Schlüssel ermöglicht Ihren Kontextmenühandler auf Geräteebene. (Klicken Sie mit der rechten Maustaste auf ein Gerät.)   | (Nicht zutreffend)                                                                                                    |
| **WPDContextMenu. Storage**             | Durch die Registrierung unter diesem Schlüssel wird Ihr Kontextmenühandler auf Speicherebene aktiviert. (Klicken Sie mit der rechten Maustaste auf einen Speicher.) | (Nicht zutreffend)                                                                                                    |
| **WPDContextMenu.Folder**              | \_ \_ WPD-INHALTSTYPORDNER \_                                                                                     | (Nicht zutreffend)                                                                                                    |
| **WPDContextMenu.Image**               | \_ \_ WPD-INHALTSTYPBILD \_                                                                                      | BMP <br/> .gif <br/> .png <br/> .jpg <br/> JPE <br/> JPEG <br/>   |
| **WPDContextMenu.Audio**               | WPD \_ CONTENT \_ TYPE \_ AUDIO                                                                                      | AIFF <br/> .mp3 <br/> WAV <br/> .wma <br/>                                     |
| **WPDContextMenu.Video**               | WPD \_ CONTENT \_ TYPE \_ VIDEO                                                                                      | .asf<br/> AVI <br/> .dvr-ms <br/> .mpeg <br/> .mpg <br/> .wmv <br/> |
| **WPDContextMenu.Playlist**<br/> | WIEDERGABELISTE DES \_ \_ WPD-INHALTSTYPS \_                                                                                   | WPL <br/> .m3u <br/> MPL <br/> .asx <br/> PLS <br/>                     |
| **WPDContextMenu.Document**            | \_ \_ WPD-INHALTSTYPDOKUMENT \_                                                                                   | .doc <br/> .txt <br/> .rtf <br/> .xls <br/> .ppt <br/>                     |
| **WPDContextMenu.Contact**<br/>  | WPD \_ CONTENT \_ TYPE \_ CONTACT                                                                                    | Keine                                                                                                     |
| **WPDContextMenu.Email**               | \_WPD-INHALTSTYP \_ \_ E-MAIL                                                                                      | Keine                                                                                                     |
| **WPDContextMenu.Appointment**         | WPD \_ CONTENT \_ TYPE \_ APPOINTMENT                                                                                | Keine                                                                                                     |
| **WPDContextMenu.Task**                | \_ \_ WPD-INHALTSTYPAUFGABE \_                                                                                       | Keine                                                                                                     |
| **WPDContextMenu.Memo**                | \_ \_ WPD-INHALTSTYP \_ MEMO                                                                                       | Keine                                                                                                     |
| **WPDContextMenu.Image Eigenschaft**          | WPD \_ CONTENT \_ TYPE \_ IMAGE \_ ALBUM                                                                               | Keine                                                                                                     |
| **WPDContextMenu.Audio Eigenschaft**          | WPD \_ CONTENT \_ TYPE \_ AUDIO \_ ALBUM                                                                               | Keine                                                                                                     |
| **WPDContextMenu.VideoKonferenz**          | WPD \_ CONTENT \_ TYPE \_ VIDEO \_ ALBUM                                                                               | Keine                                                                                                     |
| **WPDContextMenu.MixedMix**          | WPD \_ CONTENT \_ TYPE \_ MIXED \_ CONTENT \_ ALBUM                                                                      | Keine                                                                                                     |
| **WPDContextMenu.Generic**             | \_ \_ WPD-INHALTSTYP \_ NICHT ANGEGEBEN                                                                                | Alle anderen Dateierweiterungen                                                                                |



 

 

 




