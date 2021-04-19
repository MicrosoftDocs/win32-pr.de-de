---
description: Das Erstellen einer abgeleiteten Klasse in WMI ähnelt stark dem Erstellen einer Basisklasse. Wie bei einer Basisklasse müssen Sie zuerst die abgeleitete Klasse definieren und dann die abgeleitete Klasse bei WMI registrieren.
ms.assetid: 8dd483b8-8bc2-4a5c-b981-6c2ffaccdb95
ms.tgt_platform: multiple
title: Erstellen einer abgeleiteten WMI-Klasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b65079d206cb7a0a490622018f6d2e2df98867d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345878"
---
# <a name="creating-a-wmi-derived-class"></a><span data-ttu-id="1517e-104">Erstellen einer abgeleiteten WMI-Klasse</span><span class="sxs-lookup"><span data-stu-id="1517e-104">Creating a WMI Derived Class</span></span>

<span data-ttu-id="1517e-105">Das Erstellen einer abgeleiteten Klasse in WMI ähnelt stark dem Erstellen einer Basisklasse.</span><span class="sxs-lookup"><span data-stu-id="1517e-105">Creating a derived class in WMI is very similar to creating a base class.</span></span> <span data-ttu-id="1517e-106">Wie bei einer Basisklasse müssen Sie zuerst die abgeleitete Klasse definieren und dann die abgeleitete Klasse bei WMI registrieren.</span><span class="sxs-lookup"><span data-stu-id="1517e-106">As with a base class, you must first define the derived class and then register the derived class with WMI.</span></span> <span data-ttu-id="1517e-107">Der Hauptunterschied besteht darin, dass Sie zuerst die übergeordnete Klasse suchen müssen, von der abgeleitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1517e-107">The main difference is that you must first locate the parent class from which you wish to derive.</span></span> <span data-ttu-id="1517e-108">Weitere Informationen finden Sie unter [Schreiben eines Klassen Anbieters](writing-a-class-provider.md) und [Schreiben eines Instanzanbieters](writing-an-instance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="1517e-108">For more information, see [Writing a Class Provider](writing-a-class-provider.md) and [Writing an Instance Provider](writing-an-instance-provider.md).</span></span>

<span data-ttu-id="1517e-109">Die empfohlene Vorgehensweise zum Erstellen von Klassen für einen-Anbieter ist in Managed Object Format Dateien (MOF).</span><span class="sxs-lookup"><span data-stu-id="1517e-109">The recommended way to create classes for a provider is in Managed Object Format (MOF) files.</span></span> <span data-ttu-id="1517e-110">Mehrere abgeleitete Klassen, die miteinander verknüpft sind, sollten zusammen mit allen Basisklassen, von denen Eigenschaften oder Methoden abgeleitet werden, in eine MOF-Datei gruppiert werden.</span><span class="sxs-lookup"><span data-stu-id="1517e-110">Several derived classes that are related to each other should be grouped into a MOF file, along with any base classes from which they derive properties or methods.</span></span> <span data-ttu-id="1517e-111">Wenn Sie jede Klasse in einer separaten MOF-Datei platzieren, muss jede Datei kompiliert werden, bevor der Anbieter ordnungsgemäß funktionieren kann.</span><span class="sxs-lookup"><span data-stu-id="1517e-111">If you place each class in a separate MOF file then each file must be compiled before the provider can work properly.</span></span>

<span data-ttu-id="1517e-112">Nachdem Sie die Klasse erstellt haben, müssen Sie alle Instanzen der Klasse löschen, bevor Sie eine der folgenden Aktivitäten in der abgeleiteten Klasse ausführen können:</span><span class="sxs-lookup"><span data-stu-id="1517e-112">After you create your class, you must delete all instances of your class before you can perform any of the following activities on your derived class:</span></span>

-   <span data-ttu-id="1517e-113">Ändern Sie die übergeordnete Klasse ihrer abgeleiteten Klasse.</span><span class="sxs-lookup"><span data-stu-id="1517e-113">Change the parent class of your derived class.</span></span>
-   <span data-ttu-id="1517e-114">Eigenschaften hinzufügen oder entfernen.</span><span class="sxs-lookup"><span data-stu-id="1517e-114">Add or remove properties.</span></span>
-   <span data-ttu-id="1517e-115">Ändern Sie die Eigenschafts Typen.</span><span class="sxs-lookup"><span data-stu-id="1517e-115">Change property types.</span></span>
-   <span data-ttu-id="1517e-116">[**Schlüssel**](key-qualifier.md) oder **indizierte** Qualifizierer hinzufügen oder entfernen.</span><span class="sxs-lookup"><span data-stu-id="1517e-116">Add or remove [**Key**](key-qualifier.md) or **Indexed** qualifiers.</span></span>
-   <span data-ttu-id="1517e-117">Fügen Sie [**Singleton**](standard-wmi-qualifiers.md)-, **dynamische** oder [**abstrakte**](standard-qualifiers.md) Qualifizierer hinzu oder entfernen Sie Sie.</span><span class="sxs-lookup"><span data-stu-id="1517e-117">Add or remove [**Singleton**](standard-wmi-qualifiers.md), **Dynamic**, or [**Abstract**](standard-qualifiers.md) qualifiers.</span></span>

> [!Note]  
> <span data-ttu-id="1517e-118">Um eine Eigenschaft oder einen Qualifizierer hinzuzufügen, zu entfernen oder zu ändern, nennen Sie [**IWbemServices::P utclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass) oder [**errbemubject. Put \_**](swbemobject-put-.md) , und legen Sie den Flag-Parameter auf "Force Mode" fest.</span><span class="sxs-lookup"><span data-stu-id="1517e-118">To add, remove, or modify a property or qualifier, call [**IWbemServices::PutClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass) or [**SWbemObject.Put\_**](swbemobject-put-.md) and set the flag parameter to "force mode".</span></span> <span data-ttu-id="1517e-119">Der [**abstrakte**](standard-qualifiers.md) Qualifizierer kann nur verwendet werden, wenn die übergeordnete Klasse abstrakt ist.</span><span class="sxs-lookup"><span data-stu-id="1517e-119">The [**Abstract**](standard-qualifiers.md) qualifier can be used only if the parent class is abstract.</span></span>

 

<span data-ttu-id="1517e-120">Wenn Sie die abgeleitete Klasse deklarieren, beachten Sie die folgenden Regeln und Einschränkungen:</span><span class="sxs-lookup"><span data-stu-id="1517e-120">When you declare your derived class, observe the following rules and restrictions:</span></span>

-   <span data-ttu-id="1517e-121">Die übergeordnete Klasse der abgeleiteten Klasse muss bereits vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="1517e-121">The parent class of the derived class must already exist.</span></span>

    <span data-ttu-id="1517e-122">Die Deklaration der übergeordneten Klasse kann in derselben MOF-Datei wie die abgeleitete Klasse oder in einer anderen Datei vorkommen.</span><span class="sxs-lookup"><span data-stu-id="1517e-122">The declaration of the parent class can appear in the same MOF file as the derived class or in a different file.</span></span> <span data-ttu-id="1517e-123">Wenn die übergeordnete Klasse unbekannt ist, generiert der Compiler einen Laufzeitfehler.</span><span class="sxs-lookup"><span data-stu-id="1517e-123">If the parent class is unknown, the compiler generates a run-time error.</span></span>

-   <span data-ttu-id="1517e-124">Eine abgeleitete Klasse kann nur über eine einzige übergeordnete Klasse verfügen.</span><span class="sxs-lookup"><span data-stu-id="1517e-124">A derived class can have only a single parent class.</span></span>

    <span data-ttu-id="1517e-125">WMI unterstützt keine Mehrfachvererbung.</span><span class="sxs-lookup"><span data-stu-id="1517e-125">WMI does not support multiple inheritance.</span></span> <span data-ttu-id="1517e-126">Eine übergeordnete Klasse kann jedoch viele abgeleitete Klassen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="1517e-126">However, a parent class can have many derived classes.</span></span>

-   <span data-ttu-id="1517e-127">Sie können Indizes für abgeleitete Klassen definieren, aber WMI verwendet diese Indizes nicht.</span><span class="sxs-lookup"><span data-stu-id="1517e-127">You can define indices for derived classes, but WMI does not use these indices.</span></span>

    <span data-ttu-id="1517e-128">Daher wird durch die Angabe eines Indexes für eine abgeleitete Klasse die Leistung von Abfragen für Instanzen der abgeleiteten Klasse nicht verbessert.</span><span class="sxs-lookup"><span data-stu-id="1517e-128">Therefore, specifying an index on a derived class does not improve the performance of queries for instances of the derived class.</span></span> <span data-ttu-id="1517e-129">Sie können die Leistung einer Abfrage für eine abgeleitete Klasse verbessern, indem Sie indizierte Eigenschaften für die übergeordnete Klasse der abgeleiteten Klasse angeben.</span><span class="sxs-lookup"><span data-stu-id="1517e-129">You can improve the performance of a query on a derived class by specifying indexed properties for the parent class of the derived class.</span></span>

-   <span data-ttu-id="1517e-130">Abgeleitete Klassendefinitionen können komplexer sein und Funktionen wie Aliase, Qualifizierer und qualifizierervarianten enthalten.</span><span class="sxs-lookup"><span data-stu-id="1517e-130">Derived class definitions can be more complex, and can include such features as aliases, qualifiers, and qualifier flavors.</span></span>

    <span data-ttu-id="1517e-131">Weitere Informationen finden Sie unter [Erstellen eines Alias](creating-an-alias.md) und [Hinzufügen eines Qualifizierers](adding-a-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="1517e-131">For more information, see [Creating an Alias](creating-an-alias.md) and [Adding a Qualifier](adding-a-qualifier.md).</span></span>

-   <span data-ttu-id="1517e-132">Wenn Sie einen Qualifizierer ändern, den Standardwert einer Basisklassen Eigenschaft ändern oder eine Verweis-oder eingebettete Objekt Eigenschaft einer Basisklasse stark eingeben möchten, müssen Sie die gesamte Basisklasse erneut deklarieren.</span><span class="sxs-lookup"><span data-stu-id="1517e-132">If you wish to change a qualifier, change the default value of a base class property, or more strongly type a reference or embedded object property of a base class, you must declare the entire base class again.</span></span>
-   <span data-ttu-id="1517e-133">Die maximale Anzahl von Eigenschaften, die Sie in einer WMI-Klasse definieren können, ist 1024.</span><span class="sxs-lookup"><span data-stu-id="1517e-133">The maximum number of properties you can define in a WMI class is 1024.</span></span>

> [!Note]  
> <span data-ttu-id="1517e-134">Klassen können während der Ausführung von Anbietern nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="1517e-134">Classes cannot be changed during execution of providers.</span></span> <span data-ttu-id="1517e-135">Sie müssen die Aktivität abbrechen, die Klasse ändern und dann den Windows-Verwaltungsdienst neu starten.</span><span class="sxs-lookup"><span data-stu-id="1517e-135">You must stop the activity, change the class, and then restart the Windows Management service.</span></span> <span data-ttu-id="1517e-136">Es ist derzeit nicht möglich, eine Klassen Änderung zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="1517e-136">Detecting a class change is currently not possible.</span></span>

 

<span data-ttu-id="1517e-137">Wie bei der Basisklasse wird diese Technik am häufigsten von Client Anwendungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="1517e-137">As with the base class, the most common use of this technique will be by client applications.</span></span> <span data-ttu-id="1517e-138">Ein Anbieter kann jedoch auch eine abgeleitete Klasse erstellen.</span><span class="sxs-lookup"><span data-stu-id="1517e-138">However, a provider can also create a derived class.</span></span> <span data-ttu-id="1517e-139">Weitere Informationen finden Sie unter [Erstellen einer Basisklasse](creating-a-base-class.md) und [Schreiben eines Klassen Anbieters](writing-a-class-provider.md).</span><span class="sxs-lookup"><span data-stu-id="1517e-139">For more information, see [Creating a Base Class](creating-a-base-class.md) and [Writing a Class Provider](writing-a-class-provider.md).</span></span>

<span data-ttu-id="1517e-140">Das Codebeispiel in diesem Thema erfordert, dass die folgende \# include-Anweisung ordnungsgemäß kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="1517e-140">The code example in this topic requires the following \#include statement to compile correctly.</span></span>


```C++
#include <wbemidl.h>
```



<span data-ttu-id="1517e-141">Im folgenden Verfahren wird beschrieben, wie eine abgeleitete Klasse mit C++ erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="1517e-141">The following procedure describes how to create a derived class using C++.</span></span>

<span data-ttu-id="1517e-142">**So erstellen Sie eine abgeleitete Klasse mithilfe von C++**</span><span class="sxs-lookup"><span data-stu-id="1517e-142">**To create a derived class using C++**</span></span>

1.  <span data-ttu-id="1517e-143">Suchen Sie die Basisklasse mit einem Befehl von [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span><span class="sxs-lookup"><span data-stu-id="1517e-143">Locate the base class with a call to [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span></span>

    <span data-ttu-id="1517e-144">Im folgenden Codebeispiel wird gezeigt, wie Sie die Beispiel Basisklasse finden.</span><span class="sxs-lookup"><span data-stu-id="1517e-144">The following code example shows how to locate the Example base class.</span></span>

    ```C++
    // The pSv variable is of type IWbemServices *

    IWbemClassObject *pNewDerivedClass = 0;
    IWbemClassObject *pExampleClass = 0;
    IWbemContext *pCtx = 0;
    IWbemCallResult *pResult = 0;

    BSTR PathToClass = SysAllocString(L"Example");
    HRESULT hRes = pSvc->GetObject(PathToClass, 0, pCtx, &pExampleClass, &pResult);
    SysFreeString(PathToClass);
    ```

    

2.  <span data-ttu-id="1517e-145">Erstellen Sie ein abgeleitetes Objekt aus der Basisklasse mit einem-Befehl, der [**IWbemClassObject:: spawnderivedclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawnderivedclass)aufruft.</span><span class="sxs-lookup"><span data-stu-id="1517e-145">Create a derived object from the base class with a call to [**IWbemClassObject::SpawnDerivedClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawnderivedclass).</span></span>

    <span data-ttu-id="1517e-146">Im folgenden Codebeispiel wird gezeigt, wie ein abgeleitetes Klassenobjekt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="1517e-146">The following code example shows how to create a derived class object.</span></span>

    ```C++
    pExampleClass->SpawnDerivedClass(0, &pNewDerivedClass);
    pExampleClass->Release();  // Don't need the parent class any more
    ```

    

3.  <span data-ttu-id="1517e-147">Richten Sie einen Namen für die Klasse ein, indem Sie die **\_ \_ Klassen** System Eigenschaft mit einem-Befehl für die [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) -Methode festlegen.</span><span class="sxs-lookup"><span data-stu-id="1517e-147">Establish a name for the class by setting the **\_\_CLASS** system property with a call to the [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) method.</span></span>

    <span data-ttu-id="1517e-148">Im folgenden Codebeispiel wird gezeigt, wie der abgeleiteten Klasse ein Name zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="1517e-148">The following code example shows how to assign a name to the derived class.</span></span>

    ```C++
    VARIANT v;
    VariantInit(&v);

    V_VT(&v) = VT_BSTR;
    V_BSTR(&v) = SysAllocString(L"Example2");
    BSTR Class = SysAllocString(L"__CLASS");
    pNewDerivedClass->Put(Class, 0, &v, 0);
    SysFreeString(Class);
    VariantClear(&v);
    ```

    

4.  <span data-ttu-id="1517e-149">Erstellen Sie zusätzliche Eigenschaften mit [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span><span class="sxs-lookup"><span data-stu-id="1517e-149">Create additional properties with [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span></span>

    <span data-ttu-id="1517e-150">Im folgenden Codebeispiel wird gezeigt, wie zusätzliche Eigenschaften erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="1517e-150">The following code example shows how to create additional properties.</span></span>

    ```C++
    BSTR OtherProp = SysAllocString(L"OtherInfo2");
    pNewDerivedClass->Put(OtherProp, 0, NULL, CIM_STRING); 
    SysFreeString(OtherProp);
    ```

    

5.  <span data-ttu-id="1517e-151">Speichern Sie die neue Klasse durch Aufrufen von [**IWbemServices::P utclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).</span><span class="sxs-lookup"><span data-stu-id="1517e-151">Save the new class by calling [**IWbemServices::PutClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).</span></span>

    <span data-ttu-id="1517e-152">Im folgenden Codebeispiel wird gezeigt, wie die neue abgeleitete Klasse gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="1517e-152">The following code example shows how to save the new derived class.</span></span>

    ```C++
    hRes = pSvc->PutClass(pNewDerivedClass, 0, pCtx, &pResult);
    pNewDerivedClass->Release();
    ```

    

<span data-ttu-id="1517e-153">Im folgenden Codebeispiel werden die Codebeispiele kombiniert, die im vorherigen Verfahren erläutert wurden, um das Erstellen einer abgeleiteten Klasse mithilfe der WMI-API zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="1517e-153">The following code example combines the code examples discussed in the previous procedure to describe how to create a derived class using the WMI API.</span></span>


```C++
void CreateDerivedClass(IWbemServices *pSvc)
{
  IWbemClassObject *pNewDerivedClass = 0;
  IWbemClassObject *pExampleClass = 0;
  IWbemContext *pCtx = 0;
  IWbemCallResult *pResult = 0;

  BSTR PathToClass = SysAllocString(L"Example");
  HRESULT hRes = pSvc->GetObject(PathToClass, 0, pCtx, 
    &pExampleClass, &pResult);
  SysFreeString(PathToClass);

  if (hRes != 0)
    return;

  pExampleClass->SpawnDerivedClass(0, &pNewDerivedClass);
  pExampleClass->Release();  // The parent class is no longer needed

  VARIANT v;
  VariantInit(&v);

  // Create the class name.
  // =====================

  V_VT(&v) = VT_BSTR;
  V_BSTR(&v) = SysAllocString(L"Example2");
  BSTR Class = SysAllocString(L"__CLASS");
  pNewDerivedClass->Put(Class, 0, &v, 0);
  SysFreeString(Class);
  VariantClear(&v);

  // Create another property.
  // =======================
  BSTR OtherProp = SysAllocString(L"OtherInfo2");
  // No default value
  pNewDerivedClass->Put(OtherProp, 0, NULL, CIM_STRING); 
  SysFreeString(OtherProp);
  
  // Register the class with WMI. 
  // ============================
  hRes = pSvc->PutClass(pNewDerivedClass, 0, pCtx, &pResult);
  pNewDerivedClass->Release();
}
```



<span data-ttu-id="1517e-154">Im folgenden Verfahren wird beschrieben, wie eine abgeleitete Klasse mithilfe von MOF-Code definiert wird.</span><span class="sxs-lookup"><span data-stu-id="1517e-154">The following procedure describes how to define a derived class using MOF code.</span></span>

<span data-ttu-id="1517e-155">**So definieren Sie eine abgeleitete Klasse mithilfe von MOF-Code**</span><span class="sxs-lookup"><span data-stu-id="1517e-155">**To define a derived class using MOF code**</span></span>

1.  <span data-ttu-id="1517e-156">Definieren Sie Ihre abgeleitete Klasse mit dem Schlüsselwort **Class** , gefolgt vom Namen der abgeleiteten Klasse und dem Namen der übergeordneten Klasse, getrennt durch einen Doppelpunkt.</span><span class="sxs-lookup"><span data-stu-id="1517e-156">Define your derived class with the **Class** keyword, followed by the name of your derived class, and the name of the parent class separated by a colon.</span></span>

    <span data-ttu-id="1517e-157">Im folgenden Codebeispiel wird die Implementierung einer abgeleiteten Klasse beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1517e-157">The following code example describes an implementation of a derived class.</span></span>

    ``` syntax
    class MyClass 
    {
        [key] string   strProp;
        sint32   dwProp1;
        uint32       dwProp2;
    };

    class MyDerivedClass : MyClass
    {
        string   strDerivedProp;
        sint32   dwDerivedProp;
    };
    ```

2.  <span data-ttu-id="1517e-158">Kompilieren Sie den MOF-Code nach Abschluss des Vorgangs mit dem MOF-Compiler.</span><span class="sxs-lookup"><span data-stu-id="1517e-158">When complete, compile your MOF code with the MOF compiler.</span></span>

    <span data-ttu-id="1517e-159">Weitere Informationen finden Sie unter [Kompilieren von MOF-Dateien](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="1517e-159">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1517e-160">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1517e-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1517e-161">Erstellen einer Klasse</span><span class="sxs-lookup"><span data-stu-id="1517e-161">Creating a Class</span></span>](creating-a-class.md)
</dt> </dl>

 

 



