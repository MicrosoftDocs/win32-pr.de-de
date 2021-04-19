---
description: In der folgenden Tabelle werden COM-Objekte und Schnittstellen aufgelistet, die den Rendezvous-Konferenz Steuerelementen zugeordnet sind
ms.assetid: d9634586-8315-46d3-9ffc-bfa9a4d7738e
title: Rendezvous com-Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6df7fbdac45480ae7aa9d5968209f22fabe9a4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362460"
---
# <a name="rendezvous-com-interfaces"></a>Rendezvous com-Schnittstellen

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

In der folgenden Tabelle werden COM-Objekte und Schnittstellen aufgelistet, die den Rendezvous-Konferenz Steuerelementen zugeordnet sind

Weitere Informationen zum Component Object Model (com) finden Sie in den entsprechenden Abschnitten im Platform Software Development Kit (SDK).



| Schnittstellen                                                         | BESCHREIBUNG                                                                                                               |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**Ienumdialableaddrs**](/windows/desktop/api/Rend/nn-rend-ienumdialableaddrs)                   | Listet die im aktuellen Verzeichnis verfügbaren, nicht verfügbaren Adressen auf.                                                     |
| [**Ienumdirectory**](/windows/desktop/api/Rend/nn-rend-ienumdirectory)                           | Listet [**itdirectory**](/windows/desktop/api/Rend/nn-rend-itdirectory) -Objekte auf.                                                                    |
| [**Ienumdirectoryobject**](/windows/desktop/api/Rend/nn-rend-ienumdirectoryobject)               | Listet [**itdirectoryobject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject) -Objekte auf.                                                        |
| [**Ienummcastscope**](/windows/desktop/api/Mdhcp/nn-mdhcp-ienummcastscope)                         | Listet [**imcastscope**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastscope) -Objekte auf.                                                                    |
| [**Ienummedia**](ienummedia.md)                                   | Listet [**ITmedia**](itmedia.md) -Objekte auf.                                                                            |
| [**Ienumtime**](ienumtime.md)                                     | Listet [**ittime**](ittime.md) -Objekte auf.                                                                              |
| [**Imcastaddressallocation**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastaddressallocation)         | Hauptschnittstelle für COM-Wrapper der Multicast Adress Zuordnung.                                                           |
| [**Imcastleaseinfo**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastleaseinfo)                         | Stellt Methoden zum Abrufen und Festlegen von Adressleaseinformationen bereit.                                                           |
| [**Imcastscope**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastscope)                                 | Kapselt alle Eigenschaften eines Multicast Bereichs und stellt Methoden bereit, um Informationen über den Bereich zu erhalten.             |
| [**Itattributelist**](itattributelist.md)                         | Ermöglicht das erhalten und Festlegen von nicht interpretierten Attributen.                                                                   |
| [**Itconfererceblob**](itconferenceblob.md)                       | Bietet Zugriff auf anbieterspezifische Konferenz Informationen.                                                              |
| [**Itconnection**](itconnection.md)                               | Bietet Methoden zum Bearbeiten von Verbindungs Faktoren wie Konferenz Adresse, Bereich und Bandbreite.                       |
| [**Itdirectory**](/windows/desktop/api/Rend/nn-rend-itdirectory)                                 | Dient zum Abrufen und Festlegen von Verzeichnisinformationen und ermöglicht den Zugriff auf ein bestimmtes Verzeichnis Objekt.                                |
| [**Itdirectoryobject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject)                     | Ruft generische Informationen für eine Konferenz oder einen Benutzer in einem Verzeichnis ab und legt Sie fest.                                            |
| [**Itdirectoryobjectconference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference) | Dient zum Abrufen und Festlegen allgemeiner spezifischer Informationen für eine Konferenz, z. b. Start-und Endzeit.                                 |
| [**Itdirecteryobjectuser**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectuser)             | Dient zum Abrufen und Festlegen allgemeiner spezifischer Informationen für einen Benutzer, z. b. den Namen eines Computers, bei dem es sich um das primäre IP-Telefon des Benutzers handelt. |
| [**Itilsconfig**](/windows/desktop/api/Rend/nn-rend-itilsconfig)                                 | Dient zum Abrufen und Festlegen von Informationen, die für den Server eines bestimmten ILS-Verzeichnisses spezifisch sind.                                                |
| [**ITmedia**](itmedia.md)                                         | Dient zum Abrufen und Festlegen grundlegender Medien Eigenschaften, z. b. Medien Name und Transportprotokoll.                                       |
| [**Itmediacollection**](itmediacollection.md)                     | Ermöglicht den Medien Zugriff nach Index. Ermöglicht das Erstellen und Löschen von Medien.                                                     |
| [**Itrendezvous**](/windows/desktop/api/Rend/nn-rend-itrendezvous)                               | Hauptschnittstelle für das Rendezvous-Steuerelement.                                                                                |
| [**Itsdp**](itsdp.md)                                             | Bearbeitet das SDP-BLOB (Sitzungs Beschreibungs Protokoll). Referenz: RFC 2327.                                             |
| [**Ittime**](ittime.md)                                           | Ermöglicht den Zugriff auf einen Satz von Aktivierungs Zeiten für die Sitzung.                                                             |
| [**Ittimecollection**](ittimecollection.md)                       | Ermöglicht den Zeit Komponenten Zugriff nach Index. Ermöglicht das Erstellen und Löschen von Zeit Komponenten.                                  |



 

 

 



