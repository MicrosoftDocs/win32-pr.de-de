---
description: Registrieren des Eigenschaftenblatthandlers
ms.assetid: 6621529c-717b-4f36-8d9e-769d6b720b8a
title: Registrieren des Eigenschaftenblatthandlers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91f1642c03a068a24b37cd5647bcdef63222ed2dbe5d78832daeea31e8abd67d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083534"
---
# <a name="registering-your-property-sheet-handler"></a>Registrieren des Eigenschaftenblatthandlers

Damit ihr Eigenschaftenblatthandler vom WPD-Namespace erkannt wird, müssen Sie ihn ordnungsgemäß in der Windows-Registrierung registrieren. Die Registrierungseinträge für einen WPD-Eigenschaftenblatthandler ähneln denen für die Shell, werden jedoch als spezielle Dateitypen registriert. WPD-Eigenschaftenblatthandler werden entsprechend dem inhaltstyp registriert, den sie darstellen. Im Folgenden finden Sie eine Beispielregistrierungsstruktur für einen WPD-Kontextmenühandler:


```C++
HKEY_CLASSES_ROOT
 \-- WPDPropSheet.Image
      \-- shellex
           \-- PropertySheetHandlers
                \-- MyHandler (Default)  REG_SZ {0000000-0000-0000-0000-000000000000}

```



Im obigen Beispiel wird ein benutzerdefinierter Handler beim WPD-Namespace registriert. Wenn ein Benutzer über die Windows Shell mit der rechten Maustaste auf eine Bilddatei auf einem Gerät klickt und **Eigenschaften** auswählt, wird dieser Eigenschaftenblatthandler aufgerufen. Der WPD-Namespace verwendet den WPD \_ CONTENT \_ TYPE, um zu bestimmen, welche Eigenschaftenblatthandler geladen werden sollen. Wenn der Inhaltstyp keine nützliche Klassifizierung bereitstellt, lädt der Namespace die Eigenschaftenblatthandler unter dem **Registrierungsschlüssel WPDPropSheet.Generic.** In der folgenden Tabelle sind alle Dateiklassen aufgeführt, die einem Kontextmenühandler zur Verfügung stehen, und welche Inhaltstypen und Dateierweiterungen sie darstellen.



| Registrierungsschlüssel                   | WPD-Inhaltstyp                                                                                                               |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| **WPDContextMenu.Device**      | Die Registrierung unter diesem Schlüssel aktiviert den Kontextmenühandler auf Geräteebene. (Klicken Sie mit der rechten Maustaste auf ein Gerät.)                   |
| **WPDContextMenu. Storage**     | Die Registrierung unter diesem Schlüssel aktiviert den Kontextmenühandler auf Speicherebene. (Klicken Sie mit der rechten Maustaste auf einen Speicher.)                 |
| **WPDContextMenu.Folder**      | \_ \_ \_ WPD-INHALTSTYPORDNER                                                                                                     |
| **WPDContextMenu.Image**       | BILD \_ DES WPD-INHALTSTYPS \_ \_                                                                                                      |
| **WPDContextMenu.Audio**       | \_WPD-INHALTSTYP \_ \_ AUDIO                                                                                                      |
| **WPDContextMenu.Video**       | VIDEO \_ ZUM WPD-INHALTSTYP \_ \_                                                                                                      |
| **WPDContextMenu.Playlist**    | \_WIEDERGABELISTE DES WPD-INHALTSTYPS \_ \_                                                                                                   |
| **WPDContextMenu.Document**    | \_ \_ \_ WPD-INHALTSTYPDOKUMENT                                                                                                   |
| **WPDContextMenu.Contact**     | \_WPD-INHALTSTYP \_ \_ KONTAKT                                                                                                    |
| **WPDContextMenu.Email**       | \_WPD-INHALTSTYP \_ \_ E-MAIL                                                                                                      |
| **WPDContextMenu.Appointment** | WPD \_ CONTENT \_ TYPE \_ APPOINTMENT                                                                                                |
| **WPDContextMenu.Task**        | \_ \_ WPD-INHALTSTYPTASK \_                                                                                                       |
| **WPDContextMenu.Memo**        | WPD \_ CONTENT \_ TYPE \_ MEMO                                                                                                       |
| **WPDContextMenu.ImageDaten**  | WPD \_ CONTENT \_ TYPE \_ IMAGE \_ ALBUM                                                                                               |
| **WPDContextMenu.AudioDaten**  | WPD \_ CONTENT \_ TYPE \_ AUDIO \_ ALBUM                                                                                               |
| **WPDContextMenu.VideoDatenträger**  | WPD \_ CONTENT \_ TYPE \_ VIDEO \_ ALBUM                                                                                               |
| **WPDContextMenu.MixedEinander**  | WPD \_ CONTENT \_ TYPE \_ MIXED \_ CONTENT \_ ALBUM                                                                                      |
| **WPDContextMenu.Generic**     | \_WPD-INHALTSTYP \_ \_ NICHT ANGEGEBEN<br/> GENERISCHE \_ \_ \_ WPD-INHALTSTYPDATEI \_<br/> \_ \_ WPD-INHALTSTYPPROGRAMM \_<br/> |



 

 

 




