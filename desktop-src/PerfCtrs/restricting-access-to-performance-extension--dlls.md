---
description: Ab Windows Server 2003 wurden die Benutzergruppe "System Monitor Benutzer" und die Gruppe "Leistungs Protokoll Benutzer" Entwicklern und Benutzern von Leistungs-DLLs und den Leistungsdaten-API-Funktionen (PDH) zur Verfügung gestellt.
ms.assetid: 423359be-9d41-4a5f-91cd-f6d7a6a91d9d
title: Einschränken des Zugriffs auf Leistungs Erweiterungs-DLLs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd433cad68ec3e50f6b17994da98164e2ae9f237
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865092"
---
# <a name="restricting-access-to-performance-extension-dlls"></a>Einschränken des Zugriffs auf Leistungs Erweiterungs-DLLs

Ab Windows Server 2003 wurden die Benutzergruppe "System Monitor Benutzer" und die Gruppe "Leistungs Protokoll Benutzer" Entwicklern und Benutzern von Leistungs-DLLs und den Leistungsdaten-API-Funktionen (PDH) zur Verfügung gestellt. Diese Leistungs Sicherheitsgruppen können von Systemadministratoren verwendet werden, um den Zugriff auf die Informationen einzuschränken, die von Leistungs-DLLs für eine bestimmte Liste von Benutzern verfügbar gemacht werden.

Die Gruppe der System Monitor Benutzer soll Benutzer einschließen, die Leistungsindikatoren anzeigen und keine Leistungsindikatoren mit dem Leistungsprotokolle und-Warnungen-Dienst protokollieren. Die Gruppe der Leistungs Protokoll Benutzer sollte Benutzer enthalten, die über die Berechtigung zum Verwenden der Leistungs Protokolle und des Benachrichtigungs Dienstanbieter zum Protokollieren von Leistungsindikatoren auf dem lokalen Server oder Remote Server Zu den Berechtigungen dieser Gruppe zählen auch das Erstellen von Protokolldateien auf lokalen Systemen oder Remote Systemen, die Verwendung des Warnungs Dienstanbieter und das Ausführen von Programmen als Teil des Dienstanbieter.

Beachten Sie, dass es sich bei diesen Leistungs Sicherheitsgruppen nicht um einen Zugriffs Einschränkungs Mechanismus handelt. Hierfür müssen Sie diese Gruppen mit dem Windows-Objekt Zugriffs Steuerungsmodell verwenden.

Die meisten Anwendungen kommunizieren mit der Leistungs-DLL über einen IPC-Mechanismus, normalerweise gemeinsam genutzten Speicher. Daher können Sie die Mitglieder einer Leistungs Sicherheitsgruppe der Sicherheits Beschreibung des Shared Memory-Objekts hinzufügen, um den Zugriff auf die dll auf die Mitglieder der Sicherheitsgruppe einzuschränken. Dabei müssen Sie die Gruppenmitglieder der Sicherheits Beschreibung der Systemobjekte hinzufügen, auf die die Leistungs-dll zugreift, um Leistungsdaten, z. b. Protokolldateien und Ordner, bereitzustellen. Ausführlichere Informationen zum Hinzufügen von ACLs zu Objekt Sicherheits Deskriptoren finden Sie unter [Ändern der ACL eines Objekts](/windows/desktop/SecAuthZ/modifying-the-acls-of-an-object-in-c--).

Eine andere Methode, die Sie zum Ändern der ACL-Informationen der Sicherheits Beschreibung eines IPC-System Objekts verwenden können, besteht darin, die Mitglieder der Leistungs Sicherheitsgruppen Liste mit der Sicherheits Beschreibung (Security Deskriptor Definition Language, SDDL) anzugeben und [**convertstringsecuritydescriptortosecuritydescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) aufzurufen, um die Sicherheits Beschreibung zu erstellen. Diese Sicherheits Beschreibung wird dann an das IPC-Systemobjekt angefügt. Das folgende Beispiel zeigt eine SDDL-Zeichenfolge, die die Gruppe der System Monitor Benutzer, Mu und die Gruppe der Leistungs Protokoll Benutzer (LU) enthält.

``` syntax
D:(A;OICI;GA;;;SY)(A;OICI;GA;;;BA)(A;OICI;FRFWFXSDRC;;;NS)(A;OICI;FRFWFXSDRC;;;LU)(A;OICI;FRFX;;;MU) 
```

 

 
