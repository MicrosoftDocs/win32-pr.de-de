---
title: Ändern von Voreinstellungen
description: Ändern von Voreinstellungen
ms.assetid: f8a5565d-676b-4679-a4cb-4bd7551cf41c
keywords:
- Visualisierungen, Glüh Beispiel
- benutzerdefinierte Visualisierungen, Glüh Beispiel
- Programmier Handbuch, Visualisierungen
- Beispiele, Glanz Visualisierung
- Beispiel für Glanz Visualisierung
- Visualisierungen, Voreinstellungen
- benutzerdefinierte Visualisierungen, Voreinstellungen
- Voreinstellungen in Visualisierungen, Glüh Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d24841c95c3fc1029aa0c405e90b329799fdbe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342053"
---
# <a name="changing-presets"></a>Ändern von Voreinstellungen

Die folgenden vordefinierten Code Abschnitte wurden so geändert, dass Sie drei Voreinstellungen zulassen:

## <a name="getpresettitle"></a>Getpresettitle

Dieser Code wurde anstelle des generierten voreingestellten Codes eingefügt:


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

Die folgende Enumeration in "Glow. h" wurde so geändert, dass drei Voreinstellungen zulässig sind:


```C++
enum {
    PRESET_RED = 0,
    PRESET_GREEN,
    PRESET_BLUE,
    PRESET_COUNT
};

```



## <a name="resource-header"></a>Ressourcen Header

Die folgenden Ressourcen wurden in "Resource. h" definiert, um drei Voreinstellungen zuzulassen:


```C++
#define IDS_REDPRESETNAME               102
#define IDS_GREENPRESETNAME             103
#define IDS_BLUEPRESETNAME              104

```



Beachten Sie, dass Sie auch die Ressourcen Anzahl von **\_ APS \_ Next \_ symed \_ value** in 106 ändern müssen.

## <a name="resource-file"></a>Ressourcendatei

Die folgenden Zeichen folgen müssen in der Datei "glowdll. RC" geändert werden, um drei Voreinstellungen zuzulassen und Ihnen Namen zu geben:


```C++
    IDS_REDPRESETNAME       "Glow Red"
    IDS_GREENPRESETNAME     "Glow Green"
    IDS_BLUEPRESETNAME      "Glow Blue"

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Das Glüh Beispiel**](the-glow-sample.md)
</dt> </dl>

 

 




