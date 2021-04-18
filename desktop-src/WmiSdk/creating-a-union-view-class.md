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
# <a name="creating-a-union-view-class"></a><span data-ttu-id="6701a-104">Erstellen einer Union-Ansichts Klasse</span><span class="sxs-lookup"><span data-stu-id="6701a-104">Creating a Union View Class</span></span>

<span data-ttu-id="6701a-105">Eine Union-Ansichts Klasse ist eine logische Union von Quell Klassen Instanzen.</span><span class="sxs-lookup"><span data-stu-id="6701a-105">A union view class is a logical union of source class instances.</span></span> <span data-ttu-id="6701a-106">Eine Union-Ansichts Klasse enthält alle Instanzen der Quell Klassen, es sei denn, Sie beschränken die Instanzen, indem Sie eine WHERE-Klausel in die Quell Abfrage einschließen.</span><span class="sxs-lookup"><span data-stu-id="6701a-106">A union view class includes all the instances of the source classes unless you limit the instances by including a WHERE clause on the source query.</span></span>

<span data-ttu-id="6701a-107">Union-Ansichts Klassen sind nützlich, wenn Sie Instanzen ähnlicher oder identischer Klassen sehen möchten, die sich in verschiedenen Namespaces oder auf unterschiedlichen Computern befinden.</span><span class="sxs-lookup"><span data-stu-id="6701a-107">Union view classes are useful when you want to see instances of similar or identical classes that are located in different namespaces or on different computers.</span></span> <span data-ttu-id="6701a-108">Sie können z. b. eine Union-Klasse erstellen, die Instanzen verschiedener zu über Wachender Laufwerke enthält.</span><span class="sxs-lookup"><span data-stu-id="6701a-108">For example, you can create a union class that contains instances of different disk drives to monitor.</span></span>

<span data-ttu-id="6701a-109">Sie können auch die Eigenschaften einer Union-Ansichts Klasse auf Eigenschaften basieren, die nicht in allen Quell Klassen Instanzen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="6701a-109">You can also base the properties of a union view class on properties not present in all of the source class instances.</span></span> <span data-ttu-id="6701a-110">Wenn die Quell Klassen Instanzen nicht über dieselbe Eigenschaft verfügen, weisen die Eigenschaften von Union-Klassen Instanzen den Wert **null** auf.</span><span class="sxs-lookup"><span data-stu-id="6701a-110">If the source class instances do not have the same property, the properties of union class instances have a value of **NULL**.</span></span> <span data-ttu-id="6701a-111">Wenn z. b. ein Festplattenlaufwerk eine **Temperatur** Eigenschaft hat, aber eine andere nicht, können Sie dennoch eine Union zwischen den beiden erstellen.</span><span class="sxs-lookup"><span data-stu-id="6701a-111">For example, if one hard disk drive has a **temperature** property but another does not, you can still create a union between the two.</span></span>

<span data-ttu-id="6701a-112">Im folgenden Verfahren wird beschrieben, wie eine Union-Ansichts Klasse erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="6701a-112">The following procedure describes how to create a union view class.</span></span>

<span data-ttu-id="6701a-113">**So erstellen Sie eine Union-Ansichts Klasse**</span><span class="sxs-lookup"><span data-stu-id="6701a-113">**To create a union view class**</span></span>

1.  <span data-ttu-id="6701a-114">Beginnen Sie die Klassendefinition mit dem [**Union**](qualifiers-specific-to-the-view-provider.md) -Zeichen folgen Qualifizierer.</span><span class="sxs-lookup"><span data-stu-id="6701a-114">Begin your class definition with the [**Union**](qualifiers-specific-to-the-view-provider.md) string qualifier.</span></span>

    <span data-ttu-id="6701a-115">Die Qualifizierer [**joinon**](qualifiers-specific-to-the-view-provider.md), **Association** und **Union** schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="6701a-115">The [**JoinOn**](qualifiers-specific-to-the-view-provider.md), **Association**, and **Union** qualifiers are mutually exclusive.</span></span>

2.  <span data-ttu-id="6701a-116">Erstellen Sie die Abfragen, die die in der Ansichts Klasse verwendeten Quell Klassen mit dem [**viewsources**](viewsources-qualifier.md) -Qualifizierer definieren.</span><span class="sxs-lookup"><span data-stu-id="6701a-116">Create the queries that define source classes used in the view class with the [**ViewSources**](viewsources-qualifier.md) qualifier.</span></span>
3.  <span data-ttu-id="6701a-117">Definieren Sie die Namen und den Speicherort der Namespaces, in denen sich die Quell Klassen mit dem [**viewspaces**](viewspaces-qualifier.md) -Qualifizierer befinden.</span><span class="sxs-lookup"><span data-stu-id="6701a-117">Define the names and location of the namespaces in which the source classes are located with the [**ViewSpaces**](viewspaces-qualifier.md) qualifier.</span></span>
4.  <span data-ttu-id="6701a-118">Definieren Sie die Eigenschaften, die den Eigenschaften in den Quell Klassen mit dem [**propertysources**](propertysources-qualifier.md) -Qualifizierer zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="6701a-118">Define the properties that map to the properties in the source classes with the [**PropertySources**](propertysources-qualifier.md) qualifier.</span></span>

    <span data-ttu-id="6701a-119">Bei Bedarf können Sie jede der Eigenschaften mit dem [**hiddendefault-Qualifizierer**](qualifiers-specific-to-the-view-provider.md) als zu einer Quell Klasse gehörend markieren.</span><span class="sxs-lookup"><span data-stu-id="6701a-119">If necessary, you can tag any of the properties as belonging to a source class by using the [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) qualifier.</span></span>

5.  <span data-ttu-id="6701a-120">Definieren Sie die Schlüsseleigenschaften der Quell Klassen der Union-Ansichts Klasse.</span><span class="sxs-lookup"><span data-stu-id="6701a-120">Define the key properties of the source classes of your union view class.</span></span>

    <span data-ttu-id="6701a-121">Jede Quell Klasse muss die gleiche Anzahl von Schlüsseleigenschaften aufweisen, die mit [**CimType**](swbemproperty-cimtype.md)übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="6701a-121">Each source class must have the same number of key properties matched by [**CIMType**](swbemproperty-cimtype.md).</span></span> <span data-ttu-id="6701a-122">Außerdem müssen die Schlüssel der Union-Ansichts Klasse alle Quell Instanzen eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="6701a-122">Also, the keys of your union view class must uniquely identify all source instances.</span></span> <span data-ttu-id="6701a-123">In einigen Fällen müssen Sie möglicherweise Systemeigenschaften angeben, um sicherzustellen, dass die Instanzen eindeutig sind.</span><span class="sxs-lookup"><span data-stu-id="6701a-123">In some cases, you might need to specify system properties to ensure that instances are unique.</span></span> <span data-ttu-id="6701a-124">Wenn Sie z. b. eine Sicht aus der Vereinigung zweier identischer Klassen in zwei verschiedenen Namespaces erstellen, können Sie die [**\_ \_ Namespace**](--namespace.md) -Eigenschaft als Schlüssel in die Ansichts Klasse einschließen, um zwischen den beiden Instanzen zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="6701a-124">For example, if you create a view from the union of two identical classes in two different namespaces, you could include the [**\_\_Namespace**](--namespace.md) property as a key in the view class to differentiate between the two instances.</span></span> <span data-ttu-id="6701a-125">Wenn Sie zwei ähnliche Klassen desselben Namespace verwenden, um eine Ansicht zu erstellen, können Sie die- **\_ \_ Klassen** Eigenschaft verwenden, um zwischen den beiden zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="6701a-125">If you use two similar classes from the same namespace to create a view, you could use the **\_\_Class** property to distinguish between the two.</span></span> <span data-ttu-id="6701a-126">Benennen Sie alle Systemeigenschaften in der Sicht um, um einen Konflikt mit den Systemeigenschaften der Ansichts Klasse zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="6701a-126">Rename any system properties in the view so you can avoid a conflict with the system properties of the view class.</span></span>

6.  <span data-ttu-id="6701a-127">Definieren Sie alle gewünschten Methoden mit dem [**methodsource**](qualifiers-specific-to-the-view-provider.md) -Qualifizierer.</span><span class="sxs-lookup"><span data-stu-id="6701a-127">Define any methods you want using the [**MethodSource**](qualifiers-specific-to-the-view-provider.md) qualifier.</span></span>

    <span data-ttu-id="6701a-128">Im Gegensatz zu anderen Ansichts Klassen können Sie Methoden erstellen, um eine Union-Ansicht zu ändern.</span><span class="sxs-lookup"><span data-stu-id="6701a-128">Unlike other view classes, you can create methods to modify a union view.</span></span>

<span data-ttu-id="6701a-129">Im folgenden Codebeispiel wird eine Union-Ansichts Klasse beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6701a-129">The following code example describes a union view class.</span></span>

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

 

 



