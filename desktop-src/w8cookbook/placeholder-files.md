---
title: Platzhalterdateien
description: Platzhalterdateien
ms.assetid: E14655DA-CEA0-4106-B882-C9E9116FC234
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8891fef6c7fc54a66c093507b1831ab7cc6525ea96d685d06cf6fa8d9ded1e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119452500"
---
# <a name="placeholder-files"></a>Platzhalterdateien

## <a name="platform"></a>Plattform

**Clients –** Windows 8.1  
**Server –** Windows Server 2012 R2  

## <a name="description"></a>BESCHREIBUNG

Platzhalterdateien ermöglichen Es Benutzern, Microsoft OneDrive Dateien unabhängig von der Konnektivität anzuzeigen und zu verwalten. Platzhalterdateien stellen den OneDrive Namespace dar, auch wenn Dateien nicht lokal zwischengespeichert werden. Sie enthalten Dateimetadaten und Miniaturbilder von Fotos.

## <a name="manifestation"></a>Manifestation

Für Endbenutzer und Entwickler sehen Platzhalterdateien fast genauso aus und verhalten sich wie die lokalen Dateien.

Wenn Ihre App das Dialogfeld "Allgemeine Datei" verwendet, um das Dateisystem aufzuzählen, ist ihre App nicht betroffen. Wenn der Benutzer versucht, die Datei über das allgemeine Dialogfeld /file zu öffnen, wird der Dateiinhalt heruntergeladen und an Ihre App übergeben.

Wenn Ihre App direkt auf das Dateisystem zugreift, kann Ihre App die Platzhalterdateien anhand der folgenden Richtlinien nutzen.

## <a name="solution"></a>Lösung

-   Platzhalter werden basierend auf Attributen konventionsbasiert ausgeblendet.
-   Identifizieren von Platzhaltern mithilfe der ID des Wiederholungstags IO \_ REPARSE \_ TAG \_ FILE \_ PLACEHOLDER

Verwenden Sie das Shelldatenmodell für nahtloses Verhalten:

-   Verwenden von SHCreateItemFromParsingName() zum Erstellen eines Shellelements
-   Binden an den Stream mithilfe von IShellItem::BindToHandler(LDAPID \_ Stream)
-   Benutzereigenschaftenhandler für den Eigenschaftenzugriff (IShellItem2::GetPropertyHandler)
-   User Shell thumbnailhandler to get thumbnail images for placeholders (Benutzershellminiaturhandler zum Abrufen von Miniaturbildern für Platzhalter)
-   Geben Sie SupportedProtocols= \* für Ihre Verbimplementierungen an, wenn das Verb über BindToHandler an den Stream gebunden wird.


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



 

 




