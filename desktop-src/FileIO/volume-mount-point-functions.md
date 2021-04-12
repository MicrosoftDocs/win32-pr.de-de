---
description: Funktionen, die zum Verwalten bereitgestellter Ordner verwendet werden.
ms.assetid: 2624500b-11d6-4892-97d7-22efa450f681
title: Funktionen für bereitgestellte Ordner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e984b9bee902f11af9d7b2b956ea0681cd6e7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346079"
---
# <a name="mounted-folder-functions"></a>Funktionen für bereitgestellte Ordner

Die Funktionen für den bereitgestellten Ordner können in drei Gruppen unterteilt werden: allgemeine Funktionen, Funktionen, die für die Suche nach Volumes verwendet werden, und Funktionen, die zum Scannen eines Volumes für bereitgestellte Ordner verwendet werden.

## <a name="general-purpose-mounted-folder-functions"></a>Bereitgestellte Ordner Funktionen General-Purpose



| Funktion                                                                     | BESCHREIBUNG                                                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw)                     | Löscht einen Laufwerk Buchstaben oder einen bereitgestellten Ordner.                                                                                                                   |
| [**Getvolumenameforvolumemountpoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) | Ruft den Volume-GUID-Pfad für das Volume ab, das dem angegebenen volumeeinstellungspunkt (Laufwerk Buchstabe, VolumeGuid-Pfad oder eingebundener Ordner) zugeordnet ist. |
| [**Getvolumepathname**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumepathnamew)                               | Ruft den bereitgestellten Ordner ab, der dem angegebenen Volume zugeordnet ist.                                                                                  |
| [**Setvolumemountpoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa)                           | Ordnet ein Volume einem Laufwerk Buchstaben oder einem Verzeichnis auf einem anderen Volume zu.                                                                                   |



 

## <a name="volume-scanning-functions"></a>Volume-Scanning Funktionen



| Funktion                                   | BESCHREIBUNG                                                                                                                                    |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Findfirstvolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) | Gibt den Namen eines Volumes auf einem Computer zurück. " [**Findfirstvolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) " wird verwendet, um mit dem Auflisten der Volumes eines Computers zu beginnen. |
| [**Findnextvolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew)   | Setzt eine volumesuche fort, die durch einen Befehl von [**findfirstvolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew)gestartet wurde.                                                     |
| [**Findvolumeclose**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose) | Schließt eine Suche nach Volumes.                                                                                                                   |



 

## <a name="mounted-folder-scanning-functions"></a>Scanfunktionen für eingebundene Ordner



| Funktion                                                       | BESCHREIBUNG                                                                                                                                                                               |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Findfirstvolumemountpoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) | Ruft den Namen eines eingebundenen Ordners auf dem angegebenen Volume ab. [**Findfirstvolumemountpoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) wird verwendet, um mit dem Scannen der bereitgestellten Ordner auf einem Volume zu beginnen. |
| [**Findnextvolumemountpoint**](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa)   | Setzt eine bereitgestellte Ordner Suche fort, die durch einen Befehl von [**findfirstvolumemountpoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa)gestartet wurde.                                                                    |
| [**Findvolumemountpointclose**](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose) | Schließt eine Suche nach bereitgestellten Ordnern.                                                                                                                                                      |



 

 

 



