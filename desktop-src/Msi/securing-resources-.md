---
description: Die Möglichkeit der Windows Installer, Zugriffsberechtigungen für Dienste, Dateien, erstellte Ordner und Registrierungseinträge festzulegen, kann dazu beitragen, dass Installationsanwendungen sicherer werden.
ms.assetid: a25fcecf-f15f-4772-8f41-d03864484cc9
title: Sichern von Ressourcen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 415fe7b2df343a54aa0819031f4fd22b05857618
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362284"
---
# <a name="securing-resources"></a>Sichern von Ressourcen

Die Möglichkeit der Windows Installer, Zugriffsberechtigungen für Dienste, Dateien, erstellte Ordner und Registrierungseinträge festzulegen, kann dazu beitragen, dass Installationsanwendungen sicherer werden. Die Verwendung der [msilockpermissionsex](msilockpermissionsex-table.md) -Tabelle oder der [lockberechtigungs](lockpermissions-table.md) -Tabelle zum Sichern von Ressourcen ist eine der empfohlenen [Richtlinien für die Erstellung sicherer Installationen](guidelines-for-authoring-secure-installations.md). Die msilockpermissionsex-Tabelle kann einem Paket Ersteller ermöglichen, eine Ressource zu sichern, ohne eine [benutzerdefinierte Aktion](custom-actions.md)schreiben zu müssen.

Beginnend mit den für Windows Installer 5,0 entwickelten Paketen sollte die [msilockpermissionsex](msilockpermissionsex-table.md) -Tabelle die Verwendung der [lockberechtigungs](lockpermissions-table.md) -Tabelle ersetzen. Mithilfe der erweiterten Funktionalität der msilockpermissionsex-Tabelle kann ein Paket Windows- [Dienste](../services/services.md),-Dateien,-Ordner und-Registrierungsschlüssel sichern. Ein Paket sollte nicht gleichzeitig die Tabellen msilockpermissionsex und lockberechtigungs Tabelle enthalten.

In Windows Installer 4,5 und früher wird die [Tabelle "msilockpermissionsex](msilockpermissionsex-table.md)" ignoriert. Ab Windows Installer 5,0 schlägt die Installation mit der Fehlermeldung 1941 fehl, wenn das Paket sowohl eine [lockberechtigungs Tabelle](lockpermissions-table.md) als auch eine msilockpermissionsex-Tabelle enthält. Vorhandene Installationspakete, die nur die lockberechtigungs Tabelle enthalten, können weiterhin mit Windows Installer 5,0 installiert werden.

Windows Installer 5,0 verarbeitet die Informationen in der Tabelle " [msilockpermissionsex](msilockpermissionsex-table.md) ", wenn Sie die Standard Aktionen " [InstallFiles](installfiles-action.md)", " [installservices](installservices-action.md)", " [schreiteregistryvalues](writeregistryvalues-action.md) " und "Buildordner" ausführt. [](createfolders-action.md) Ein Sicherungs fähiges Objekt muss installiert oder neu installiert werden, damit es gesichert werden kann, und es ist nicht möglich, eine [Access Control Liste](../secauthz/access-control-lists.md) (ACL) an ein vorhandenes Objekt anzufügen, ohne das Objekt erneut zu installieren.

Um den zu sichernden Dienst, die Datei, das Verzeichnis oder den Registrierungsschlüssel anzugeben, geben Sie die identifizierenden Informationen in die Felder lockobject und Table der Tabelle [msilockpermissionsex](msilockpermissionsex-table.md) ein. Ein Objekt wird durch seinen Primärschlüssel in der [Tabelle ServiceInstall](serviceinstall-table.md), der [Dateitabelle](file-table.md), der [Registrierungs Tabelle](registry-table.md)oder der [Tabelle "Tabelle](createfolder-table.md)" identifiziert.

Um anzufordern, dass bestimmte Berechtigungen für ein Objekt gelten, geben Sie eine gültige Sicherheits Deskriptor-Zeichenfolge in das Feld *sddltext* der Tabelle [msilockpermissionsex](msilockpermissionsex-table.md) ein, indem Sie die gültige SDDL ( [Security Deskriptor Definition Language](../secauthz/security-descriptor-definition-language.md) ) verwenden. Die **msilockpermissionsex** -Tabelle kann eine Sicherheits Beschreibung angeben, die Berechtigungen ablehnt, die Vererbung von Berechtigungen für eine übergeordnete Ressource angibt oder die Berechtigungen eines neuen Kontos angibt. Eine Liste aller Berechtigungen, die gewährt, verweigert oder geerbt werden können, finden Sie unter [ACE](../secauthz/ace-strings.md)-Zeichen folgen. Windows Installer 5,0 erweitert den Satz verfügbarer Sicherheits-IDs (SIDs). Eine Liste der gültigen SIDs finden Sie unter [sid](../secauthz/sid-strings.md)-Zeichen folgen.

> [!NOTE]
> Wenn Sie die Sicherheits Beschreibung einer übergeordneten Ressource konfigurieren möchten, um anzugeben, dass die Berechtigungen von untergeordneten Objekten geerbt werden sollen, muss das Installationsprogramm Berechtigungen für die übergeordnete Ressource anwenden, bevor die untergeordneten Objekte erstellt werden. Wenn das Installationsprogramm die untergeordneten Objekte erstellt, bevor die vererbbaren Berechtigungen auf die übergeordnete Ressource angewendet werden, werden die Berechtigungen der übergeordneten Ressource nicht an die untergeordneten Objekte weitergegeben.

Ab Windows Installer 5,0 erweitert der [formattedsddltext](formattedsddltext.md) -Datentyp den [formatierten](formatted.md) Datentyp. Der Windows Installer überprüft, ob die in der sddltext-Spalte der [msilockpermissionsex](msilockpermissionsex-table.md) -Tabelle eingegebene formattedsddltext-Zeichenfolge dem [Format der Sicherheits Deskriptor-Zeichenfolge](../secauthz/security-descriptor-string-format.md)entspricht.

**[Windows Installer 4,5 oder früher](not-supported-in-windows-installer-4-5.md):** Nicht unterstützt. Die [msilockpermissionsex](msilockpermissionsex-table.md) -Tabelle und der [formattedsddltext](formattedsddltext.md) -Datentyp sind ab Windows Installer 5,0 verfügbar.

 

 
