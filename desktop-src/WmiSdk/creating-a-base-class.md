---
description: Die empfohlene Vorgehensweise zum Erstellen einer neuen WMI-Basisklasse für einen WMI-Anbieter befindet sich in einer MOF-Datei (Managed Object Format).
ms.assetid: d46060aa-77c3-4f51-b4a7-2c3612f2bc5c
ms.tgt_platform: multiple
title: Erstellen einer WMI-Basisklasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebdcbe6995a7782d854a4d0950db841f23a30b45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960617"
---
# <a name="creating-a-wmi-base-class"></a><span data-ttu-id="cff55-103">Erstellen einer WMI-Basisklasse</span><span class="sxs-lookup"><span data-stu-id="cff55-103">Creating a WMI Base Class</span></span>

<span data-ttu-id="cff55-104">Die empfohlene Vorgehensweise zum Erstellen einer neuen WMI-Basisklasse für einen WMI-Anbieter befindet sich in einer MOF-Datei (Managed Object Format).</span><span class="sxs-lookup"><span data-stu-id="cff55-104">The recommended way to create a new WMI base class for a WMI provider is in a Managed Object Format (MOF) file.</span></span> <span data-ttu-id="cff55-105">Sie können auch eine Basisklasse mithilfe der [com-API für WMI](com-api-for-wmi.md)erstellen.</span><span class="sxs-lookup"><span data-stu-id="cff55-105">You can also create a base class using the [COM API for WMI](com-api-for-wmi.md).</span></span> <span data-ttu-id="cff55-106">Obwohl Sie eine Basisklasse oder eine abgeleitete Klasse im Skript erstellen können, ohne dass ein Anbieter Daten für die Klasse und deren Unterklassen bereitstellt, ist die Klasse nicht nützlich.</span><span class="sxs-lookup"><span data-stu-id="cff55-106">While you can create a base or derived class in script, without a provider supplying data to the class and its subclasses, the class is not useful.</span></span>

<span data-ttu-id="cff55-107">In diesem Thema werden die folgenden Abschnitte erläutert:</span><span class="sxs-lookup"><span data-stu-id="cff55-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="cff55-108">Erstellen einer Basisklasse mithilfe von MOF</span><span class="sxs-lookup"><span data-stu-id="cff55-108">Creating a Base Class Using MOF</span></span>](#creating-a-base-class-using-mof)
-   [<span data-ttu-id="cff55-109">Erstellen einer Basisklasse mit C++</span><span class="sxs-lookup"><span data-stu-id="cff55-109">Creating a Base Class with C++</span></span>](#creating-a-base-class-with-c)
-   [<span data-ttu-id="cff55-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cff55-110">Related topics</span></span>](#related-topics)

## <a name="creating-a-base-class-using-mof"></a><span data-ttu-id="cff55-111">Erstellen einer Basisklasse mithilfe von MOF</span><span class="sxs-lookup"><span data-stu-id="cff55-111">Creating a Base Class Using MOF</span></span>

<span data-ttu-id="cff55-112">WMI-Klassen basieren in der Regel auf Vererbung.</span><span class="sxs-lookup"><span data-stu-id="cff55-112">WMI classes usually rely on inheritance.</span></span> <span data-ttu-id="cff55-113">Überprüfen Sie vor dem Erstellen einer Basisklasse die in der[DMTF](https://www.dmtf.org/)(verteilte Management Task Force) verfügbaren Common Information Model (CIM)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="cff55-113">Before creating a base class, check the Common Information Model (CIM) classes available from the Distributed Management Task Force ([DMTF](https://www.dmtf.org/)).</span></span>

<span data-ttu-id="cff55-114">Wenn viele abgeleitete Klassen die gleichen Eigenschaften verwenden, platzieren Sie diese Eigenschaften und Methoden in ihrer Basisklasse.</span><span class="sxs-lookup"><span data-stu-id="cff55-114">If many derived classes will use the same properties, put these properties and methods in your base class.</span></span> <span data-ttu-id="cff55-115">Die maximale Anzahl von Eigenschaften, die Sie in einer WMI-Klasse definieren können, ist 1024.</span><span class="sxs-lookup"><span data-stu-id="cff55-115">The maximum number of properties you can define in a WMI class is 1024.</span></span>

<span data-ttu-id="cff55-116">Beachten Sie beim Erstellen einer Basisklasse die folgende Liste von Richtlinien für Klassennamen:</span><span class="sxs-lookup"><span data-stu-id="cff55-116">When creating a base class, observe the following list of guidelines for class names:</span></span>

-   <span data-ttu-id="cff55-117">Verwenden Sie groß-und Kleinbuchstaben.</span><span class="sxs-lookup"><span data-stu-id="cff55-117">Use both uppercase and lowercase letters.</span></span>
-   <span data-ttu-id="cff55-118">Beginnen Sie einen Klassennamen mit einem Buchstaben.</span><span class="sxs-lookup"><span data-stu-id="cff55-118">Begin a class name with a letter.</span></span>
-   <span data-ttu-id="cff55-119">Verwenden Sie weder einen führenden noch einen nachfolgenden unterstrich.</span><span class="sxs-lookup"><span data-stu-id="cff55-119">Do not use either a leading or trailing underscore.</span></span>
-   <span data-ttu-id="cff55-120">Definieren Sie alle verbleibenden Zeichen als Buchstaben, Ziffern oder Unterstriche.</span><span class="sxs-lookup"><span data-stu-id="cff55-120">Define all remaining characters as letters, digits, or underscores.</span></span>
-   <span data-ttu-id="cff55-121">Verwenden Sie eine konsistente Benennungs Konvention.</span><span class="sxs-lookup"><span data-stu-id="cff55-121">Use a consistent naming convention.</span></span>

    <span data-ttu-id="cff55-122">Eine gute Benennungs Konvention für eine Klasse ist zwar nicht erforderlich, ist jedoch zwei Komponenten, die mit einem Unterstrich verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="cff55-122">While not necessary, a good naming convention for a class is two components joined by an underscore.</span></span> <span data-ttu-id="cff55-123">Wenn möglich, sollte ein Herstellername die erste Hälfte des Namens ausmachen, und ein beschreibender Klassenname sollte der zweite Teil sein.</span><span class="sxs-lookup"><span data-stu-id="cff55-123">When possible, a vendor name should make up the first half of the name, and a descriptive class name should be the second part.</span></span>

> [!Note]  
> <span data-ttu-id="cff55-124">Klassen können während der Ausführung von Anbietern nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="cff55-124">Classes cannot be changed during execution of providers.</span></span> <span data-ttu-id="cff55-125">Sie müssen die Aktivität abbrechen, die Klasse ändern und dann den Windows-Verwaltungsdienst neu starten.</span><span class="sxs-lookup"><span data-stu-id="cff55-125">You must stop the activity, change the class, and then restart the Windows Management service.</span></span> <span data-ttu-id="cff55-126">Es ist derzeit nicht möglich, eine Klassen Änderung zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="cff55-126">Detecting a class change is currently not possible.</span></span>

 

<span data-ttu-id="cff55-127">Erstellen Sie in MOF eine Basisklasse, indem Sie Sie mit dem Schlüsselwort **Class** benennen, ohne eine übergeordnete Klasse anzugeben.</span><span class="sxs-lookup"><span data-stu-id="cff55-127">In MOF, create a base class by naming it with the **class** keyword, but not indicating a parent class.</span></span>

<span data-ttu-id="cff55-128">**So erstellen Sie eine Basisklasse mithilfe von MOF-Code**</span><span class="sxs-lookup"><span data-stu-id="cff55-128">**To create a base class using MOF code**</span></span>

1.  <span data-ttu-id="cff55-129">Verwenden Sie das **Class** -Schlüsselwort mit dem Namen der neuen Klasse, gefolgt von einem Paar aus geschweiften Klammern und einem Semikolon.</span><span class="sxs-lookup"><span data-stu-id="cff55-129">Use the **class** keyword with the name of the new class, followed by a pair of curly braces and a semicolon.</span></span> <span data-ttu-id="cff55-130">Fügen Sie Eigenschaften und Methoden für die-Klasse zwischen den geschweiften Klammern hinzu.</span><span class="sxs-lookup"><span data-stu-id="cff55-130">Add properties and methods for the class between the curly braces.</span></span> <span data-ttu-id="cff55-131">Das folgende Codebeispiel wird bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="cff55-131">The following code example is provided.</span></span>

    <span data-ttu-id="cff55-132">Im folgenden Codebeispiel wird gezeigt, wie eine Basisklasse definiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="cff55-132">The following code example shows how a base class should be defined.</span></span>

    ``` syntax
    class MyClass_BaseDisk
    {
    };
    ```

    <span data-ttu-id="cff55-133">Das folgende Codebeispiel zeigt eine falsche Definition einer Basisklasse.</span><span class="sxs-lookup"><span data-stu-id="cff55-133">The following code example shows an incorrect definition of a base class.</span></span>

    ``` syntax
    class MyClass_BaseDisk : CIM_LogicalDisk
    {
    };
    ```

2.  <span data-ttu-id="cff55-134">Fügen Sie vor dem Schlüsselwort class alle Klassen [*Qualifizierer*](gloss-q.md) hinzu, um die Verwendung der-Klasse zu ändern.</span><span class="sxs-lookup"><span data-stu-id="cff55-134">Add any class [*qualifiers*](gloss-q.md) before the class keyword to modify the way the class is used.</span></span> <span data-ttu-id="cff55-135">Platzieren Sie die Qualifizierer zwischen eckigen Klammern.</span><span class="sxs-lookup"><span data-stu-id="cff55-135">Place the qualifiers between square brackets.</span></span> <span data-ttu-id="cff55-136">Weitere Informationen zu Qualifizierern zum Ändern von Klassen finden Sie unter [WMI-Qualifizierer](wmi-qualifiers.md).</span><span class="sxs-lookup"><span data-stu-id="cff55-136">For more information about qualifiers for modifying classes, see [WMI Qualifiers](wmi-qualifiers.md).</span></span> <span data-ttu-id="cff55-137">Verwenden Sie den **abstrakten** Qualifizierer, um anzugeben, dass keine Instanz dieser Klasse direkt erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="cff55-137">Use the **Abstract** qualifier to indicate that you cannot create an instance of this class directly.</span></span> <span data-ttu-id="cff55-138">Abstrakte Klassen werden häufig verwendet, um Eigenschaften oder Methoden zu definieren, die von mehreren abgeleiteten Klassen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cff55-138">Abstract classes are often used to define properties or methods that will be used by several derived classes.</span></span> <span data-ttu-id="cff55-139">Weitere Informationen finden Sie unter [Erstellen einer abgeleiteten Klasse](creating-a-derived-class.md).</span><span class="sxs-lookup"><span data-stu-id="cff55-139">For more information, see [Creating a Derived Class](creating-a-derived-class.md).</span></span>

    <span data-ttu-id="cff55-140">Im folgenden Codebeispiel wird die-Klasse als abstrakt definiert und der Anbieter definiert, der die Daten bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="cff55-140">The following code example defines the class as abstract and defines the provider that will supply the data.</span></span> <span data-ttu-id="cff55-141">Der " **desubclass** "-qualifiziererwert gibt an, dass die Informationen im **Anbieter Qualifizierer** von abgeleiteten Klassen geerbt werden [](gloss-f.md)</span><span class="sxs-lookup"><span data-stu-id="cff55-141">The **ToSubClass** qualifier [*flavor*](gloss-f.md) indicates that the information in the **Provider** qualifier is inherited by derived classes.</span></span>

    ``` syntax
    [Abstract, Provider("MyProvider") : ToSubClass]
    class MyClass_BaseDisk
    {
    };
    ```

3.  <span data-ttu-id="cff55-142">Fügen Sie die Eigenschaften und Methoden für die Klasse in eckigen Klammern vor dem Eigenschafts-oder Methodennamen hinzu.</span><span class="sxs-lookup"><span data-stu-id="cff55-142">Add the properties and methods for the class inside square brackets before the property or method name.</span></span> <span data-ttu-id="cff55-143">Weitere Informationen finden Sie unter [Hinzufügen einer Eigenschaft](adding-a-property.md) und [Erstellen einer Methode](creating-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="cff55-143">For more information, see [Adding a Property](adding-a-property.md) and [Creating a Method](creating-a-method.md).</span></span> <span data-ttu-id="cff55-144">Sie können diese Eigenschaften und Methoden mithilfe von MOF-Qualifizierern ändern.</span><span class="sxs-lookup"><span data-stu-id="cff55-144">You can modify these properties and methods using MOF qualifiers.</span></span> <span data-ttu-id="cff55-145">Weitere Informationen finden Sie unter [Hinzufügen eines Qualifizierers](adding-a-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="cff55-145">For more information, see [Adding a Qualifier](adding-a-qualifier.md).</span></span>

    <span data-ttu-id="cff55-146">Im folgenden Codebeispiel wird gezeigt, wie Eigenschaften und Methoden mit MOF-Qualifizierern geändert werden.</span><span class="sxs-lookup"><span data-stu-id="cff55-146">The following code example shows how to modify properties and methods with MOF qualifiers.</span></span>

    ``` syntax
    [read : ToSubClass, key : ToSubClass ] string DeviceID;
      [read : ToSubClass] uint32 State;
      [read : ToSubclass, write : ToSubClass] uint64 LimitUsers;
    ```

4.  <span data-ttu-id="cff55-147">Speichern Sie die MOF-Datei mit der Erweiterung. mof.</span><span class="sxs-lookup"><span data-stu-id="cff55-147">Save the MOF file with an extension of .mof.</span></span>
5.  <span data-ttu-id="cff55-148">Registrieren Sie die Klasse bei WMI, indem Sie [**Mofcomp.exe**](mofcomp.md) für die Datei ausführen.</span><span class="sxs-lookup"><span data-stu-id="cff55-148">Register the class with WMI by running [**Mofcomp.exe**](mofcomp.md) on the file.</span></span>

    <span data-ttu-id="cff55-149">**mofcomp.exe** *newmof. MOF*</span><span class="sxs-lookup"><span data-stu-id="cff55-149">**mofcomp.exe** *newmof.mof*</span></span>

    <span data-ttu-id="cff55-150">Wenn Sie den Schalter **-N** oder den Pragma-Namespace des Präprozessorbefehls nicht verwenden \# [](pragma-namespace.md) , um einen Namespace anzugeben, werden die kompilierten MOF-Klassen im Stamm- \\ Standard Namespace im Repository gespeichert.</span><span class="sxs-lookup"><span data-stu-id="cff55-150">If you do not use the **-N** switch or the preprocessor command \#[**pragma namespace**](pragma-namespace.md) to specify a namespace, the compiled MOF classes will be stored in the root\\default namespace in the repository.</span></span> <span data-ttu-id="cff55-151">Weitere Informationen finden Sie unter " [**MUF**](mofcomp.md)".</span><span class="sxs-lookup"><span data-stu-id="cff55-151">For more information, see [**mofcomp**](mofcomp.md).</span></span>

<span data-ttu-id="cff55-152">Im folgenden Codebeispiel werden die MOF-Codebeispiele kombiniert, die in der vorherigen Prozedur erläutert wurden, und es wird gezeigt, wie eine Basisklasse im root \\ CIMV2-Namespace mithilfe von MOF erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="cff55-152">The following code example combines the MOF code examples discussed in the previous procedure and shows how to create a base class in the root\\cimv2 namespace using MOF.</span></span>

``` syntax
#pragma namespace("\\\\.\\Root\\cimv2")

[Abstract, Provider("MyProvider") : ToSubClass]
class MyClass_BaseDisk
{
  [read : ToSubClass, key : ToSubClass ] string DeviceID;
  [read : ToSubClass] uint32 State;
  [read : ToSubClass, write : ToSubClass] uint64 LimitUsers;
};
```

<span data-ttu-id="cff55-153">Weitere Informationen finden Sie unter [Erstellen einer abgeleiteten Klasse](creating-a-derived-class.md) für ein Beispiel für eine dynamische Klasse, die von dieser Basisklasse abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="cff55-153">For more information, see [Creating a Derived Class](creating-a-derived-class.md) for an example of a dynamic class derived from this base class.</span></span>

## <a name="creating-a-base-class-with-c"></a><span data-ttu-id="cff55-154">Erstellen einer Basisklasse mit C++</span><span class="sxs-lookup"><span data-stu-id="cff55-154">Creating a Base Class with C++</span></span>

<span data-ttu-id="cff55-155">Das Erstellen einer Basisklasse mithilfe der WMI-API ist hauptsächlich eine Reihe von Put-Befehlen, mit denen die Klasse definiert und die Klasse bei WMI registriert wird.</span><span class="sxs-lookup"><span data-stu-id="cff55-155">Creating a base class using the WMI API is mainly a series of Put commands that define the class and register the class with WMI.</span></span> <span data-ttu-id="cff55-156">Der Hauptzweck dieser API besteht darin, Client Anwendungen das Erstellen von Basisklassen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="cff55-156">The main purpose of this API is to enable client applications to create base classes.</span></span> <span data-ttu-id="cff55-157">Sie können jedoch auch einen Anbieter verwenden, um eine Basisklasse mithilfe dieser API zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="cff55-157">However, you can also have a provider use this API to create a base class.</span></span> <span data-ttu-id="cff55-158">Wenn Sie z. b. der Meinung sind, dass der MOF-Code für den Anbieter nicht ordnungsgemäß installiert wird, können Sie den Anbieter anweisen, automatisch die richtigen Klassen im WMI-Repository zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="cff55-158">For example, if you believe that the MOF code for your provider will not be installed properly, you can instruct your provider to automatically create the correct classes in the WMI repository.</span></span> <span data-ttu-id="cff55-159">Weitere Informationen zu Anbietern finden Sie unter [Schreiben eines Klassen Anbieters](writing-a-class-provider.md).</span><span class="sxs-lookup"><span data-stu-id="cff55-159">For more information about providers, see [Writing a Class Provider](writing-a-class-provider.md).</span></span>

> [!Note]  
> <span data-ttu-id="cff55-160">Klassen können während der Ausführung von Anbietern nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="cff55-160">Classes cannot be changed during execution of providers.</span></span> <span data-ttu-id="cff55-161">Sie müssen die Aktivität abbrechen, die Klasse ändern und dann den Windows-Verwaltungsdienst neu starten.</span><span class="sxs-lookup"><span data-stu-id="cff55-161">You must stop the activity, change the class, and then restart the Windows Management service.</span></span> <span data-ttu-id="cff55-162">Es ist derzeit nicht möglich, eine Klassen Änderung zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="cff55-162">Detecting a class change is currently not possible.</span></span>

 

<span data-ttu-id="cff55-163">Der Code erfordert, dass der folgende Verweis ordnungsgemäß kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="cff55-163">The code requires the following reference to compile correctly.</span></span>


```C++
#include <wbemidl.h>
```



<span data-ttu-id="cff55-164">Sie können eine neue Basisklasse mithilfe der [com-API für WMI](com-api-for-wmi.md)Programm gesteuert erstellen.</span><span class="sxs-lookup"><span data-stu-id="cff55-164">You can create a new base class programmatically using the [COM API for WMI](com-api-for-wmi.md).</span></span>

<span data-ttu-id="cff55-165">**So erstellen Sie eine neue Basisklasse mit der WMI-API**</span><span class="sxs-lookup"><span data-stu-id="cff55-165">**To create a new base class with the WMI API**</span></span>

1.  <span data-ttu-id="cff55-166">Rufen Sie eine Definition für die neue Klasse ab, indem Sie die [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) -Methode aufrufen, wobei der Parameter " *strobjectpath* " auf einen **null** -Wert festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="cff55-166">Retrieve a definition for the new class by calling the [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) method with the *strObjectPath* parameter set to a **null** value.</span></span>

    <span data-ttu-id="cff55-167">Im folgenden Codebeispiel wird gezeigt, wie eine Definition für eine neue Klasse abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="cff55-167">The following code example shows how to retrieve a definition for a new class.</span></span>

    ```C++
    IWbemServices* pSvc = 0;
    IWbemContext* pCtx = 0;
    IWbemClassObject* pNewClass = 0;
    IWbemCallResult* pResult = 0;
    HRESULT hRes = pSvc->GetObject(0, 0, pCtx, &pNewClass, &pResult);
    ```

    

2.  <span data-ttu-id="cff55-168">Richten Sie einen Namen für die Klasse ein, indem Sie die **\_ \_ Klassen** System Eigenschaft mit einem-Befehl für die [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) -Methode festlegen.</span><span class="sxs-lookup"><span data-stu-id="cff55-168">Establish a name for the class by setting the **\_\_CLASS** system property with a call to the [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) method.</span></span>

    <span data-ttu-id="cff55-169">Im folgenden Codebeispiel wird gezeigt, wie die-Klasse durch Festlegen der **\_ \_ Klassen** System-Eigenschaft benennen kann.</span><span class="sxs-lookup"><span data-stu-id="cff55-169">The following code example shows how to name the class by setting the **\_\_CLASS** system property.</span></span>

    ```C++
    VARIANT v;
    VariantInit(&v);
    V_VT(&v) = VT_BSTR;

    V_BSTR(&v) = SysAllocString(L"Example");
    BSTR Class = SysAllocString(L"__CLASS");
    pNewClass->Put(Class, 0, &v, 0);
    SysFreeString(Class);
    VariantClear(&v);
    ```

    

3.  <span data-ttu-id="cff55-170">Erstellen Sie die Schlüsseleigenschaft oder die Eigenschaften, indem Sie [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="cff55-170">Create the key property or properties by calling [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span></span>

    <span data-ttu-id="cff55-171">Im folgenden Codebeispiel wird beschrieben, wie die [**Index**](swbemrefreshableitem-index.md) -Eigenschaft erstellt wird, die in Schritt 4 als Schlüsseleigenschaft bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="cff55-171">The following code example describes how to create the [**Index**](swbemrefreshableitem-index.md) property, which is labeled as a key property in Step 4.</span></span>

    ```C++
      BSTR KeyProp = SysAllocString(L"Index");
      pNewClass->Put(KeyProp, 0, NULL, CIM_STRING);
    ```

    

4.  <span data-ttu-id="cff55-172">Fügen Sie den [**Schlüssel**](standard-qualifiers.md) Standard Qualifizierer an die Schlüsseleigenschaft an, indem Sie zuerst die [**IWbemClassObject:: getpropertyqualifierset**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset) -Methode und dann die [**iwbemqualifierset::P UT**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="cff55-172">Attach the [**Key**](standard-qualifiers.md) standard qualifier to the key property by first calling the [**IWbemClassObject::GetPropertyQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset) method and then the [**IWbemQualifierSet::Put**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) method.</span></span>

    <span data-ttu-id="cff55-173">Im folgenden Codebeispiel wird gezeigt, wie der [**Schlüssel**](standard-qualifiers.md) Standard Qualifizierer an die Schlüsseleigenschaft angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="cff55-173">The following code example shows how to attach the [**Key**](standard-qualifiers.md) standard qualifier to the key property.</span></span>

    ```C++
      IWbemQualifierSet *pQual = 0;
      pNewClass->GetPropertyQualifierSet(KeyProp, &pQual);
      SysFreeString(KeyProp);

      V_VT(&v) = VT_BOOL;
      V_BOOL(&v) = VARIANT_TRUE;
      BSTR Key = SysAllocString(L"Key");

      pQual->Put(Key, &v, 0);   // Flavors not required for Key 
      SysFreeString(Key);

      // No longer need the qualifier set for "Index"
      pQual->Release();   
      VariantClear(&v);
    ```

    

5.  <span data-ttu-id="cff55-174">Erstellen Sie mit [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)weitere Eigenschaften der Klasse.</span><span class="sxs-lookup"><span data-stu-id="cff55-174">Create other properties of the class with [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span></span>

    <span data-ttu-id="cff55-175">Im folgenden Codebeispiel wird beschrieben, wie zusätzliche Eigenschaften erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="cff55-175">The following code example describes how to create additional properties.</span></span>

    ```C++
      V_VT(&v) = VT_BSTR;
      V_BSTR(&v) = SysAllocString(L"<default>");
      BSTR OtherProp = SysAllocString(L"OtherInfo");
      pNewClass->Put(OtherProp, 0, &v, CIM_STRING);
      SysFreeString(OtherProp);
      VariantClear(&v);

      OtherProp = SysAllocString(L"IntVal");
      pNewClass->Put(OtherProp, 0, NULL, CIM_SINT32); // NULL is default
      SysFreeString(OtherProp);
    ```

    

6.  <span data-ttu-id="cff55-176">Registrieren Sie die neue Klasse durch Aufrufen von [**IWbemServices::P utclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).</span><span class="sxs-lookup"><span data-stu-id="cff55-176">Register the new class by calling [**IWbemServices::PutClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).</span></span>

    <span data-ttu-id="cff55-177">Da Sie nach dem Registrieren einer neuen Klasse keine Schlüssel und Indizes definieren können, stellen Sie sicher, dass Sie alle Eigenschaften vor dem Aufruf von [**putclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass)definiert haben.</span><span class="sxs-lookup"><span data-stu-id="cff55-177">Because you cannot define keys and indices after you register a new class, ensure that you have defined all of your properties before calling [**PutClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).</span></span>

    <span data-ttu-id="cff55-178">Im folgenden Codebeispiel wird beschrieben, wie eine neue Klasse registriert wird.</span><span class="sxs-lookup"><span data-stu-id="cff55-178">The following code example describes how to register a new class.</span></span>

    ```C++
      hRes = pSvc->PutClass(pNewClass, 0, pCtx, &pResult);
      pNewClass->Release();
    ```

    

<span data-ttu-id="cff55-179">Im folgenden Codebeispiel werden die Codebeispiele kombiniert, die in der vorherigen Prozedur erläutert wurden, und es wird gezeigt, wie Sie eine Basisklasse mithilfe der WMI-API erstellen.</span><span class="sxs-lookup"><span data-stu-id="cff55-179">The following code example combines the code examples discussed in the previous procedure and shows how to create a base class using the WMI API.</span></span>


```C++
void CreateClass(IWbemServices *pSvc)
{
  IWbemClassObject *pNewClass = 0;
  IWbemContext *pCtx = 0;
  IWbemCallResult *pResult = 0;

  // Get a class definition. 
  // ============================
  HRESULT hRes = pSvc->GetObject(0, 0, pCtx, &pNewClass, &pResult);
  VARIANT v;
  VariantInit(&v);

  // Create the class name.
  // ============================
  V_VT(&v) = VT_BSTR;
  V_BSTR(&v) = SysAllocString(L"Example");
  BSTR Class = SysAllocString(L"__CLASS");
  pNewClass->Put(Class, 0, &v, 0);
  SysFreeString(Class);
  VariantClear(&v);

  // Create the key property. 
  // ============================
  BSTR KeyProp = SysAllocString(L"Index");
  pNewClass->Put(KeyProp, 0, NULL, CIM_STRING);

  // Attach Key qualifier to mark the "Index" property as the key.
  // ============================
  IWbemQualifierSet *pQual = 0;
  pNewClass->GetPropertyQualifierSet(KeyProp, &pQual);
  SysFreeString(KeyProp);

  V_VT(&v) = VT_BOOL;
  V_BOOL(&v) = VARIANT_TRUE;
  BSTR Key = SysAllocString(L"Key");

  pQual->Put(Key, &v, 0);   // Flavors not required for Key 
  SysFreeString(Key);

  // No longer need the qualifier set for "Index"
  pQual->Release();     
  VariantClear(&v);

  // Create other properties.
  // ============================
  V_VT(&v) = VT_BSTR;
  V_BSTR(&v) = SysAllocString(L"<default>");
  BSTR OtherProp = SysAllocString(L"OtherInfo");
  pNewClass->Put(OtherProp, 0, &v, CIM_STRING);
  SysFreeString(OtherProp);
  VariantClear(&v);

  OtherProp = SysAllocString(L"IntVal");
  pNewClass->Put(OtherProp, 0, NULL, CIM_SINT32); // NULL is default
  SysFreeString(OtherProp);
  
  // Register the class with WMI
  // ============================
  hRes = pSvc->PutClass(pNewClass, 0, pCtx, &pResult);
  pNewClass->Release();
}
```



## <a name="related-topics"></a><span data-ttu-id="cff55-180">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cff55-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cff55-181">Erstellen einer Klasse</span><span class="sxs-lookup"><span data-stu-id="cff55-181">Creating a Class</span></span>](creating-a-class.md)
</dt> </dl>

 

 



