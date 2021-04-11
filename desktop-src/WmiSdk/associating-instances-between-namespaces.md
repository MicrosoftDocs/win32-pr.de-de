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
# <a name="associating-instances-between-namespaces"></a>Zuordnen von Instanzen zwischen Namespaces

Eine Zuordnungs Ansichts Klasse ermöglicht es Ihnen, [assoziatoren von](associators-of-statement.md) Abfragen für Klassen zu verwenden, die sich in verschiedenen Namespaces befinden.

Im folgenden Verfahren wird beschrieben, wie Instanzen zwischen Namespaces zugeordnet werden.

**So ordnen Sie Instanzen zwischen Namespaces zu**

1.  Beginnen Sie die Klassendefinition mit dem Qualifizierer der [**Assoziations**](meta-qualifiers.md) Zeichenfolge

    Die Qualifizierer **joinon**, [**Association**](meta-qualifiers.md)und **Union** schließen sich gegenseitig aus.

2.  Erstellen Sie die Abfragen, die die in der Ansichts Klasse verwendeten Quell Instanzen mit dem [**viewsources**](viewsources-qualifier.md) -Qualifizierer definieren.
3.  Definieren Sie die Namen und den Speicherort der Namespaces, in denen sich die Quell Instanzen mit dem [**viewspaces**](viewspaces-qualifier.md) -Qualifizierer befinden.
4.  Definieren Sie die gewünschten Eigenschaften in der Zuordnungs Ansichts Klasse mit dem [**propertysources**](propertysources-qualifier.md) -Qualifizierer.

    Bei Bedarf können Sie jede der Eigenschaften mit dem [**hiddendefault-Qualifizierer**](qualifiers-specific-to-the-view-provider.md) als zu einer Quell Klasse gehörend markieren.

5.  Markieren Sie alle relevanten Eigenschaften mit dem **direkten** Qualifizierer.

    Der **direkte** Qualifizierer verhindert, dass der Ansichts Anbieter den markierten Zuordnungs Verweis einem Sicht Verweis zuordnet.

In den folgenden Codebeispielen wird gezeigt, wie Zuordnungs Ansichts Klassen erstellt werden.

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

 

 



