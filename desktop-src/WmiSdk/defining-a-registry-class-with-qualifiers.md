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
# <a name="defining-a-registry-class-with-qualifiers"></a><span data-ttu-id="ab3cc-103">Definieren einer Registrierungs Klasse mit Qualifizierern</span><span class="sxs-lookup"><span data-stu-id="ab3cc-103">Defining a Registry Class With Qualifiers</span></span>

<span data-ttu-id="ab3cc-104">Die zum Speichern von Registrierungsdaten verwendeten Klassen werden mit mehreren Standard Qualifizierern definiert.</span><span class="sxs-lookup"><span data-stu-id="ab3cc-104">The classes used to hold registry data are defined with several standard qualifiers.</span></span>

<span data-ttu-id="ab3cc-105">Im folgenden finden Sie eine Liste der Standard Qualifizierer:</span><span class="sxs-lookup"><span data-stu-id="ab3cc-105">The following is a list of the standard qualifiers:</span></span>

-   <span data-ttu-id="ab3cc-106">[Dynamischer](standard-wmi-qualifiers.md) und- [ **Anbieter**](/windows/desktop/api/Provider/nl-provider-provider)</span><span class="sxs-lookup"><span data-stu-id="ab3cc-106">[Dynamic](standard-wmi-qualifiers.md) and [**Provider**](/windows/desktop/api/Provider/nl-provider-provider)</span></span>

    <span data-ttu-id="ab3cc-107">Sie können den **dynamischen** Qualifizierer entweder an eine Klasse oder eine Instanz anfügen.</span><span class="sxs-lookup"><span data-stu-id="ab3cc-107">You can attach the **Dynamic** qualifier to either a class or an instance.</span></span> <span data-ttu-id="ab3cc-108">Der **dynamische** Qualifizierer kennzeichnet die Klasse oder Instanz als dynamisch von einem Anbieter verwaltet.</span><span class="sxs-lookup"><span data-stu-id="ab3cc-108">The **Dynamic** qualifier marks the class or instance as managed dynamically by a provider.</span></span> <span data-ttu-id="ab3cc-109">Wenn **Dynamic** für eine Klasse oder eine Instanz angezeigt wird, muss der [**Anbieter Qualifizierer**](/windows/desktop/api/Provider/nl-provider-provider) ebenfalls angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ab3cc-109">When **Dynamic** appears on a class or instance, the [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier must also appear.</span></span> <span data-ttu-id="ab3cc-110">Der **Anbieter Qualifizierer** identifiziert den bestimmten Anbieter, der die dynamische Klasse oder Instanz verwalten muss.</span><span class="sxs-lookup"><span data-stu-id="ab3cc-110">The **Provider** qualifier identifies the particular provider that must manage the dynamic class or instance.</span></span>

-   [<span data-ttu-id="ab3cc-111">ClassContext</span><span class="sxs-lookup"><span data-stu-id="ab3cc-111">ClassContext</span></span>](standard-wmi-qualifiers.md)

    <span data-ttu-id="ab3cc-112">Der **ClassContext** -Qualifizierer ist an eine Klasse angefügt.</span><span class="sxs-lookup"><span data-stu-id="ab3cc-112">The **ClassContext** qualifier is attached to a class.</span></span> <span data-ttu-id="ab3cc-113">Gibt den Pfad zum Registrierungsschlüssel an, der die Informationen enthält, die die Klasse darstellt.</span><span class="sxs-lookup"><span data-stu-id="ab3cc-113">It specifies the path to the registry key that contains the information the class represents.</span></span>

    <span data-ttu-id="ab3cc-114">Der **ClassContext** -Qualifizierer weist das folgende Format auf.</span><span class="sxs-lookup"><span data-stu-id="ab3cc-114">The **ClassContext** qualifier has the following format.</span></span>

    ``` syntax
    MACHINE_NAME|Subtree\\KeyPath
    ```

    <span data-ttu-id="ab3cc-115">Der Wert für KEYPATH kann lang sein, wenn er Schlüssel mit unter Schlüsseln enthält.</span><span class="sxs-lookup"><span data-stu-id="ab3cc-115">The value for KeyPath can be long if it includes keys with subkeys.</span></span>

    <span data-ttu-id="ab3cc-116">Das folgende Beispiel zeigt den **ClassContext** -Qualifizierer, der den Pfad zu einem bestimmten Computer Transportgerät enthält.</span><span class="sxs-lookup"><span data-stu-id="ab3cc-116">The following example shows the **ClassContext** qualifier that contains the path to a particular computer transport device.</span></span>

    ``` syntax
    Machine_Name|HKEY_LOCAL_MACHINE\\SOFTWARE\\MICROSOFT\\WBEM\\TRANSPORTS
    ```

<span data-ttu-id="ab3cc-117">Die folgende Vorlage für eine Klassendefinition veranschaulicht die Verwendung der [**Qualifizierer**](/windows/desktop/api/Provider/nl-provider-provider)" **Dynamic**", "Provider" und " **ClassContext** ".</span><span class="sxs-lookup"><span data-stu-id="ab3cc-117">The following template for a class definition illustrates the use of the **Dynamic**, [**Provider**](/windows/desktop/api/Provider/nl-provider-provider), and **ClassContext** qualifiers.</span></span> <span data-ttu-id="ab3cc-118">Der vom **Anbieter** Qualifizierer benannte Anbieter ist der instanzsystemregistrierungs-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="ab3cc-118">The provider named by the **Provider** qualifier is the instance System Registry provider.</span></span> <span data-ttu-id="ab3cc-119">Beachten Sie, dass bei Registrierungs Pfaden die Groß-/Kleinschreibung nicht beachtet wird.</span><span class="sxs-lookup"><span data-stu-id="ab3cc-119">Be aware that registry paths are case-insensitive, as are qualifier names.</span></span>

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

<span data-ttu-id="ab3cc-120">Verwaltungs Anwendungen können auch den System Registrierungs Anbieter verwenden, um Registrierungsdaten für einen bestimmten Schlüssel abzurufen und zu ändern.</span><span class="sxs-lookup"><span data-stu-id="ab3cc-120">Management applications can also use the System Registry provider to retrieve and modify registry data for a particular key.</span></span>

 

 



