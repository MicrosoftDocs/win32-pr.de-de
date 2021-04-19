---
description: Sie können eine Instanz in C++ über die IWbemServices-Schnittstelle erstellen.
ms.assetid: ee54c1ef-bc91-4771-8c11-9ee3aacd8112
ms.tgt_platform: multiple
title: Erstellen und Deklarieren einer Instanz mithilfe von C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd316975c68625383a9d2a2d1fe2fc389d30494a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356970"
---
# <a name="creating-and-declaring-an-instance-using-c"></a><span data-ttu-id="d63fd-103">Erstellen und Deklarieren einer Instanz mithilfe von C++</span><span class="sxs-lookup"><span data-stu-id="d63fd-103">Creating and Declaring an Instance Using C++</span></span>

<span data-ttu-id="d63fd-104">Sie können eine Instanz in C++ über die [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Schnittstelle erstellen.</span><span class="sxs-lookup"><span data-stu-id="d63fd-104">You can create an instance in C++ through the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface.</span></span>

<span data-ttu-id="d63fd-105">Die Codebeispiele in diesem Thema erfordern, dass die folgende \# include-Anweisung ordnungsgemäß kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="d63fd-105">The code examples in this topic require the following \#include statement to compile correctly.</span></span>


```C++
#include <wbemidl.h>
```



<span data-ttu-id="d63fd-106">Im folgenden Verfahren wird beschrieben, wie eine Instanz einer vorhandenen Klasse erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d63fd-106">The following procedure describes how to create an instance of an existing class.</span></span>

<span data-ttu-id="d63fd-107">**So erstellen Sie eine Instanz einer vorhandenen Klasse**</span><span class="sxs-lookup"><span data-stu-id="d63fd-107">**To create an instance of an existing class**</span></span>

1.  <span data-ttu-id="d63fd-108">Rufen Sie die Definition der vorhandenen Klasse ab, indem Sie die [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) -Methode oder die [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d63fd-108">Retrieve the definition of the existing class by calling the [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) methods.</span></span>

    <span data-ttu-id="d63fd-109">Im folgenden Codebeispiel wird gezeigt, wie die [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) -Methode und die [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) -Methode verwendet werden, um einen Zeiger auf die [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) -Schnittstelle zu erhalten, die Zugriff auf die Klassendefinition bietet.</span><span class="sxs-lookup"><span data-stu-id="d63fd-109">The following code example shows how to use the [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) and [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) methods to get a pointer to the [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) interface that provides access to the class definition.</span></span>

    ```C++
    // The pSv variable is of type IWbemServices *

    IWbemClassObject *pNewInstance = 0;
    IWbemClassObject *pExampleClass = 0;
    IWbemContext *pCtx = 0;
    IWbemCallResult *pResult = 0;

    BSTR PathToClass = SysAllocString(L"Example");
    HRESULT hRes = pSvc->GetObject(PathToClass, 0, pCtx, 
                  &pExampleClass, &pResult);
    SysFreeString(PathToClass);
    ```

    

2.  <span data-ttu-id="d63fd-110">Erstellen Sie die neue-Instanz, indem Sie die [**IWbemClassObject:: SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d63fd-110">Create the new instance by calling the [**IWbemClassObject::SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) method.</span></span>

    <span data-ttu-id="d63fd-111">Im folgenden Codebeispiel wird gezeigt, wie Sie eine neue-Instanz erstellen und dann die-Klasse freigeben.</span><span class="sxs-lookup"><span data-stu-id="d63fd-111">The following code example shows how to create a new instance and then release the class.</span></span>

    ```C++
    pExampleClass->SpawnInstance(0, &pNewInstance);
    pExampleClass->Release();  // Don't need the class any more
    ```

    

3.  <span data-ttu-id="d63fd-112">Legen Sie Werte für alle Eigenschaften fest, die die Werte, die für die Klasse definiert sind, durch Aufrufen der Methode [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) nicht erben.</span><span class="sxs-lookup"><span data-stu-id="d63fd-112">Set values for any properties that do not inherit the values defined for the class by calling the [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) method.</span></span>

    <span data-ttu-id="d63fd-113">Jede Instanz einer Klasse erbt alle Eigenschaften, die für die Klasse definiert sind.</span><span class="sxs-lookup"><span data-stu-id="d63fd-113">Each instance of a class inherits all of the properties that are defined for the class.</span></span> <span data-ttu-id="d63fd-114">Sie können jedoch andere Eigenschaftswerte angeben, wenn Sie auswählen.</span><span class="sxs-lookup"><span data-stu-id="d63fd-114">However, you can specify different property values if you choose.</span></span>

    <span data-ttu-id="d63fd-115">Wenn die vorhandene Klasse über eine Schlüsseleigenschaft verfügt, sollten Sie die-Eigenschaft entweder auf **null** oder einen garantierten eindeutigen Wert festlegen.</span><span class="sxs-lookup"><span data-stu-id="d63fd-115">If the existing class has a key property, you should set the property either to **NULL** or a guaranteed unique value.</span></span> <span data-ttu-id="d63fd-116">Wenn Sie den Schlüssel auf **null** festlegen und der Schlüssel eine Zeichenfolge ist, generiert [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) oder [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) intern eine GUID und weist Sie dem Schlüssel zu.</span><span class="sxs-lookup"><span data-stu-id="d63fd-116">If you set the key to **NULL** and the key is a string, then [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) or [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) internally generates and assigns a GUID to the key.</span></span> <span data-ttu-id="d63fd-117">Auf diese Weise können Sie bei Angabe von **null** für eine Schlüsseleigenschaft eine eindeutige-Instanz erstellen, die keine vorherige Instanz überschreibt.</span><span class="sxs-lookup"><span data-stu-id="d63fd-117">This way, specifying **NULL** for a key property lets you create a unique instance that will not overwrite any previous instance.</span></span>

    <span data-ttu-id="d63fd-118">Im folgenden Codebeispiel wird veranschaulicht, wie der Wert der [**Index**](swbemrefreshableitem-index.md) Eigenschaft der Instanzklasse example festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="d63fd-118">The following code example shows how to set the [**Index**](swbemrefreshableitem-index.md) property value of the example instance class.</span></span>

    ```C++
    VARIANT v;
    VariantInit(&v);

    V_VT(&v) = VT_BSTR;
    V_BSTR(&v) = SysAllocString(L"IX100");

    BSTR KeyProp = SysAllocString(L"Index");
    pNewInstance->Put(KeyProp, 0, &v, 0);
    SysFreeString(KeyProp);
    VariantClear(&v);
    ```

    

4.  <span data-ttu-id="d63fd-119">Legen Sie die Werte für alle relevanten Qualifizierer durch einen Befehl von [**IWbemClassObject:: getqualifierset**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset)fest.</span><span class="sxs-lookup"><span data-stu-id="d63fd-119">Set the values for any relevant qualifiers through a call to [**IWbemClassObject::GetQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset).</span></span>

    <span data-ttu-id="d63fd-120">Die [**getqualifierset**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset) -Methode gibt einen Zeiger auf eine [**iwbemqualifierset**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) -Schnittstelle zurück, die für den Zugriff auf die Qualifizierer für eine Klasse oder eine Instanz verwendet.</span><span class="sxs-lookup"><span data-stu-id="d63fd-120">The [**GetQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset) method returns a pointer to an [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) interface, which use to access the qualifiers for a class or instance.</span></span> <span data-ttu-id="d63fd-121">Sie können unterschiedliche Werte für einen Qualifizierer angeben, der für die Klasse definiert ist, wenn die klassenqualifizierungskonfiguration **EnableOverride**</span><span class="sxs-lookup"><span data-stu-id="d63fd-121">You can specify different values for a qualifier defined for the class if the class qualifier flavor is **EnableOverride**.</span></span> <span data-ttu-id="d63fd-122">Klassen Qualifizierer können nicht geändert oder gelöscht werden </span><span class="sxs-lookup"><span data-stu-id="d63fd-122">You cannot modify or delete a class qualifier with the flavor set to **DisableOverride**.</span></span> <span data-ttu-id="d63fd-123">Weitere Informationen finden Sie unter [qualifizierervarianten](qualifier-flavors.md).</span><span class="sxs-lookup"><span data-stu-id="d63fd-123">For more information, see [Qualifier Flavors](qualifier-flavors.md).</span></span>

    <span data-ttu-id="d63fd-124">Optional können Sie auch zusätzliche Qualifizierer für Ihre Instanzklasse definieren.</span><span class="sxs-lookup"><span data-stu-id="d63fd-124">As an option, you can also define additional qualifiers for your instance class.</span></span> <span data-ttu-id="d63fd-125">Sie können zusätzliche Qualifizierer für die Instanz oder die Instanzeigenschaft definieren, die nicht in der Klassen Deklaration enthalten sein müssen.</span><span class="sxs-lookup"><span data-stu-id="d63fd-125">You can define additional qualifiers for the instance or instance property which do not need to appear in the class declaration.</span></span>

5.  <span data-ttu-id="d63fd-126">Speichern Sie die Instanz, indem Sie die [**IWbemServices::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) -Methode oder die [**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d63fd-126">Save the instance by calling the [**IWbemServices::PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) or [**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) method.</span></span>

    <span data-ttu-id="d63fd-127">WMI speichert die Instanz im aktuellen WMI-Namespace.</span><span class="sxs-lookup"><span data-stu-id="d63fd-127">WMI saves the instance in the current WMI namespace.</span></span> <span data-ttu-id="d63fd-128">Daher ist der vollständige Pfad der-Instanz vom-Namespace abhängig, bei dem es sich in der Regel um einen Stamm \\ Standard handelt.</span><span class="sxs-lookup"><span data-stu-id="d63fd-128">As such, the full path of the instance is dependent on the namespace, which is typically root\\default.</span></span> <span data-ttu-id="d63fd-129">Für dieses Codebeispiel lautet der vollständige Pfadname \\ \\ . \\ root \\ Default: example. Index = "IX100".</span><span class="sxs-lookup"><span data-stu-id="d63fd-129">For this code example, the full path name would be \\\\.\\root\\default:Example.Index="IX100".</span></span>

    <span data-ttu-id="d63fd-130">Im folgenden Codebeispiel wird gezeigt, wie eine-Instanz gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="d63fd-130">The following code example shows how to save an instance.</span></span>

    ```C++
        hRes = pSvc->PutInstance(pNewInstance, 0, pCtx, &pResult);
        pNewInstance->Release();
    ```

    

<span data-ttu-id="d63fd-131">Das Speichern der Instanz in WMI sperrt mehrere der Eigenschaften der Instanz.</span><span class="sxs-lookup"><span data-stu-id="d63fd-131">Saving the instance to WMI locks down several of the properties of the instance.</span></span>

<span data-ttu-id="d63fd-132">Vor allem können Sie die folgenden Vorgänge nicht über die WMI-API ausführen, nachdem eine Instanz in der WMI-Infrastruktur vorhanden ist:</span><span class="sxs-lookup"><span data-stu-id="d63fd-132">Specifically, you cannot perform any of the following operations through the WMI API after an instance exists within the WMI infrastructure:</span></span>

-   <span data-ttu-id="d63fd-133">Ändern Sie die übergeordnete Klasse der Klasse, zu der die Instanz gehört.</span><span class="sxs-lookup"><span data-stu-id="d63fd-133">Change the parent class of the class to which the instance belongs.</span></span>
-   <span data-ttu-id="d63fd-134">Eigenschaften hinzufügen oder entfernen.</span><span class="sxs-lookup"><span data-stu-id="d63fd-134">Add or remove properties.</span></span>
-   <span data-ttu-id="d63fd-135">Ändern Sie die Eigenschafts Typen.</span><span class="sxs-lookup"><span data-stu-id="d63fd-135">Change property types.</span></span>
-   <span data-ttu-id="d63fd-136">[**Schlüssel**](standard-qualifiers.md) oder **indizierte** Qualifizierer hinzufügen oder entfernen.</span><span class="sxs-lookup"><span data-stu-id="d63fd-136">Add or remove [**Key**](standard-qualifiers.md) or **Indexed** qualifiers.</span></span>
-   <span data-ttu-id="d63fd-137">Fügen Sie [**Singleton**](standard-wmi-qualifiers.md)-, **dynamische** oder [**abstrakte**](standard-qualifiers.md) Qualifizierer hinzu oder entfernen Sie Sie.</span><span class="sxs-lookup"><span data-stu-id="d63fd-137">Add or remove [**Singleton**](standard-wmi-qualifiers.md), **Dynamic**, or [**Abstract**](standard-qualifiers.md) qualifiers.</span></span>

<span data-ttu-id="d63fd-138">Im folgenden Codebeispiel werden die Codebeispiele kombiniert, die im vorherigen Verfahren erläutert wurden, um zu veranschaulichen, wie eine-Instanz mithilfe der WMI-API erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d63fd-138">The following code example combines the code examples discussed in the previous procedure to show how to create an instance using the WMI API.</span></span>


```C++
void CreateInstance (IWbemServices *pSvc)
{
    IWbemClassObject *pNewInstance = 0;
    IWbemClassObject *pExampleClass = 0;
    IWbemContext *pCtx = 0;
    IWbemCallResult *pResult = 0;

    // Get the class definition.
    BSTR PathToClass = SysAllocString(L"Example");
    HRESULT hRes = pSvc->GetObject(PathToClass, 0, pCtx, 
                 &pExampleClass, &pResult);
    SysFreeString(PathToClass);

    if (hRes != 0)
       return;

    // Create a new instance.
    pExampleClass->SpawnInstance(0, &pNewInstance);
    pExampleClass->Release();  // Don't need the class any more

    VARIANT v;
    VariantInit(&v);

    // Set the Index property (the key).
    V_VT(&v) = VT_BSTR;
    V_BSTR(&v) = SysAllocString(L"IX100");

    BSTR KeyProp = SysAllocString(L"Index");
    pNewInstance->Put(KeyProp, 0, &v, 0);
    SysFreeString(KeyProp);
    VariantClear(&v);

    // Set the IntVal property.
    V_VT(&v) = VT_I4;
    V_I4(&v) = 1001;  
    
    BSTR Prop = SysAllocString(L"IntVal");
    pNewInstance->Put(Prop, 0, &v, 0);
    SysFreeString(Prop);
    VariantClear(&v);    
    
    // Other properties acquire the 'default' value specified
    // in the class definition unless otherwise modified here.

    // Write the instance to WMI. 
    hRes = pSvc->PutInstance(pNewInstance, 0, pCtx, &pResult);
    pNewInstance->Release();
}
```



 

 



