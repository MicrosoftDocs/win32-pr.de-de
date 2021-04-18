---
description: Das Windows-Sicherheitsmodell ermöglicht es Ihnen, den Zugriff auf Datei Zuordnungsobjekte zu steuern. Weitere Informationen finden Sie unter Access-Control Modell.
ms.assetid: 8bbf7c98-ff83-4ed9-8b82-f08dcd31295c
title: Sicherheit und Zugriffsrechte für die Datei Zuordnung
ms.topic: article
ms.date: 10/06/2018
ms.openlocfilehash: 65d520e12d1b555e7c633f0d1e0ba5142c330ce8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347145"
---
# <a name="file-mapping-security-and-access-rights"></a>Sicherheit und Zugriffsrechte für die Datei Zuordnung

Mithilfe des Windows-Sicherheitsmodells können Sie den Zugriff auf Datei Zuordnungsobjekte steuern. Weitere Informationen finden Sie unter [Zugriffs Steuerungsmodell](../secauthz/access-control-model.md).

Sie können eine [Sicherheits Beschreibung](../secauthz/security-descriptors.md) für ein Datei Zuordnung-Objekt angeben, wenn Sie die Funktion "up [**FileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) " aufrufen. Wenn Sie **null** angeben, erhält das Objekt eine Standard Sicherheits Beschreibung. Die ACLs in der Standard Sicherheits Beschreibung für ein Datei Zuordnungsobjekt stammen aus dem primären Token oder dem Identitätswechsel Token des Erstellers.

Um die Sicherheits Beschreibung eines Datei Zuordnungs Objekts abzurufen, rufen Sie die [**GetNamedSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-getnamedsecurityinfoa) -oder [**GetSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-getsecurityinfo) -Funktion auf. Um die Sicherheits Beschreibung eines Datei Zuordnungs Objekts festzulegen, müssen Sie die Funktion [**SetNamedSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-setnamedsecurityinfoa) oder [**setsecurityinfo**](/windows/win32/api/aclapi/nf-aclapi-setsecurityinfo) aufrufen.

Zu den gültigen Zugriffsrechten für Datei Zuordnungsobjekte zählen die [Standard Zugriffsrechte](../secauthz/standard-access-rights.md) **Delete**, **Read \_ Control**, **Write \_ DAC** und **Write \_ Owner** . Das **Synchronisieren** des Standard Zugriffsrechts wird von Datei Zuordnungsobjekten nicht unterstützt. In der folgenden Tabelle werden die Zugriffsrechte aufgelistet, die für Datei Zuordnungsobjekte spezifisch sind.

| Zugriffsrecht | Bedeutung |
|-|-|
| **Datei Zuordnung für den \_ \_ gesamten \_ Zugriff** | Schließt alle Zugriffsrechte für ein Datei Zuordnungs Objekt ein, außer wenn die **Datei Zuordnung \_ \_ ausgeführt** wird. Die Funktionen [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) und [**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) behandeln diese identisch mit dem angeben **des \_ \_ Schreib** Zugriffs auf die Datei Zuordnung. |
| **Datei \_ Zuordnung \_ Ausführen** | Ermöglicht die Zuordnung von ausführbaren Ansichten des Datei Zuordnung Objekts. Das Objekt muss mit Seitenschutz erstellt worden sein, um den Ausführungs Zugriff zu ermöglichen, z. b. **\_ \_ Lese**-und Schreibschutz für Seiten ausführen oder Lese- **\_ \_ /Schreibzugriff für die Seite ausführen** . **\_ \_**  |
| **Datei \_ Zuordnung \_ Lesen** | Ermöglicht die Zuordnung von schreibgeschützten oder kopierbaren Sichten des Datei Zuordnungsobjekts.  |
| **Datei \_ Zuordnung \_ schreiben** | Ermöglicht die Zuordnung von schreibgeschützten, kopierenden oder Lese-/schreibsichten eines Datei Zuordnungsobjekts. Das Objekt muss mit Seitenschutz erstellt worden sein, um Schreibzugriff zu ermöglichen, z. b. **Seiten \_ Lese** Vorgänge oder **Lese- \_ \_ /Schreibzugriff auf Seiten ausführen** . |

Das Mapping einer Copy-on-Write-Ansicht eines Datei Zuordnungsobjekts erfordert denselben Zugriff wie die Zuordnung einer schreibgeschützten Sicht. Das **\_ dateimapkopie \_** -Flag ist kein Zugriffsrecht und sollte nicht als Teil einer DACL in einer Sicherheits Beschreibung angegeben werden. Dieser Wert kann nur mit Funktionen verwendet werden, die eine Ansicht eines Datei Zuordnungs Objekts zuordnen, wie z. b. die Funktionen [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) und [**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) oder mit der [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) -Funktion, die das **\_ \_ Kopieren der Datei** Zuordnung auf die gleiche Weise behandelt wie das **\_ \_ Lesen der Datei** Zuordnung.

Sie können das **Zugriffs \_ System- \_ Sicherheits** Zugriffsrecht auf ein Datei Zuordnungsobjekt anfordern, wenn Sie die SACL des Objekts lesen oder schreiben möchten. Weitere Informationen finden Sie unter [Zugriffs Steuerungs Listen (Access Control Lists, ACLs)](../secauthz/access-control-lists.md) und [SACL-Zugriffsrecht](../secauthz/sacl-access-right.md).
