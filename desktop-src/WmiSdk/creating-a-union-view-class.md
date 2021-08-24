---
description: Eine Union-Ansichtsklasse ist eine logische Vereinigung von Quellklasseninstanzen. Eine Union-Ansichtsklasse enthält alle Instanzen der Quellklassen, es sei denn, Sie beschränken die Instanzen, indem Sie eine WHERE-Klausel in die Quellabfrage einschließen.
ms.assetid: 54a9804d-644d-4ab6-a3d5-c9c4f7761967
ms.tgt_platform: multiple
title: Erstellen einer Union-Ansichtsklasse
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3408e3aaec9ee809711b3f400c77ffab5ab2b376eaace3311bd0367f61937c30
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612390"
---
# <a name="creating-a-union-view-class"></a>Erstellen einer Union-Ansichtsklasse

Eine Union-Ansichtsklasse ist eine logische Vereinigung von Quellklasseninstanzen. Eine Union-Ansichtsklasse enthält alle Instanzen der Quellklassen, es sei denn, Sie beschränken die Instanzen, indem Sie eine WHERE-Klausel in die Quellabfrage einschließen.

Union-Ansichtsklassen sind nützlich, wenn Sie Instanzen ähnlicher oder identischer Klassen anzeigen möchten, die sich in unterschiedlichen Namespaces oder auf verschiedenen Computern befinden. Sie können z. B. eine Union-Klasse erstellen, die Instanzen von verschiedenen Datenträgerlaufwerken enthält, die überwacht werden sollen.

Sie können die Eigenschaften einer Union-Ansichtsklasse auch auf Eigenschaften basieren, die nicht in allen Quellklasseninstanzen vorhanden sind. Wenn die Quellklasseninstanzen nicht über die gleiche Eigenschaft verfügen, weisen die Eigenschaften von Union-Klasseninstanzen den Wert **NULL** auf. Wenn beispielsweise ein Festplattenlaufwerk über eine **Temperatureigenschaft** verfügt, die andere jedoch nicht, können Sie trotzdem eine Union zwischen den beiden erstellen.

Im folgenden Verfahren wird beschrieben, wie eine Union-Ansichtsklasse erstellt wird.

**So erstellen Sie eine Union-Ansichtsklasse**

1.  Beginnen Sie ihre [](qualifiers-specific-to-the-view-provider.md) Klassendefinition mit dem Union-Zeichenfolgenqualifizierer.

    Die [**JoinOn-,**](qualifiers-specific-to-the-view-provider.md) **Association-** und Union-Qualifizierer schließen sich gegenseitig aus. 

2.  Erstellen Sie mit dem ViewSources-Qualifizierer die Abfragen, die Quellklassen definieren, die in der [**Ansichtsklasse**](viewsources-qualifier.md) verwendet werden.
3.  Definieren Sie mit dem ViewSpaces-Qualifizierer die Namen und den Speicherort der [**Namespaces,**](viewspaces-qualifier.md) in denen sich die Quellklassen befinden.
4.  Definieren Sie die Eigenschaften, die den Eigenschaften in den Quellklassen zugeordnet sind, mit dem [**PropertySources-Qualifizierer.**](propertysources-qualifier.md)

    Bei Bedarf können Sie jede der Eigenschaften mithilfe des [**HiddenDefault-Qualifizierers**](qualifiers-specific-to-the-view-provider.md) als zu einer Quellklasse gehörend markieren.

5.  Definieren Sie die Schlüsseleigenschaften der Quellklassen Ihrer Union-Ansichtsklasse.

    Jede Quellklasse muss über die gleiche Anzahl von Schlüsseleigenschaften verfügen, die mit [**CIMType**](swbemproperty-cimtype.md)übereinstimmen. Außerdem müssen die Schlüssel der Union-Ansichtsklasse alle Quellinstanzen eindeutig identifizieren. In einigen Fällen müssen Sie möglicherweise Systemeigenschaften angeben, um sicherzustellen, dass Instanzen eindeutig sind. Wenn Sie beispielsweise eine Ansicht aus der Vereinigung zweier identischer Klassen in zwei verschiedenen Namespaces erstellen, können Sie die [**\_ \_ Namespace-Eigenschaft**](--namespace.md) als Schlüssel in die Ansichtsklasse einschließen, um zwischen den beiden Instanzen zu unterscheiden. Wenn Sie zwei ähnliche Klassen aus demselben Namespace verwenden, um eine Sicht zu erstellen, können Sie die **\_ \_ Class-Eigenschaft** verwenden, um zwischen den beiden klassen zu unterscheiden. Benennen Sie alle Systemeigenschaften in der Ansicht um, damit Sie einen Konflikt mit den Systemeigenschaften der Ansichtsklasse vermeiden können.

6.  Definieren Sie alle gewünschten Methoden mit dem [**MethodSource-Qualifizierer.**](qualifiers-specific-to-the-view-provider.md)

    Im Gegensatz zu anderen Ansichtsklassen können Sie Methoden erstellen, um eine Union-Ansicht zu ändern.

Im folgenden Codebeispiel wird eine Union-Ansichtsklasse beschrieben.

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

 

 



