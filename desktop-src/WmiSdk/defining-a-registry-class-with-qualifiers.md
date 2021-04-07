---
description: Die zum Speichern von Registrierungsdaten verwendeten Klassen werden mit mehreren Standard Qualifizierern definiert.
ms.assetid: d4786880-6c50-4e36-9a16-47de430e77a9
ms.tgt_platform: multiple
title: Definieren einer Registrierungs Klasse mit Qualifizierern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f45fdff611814eadbf57eabedf7444d098666918
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864027"
---
# <a name="defining-a-registry-class-with-qualifiers"></a>Definieren einer Registrierungs Klasse mit Qualifizierern

Die zum Speichern von Registrierungsdaten verwendeten Klassen werden mit mehreren Standard Qualifizierern definiert.

Im folgenden finden Sie eine Liste der Standard Qualifizierer:

-   [Dynamischer](standard-wmi-qualifiers.md) und- [ **Anbieter**](/windows/desktop/api/Provider/nl-provider-provider)

    Sie können den **dynamischen** Qualifizierer entweder an eine Klasse oder eine Instanz anfügen. Der **dynamische** Qualifizierer kennzeichnet die Klasse oder Instanz als dynamisch von einem Anbieter verwaltet. Wenn **Dynamic** für eine Klasse oder eine Instanz angezeigt wird, muss der [**Anbieter Qualifizierer**](/windows/desktop/api/Provider/nl-provider-provider) ebenfalls angezeigt werden. Der **Anbieter Qualifizierer** identifiziert den bestimmten Anbieter, der die dynamische Klasse oder Instanz verwalten muss.

-   [ClassContext](standard-wmi-qualifiers.md)

    Der **ClassContext** -Qualifizierer ist an eine Klasse angefügt. Gibt den Pfad zum Registrierungsschlüssel an, der die Informationen enthält, die die Klasse darstellt.

    Der **ClassContext** -Qualifizierer weist das folgende Format auf.

    ``` syntax
    MACHINE_NAME|Subtree\\KeyPath
    ```

    Der Wert für KEYPATH kann lang sein, wenn er Schlüssel mit unter Schlüsseln enthält.

    Das folgende Beispiel zeigt den **ClassContext** -Qualifizierer, der den Pfad zu einem bestimmten Computer Transportgerät enthält.

    ``` syntax
    Machine_Name|HKEY_LOCAL_MACHINE\\SOFTWARE\\MICROSOFT\\WBEM\\TRANSPORTS
    ```

Die folgende Vorlage für eine Klassendefinition veranschaulicht die Verwendung der [**Qualifizierer**](/windows/desktop/api/Provider/nl-provider-provider)" **Dynamic**", "Provider" und " **ClassContext** ". Der vom **Anbieter** Qualifizierer benannte Anbieter ist der instanzsystemregistrierungs-Anbieter. Beachten Sie, dass bei Registrierungs Pfaden die Groß-/Kleinschreibung nicht beachtet wird.

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

Verwaltungs Anwendungen können auch den System Registrierungs Anbieter verwenden, um Registrierungsdaten für einen bestimmten Schlüssel abzurufen und zu ändern.

 

 



