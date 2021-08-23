---
description: Layout der Registrierungsschlüssel
ms.assetid: c041d094-8165-446f-bf77-0d53b728fe7a
title: Layout der Registrierungsschlüssel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4473027b2612d16b3c6daee4f8e708d90b993397b133db111aa55c58e9c4ceb0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502290"
---
# <a name="layout-of-the-registry-keys"></a>Layout der Registrierungsschlüssel

DirectShow-Filter werden an zwei Stellen registriert:

-   Die DLL, die den Filter enthält, wird als COM-Server des Filters registriert. Wenn eine Anwendung **CoCreateInstance aufruft,** um den Filter zu erstellen, verwendet die Microsoft Windows COM-Bibliothek diesen Registrierungseintrag, um die DLL zu suchen.
-   Zusätzliche Informationen zum Filter können innerhalb einer Filterkategorie registriert werden. Diese Informationen ermöglichen es dem [Systemgeräte-Enumerator](system-device-enumerator.md) und der [Filterzuordnung,](filter-mapper.md) den Filter zu suchen.

Filter sind nicht erforderlich, um die zusätzlichen Filterinformationen zu registrieren. Solange die DLL als COM-Server registriert ist, kann eine Anwendung den Filter erstellen und einem Filterdiagramm hinzufügen. Wenn Der Filter jedoch vom Systemgeräte-Enumerator oder filter mapper ermittelt werden kann, müssen Sie die zusätzlichen Informationen registrieren.

Der Registrierungseintrag für die DLL verfügt über die folgenden Schlüssel:


```
HKEY_CLASSES_ROOT
    CLSID
        Filter CLSID 
            REG_SZ: (Default) = Friendly name

            InprocServer32
                REG_SZ: (Default) = File name of the DLL
                REG_SZ: ThreadingModel = Both
```



Der Registrierungseintrag für die Filterinformationen verfügt über die folgenden Schlüssel:


```
HKEY_CLASSES_ROOT
    CLSID
        Category
            Instance
                Filter CLSID
                    REG_SZ: CLSID = Filter CLSID
                    REG_BINARY: FilterData = Filter information
                    REG_SZ: FriendlyName = Friendly name
```




```
Category
```



ist die GUID einer Filterkategorie. (Siehe [Filterkategorien](filter-categories.md).) Die Filterinformationen werden in ein Binärformat gepackt. Die [**IFilterMapper2-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) entpackt diese Daten, wenn sie die Registrierung nach einem Filter durchsucht.

Alle GUIDs der Filterkategorie werden in der Registrierung unter dem folgenden Schlüssel aufgeführt:


```C++
HKEY_CLASSES_ROOT\CLSID\{DA4E3DA0-D07D-11d0-BD50-00A0C911CE86}\Instance
```



 

 



