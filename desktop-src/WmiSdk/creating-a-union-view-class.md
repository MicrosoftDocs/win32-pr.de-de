---
description: Eine Union-Ansichts Klasse ist eine logische Union von Quell Klassen Instanzen. Eine Union-Ansichts Klasse enthält alle Instanzen der Quell Klassen, es sei denn, Sie beschränken die Instanzen, indem Sie eine WHERE-Klausel in die Quell Abfrage einschließen.
ms.assetid: 54a9804d-644d-4ab6-a3d5-c9c4f7761967
ms.tgt_platform: multiple
title: Erstellen einer Union-Ansichts Klasse
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2ff9327645828c3db78a82811831f058cc27f202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350890"
---
# <a name="creating-a-union-view-class"></a>Erstellen einer Union-Ansichts Klasse

Eine Union-Ansichts Klasse ist eine logische Union von Quell Klassen Instanzen. Eine Union-Ansichts Klasse enthält alle Instanzen der Quell Klassen, es sei denn, Sie beschränken die Instanzen, indem Sie eine WHERE-Klausel in die Quell Abfrage einschließen.

Union-Ansichts Klassen sind nützlich, wenn Sie Instanzen ähnlicher oder identischer Klassen sehen möchten, die sich in verschiedenen Namespaces oder auf unterschiedlichen Computern befinden. Sie können z. b. eine Union-Klasse erstellen, die Instanzen verschiedener zu über Wachender Laufwerke enthält.

Sie können auch die Eigenschaften einer Union-Ansichts Klasse auf Eigenschaften basieren, die nicht in allen Quell Klassen Instanzen vorhanden sind. Wenn die Quell Klassen Instanzen nicht über dieselbe Eigenschaft verfügen, weisen die Eigenschaften von Union-Klassen Instanzen den Wert **null** auf. Wenn z. b. ein Festplattenlaufwerk eine **Temperatur** Eigenschaft hat, aber eine andere nicht, können Sie dennoch eine Union zwischen den beiden erstellen.

Im folgenden Verfahren wird beschrieben, wie eine Union-Ansichts Klasse erstellt wird.

**So erstellen Sie eine Union-Ansichts Klasse**

1.  Beginnen Sie die Klassendefinition mit dem [**Union**](qualifiers-specific-to-the-view-provider.md) -Zeichen folgen Qualifizierer.

    Die Qualifizierer [**joinon**](qualifiers-specific-to-the-view-provider.md), **Association** und **Union** schließen sich gegenseitig aus.

2.  Erstellen Sie die Abfragen, die die in der Ansichts Klasse verwendeten Quell Klassen mit dem [**viewsources**](viewsources-qualifier.md) -Qualifizierer definieren.
3.  Definieren Sie die Namen und den Speicherort der Namespaces, in denen sich die Quell Klassen mit dem [**viewspaces**](viewspaces-qualifier.md) -Qualifizierer befinden.
4.  Definieren Sie die Eigenschaften, die den Eigenschaften in den Quell Klassen mit dem [**propertysources**](propertysources-qualifier.md) -Qualifizierer zugeordnet werden.

    Bei Bedarf können Sie jede der Eigenschaften mit dem [**hiddendefault-Qualifizierer**](qualifiers-specific-to-the-view-provider.md) als zu einer Quell Klasse gehörend markieren.

5.  Definieren Sie die Schlüsseleigenschaften der Quell Klassen der Union-Ansichts Klasse.

    Jede Quell Klasse muss die gleiche Anzahl von Schlüsseleigenschaften aufweisen, die mit [**CimType**](swbemproperty-cimtype.md)übereinstimmen. Außerdem müssen die Schlüssel der Union-Ansichts Klasse alle Quell Instanzen eindeutig identifizieren. In einigen Fällen müssen Sie möglicherweise Systemeigenschaften angeben, um sicherzustellen, dass die Instanzen eindeutig sind. Wenn Sie z. b. eine Sicht aus der Vereinigung zweier identischer Klassen in zwei verschiedenen Namespaces erstellen, können Sie die [**\_ \_ Namespace**](--namespace.md) -Eigenschaft als Schlüssel in die Ansichts Klasse einschließen, um zwischen den beiden Instanzen zu unterscheiden. Wenn Sie zwei ähnliche Klassen desselben Namespace verwenden, um eine Ansicht zu erstellen, können Sie die- **\_ \_ Klassen** Eigenschaft verwenden, um zwischen den beiden zu unterscheiden. Benennen Sie alle Systemeigenschaften in der Sicht um, um einen Konflikt mit den Systemeigenschaften der Ansichts Klasse zu vermeiden.

6.  Definieren Sie alle gewünschten Methoden mit dem [**methodsource**](qualifiers-specific-to-the-view-provider.md) -Qualifizierer.

    Im Gegensatz zu anderen Ansichts Klassen können Sie Methoden erstellen, um eine Union-Ansicht zu ändern.

Im folgenden Codebeispiel wird eine Union-Ansichts Klasse beschrieben.

``` syntax
[Union, ViewSources{"SELECT Description, DeviceID, __Namespace, FileSystem, FreeSpace, VolumeName FROM LocalDisk", 
    "SELECT Description, DeviceID, __Namespace, FileSystem, FreeSpace, VolumeName FROM RemoteDisk"}, 
    ViewSpaces{"\\\\.\\Root\\LocalNamespace","\\\\.\\Root\\RemoteNamespace"}, 
    dynamic: ToInstance, provider("MS_VIEW_INSTANCE_PROVIDER")]

class UnionOfDrives

{
    [PropertySources{"Description", "Description"}] string des;
    [PropertySources{"DeviceID", "DeviceID"}, key] String did;
    [PropertySources{"__Namespace", "__Namespace"}, key] String KEYID;
    [PropertySources{"FileSystem", "FileSystem"}] String fsystem ;
    [PropertySources{"FreeSpace", "FreeSpace"}] uint64 fspace;
    [PropertySources{"VolumeName", "VolumeName"}] String vname;
};
```

 

 



