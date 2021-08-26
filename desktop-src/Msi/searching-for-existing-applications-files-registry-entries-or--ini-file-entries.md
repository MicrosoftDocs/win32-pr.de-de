---
description: Windows Das Installationsprogramm kann während einer Installation nach einer bestimmten Datei oder einem bestimmten Verzeichnis suchen. Datei- oder Verzeichnissuchen werden verwendet, um zu bestimmen, ob ein Benutzer bereits eine Version einer Anwendung installiert hat.
ms.assetid: a78ca652-c730-4231-80f2-60cf0bad5b02
title: Suchen nach vorhandenen Anwendungen, Dateien, Registrierungseinträgen oder .ini Dateieinträgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ac9cf4b39f8a46ccd16e83c96ee6ca808b3a1bee32094da480d0226d8bdf283
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041050"
---
# <a name="searching-for-existing-applications-files-registry-entries-or-ini-file-entries"></a>Suchen nach vorhandenen Anwendungen, Dateien, Registrierungseinträgen oder .ini Dateieinträgen

Windows Das Installationsprogramm kann während einer Installation nach einer bestimmten Datei oder einem bestimmten Verzeichnis suchen. Datei- oder Verzeichnissuchen werden verwendet, um zu bestimmen, ob ein Benutzer bereits eine Version einer Anwendung installiert hat.

[Die AppSearch-Aktion](appsearch-action.md) durchsucht ein Benutzersystem nach Dateisignaturen, die in der [AppSearch-Tabelle](appsearch-table.md)angegeben sind. Wenn die AppSearch-Aktion eine installierte Datei oder ein Verzeichnis mit der angegebenen Signatur findet, legt sie eine entsprechende Eigenschaft, die auch in der AppSearch-Tabelle angegeben ist, auf den Speicherort der Datei oder des Verzeichnisses fest. Bei der Suche nach einer Datei muss die Dateisignatur auch in der [Signaturtabelle](signature-table.md)aufgeführt werden. Wenn eine Dateisignatur in der Tabelle AppSearch und nicht in der Signaturtabelle aufgeführt ist, sucht die Suche nach einem Verzeichnis, registrierungseintrag oder .ini Dateieintrag.

Um die Suche eines Benutzercomputers zu beschleunigen, fragt der Installer die folgenden Locatordatenbanktabellen in der reihenfolge ab, die nach einem vorgeschlagenen Suchspeicherort aufgelistet ist:

-   Wenn die Dateisignatur in der [CompLocator-Tabelle](complocator-table.md)aufgeführt ist, ist der vorgeschlagene Suchspeicherort der Schlüsselpfad einer Komponente. Wenn die Signatur in dieser Tabelle nicht aufgeführt oder nicht am vorgeschlagenen Speicherort installiert ist, fragt der Installer die [RegLocator-Tabelle](reglocator-table.md) nach einem vorgeschlagenen Speicherort ab.
-   Wenn die Dateisignatur in der [RegLocator-Tabelle](reglocator-table.md)aufgeführt ist, ist der vorgeschlagene Suchspeicherort ein Schlüsselpfad, der in der Benutzerregistrierung geschrieben wurde. Wenn die Signatur in dieser Tabelle nicht aufgeführt oder nicht am vorgeschlagenen Speicherort installiert ist, fragt der Installer die [IniLocator-Tabelle](inilocator-table.md) nach einem vorgeschlagenen Speicherort ab.
-   Wenn die Dateisignatur in der [IniLocator-Tabelle](inilocator-table.md)aufgeführt ist, ist der vorgeschlagene Suchspeicherort ein Schlüsselpfad, der in einer .ini Datei geschrieben wurde, die im Standardverzeichnis Windows eines Benutzersystems vorhanden ist. Wenn die Signatur in dieser Tabelle nicht aufgeführt oder nicht am vorgeschlagenen Speicherort installiert ist, fragt der Installer die [DrLocator-Tabelle](drlocator-table.md) nach einem vorgeschlagenen Speicherort ab.
-   Wenn die Dateisignatur in der [DrLocator-Tabelle](drlocator-table.md)aufgeführt ist, ist der vorgeschlagene Suchspeicherort ein Pfad in der Benutzerverzeichnisstruktur. Die Tiefe der Unterverzeichnisebenen, die unterhalb dieses Speicherorts durchsucht werden sollen, wird auch in dieser Tabelle angegeben.

Wenn der Installer die Dateisignatur zum ersten Mal an einem vorgeschlagenen Speicherort findet, beendet er die Suche nach dieser Datei oder diesem Verzeichnis und legt die entsprechende Eigenschaft in der [AppSearch-Tabelle](appsearch-table.md)fest. Weitere Informationen finden Sie unter

-   [Suchen aller Festplattenlaufwerke nach einer Datei](searching-all-fixed-drives-for-a-file.md)
-   [Suchen nach einem Verzeichnis und einer Datei im Verzeichnis](searching-for-a-directory-and-a-file-in-the-directory.md)
-   [Suchen nach einer Datei und Erstellen einer Eigenschaft, die den Pfad der Datei enthält](searching-for-a-file-and-creating-a-property-holding-the-file-s-path.md)
-   [Suchen nach einer Datei an einem bestimmten Speicherort](searching-for-a-file-in-a-specific-location.md)
-   [Suchen nach einem Registrierungseintrag und Erstellen einer Eigenschaft mit dem Wert der Registrierung](searching-for-a-registry-entry-and-creating-a-property-holding-the-value-of-the-registry.md)

 

 



