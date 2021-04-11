---
description: WMI basiert auf standardmäßigen Windows-Sicherheits Deskriptoren zum Steuern und schützen des Zugriffs auf Sicherungs fähige Objekte wie WMI-Namespaces, Drucker, Dienste und DCOM-Anwendungen.
ms.assetid: 5893457d-3fc2-4d64-a6c2-0f410052ce52
ms.tgt_platform: multiple
title: Zugriff auf Sicherungs fähige WMI-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad4ea78cd45d57856b0909283e7c2624fb26bd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217972"
---
# <a name="access-to-wmi-securable-objects"></a>Zugriff auf Sicherungs fähige WMI-Objekte

WMI basiert auf standardmäßigen Windows- [*Sicherheits Deskriptoren*](/windows/desktop/SecGloss/s-gly) zum Steuern und schützen des Zugriffs auf Sicherungs fähige Objekte wie WMI-Namespaces, Drucker, Dienste und DCOM-Anwendungen. Weitere Informationen finden Sie unter [zugreifen auf WMI-Namespaces](access-to-wmi-namespaces.md).

In diesem Abschnitt werden folgende Themen erörtert:

-   [Sicherheits Deskriptoren und SIDs](#security-descriptors-and-sids)
-   [Zugriffssteuerung](#access-control)
-   [Ändern der Zugriffssicherheit](#changing-access-security)
-   [Zugehörige Themen](#related-topics)

## <a name="security-descriptors-and-sids"></a>Sicherheits Deskriptoren und SIDs

WMI behält die Zugriffssicherheit bei, indem das [*Zugriffs Token*](/windows/desktop/SecGloss/a-gly) des Benutzers, der versucht, auf ein Sicherungs fähiges Objekt zuzugreifen, mit der Sicherheits Beschreibung des Objekts verglichen wird.

Wenn ein Benutzer oder eine Gruppe auf einem System erstellt wird, erhält das Konto eine [*Sicherheits-ID (SID)*](/windows/desktop/SecGloss/s-gly) . die SID stellt sicher, dass ein Konto, das mit dem gleichen Namen wie ein zuvor gelöschtes Konto erstellt wurde, die vorherigen Sicherheitseinstellungen nicht erbt. Ein Zugriffs Token wird erstellt, indem die SID, die Liste der Gruppen, denen der Benutzer angehört, und die Liste der aktivierten oder deaktivierten Berechtigungen kombiniert werden. Diese Token werden allen Prozessen und Threads zugewiesen, die sich im Besitz des Benutzers befinden.

## <a name="access-control"></a>Zugriffssteuerung

Wenn der Benutzer ein gesichertes Objekt verwenden möchte, wird das Zugriffs Token in der Sicherheits Beschreibung des-Objekts mit der freigegebenen [*Zugriffs Steuerungs Liste (DACL)*](/windows/desktop/SecGloss/d-gly) verglichen. Die DACL enthält Berechtigungen, die als [*Zugriffs Steuerungs Einträge (ACE)*](/windows/desktop/SecGloss/a-gly)bezeichnet werden. [*System-Zugriffs Steuerungs Listen (SACL)*](/windows/desktop/SecGloss/s-gly) tun das gleiche wie DACLs, können jedoch Sicherheits Überwachungs Ereignisse generieren. Ab Windows Vista kann WMI Überwachungs Einträge im Windows-Sicherheitsprotokoll erstellen. Weitere Informationen zur Überwachung in WMI finden Sie unter [zugreifen auf WMI-Namespaces](access-to-wmi-namespaces.md).

Die DACL und die SACL bestehen aus einer Liste von ACEs, die beschreiben, welche Benutzer über bestimmte Zugriffsrechte verfügen, einschließlich des Schreibvorgangs in das WMI-Repository, des Remote Zugriffs und der Ausführung sowie der Anmelde Berechtigungen. WMI speichert diese ACLs im WMI-Repository.

ACEs enthalten drei Typen von Zugriffsebenen oder GRANT/DENY-rechten: allow, Deny für DACL und System Audit (für SACLs). Deny ACEs vor zulassen von ACEs in der DACL oder SACL. Wenn Sie die Benutzer Zugriffsrechte überprüfen, wird WMI in der Zugriffs Steuerungs Liste nacheinander ausgeführt, bis ein allow-ACE gefunden wird, der für das anfordernde Zugriffs Token gilt. Die verbleibenden ACEs werden nach diesem Punkt nicht geprüft. Wenn kein entsprechender Allow ACE gefunden wird, wird der Zugriff verweigert. Weitere Informationen finden Sie unter [Reihenfolge von ACEs in einer DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl) und [Erstellen einer DACL](/windows/desktop/SecBP/creating-a-dacl).

## <a name="changing-access-security"></a>Ändern der Zugriffssicherheit

Mit den entsprechenden Berechtigungen können Sie die Sicherheit für ein Sicherungs fähiges Objekt mit einem Skript oder einer Anwendung ändern. Sie können auch die Sicherheitseinstellungen für WMI-Namespaces mithilfe des [*WMI-Steuer*](gloss-w.md) Elements oder durch Hinzufügen einer SDDL-Zeichenfolge [(Security Descriptor Definition Language)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) in der [*MOF*](gloss-m.md) -Datei (Managed Object Format) ändern, die Klassen für den Namespace definiert. Weitere Informationen finden Sie unter [zugreifen auf WMI-Namespaces](access-to-wmi-namespaces.md), [Sichern von WMI-Namespaces](securing-wmi-namespaces.md)und [Ändern der Zugriffssicherheit für Sicherungs fähige Objekte](changing-access-security-on-securable-objects.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-sicherheitsdeskriptorobjekte](wmi-security-descriptor-objects.md)
</dt> <dt>

[WMI-Sicherheits Konstanten](wmi-security-constants.md)
</dt> <dt>

[Benutzerkontensteuerung und WMI](user-account-control-and-wmi.md)
</dt> <dt>

[WMI-sicherheitsdeskriptorobjekte](wmi-security-descriptor-objects.md)
</dt> <dt>

[Zugriff auf WMI-Namespaces](access-to-wmi-namespaces.md)
</dt> </dl>

 

 
