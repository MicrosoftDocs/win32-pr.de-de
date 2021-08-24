---
title: Lokalisierte Systemprofile
description: Lokalisierte Systemprofile
ms.assetid: 2c218ab4-ecdb-414c-aa42-b71a42e340e5
keywords:
- Windows Medienformat-SDK, Systemprofile
- Advanced Systems Format (ASF), Systemprofile
- ASF (Advanced Systems Format), Systemprofile
- Windows Medienformat-SDK, lokalisierte Systemprofile
- Advanced Systems Format (ASF), lokalisierte Systemprofile
- ASF (Advanced Systems Format), lokalisierte Systemprofile
- Systemprofile, lokalisiert
- lokalisierte Systemprofile, Liste der
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbe3ca0abbe0e5b92645f6adaa1f6ebfdc44d52064d6fb8e1389420d19651b7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707710"
---
# <a name="localized-system-profiles"></a>Lokalisierte Systemprofile

In der folgenden Tabelle sind die lokalisierten Systemprofildateien aufgeführt, die im Windows Media Format SDK enthalten sind, sowie die jeweils zugeordneten Sprachen. Diese Dateien werden im \[ Ordner SDKRoot \] \\ WMSDK \\ WMFSDK9 \\ LocalizedProfiles installiert. Um mit den **IWMProfileManagerLanguage-Methoden** auf eine bestimmte Datei zuzugreifen, müssen Sie sie zusammen mit den Standardsystemprofildateien in das Systemstammverzeichnis verschieben.



| Sprache              | Dateiname    |
|-----------------------|--------------|
| Arabisch                | WMPrfAra.prx |
| Chinesisch – vereinfacht  | WMPrfCHS.prx |
| Chinesisch – traditionell | WMPrfCHT.prx |
| Tschechisch                 | WMPrfCsy.prx |
| Dänisch                | WMPrfDan.prx |
| Niederländisch                 | WMPrfNld.prx |
| Finnisch               | WMPrfFin.prx |
| Französisch                | WMPrfFra.prx |
| Deutsch                | WMPrfDeu.prx |
| Griechisch                 | WMPrfEll.prx |
| Hebräisch                | WMPrfHeb.prx |
| Ungarisch             | WMPrfHun.prx |
| Italienisch               | WMPrfIta.prx |
| Japanisch              | WMPrfJpn.prx |
| Koreanisch                | WMPrfKor.prx |
| Norwegisch             | WMPrfNor.prx |
| Polnisch                | WMPrfPlk.prx |
| Portugiesisch (Brasilien)   | WMPrfPtb.prx |
| Portugiesisch (Portugal) | WMPrfPtg.prx |
| Russisch               | WMPrfRus.prx |
| Slowakisch                | WMPrfSky.prx |
| Slowenisch             | WMPrfSlv.prx |
| Spanisch               | WMPrfEsp.prx |
| Schwedisch               | WMPrfSve.prx |
| Türkisch               | WMPrfTrk.prx |



 

Sie können die Sprache für das Profil-Manager-Objekt festlegen, indem Sie die [**IWMProfileManagerLanguage::SetUserLanguageID-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanagerlanguage-setuserlanguageid) aufrufen. Für die meisten Sprachen wird nur der primäre Sprachbezeichner in der LANGID untersucht. Ausnahmen gelten für die Sprachen Chinesisch und Portugiesisch, wobei auch der bezeichner der sekundären Sprache verwendet wird. Die folgende Tabelle zeigt, wie Sie eine LANGID erstellen, die in der **SetUserLanguageID-Methode** angegeben wird.



| Primär-sekundäre Sprache | MAKELANGID-Makro                                             |
|----------------------------|--------------------------------------------------------------|
| Chinesisch (vereinfacht)       | MAKELANGID( LANG \_ CHINESISCH, SUBLANG \_ CHINESISCH \_ VEREINFACHT)     |
| Chinesisch (traditionell)      | MAKELANGID( LANG \_ CHINESISCH, SUBLANG \_ CHINESISCH \_ SINGAPUR)      |
| Portugiesisch (Brasilien)        | MAKELANGID(LANG \_ PORTUGIESISCH, SUBLANG \_ PORTUGIESISCH \_ BRASILIEN) |
| Portugiesisch (Portugal)      | MAKELANGID(LANG \_ PORTUGIESISCH, SUBLANG \_ PORTUGIESISCH)            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierverzeichnis**](programming-reference.md)
</dt> <dt>

[**Systemprofile**](system-profiles.md)
</dt> </dl>

 

 




