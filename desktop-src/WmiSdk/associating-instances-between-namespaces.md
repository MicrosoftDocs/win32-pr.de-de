---
description: Eine Zuordnungs Ansichts Klasse ermöglicht es Ihnen, assoziatoren von Abfragen für Klassen zu verwenden, die sich in verschiedenen Namespaces befinden.
ms.assetid: 4af4fe1b-2b19-472e-8261-798b374ae57e
ms.tgt_platform: multiple
title: Zuordnen von Instanzen zwischen Namespaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8347d3a35f06f72d3344f5c12606d82709a1370
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346228"
---
# <a name="associating-instances-between-namespaces"></a><span data-ttu-id="ba2f0-103">Zuordnen von Instanzen zwischen Namespaces</span><span class="sxs-lookup"><span data-stu-id="ba2f0-103">Associating Instances Between Namespaces</span></span>

<span data-ttu-id="ba2f0-104">Eine Zuordnungs Ansichts Klasse ermöglicht es Ihnen, [assoziatoren von](associators-of-statement.md) Abfragen für Klassen zu verwenden, die sich in verschiedenen Namespaces befinden.</span><span class="sxs-lookup"><span data-stu-id="ba2f0-104">An association view class allows you to use [ASSOCIATORS OF](associators-of-statement.md) queries on classes that reside in different namespaces.</span></span>

<span data-ttu-id="ba2f0-105">Im folgenden Verfahren wird beschrieben, wie Instanzen zwischen Namespaces zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="ba2f0-105">The following procedure describes how to associate instances between namespaces.</span></span>

<span data-ttu-id="ba2f0-106">**So ordnen Sie Instanzen zwischen Namespaces zu**</span><span class="sxs-lookup"><span data-stu-id="ba2f0-106">**To associate instances between namespaces**</span></span>

1.  <span data-ttu-id="ba2f0-107">Beginnen Sie die Klassendefinition mit dem Qualifizierer der [**Assoziations**](meta-qualifiers.md) Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ba2f0-107">Begin your class definition with the [**Association**](meta-qualifiers.md) string qualifier.</span></span>

    <span data-ttu-id="ba2f0-108">Die Qualifizierer **joinon**, [**Association**](meta-qualifiers.md)und **Union** schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="ba2f0-108">The **JoinOn**, [**Association**](meta-qualifiers.md), and **Union** qualifiers are mutually exclusive.</span></span>

2.  <span data-ttu-id="ba2f0-109">Erstellen Sie die Abfragen, die die in der Ansichts Klasse verwendeten Quell Instanzen mit dem [**viewsources**](viewsources-qualifier.md) -Qualifizierer definieren.</span><span class="sxs-lookup"><span data-stu-id="ba2f0-109">Create the queries that define source instances used in the view class with the [**ViewSources**](viewsources-qualifier.md) qualifier.</span></span>
3.  <span data-ttu-id="ba2f0-110">Definieren Sie die Namen und den Speicherort der Namespaces, in denen sich die Quell Instanzen mit dem [**viewspaces**](viewspaces-qualifier.md) -Qualifizierer befinden.</span><span class="sxs-lookup"><span data-stu-id="ba2f0-110">Define the names and location of the namespaces in which the source instances are located with the [**ViewSpaces**](viewspaces-qualifier.md) qualifier.</span></span>
4.  <span data-ttu-id="ba2f0-111">Definieren Sie die gewünschten Eigenschaften in der Zuordnungs Ansichts Klasse mit dem [**propertysources**](propertysources-qualifier.md) -Qualifizierer.</span><span class="sxs-lookup"><span data-stu-id="ba2f0-111">Define the properties you want in your association view class with the [**PropertySources**](propertysources-qualifier.md) qualifier.</span></span>

    <span data-ttu-id="ba2f0-112">Bei Bedarf können Sie jede der Eigenschaften mit dem [**hiddendefault-Qualifizierer**](qualifiers-specific-to-the-view-provider.md) als zu einer Quell Klasse gehörend markieren.</span><span class="sxs-lookup"><span data-stu-id="ba2f0-112">If necessary, you can tag any of the properties as belonging to a source class by using the [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) qualifier.</span></span>

5.  <span data-ttu-id="ba2f0-113">Markieren Sie alle relevanten Eigenschaften mit dem **direkten** Qualifizierer.</span><span class="sxs-lookup"><span data-stu-id="ba2f0-113">Tag any relevant properties with the **Direct** qualifier.</span></span>

    <span data-ttu-id="ba2f0-114">Der **direkte** Qualifizierer verhindert, dass der Ansichts Anbieter den markierten Zuordnungs Verweis einem Sicht Verweis zuordnet.</span><span class="sxs-lookup"><span data-stu-id="ba2f0-114">The **Direct** qualifier prevents the View Provider from mapping the tagged association reference to a view reference.</span></span>

<span data-ttu-id="ba2f0-115">In den folgenden Codebeispielen wird gezeigt, wie Zuordnungs Ansichts Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="ba2f0-115">The following code examples show how to create association view classes.</span></span>

``` syntax
[union,
ViewSources {"SELECT * FROM Win32_OperatingSystem"},
    ViewSpaces {"\\\\.\\root\\cimv2"},
    dynamic, provider("MS_VIEW_INSTANCE_PROVIDER")
]
class Union_OS_For_AssociationExample
{
    [key, PropertySources{"Name"}]
    string Name;

    [PropertySources{"Version"}]
    string Version;

    [PropertySources{"BuildNumber"}]
    string BuildNumber;
};

[
Association,
ViewSources {"SELECT * FROM Win32_SystemOperatingSystem"}, 
ViewSpaces {"\\\\.\\root\\cimv2"},
dynamic, provider("MS_VIEW_INSTANCE_PROVIDER")
]
class Association_SystemViewOperatingSystem
{
    [Direct, key, PropertySources{"GroupComponent"}]
    Win32_ComputerSystem ref Computer;
    
    [key, PropertySources{"PartComponent"}]
    Union_OS_For_AssociationExample ref OperatingSystem;
};
```

 

 



