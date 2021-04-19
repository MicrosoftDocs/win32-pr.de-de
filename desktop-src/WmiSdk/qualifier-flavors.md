---
description: Qualifizierervarianten bieten weitere Informationen zu einem Qualifizierer, z. b. ob eine abgeleitete Klasse oder eine Instanz den ursprünglichen Wert des Qualifizierers über
ms.assetid: 6a0769ac-e16c-45e1-92b6-26e4969bf23d
ms.tgt_platform: multiple
title: Qualifizierervarianten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec8ddf6c2daea59931e533174c532e3d07b147a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352338"
---
# <a name="qualifier-flavors"></a><span data-ttu-id="c6136-103">Qualifizierervarianten</span><span class="sxs-lookup"><span data-stu-id="c6136-103">Qualifier Flavors</span></span>

<span data-ttu-id="c6136-104">Qualifizierervarianten bieten weitere Informationen zu einem Qualifizierer, z. b. ob eine abgeleitete Klasse oder Instanz den ursprünglichen Wert des Qualifizierers überschreiben kann</span><span class="sxs-lookup"><span data-stu-id="c6136-104">Qualifier flavors provide more information about a qualifier, such as whether a derived class or instance can override the qualifier's original value.</span></span>

<span data-ttu-id="c6136-105">Qualifizierervarianten können am Anfang der MOF-Datei mithilfe der folgenden Syntax hinzugefügt werden, wodurch Sie in der gesamten Definition angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6136-105">Qualifier flavors may be added to the top of the MOF file, using the following syntax, causing them to be applied throughout the definition.</span></span> <span data-ttu-id="c6136-106">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="c6136-106">For example:</span></span>

``` syntax
Qualifier Description : ToSubClass Amended;
```

<span data-ttu-id="c6136-107">Die unter **Klasse** und die **geänderten** Varianten gelten für alle **Beschreibungs** Qualifizierer in der MOF-Datei.</span><span class="sxs-lookup"><span data-stu-id="c6136-107">The **ToSubClass** and **Amended** flavors applies to all the **Description** qualifiers in the MOF.</span></span>

<span data-ttu-id="c6136-108">In der folgenden Tabelle sind die qualifizierervarianten aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="c6136-108">The following table lists the qualifier flavors.</span></span>



| <span data-ttu-id="c6136-109">Qualifiziererkonfiguration</span><span class="sxs-lookup"><span data-stu-id="c6136-109">Qualifier Flavor</span></span>    | <span data-ttu-id="c6136-110">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c6136-110">Meaning</span></span>                                                                                                                                                                                                                                         |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6136-111">**Abge**</span><span class="sxs-lookup"><span data-stu-id="c6136-111">**Amended**</span></span>         | <span data-ttu-id="c6136-112">Der Qualifizierer ist in der Basisklassendefinition nicht erforderlich und kann zur Lokalisierung in die Ergänzung verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="c6136-112">The qualifier is not required in the basic class definition and can be moved to the amendment to be localized.</span></span>                                                                                                                                  |
| <span data-ttu-id="c6136-113">**DisableOverride**</span><span class="sxs-lookup"><span data-stu-id="c6136-113">**DisableOverride**</span></span> | <span data-ttu-id="c6136-114">Der Qualifizierer kann in einer abgeleiteten Klasse oder Instanz nicht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="c6136-114">The qualifier cannot be overridden in a derived class or instance.</span></span> <span data-ttu-id="c6136-115">Beachten Sie, dass das Überschreiben eines weitergegebenen Qualifizierers die Standardeinstellung ist.</span><span class="sxs-lookup"><span data-stu-id="c6136-115">Note that being able to override a propagated qualifier is the default.</span></span>                                                                                                      |
| <span data-ttu-id="c6136-116">**EnableOverride**</span><span class="sxs-lookup"><span data-stu-id="c6136-116">**EnableOverride**</span></span>  | <span data-ttu-id="c6136-117">Bei der Weitergabe an eine abgeleitete Klasse oder eine abgeleitete Instanz kann der Wert des Qualifizierers überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="c6136-117">When propagated to a derived class or instance, the value of the qualifier can be overridden.</span></span> <span data-ttu-id="c6136-118">Das Festlegen von **EnableOverride** ist optional, da der qualifiziererwert überschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="c6136-118">Setting **EnableOverride** is optional because being able to override the qualifier value is the default functionality for propagated qualifiers.</span></span> |
| <span data-ttu-id="c6136-119">**Notat instance**</span><span class="sxs-lookup"><span data-stu-id="c6136-119">**NotToInstance**</span></span>   | <span data-ttu-id="c6136-120">Der Qualifizierer wird nicht an Klassen Instanzen weitergegeben.</span><span class="sxs-lookup"><span data-stu-id="c6136-120">The qualifier is not propagated to class instances.</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="c6136-121">**NotTo subclass**</span><span class="sxs-lookup"><span data-stu-id="c6136-121">**NotToSubClass**</span></span>   | <span data-ttu-id="c6136-122">Der Q wird nicht an abgeleitete Klassen weitergegeben.</span><span class="sxs-lookup"><span data-stu-id="c6136-122">The qualifier is not propagated to derived classes.</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="c6136-123">**Eingeschränkt**</span><span class="sxs-lookup"><span data-stu-id="c6136-123">**Restricted**</span></span>      | <span data-ttu-id="c6136-124">Der Qualifizierer wird nicht an-Instanzen oder abgeleitete Klassen weitergegeben.</span><span class="sxs-lookup"><span data-stu-id="c6136-124">The qualifier is not propagated to instances or derived classes.</span></span>                                                                                                                                                                                |
| <span data-ttu-id="c6136-125">**Instanz von**</span><span class="sxs-lookup"><span data-stu-id="c6136-125">**ToInstance**</span></span>      | <span data-ttu-id="c6136-126">Der Qualifizierer wird an Instanzen weitergegeben.</span><span class="sxs-lookup"><span data-stu-id="c6136-126">The qualifier is propagated to instances.</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="c6136-127">**ToSubClass**</span><span class="sxs-lookup"><span data-stu-id="c6136-127">**ToSubClass**</span></span>      | <span data-ttu-id="c6136-128">Der Qualifizierer wird an abgeleitete Klassen weitergegeben.</span><span class="sxs-lookup"><span data-stu-id="c6136-128">The qualifier is propagated to derived classes.</span></span> <span data-ttu-id="c6136-129">Diese Konfiguration eignet sich nur für Qualifizierer, die für eine Klasse definiert sind, und kann nicht an einen Qualifizierer angehängt werden, der eine Klasseninstanz</span><span class="sxs-lookup"><span data-stu-id="c6136-129">This flavor is only appropriate for qualifiers defined for a class and cannot be attached to a qualifier describing a class instance.</span></span>                                                           |



 

 

 



