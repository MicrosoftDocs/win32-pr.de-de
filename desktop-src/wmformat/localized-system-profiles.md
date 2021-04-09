---
title: Lokalisierte System profile
description: Lokalisierte System profile
ms.assetid: 2c218ab4-ecdb-414c-aa42-b71a42e340e5
keywords:
- Windows Media-Format-SDK, Systemprofile
- Advanced Systems Format (ASF), Systemprofile
- ASF (Advanced Systems Format), Systemprofile
- Windows Media-Format-SDK, lokalisierte Systemprofile
- Advanced Systems Format (ASF), lokalisierte Systemprofile
- ASF (Advanced Systems Format), lokalisierte Systemprofile
- Systemprofile, lokalisiert
- lokalisierte Systemprofile, Liste der
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aaeecdf1d1d62d78df18e0ac1c5bffbf39f9778
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038512"
---
# <a name="localized-system-profiles"></a>Lokalisierte System profile

In der folgenden Tabelle werden die lokalisierten Systemprofil Dateien aufgelistet, die im Windows Media-Format-SDK enthalten sind, sowie die jeweils zugeordneten Sprachen. Diese Dateien werden im \[ Ordner SDKRoot \] \\ wmsdk \\ WMFSDK9 \\ localizedprofiles installiert. Wenn Sie mit den **iwmprofilemanagerlanguage** -Methoden auf eine bestimmte Datei zugreifen möchten, müssen Sie sie zusammen mit den standardmäßigen Systemprofil Dateien in das Stammverzeichnis des Systems verschieben.



| Sprache              | Dateiname    |
|-----------------------|--------------|
| Arabisch                | Wmprfara. PRX |
| Chinesisch – vereinfacht  | Wmprf. PRX |
| Chinesisch – traditionell | Wmprf. PRX |
| Tschechisch                 | Wmprfcsy. PRX |
| Dänisch                | Wmprf. PRX |
| Niederländisch                 | Wmprfnld. PRX |
| Finnisch               | Wmprffin. PRX |
| Französisch                | Wmprffra. PRX |
| Deutsch                | Wmprf deu. PRX |
| Griechisch                 | Wmprfell. PRX |
| Hebräisch                | Wmprf Heb. PRX |
| Ungarisch             | Wmprf. PRX |
| Italienisch               | Wmprfta. PRX |
| Japanisch              | Wmprfjpn. PRX |
| Koreanisch                | Wmprf kor. PRX |
| Norwegisch             | Wmprf und. PRX |
| Polnisch                | Wmprf. PRX |
| Portugiesisch (Brasilien)   | Wmprfptb. PRX |
| Portugiesisch (Portugal) | Wmprfptg. PRX |
| Russisch               | Wmprfrus. PRX |
| Slowakisch                | Wmprf. PRX |
| Slowenisch             | Wmprf SLV. PRX |
| Spanisch               | Wmprfesp. PRX |
| Schwedisch               | Wmprfsve. PRX |
| Türkisch               | Wmprf TRK. PRX |



 

Sie können die Sprache für das Profil-Manager-Objekt festlegen, indem Sie die [**iwmprofilemanagerlanguage:: setuserlanguageid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanagerlanguage-setuserlanguageid) -Methode aufrufen. In den meisten Sprachen wird nur der primäre Sprach Bezeichner in der langid untersucht. Die Ausnahmen gelten für die Sprachen Chinesisch und Portugiesisch, bei denen auch der Bezeichner der sekundären Sprache verwendet wird. In der folgenden Tabelle wird gezeigt, wie eine langid erstellt wird, um in der **setuserlanguageid** -Methode anzugeben.



| Primäre sekundäre Sprache | Makelangid-Makro                                             |
|----------------------------|--------------------------------------------------------------|
| Chinesisch (vereinfacht)       | makelangid (lang \_ Chinesisch, sublang \_ Chinesisch \_ vereinfacht)     |
| Chinesisch (traditionell)      | makelangid (lang \_ Chinesisch, sublang \_ Chinesisch, \_ Singapur)      |
| Portugiesisch (Brasilien)        | makelangid (lang \_ Portugiesisch, sublang \_ Portugiesisch \_ Brasilianisch) |
| Portugiesisch (Portugal)      | makelangid (lang \_ Portugiesisch, sublang \_ Portugiesisch)            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierverzeichnis**](programming-reference.md)
</dt> <dt>

[**System profile**](system-profiles.md)
</dt> </dl>

 

 




