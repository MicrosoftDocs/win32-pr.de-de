---
description: Sie können eine einfache Instanz einer Klasse im Windows-Verwaltungsdienst mit Managed Object Format (MOF) deklarieren. Sie können auch die Standardwerte für eine Instanz überschreiben. Weitere Informationen finden Sie unter Festlegen des Eigenschafts Werts einer Instanz.
ms.assetid: 12eda062-9614-455d-ae99-7706c685137b
ms.tgt_platform: multiple
title: Erstellen einer Instanz mit MOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5078c5fcddaab4e8437a33e8cb3210d515360fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343435"
---
# <a name="creating-an-instance-using-mof"></a><span data-ttu-id="ff0b4-105">Erstellen einer Instanz mit MOF</span><span class="sxs-lookup"><span data-stu-id="ff0b4-105">Creating an Instance Using MOF</span></span>

<span data-ttu-id="ff0b4-106">Sie können eine einfache Instanz einer Klasse im Windows-Verwaltungsdienst mit Managed Object Format (MOF) deklarieren.</span><span class="sxs-lookup"><span data-stu-id="ff0b4-106">You can declare a basic instance of a class in the Windows Management service using Managed Object Format (MOF).</span></span> <span data-ttu-id="ff0b4-107">Sie können auch die Standardwerte für eine Instanz überschreiben.</span><span class="sxs-lookup"><span data-stu-id="ff0b4-107">You can also override the default values for an instance.</span></span> <span data-ttu-id="ff0b4-108">Weitere Informationen finden Sie unter [Festlegen des Eigenschafts Werts einer Instanz](#setting-an-instance-property-value).</span><span class="sxs-lookup"><span data-stu-id="ff0b4-108">For more information, see [Setting an Instance Property Value](#setting-an-instance-property-value).</span></span>

<span data-ttu-id="ff0b4-109">Im folgenden Verfahren wird beschrieben, wie Sie mithilfe von MOF-Code eine einfache Instanz einer Klasse deklarieren.</span><span class="sxs-lookup"><span data-stu-id="ff0b4-109">The following procedure describes how to declare a basic instance of a class using MOF code.</span></span>

<span data-ttu-id="ff0b4-110">**So deklarieren Sie eine einfache Instanz einer Klasse mithilfe von MOF-Code**</span><span class="sxs-lookup"><span data-stu-id="ff0b4-110">**To declare a basic instance of a class using MOF code**</span></span>

1.  <span data-ttu-id="ff0b4-111">Verwenden Sie die **Instanz von** -Schlüsselwörtern, gefolgt vom Klassennamen, geschweiften Klammern und einem Semikolon.</span><span class="sxs-lookup"><span data-stu-id="ff0b4-111">Use the **Instance of** keywords followed by the class name, curly braces, and a semicolon.</span></span>

    <span data-ttu-id="ff0b4-112">Im folgenden Codebeispiel wird gezeigt, wie eine Instanz einer-Klasse deklariert wird.</span><span class="sxs-lookup"><span data-stu-id="ff0b4-112">The following code example shows how to declare an instance of a class.</span></span>

    ```mof
    instance of ClassName
    {
    };
    ```

    

2.  <span data-ttu-id="ff0b4-113">Wenn Sie fertig sind, fügen Sie den MOF-Code mithilfe des MOF-Compilers in das WMI-Repository ein.</span><span class="sxs-lookup"><span data-stu-id="ff0b4-113">When finished, insert your MOF code into the WMI repository using the MOF compiler.</span></span>

    <span data-ttu-id="ff0b4-114">Weitere Informationen finden Sie unter [Kompilieren von MOF-Dateien](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="ff0b4-114">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

<span data-ttu-id="ff0b4-115">Eine Instanz einer-Klasse enthält alle Eigenschaften der-Klasse.</span><span class="sxs-lookup"><span data-stu-id="ff0b4-115">An instance of a class includes all of the properties of the class.</span></span> <span data-ttu-id="ff0b4-116">Wenn die Klasse eine abgeleitete Klasse ist, schließen-Instanzen die Eigenschaften ein, die zu allen in der Hierarchie höheren Klassen gehören.</span><span class="sxs-lookup"><span data-stu-id="ff0b4-116">If the class is a derived class, instances include the properties belonging to all of the classes higher in the hierarchy.</span></span> <span data-ttu-id="ff0b4-117">Jede Klasse, von der eine Instanz erstellt wird, verfügt über eine oder mehrere Schlüsseleigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ff0b4-117">Each class that an instance is created from has one or more key properties.</span></span> <span data-ttu-id="ff0b4-118">Eine Instanz mit mehr als 256 Schlüsseln kann nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="ff0b4-118">You cannot create an instance with more than 256 keys.</span></span>

## <a name="setting-an-instance-property-value"></a><span data-ttu-id="ff0b4-119">Festlegen des Werts einer Instanzeigenschaft</span><span class="sxs-lookup"><span data-stu-id="ff0b4-119">Setting an Instance Property Value</span></span>

<span data-ttu-id="ff0b4-120">Da Eigenschaften von WMI stark Typen sind, können Sie keine Eigenschafts Typen ändern.</span><span class="sxs-lookup"><span data-stu-id="ff0b4-120">Because WMI strongly types properties, you cannot modify property types.</span></span> <span data-ttu-id="ff0b4-121">Sie können jedoch Eigenschaftswerte in-Instanzen festlegen.</span><span class="sxs-lookup"><span data-stu-id="ff0b4-121">You can, however, set property values in instances.</span></span> <span data-ttu-id="ff0b4-122">Wenn eine Klasse eine Standardwert einer Eigenschaft zuweist, weist WMI jeder Instanz den Standardwert zu.</span><span class="sxs-lookup"><span data-stu-id="ff0b4-122">When a class assigns a default value to a property, WMI assigns the default value to each instance.</span></span> <span data-ttu-id="ff0b4-123">Sie können diesen Wert in der Instanzdeklaration überschreiben.</span><span class="sxs-lookup"><span data-stu-id="ff0b4-123">You can override this value in your instance declaration.</span></span>

<span data-ttu-id="ff0b4-124">Im folgenden Verfahren wird beschrieben, wie Sie einen Eigenschafts Wert festlegen oder einen Standardwert überschreiben, indem Sie MOF-Code verwenden.</span><span class="sxs-lookup"><span data-stu-id="ff0b4-124">The following procedure describes how to set a property value or overwrite a default value using MOF code.</span></span>

<span data-ttu-id="ff0b4-125">**So legen Sie einen Eigenschafts Wert fest oder Überschreiben einen Standardwert mithilfe von MOF-Code**</span><span class="sxs-lookup"><span data-stu-id="ff0b4-125">**To set a property value or overwrite a default value using MOF code**</span></span>

1.  <span data-ttu-id="ff0b4-126">Platzieren Sie eine Zuweisungsanweisung zwischen den geschweiften Klammern der Instanzdeklaration.</span><span class="sxs-lookup"><span data-stu-id="ff0b4-126">Place an assignment statement between the curly braces of the instance declaration.</span></span>

    <span data-ttu-id="ff0b4-127">Im folgenden Codebeispiel wird gezeigt, wie ein Eigenschafts Wert festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="ff0b4-127">The following code example shows how to set a property value.</span></span>

    ``` syntax
    instance of ClassName
    {
        Prop = "value";
    };
    ```

    <span data-ttu-id="ff0b4-128">WMI erfordert nicht, dass Sie während der Instanzerstellung eine Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="ff0b4-128">WMI does not require that you set any property during instance creation.</span></span> <span data-ttu-id="ff0b4-129">Die Ausnahme ist jede Eigenschaft, die mit dem [**Schlüssel**](key-qualifier.md) Qualifizierer gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="ff0b4-129">The exception is any property marked with the [**Key**](key-qualifier.md) qualifier.</span></span> <span data-ttu-id="ff0b4-130">Da WMI Schlüsseleigenschaften zum eindeutigen Identifizieren von Instanzen verwendet, müssen Sie alle Schlüsseleigenschaften so festlegen, wie Sie Sie finden.</span><span class="sxs-lookup"><span data-stu-id="ff0b4-130">Because WMI uses key properties to uniquely identify instances, you must set all key properties as you encounter them.</span></span> <span data-ttu-id="ff0b4-131">Im Gegensatz dazu dürfen Sie in einer Instanzdeklaration keine System Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="ff0b4-131">In contrast, you must not set a system property in an instance declaration.</span></span> <span data-ttu-id="ff0b4-132">Stattdessen weist WMI bei Bedarf die entsprechenden Werte einer System Eigenschaft zu.</span><span class="sxs-lookup"><span data-stu-id="ff0b4-132">Instead, WMI assigns the appropriate values to a system property when necessary.</span></span>

2.  <span data-ttu-id="ff0b4-133">Wenn Sie fertig sind, fügen Sie den MOF-Code in das WMI-Repository ein, indem Sie den MOF-Compiler aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="ff0b4-133">When finished, insert your MOF code into the WMI repository with a call to the MOF compiler.</span></span>

    <span data-ttu-id="ff0b4-134">Weitere Informationen finden Sie unter [Kompilieren von MOF-Dateien](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="ff0b4-134">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

<span data-ttu-id="ff0b4-135">In den folgenden Codebeispielen wird veranschaulicht, wie eine Instanz Daten für Eigenschaften angibt, die von einer-Klasse definiert werden.</span><span class="sxs-lookup"><span data-stu-id="ff0b4-135">The following code examples show how an instance specifies data for properties defined by a class.</span></span>

``` syntax
class MyClass 
{
    [key] string   strProp;
    sint32   dwProp1;
    uint32       dwProp2;
};

instance of MyClass 
{
    strProp = "hello";
    dwProp1 = -1;
    dwProp2 = 0xffffffff;
};
```

<span data-ttu-id="ff0b4-136">Im vorherigen Beispiel definiert die-Klasse drei Eigenschaften: eine Zeichenfolge, eine 32-Bit-Ganzzahl mit Vorzeichen und eine 32-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="ff0b4-136">In the preceding example, the class defines three properties: a character string, a 32-bit signed integer, and a 32-bit unsigned integer.</span></span> <span data-ttu-id="ff0b4-137">Die-Instanz stellt Datenwerte für jede dieser Eigenschaften bereit.</span><span class="sxs-lookup"><span data-stu-id="ff0b4-137">The instance provides data values for each of these properties.</span></span>

 

 



