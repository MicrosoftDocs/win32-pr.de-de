---
title: Platzhalter Dateien
description: Platzhalter Dateien
ms.assetid: E14655DA-CEA0-4106-B882-C9E9116FC234
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93c15037b0daec7a6521a299b6c4587c956e0be3
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "106337270"
---
# <a name="placeholder-files"></a>Platzhalter Dateien

## <a name="platform"></a>Plattform

**Clients:** Windows 8.1  
**Server:** Windows Server 2012 R2  

## <a name="description"></a>BESCHREIBUNG

Platzhalter Dateien ermöglichen es Benutzern, Microsoft onedrive-Dateien unabhängig von der Konnektivität anzuzeigen und zu verwalten. Platzhalter Dateien stellen den onedrive-Namespace dar, auch wenn Dateien nicht lokal zwischengespeichert werden. Sie enthalten Datei Metadaten und Miniaturbilder von Fotos.

## <a name="manifestation"></a>Ausstrahlung

Für Endbenutzer und Entwickler Verhalten sich Platzhalter Dateien fast identisch mit den lokalen Dateien.

Wenn Ihre APP das Dateisystem mit dem allgemeinen Datei Dialogfeld aufzählt, wird Ihre APP nicht beeinträchtigt. Wenn der Benutzer versucht, die Datei im allgemeinen/File-Dialog Feld zu öffnen, wird der Inhalt der Datei heruntergeladen und an Ihre APP übermittelt.

Wenn Ihre APP direkt auf das Dateisystem zugreift, kann Ihre APP die Platzhalter Dateien mithilfe der unten aufgeführten Richtlinien nutzen.

## <a name="solution"></a>Lösung

-   Platzhalter werden auf der Grundlage von Attributen ausgeblendet.
-   Identifizieren von Platzhaltern mithilfe der Analyse-Tag-ID e/a- \_ \_ \_ Datei \_ Platzhalter

Verwenden Sie das Shell-Datenmodell für nahtloses Verhalten:

-   Verwenden Sie shkreateitemfromparametename () zum Erstellen eines shellelements.
-   Binden an den Datenstrom mithilfe von IShellItem:: bindtohandler (bhid- \_ Stream)
-   Benutzereigenschaften Handler für den Eigenschaften Zugriff (IShellItem2:: getpropertyhandler)
-   Benutzershellfingernailhandler zum Aufrufen von Miniaturbildern für Platzhalter
-   Geben Sie supportedprotokolls = \* für Ihre Verb-Implementierung an, wenn das Verb über bindtohandler an den Stream gebunden wird.


```
#include <winnth> //for IO_REPARSE_TAG_FILE_PLACEHOLDER
//  Helper that indicates this is a 
bool IsFilePlaceholder(WIN32_FIND_DATA const &findData)
{
  return (findData.dwFileAttributes & FILE_ATTRIBUTE_REPARSE_POINT) &&
    (findData.dwReserved0 == IO_REPARSE_TAG_FILE_PLACEHOLDER);
}
bool IsFilePlaceholder(_In_PCWSTR filePath)
{
  bool isPlaceholder = false;
  WIN32_FIND_DATA findData;
  HANDLE hFind = FindFirstFile(filePath, &findData);
  if (hFind ! = INVALID_HANDLE_VALUE)
  {
    isPlaceholder = (findData.dwFileAttributes &    FILE_ATTRIBUTE_REPARSE_POINT) &&
    (findData.dwReserved0 == IO_REPARSE_TAG_FILE_PLACEHOLDER);
    FindClose(hFind);
  }
  Return isPlaceholder;
}
```



 

 




