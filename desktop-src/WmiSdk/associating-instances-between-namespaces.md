---
description: Mit einer Zuordnungsansichtsklasse können Sie ASSOCIATORS OF-Abfragen für Klassen verwenden, die sich in verschiedenen Namespaces befinden.
ms.assetid: 4af4fe1b-2b19-472e-8261-798b374ae57e
ms.tgt_platform: multiple
title: Zuordnen von Instanzen zwischen Namespaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d743b835d28af4fe0a8dd5d09858b2ba6ff0abacd0f35219c3dd90d39d0810d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118557018"
---
# <a name="associating-instances-between-namespaces"></a>Zuordnen von Instanzen zwischen Namespaces

Mit einer Zuordnungsansichtsklasse können Sie [ASSOCIATORS OF-Abfragen](associators-of-statement.md) für Klassen verwenden, die sich in verschiedenen Namespaces befinden.

Im folgenden Verfahren wird beschrieben, wie Instanzen zwischen Namespaces zugeordnet werden.

**So ordnen Sie Instanzen zwischen Namespaces zu**

1.  Beginnen Sie ihre [](meta-qualifiers.md) Klassendefinition mit dem Zuordnungszeichenfolgen-Qualifizierer.

    Die **JoinOn-,** [**Association-**](meta-qualifiers.md)und Union-Qualifizierer schließen sich gegenseitig aus. 

2.  Erstellen Sie mit dem ViewSources-Qualifizierer die Abfragen, die Quellinstanzen definieren, die in der [**Ansichtsklasse**](viewsources-qualifier.md) verwendet werden.
3.  Definieren Sie die Namen und den Speicherort der Namespaces, in denen sich die Quellinstanzen befinden, mit dem [**ViewSpaces-Qualifizierer.**](viewspaces-qualifier.md)
4.  Definieren Sie die gewünschten Eigenschaften in der [**Zuordnungsansichtsklasse**](propertysources-qualifier.md) mit dem PropertySources-Qualifizierer.

    Bei Bedarf können Sie jede der Eigenschaften mithilfe des [**HiddenDefault-Qualifizierers**](qualifiers-specific-to-the-view-provider.md) als zu einer Quellklasse gehörend markieren.

5.  Markieren Sie alle  relevanten Eigenschaften mit dem Direct-Qualifizierer.

    Der **Direktqualifizierer** verhindert, dass der Ansichtsanbieter den markierten Zuordnungsverweis einem Ansichtsverweis zuzuordnen kann.

Die folgenden Codebeispiele zeigen, wie Zuordnungsansichtsklassen erstellt werden.

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

 

 



