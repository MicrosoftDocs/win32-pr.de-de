---
description: Funktionen, die zum Verwalten von bereitgestellten Ordnern verwendet werden.
ms.assetid: 2624500b-11d6-4892-97d7-22efa450f681
title: Funktionen für bereitgestellte Ordner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13175dc4846d8f8438a3f1b94b3e407aaf347e2b6d10ad5c3761899882ecdfaf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870780"
---
# <a name="mounted-folder-functions"></a>Funktionen für bereitgestellte Ordner

Die bereitgestellten Ordnerfunktionen können in drei Gruppen unterteilt werden: allgemeine Funktionen, Funktionen, die zum Suchen nach Volumes verwendet werden, und Funktionen, die zum Überprüfen eines Volumes auf bereitgestellte Ordner verwendet werden.

## <a name="general-purpose-mounted-folder-functions"></a>General-Purpose Mounted Folder Functions



| Funktion                                                                     | BESCHREIBUNG                                                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw)                     | Löscht einen Laufwerkbuchstaben oder bereitgestellten Ordner.                                                                                                                   |
| [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) | Ruft den Volume-GUID-Pfad für das Volume ab, das dem angegebenen Volume-Bereitstellungspunkt (Laufwerkbuchstaben, Volume-GUID-Pfad oder bereitgestellter Ordner) zugeordnet ist. |
| [**GetVolumePathName**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumepathnamew)                               | Ruft den bereitgestellten Ordner ab, der dem angegebenen Volume zugeordnet ist.                                                                                  |
| [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa)                           | Ordnet ein Volume einem Laufwerkbuchstaben oder einem Verzeichnis auf einem anderen Volume zu.                                                                                   |



 

## <a name="volume-scanning-functions"></a>Volume-Scanning Functions



| Funktion                                   | BESCHREIBUNG                                                                                                                                    |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) | Gibt den Namen eines Volumes auf einem Computer zurück. [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) wird verwendet, um mit dem Aufzählen der Volumes eines Computers zu beginnen. |
| [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew)   | Setzt eine Volumesuche fort, die durch einen Aufruf von [**FindFirstVolume gestartet wurde.**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew)                                                     |
| [**FindVolumeClose**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose) | Schließt eine Suche nach Volumes.                                                                                                                   |



 

## <a name="mounted-folder-scanning-functions"></a>Funktionen zum Überprüfen von bereitgestellten Ordnern



| Funktion                                                       | BESCHREIBUNG                                                                                                                                                                               |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) | Ruft den Namen eines bereitgestellten Ordners auf dem angegebenen Volume ab. [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) wird verwendet, um mit dem Scannen der bereitgestellten Ordner auf einem Volume zu beginnen. |
| [**FindNextVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa)   | Setzt eine durch einen Aufruf von [**FindFirstVolumeMountPoint gestartete Ordnersuche fort.**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa)                                                                    |
| [**FindVolumeMountPointClose**](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose) | Schließt eine Suche nach bereitgestellten Ordnern.                                                                                                                                                      |



 

 

 



