---
title: Ändern von Voreinstellungen
description: Ändern von Voreinstellungen
ms.assetid: f8a5565d-676b-4679-a4cb-4bd7551cf41c
keywords:
- Visualisierungen,Leuchtbeispiel
- Benutzerdefinierte Visualisierungen, Beispiel "Leucht"
- Programmierhandbuch,Visualisierungen
- Beispiele,Leuchtvisualisierung
- Beispiel für die Visualisierung von Leuchtern
- Visualisierungen,Voreinstellungen
- Benutzerdefinierte Visualisierungen,Voreinstellungen
- Voreinstellungen in Visualisierungen,Leuchtbeispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03828614093836c5f9a3b422167b62f11b8f2489eb30556d42a2d80495935ec5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863910"
---
# <a name="changing-presets"></a>Ändern von Voreinstellungen

Die folgenden voreingestellten Codeabschnitte wurden geändert, um drei Voreinstellungen zu ermöglichen:

## <a name="getpresettitle"></a>GetPresetTitle

Dieser Code wurde statt des generierten Voreinstellungscodes eingefügt:


```C++
    switch (nPreset)
    {
    case PRESET_RED:
        bstrTemp.LoadString(IDS_REDPRESETNAME); 
        break;

    case PRESET_GREEN:
        bstrTemp.LoadString(IDS_GREENPRESETNAME); 
        break;

    case PRESET_BLUE:
        bstrTemp.LoadString(IDS_BLUEPRESETNAME); 
        break;
    }

```



## <a name="enumerations"></a>Enumerationen

Die folgende Enumeration in "Glow.h" wurde geändert, um drei Voreinstellungen zu ermöglichen:


```C++
enum {
    PRESET_RED = 0,
    PRESET_GREEN,
    PRESET_BLUE,
    PRESET_COUNT
};

```



## <a name="resource-header"></a>Ressourcenheader

Die folgenden Ressourcen wurden in Resource.h definiert, um drei Voreinstellungen zu ermöglichen:


```C++
#define IDS_REDPRESETNAME               102
#define IDS_GREENPRESETNAME             103
#define IDS_BLUEPRESETNAME              104

```



Beachten Sie, dass Sie auch die Ressourcennummer von APS **\_ \_ NEXT \_ SYMED \_ VALUE** in 106 ändern müssen.

## <a name="resource-file"></a>Ressourcendatei

Die folgenden Zeichenfolgen müssen in der Datei "Glowdll.rc" geändert werden, um drei Voreinstellungen zu ermöglichen und ihnen Namen zu geben:


```C++
    IDS_REDPRESETNAME       "Glow Red"
    IDS_GREENPRESETNAME     "Glow Green"
    IDS_BLUEPRESETNAME      "Glow Blue"

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**The Glow Sample**](the-glow-sample.md)
</dt> </dl>

 

 




