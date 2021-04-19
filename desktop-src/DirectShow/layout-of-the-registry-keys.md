---
description: Layout der Registrierungsschlüssel
ms.assetid: c041d094-8165-446f-bf77-0d53b728fe7a
title: Layout der Registrierungsschlüssel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5783a9f083f639912188f418238f46a5d45ed922
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106345384"
---
# <a name="layout-of-the-registry-keys"></a>Layout der Registrierungsschlüssel

DirectShow-Filter werden an zwei Stellen registriert:

-   Die dll, die den Filter enthält, wird als com-Server des Filters registriert. Wenn eine Anwendung **cokreateinstance** aufruft, um den Filter zu erstellen, verwendet die Microsoft Windows com-Bibliothek diesen Registrierungs Eintrag, um die dll zu suchen.
-   Weitere Informationen über den Filter können in einer Filterkategorie registriert werden. Diese Informationen ermöglichen es dem [Enumerator des System Geräts](system-device-enumerator.md) und dem [Filter-Mapper](filter-mapper.md) , den Filter zu suchen.

Zum Registrieren der zusätzlichen Filter Informationen sind keine Filter erforderlich. Solange die dll als com-Server registriert ist, kann eine Anwendung den Filter erstellen und einem Filter Diagramm hinzufügen. Wenn Sie jedoch möchten, dass der Filter vom Enumerator für System Geräte oder vom Filter Mapper erkannt werden kann, müssen Sie die zusätzlichen Informationen registrieren.

Der Registrierungs Eintrag für die dll verfügt über die folgenden Schlüssel:


```
HKEY_CLASSES_ROOT
    CLSID
        Filter CLSID 
            REG_SZ: (Default) = Friendly name

            InprocServer32
                REG_SZ: (Default) = File name of the DLL
                REG_SZ: ThreadingModel = Both
```



Der Registrierungs Eintrag für die Filter Informationen verfügt über die folgenden Schlüssel:


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



die GUID einer Filterkategorie. (Weitere Informationen finden Sie unter [Filter Kategorien](filter-categories.md).) Die Filter Informationen werden in ein Binärformat verpackt. Die [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) -Schnittstelle entpackt diese Daten, wenn Sie die Registrierung nach einem Filter durchsucht.

Alle Filterkategorie-GUIDs sind in der Registrierung unter dem folgenden Schlüssel aufgeführt:


```C++
HKEY_CLASSES_ROOT\CLSID\{DA4E3DA0-D07D-11d0-BD50-00A0C911CE86}\Instance
```



 

 



