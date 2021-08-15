---
description: Die Klassen, die zum Speichern von Registrierungsdaten verwendet werden, werden mit mehreren Standardqualifizierern definiert.
ms.assetid: d4786880-6c50-4e36-9a16-47de430e77a9
ms.tgt_platform: multiple
title: Definieren einer Registrierungsklasse mit Qualifizierern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f42e3c383a5d71d66c88f388aa1745f8a8324568a7fd85ac0f48e5e2cff30e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117925226"
---
# <a name="defining-a-registry-class-with-qualifiers"></a>Definieren einer Registrierungsklasse mit Qualifizierern

Die Klassen, die zum Speichern von Registrierungsdaten verwendet werden, werden mit mehreren Standardqualifizierern definiert.

Es folgt eine Liste der Standardqualifizierer:

-   [Dynamisch](standard-wmi-qualifiers.md) und [ **Anbieter**](/windows/desktop/api/Provider/nl-provider-provider)

    Sie können den **dynamischen** Qualifizierer entweder an eine Klasse oder eine Instanz anfügen. Der **dynamische** Qualifizierer markiert die Klasse oder Instanz als dynamisch von einem Anbieter verwaltet. Wenn **Dynamisch** für eine Klasse oder Instanz angezeigt wird, muss auch der [**Anbieterqualifizierer**](/windows/desktop/api/Provider/nl-provider-provider) angezeigt werden. Der **Anbieterqualifizierer** identifiziert den bestimmten Anbieter, der die dynamische Klasse oder Instanz verwalten muss.

-   [ClassContext](standard-wmi-qualifiers.md)

    Der **ClassContext-Qualifizierer** wird an eine Klasse angefügt. Er gibt den Pfad zum Registrierungsschlüssel an, der die Informationen enthält, die die Klasse darstellt.

    Der **ClassContext-Qualifizierer** hat das folgende Format.

    ``` syntax
    MACHINE_NAME|Subtree\\KeyPath
    ```

    Der Wert für KeyPath kann lang sein, wenn er Schlüssel mit Unterschlüsseln enthält.

    Das folgende Beispiel zeigt den **ClassContext-Qualifizierer,** der den Pfad zu einem bestimmten Computertransportgerät enthält.

    ``` syntax
    Machine_Name|HKEY_LOCAL_MACHINE\\SOFTWARE\\MICROSOFT\\WBEM\\TRANSPORTS
    ```

Die folgende Vorlage für eine Klassendefinition veranschaulicht die Verwendung der **Qualifizierer Dynamic,** [**Provider**](/windows/desktop/api/Provider/nl-provider-provider)und **ClassContext.** Der vom **Anbieterqualifizierer** benannte Anbieter ist der Systemregistrierungsanbieter der Instanz. Beachten Sie, dass bei Registrierungspfaden die Groß-/Kleinschreibung nicht beachtet wird, ebenso wie bei Qualifizierernamen.

``` syntax
[dynamic, provider("RegProv"), 
    ClassContext("local|hkey_local_machine\\software\\microsoft
    \\WBEM\\transports\\Network Transport Modules")]

class RegTrans
{
  [key] string  TransportsGUID;
  [PropertyContext("Name")] string Name;
  [PropertyContext("Independent")] uint32 Enabled;
};
```

Verwaltungsanwendungen können auch den Systemregistrierungsanbieter verwenden, um Registrierungsdaten für einen bestimmten Schlüssel abzurufen und zu ändern.

 

 



