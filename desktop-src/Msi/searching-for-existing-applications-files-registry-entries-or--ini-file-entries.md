---
description: Windows Installer können während einer Installation nach einer bestimmten Datei oder einem bestimmten Verzeichnis suchen. Datei-oder Verzeichnis suchen werden verwendet, um zu bestimmen, ob ein Benutzer bereits eine Version einer Anwendung installiert hat.
ms.assetid: a78ca652-c730-4231-80f2-60cf0bad5b02
title: Suchen nach vorhandenen Anwendungen, Dateien, Registrierungs Einträgen oder INI-Datei Einträgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a41d0ebf8943d1fb82b7c0901a62230e6befdcba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351587"
---
# <a name="searching-for-existing-applications-files-registry-entries-or-ini-file-entries"></a>Suchen nach vorhandenen Anwendungen, Dateien, Registrierungs Einträgen oder INI-Datei Einträgen

Windows Installer können während einer Installation nach einer bestimmten Datei oder einem bestimmten Verzeichnis suchen. Datei-oder Verzeichnis suchen werden verwendet, um zu bestimmen, ob ein Benutzer bereits eine Version einer Anwendung installiert hat.

Die [AppSearch-Aktion](appsearch-action.md) durchsucht ein Benutzersystem nach Datei Signaturen, die in der [AppSearch-Tabelle](appsearch-table.md)angegeben sind. Wenn von der AppSearch-Aktion eine installierte Datei oder ein Verzeichnis mit der angegebenen Signatur gefunden wird, wird eine entsprechende Eigenschaft, die auch in der AppSearch-Tabelle angegeben ist, auf den Speicherort der Datei oder des Verzeichnisses festgelegt. Wenn Sie nach einer Datei suchen, muss die Datei Signatur auch in der [Signatur Tabelle](signature-table.md)aufgeführt werden. Wenn eine Datei Signatur in der Tabelle "AppSearch" aufgeführt ist und nicht in der Signatur Tabelle aufgeführt ist, sucht die Suche nach einem Verzeichnis, einem Registrierungs Eintrag oder einem Eintrag der INI-Datei.

Um die Suche nach einem Benutzer Computer zu beschleunigen, fragt das Installationsprogramm die folgenden Serverlocatorpunkt-Datenbanktabellen in der Reihenfolge ab, die für einen vorgeschlagenen Such Speicherort aufgeführt ist:

-   Wenn die Datei Signatur in der [Tabelle complocator](complocator-table.md)aufgeführt ist, ist der empfohlene Suchort der Schlüssel Pfad einer Komponente. Wenn die Signatur nicht in dieser Tabelle aufgeführt ist oder nicht am vorgeschlagenen Speicherort installiert ist, fragt das Installationsprogramm die [reglocator-Tabelle](reglocator-table.md) nach einem vorgeschlagenen Speicherort ab.
-   Wenn die Datei Signatur in der [reglocator-Tabelle](reglocator-table.md)aufgeführt ist, ist der vorgeschlagene Suchort ein Schlüssel Pfad, der in der Benutzerregistrierung geschrieben wurde. Wenn die Signatur nicht in dieser Tabelle aufgeführt ist oder nicht am vorgeschlagenen Speicherort installiert ist, fragt das Installationsprogramm die [Tabelle "inilocator](inilocator-table.md) " nach einem vorgeschlagenen Speicherort ab.
-   Wenn die Datei Signatur in der Tabelle " [inilocator](inilocator-table.md)" aufgeführt ist, ist der vorgeschlagene Suchort ein Schlüssel Pfad, der in einer INI-Datei im standardmäßigen Windows-Verzeichnis eines Benutzer Systems geschrieben ist. Wenn die Signatur nicht in dieser Tabelle aufgeführt ist oder nicht am vorgeschlagenen Speicherort installiert ist, fragt das Installationsprogramm die [drlocator-Tabelle](drlocator-table.md) nach einem vorgeschlagenen Speicherort ab.
-   Wenn die Datei Signatur in der [drlocator-Tabelle](drlocator-table.md)aufgeführt ist, ist der empfohlene Suchort ein Pfad in der Benutzerverzeichnis Struktur. Die Tiefe der Unterverzeichnis Ebenen, die unterhalb dieses Standorts durchsucht werden sollen, wird auch in dieser Tabelle angegeben.

Wenn das Installationsprogramm die Datei Signatur zum ersten Mal an einem vorgeschlagenen Speicherort findet, wird die Suche nach dieser Datei oder diesem Verzeichnis beendet, und die entsprechende Eigenschaft wird in der [AppSearch-Tabelle](appsearch-table.md)festgelegt. Weitere Informationen finden Sie unter

-   [Suchen aller Festplattenlaufwerke nach einer Datei](searching-all-fixed-drives-for-a-file.md)
-   [Suchen nach einem Verzeichnis und einer Datei im Verzeichnis](searching-for-a-directory-and-a-file-in-the-directory.md)
-   [Suchen nach einer Datei und Erstellen einer Eigenschaft mit dem Pfad der Datei](searching-for-a-file-and-creating-a-property-holding-the-file-s-path.md)
-   [Suchen nach einer Datei an einem bestimmten Speicherort](searching-for-a-file-in-a-specific-location.md)
-   [Suchen nach einem Registrierungs Eintrag und Erstellen einer Eigenschaft mit dem Wert der Registrierung](searching-for-a-registry-entry-and-creating-a-property-holding-the-value-of-the-registry.md)

 

 



