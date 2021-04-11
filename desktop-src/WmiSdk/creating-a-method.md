---
description: Um eine WMI-Methode zu erstellen, definieren Sie die Eingabe-und Ausgabeparameter für die Methode.
ms.assetid: 71cbecde-33c4-4bf1-9793-bef6d823dcac
ms.tgt_platform: multiple
title: Erstellen einer WMI-Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2489a5dd4e97ed6c8d26eeb292c45fa66901cbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217965"
---
# <a name="creating-a-wmi-method"></a><span data-ttu-id="76496-103">Erstellen einer WMI-Methode</span><span class="sxs-lookup"><span data-stu-id="76496-103">Creating a WMI Method</span></span>

<span data-ttu-id="76496-104">Um eine WMI-Methode zu erstellen, definieren Sie die Eingabe-und Ausgabeparameter für die Methode.</span><span class="sxs-lookup"><span data-stu-id="76496-104">To create a WMI method, define the input and output parameters for the method.</span></span> <span data-ttu-id="76496-105">Die Eingabe-und Ausgabeparameter werden durch einen speziellen WMI-System Klassen [**\_ \_ Parameter**](--parameters.md)dargestellt.</span><span class="sxs-lookup"><span data-stu-id="76496-105">The input and output parameters are represented by a special WMI system class [**\_\_PARAMETERS**](--parameters.md).</span></span> <span data-ttu-id="76496-106">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md) und [Schreiben eines Methoden Anbieters](writing-a-method-provider.md).</span><span class="sxs-lookup"><span data-stu-id="76496-106">For more information, see [Calling a Method](calling-a-method.md) and [Writing a Method Provider](writing-a-method-provider.md).</span></span>

<span data-ttu-id="76496-107">In diesem Thema werden die folgenden Abschnitte erläutert:</span><span class="sxs-lookup"><span data-stu-id="76496-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="76496-108">Erstellen einer WMI-Klassenmethode in MOF</span><span class="sxs-lookup"><span data-stu-id="76496-108">Creating a WMI Class Method in MOF</span></span>](#creating-a-wmi-class-method-in-mof)
-   [<span data-ttu-id="76496-109">Erstellen einer WMI-Klassenmethode in C++</span><span class="sxs-lookup"><span data-stu-id="76496-109">Creating a WMI Class Method in C++</span></span>](#creating-a-wmi-class-method-in-c)
-   [<span data-ttu-id="76496-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="76496-110">Related topics</span></span>](#related-topics)

## <a name="creating-a-wmi-class-method-in-mof"></a><span data-ttu-id="76496-111">Erstellen einer WMI-Klassenmethode in MOF</span><span class="sxs-lookup"><span data-stu-id="76496-111">Creating a WMI Class Method in MOF</span></span>

<span data-ttu-id="76496-112">In WMI sind Anbieter Methoden in der Regel unterschiedliche Aktionen im Zusammenhang mit dem Objekt, das die-Klasse darstellt.</span><span class="sxs-lookup"><span data-stu-id="76496-112">In WMI, provider methods are generally distinct actions related to the object that the class represents.</span></span> <span data-ttu-id="76496-113">Anstatt den Wert einer Eigenschaft zu ändern, um eine Aktion auszuführen, sollte eine Methode erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="76496-113">Rather than change the value of a property to execute an action, a method should be created.</span></span> <span data-ttu-id="76496-114">Beispielsweise können Sie ein Netzwerk Informations Center (Network Information Center, NIC), das durch den [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-networkadapter) -Netzwerkadapter dargestellt wird, mithilfe der Methoden [**enable**](/windows/desktop/CIMWin32Prov/enable-method-in-class-win32-networkadapter) und [**Deaktivieren**](/windows/desktop/CIMWin32Prov/disable-method-in-class-win32-networkadapter) aktivieren oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="76496-114">For example, you can enable or disable a network information center (NIC) that is represented by [**Win32\_NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter) by using the [**Enable**](/windows/desktop/CIMWin32Prov/enable-method-in-class-win32-networkadapter) and [**Disable**](/windows/desktop/CIMWin32Prov/disable-method-in-class-win32-networkadapter) methods.</span></span> <span data-ttu-id="76496-115">Diese Aktionen können zwar als Lese-/Schreibeigenschaft dargestellt werden, aber der empfohlene Entwurf ist das Erstellen einer Methode.</span><span class="sxs-lookup"><span data-stu-id="76496-115">While these actions can be represented as a read/write property, the recommended design is to create a method.</span></span> <span data-ttu-id="76496-116">Wenn Sie einen Status oder Wert für die Klasse sichtbar machen möchten, wird empfohlen, anstelle einer Methode eine Lese-/Schreibeigenschaft zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="76496-116">Alternatively, if you want to make a state or value visible for the class, then the recommended approach is to create a read/write property rather than a method.</span></span> <span data-ttu-id="76496-117">In **Win32 \_ Network Adapter** bewirkt die Eigenschaft " **nettenabled** ", dass der Status des Adapters sichtbar ist, aber Änderungen zwischen Zuständen durch die Methoden " **enable** " und " **Deaktivieren** " ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="76496-117">In **Win32\_NetworkAdapter**, the **NetEnabled** property makes the state of the adapter visible but changes between states are executed by the **Enable** or **Disable** methods.</span></span>

<span data-ttu-id="76496-118">Klassen Deklarationen können die Deklaration von einer oder mehreren Methoden einschließen.</span><span class="sxs-lookup"><span data-stu-id="76496-118">Class declarations can include the declaration of one or more methods.</span></span> <span data-ttu-id="76496-119">Sie können entweder die Methoden einer übergeordneten Klasse erben oder Ihre eigene Klasse implementieren.</span><span class="sxs-lookup"><span data-stu-id="76496-119">You can either choose to inherit the methods of a parent class, or implement your own.</span></span> <span data-ttu-id="76496-120">Wenn Sie sich für die Implementierung Ihrer eigenen Methoden entscheiden, müssen Sie die-Methode deklarieren und die Methode mit bestimmten qualifizierertags markieren.</span><span class="sxs-lookup"><span data-stu-id="76496-120">If you choose to implement your own methods, you must declare the method and mark the method with specific qualifier tags.</span></span>

<span data-ttu-id="76496-121">Im folgenden Verfahren wird beschrieben, wie Sie eine Methode in einer Klasse deklarieren, die nicht von einer Basisklasse erbt.</span><span class="sxs-lookup"><span data-stu-id="76496-121">The following procedure describes how to declare a method in a class that does not inherit from a base class.</span></span>

<span data-ttu-id="76496-122">**So deklarieren Sie eine Methode**</span><span class="sxs-lookup"><span data-stu-id="76496-122">**To declare a method**</span></span>

1.  <span data-ttu-id="76496-123">Definieren Sie den Namen der Methode zwischen den geschweiften Klammern einer Klassen Deklaration, gefolgt von allen Qualifizierern.</span><span class="sxs-lookup"><span data-stu-id="76496-123">Define the name of your method between the curly braces of a class declaration, followed by any qualifiers.</span></span>

    <span data-ttu-id="76496-124">Im folgenden Codebeispiel wird die Syntax für eine-Methode beschrieben.</span><span class="sxs-lookup"><span data-stu-id="76496-124">The following code example describes the syntax for a method.</span></span>

    ``` syntax
    [Dynamic, Provider ("ProviderName")]
    class ClassName
    {
        [Implemented] <ReturnType> <MethodName>
            ([ParameterDirection, IDQualifier] 
            <ParameterType> <ParameterName>);
    };
    ```

2.  <span data-ttu-id="76496-125">Wenn Sie fertig sind, fügen Sie den MOF-Code (Managed Object Format) in das WMI-Repository ein, indem Sie den MOF-Compiler aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="76496-125">When finished, insert your Managed Object Format (MOF) code into the WMI repository with a call to the MOF compiler.</span></span>

    <span data-ttu-id="76496-126">Weitere Informationen finden Sie unter [Kompilieren von MOF-Dateien](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="76496-126">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

<span data-ttu-id="76496-127">In der folgenden Liste sind die Elemente der Methoden Deklaration definiert.</span><span class="sxs-lookup"><span data-stu-id="76496-127">The following list defines the elements of the method declaration.</span></span>

<dl> <dt>

<span data-ttu-id="76496-128"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>[**Ab**](/windows/desktop/api/Provider/nl-provider-provider)</span><span class="sxs-lookup"><span data-stu-id="76496-128"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>[**Provider**](/windows/desktop/api/Provider/nl-provider-provider)</span></span>
</dt> <dd>

<span data-ttu-id="76496-129">Verknüpft einen bestimmten Anbieter mit ihrer Klassen Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="76496-129">Links a specific provider to your class description.</span></span> <span data-ttu-id="76496-130">Der Wert des [**Anbieter**](/windows/desktop/api/Provider/nl-provider-provider) Qualifizierers ist der Name des Anbieters, der WMI anweist, wo sich der Code befindet, der die Methode unterstützt.</span><span class="sxs-lookup"><span data-stu-id="76496-130">The value of the [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier is the name of the provider, which tells WMI where the code that supports your method resides.</span></span> <span data-ttu-id="76496-131">Ein Anbieter sollte auch eine beliebige Klasse mit dynamischen Instanzen mit dem **dynamischen** Qualifizierer markieren.</span><span class="sxs-lookup"><span data-stu-id="76496-131">A provider should also mark with the **Dynamic** qualifier any class that has dynamic instances.</span></span> <span data-ttu-id="76496-132">Verwenden Sie hingegen nicht den **dynamischen** Qualifizierer, um eine Klasse zu markieren, die eine statische Instanz mit **implementierten** Methoden enthält.</span><span class="sxs-lookup"><span data-stu-id="76496-132">In contrast, do not use the **Dynamic** qualifier to mark a class that contains a static instance with **Implemented** methods.</span></span>

</dd> <dt>

<span data-ttu-id="76496-133"><span id="Implemented"></span><span id="implemented"></span><span id="IMPLEMENTED"></span>**Realisierte**</span><span class="sxs-lookup"><span data-stu-id="76496-133"><span id="Implemented"></span><span id="implemented"></span><span id="IMPLEMENTED"></span>**Implemented**</span></span>
</dt> <dd>

<span data-ttu-id="76496-134">Deklariert, dass Sie eine Methode implementieren, anstatt die Methoden Implementierung von der übergeordneten Klasse zu erben.</span><span class="sxs-lookup"><span data-stu-id="76496-134">Declares that you will implement a method, rather than inherit the method implementation from the parent class.</span></span> <span data-ttu-id="76496-135">Standardmäßig wird die Implementierung der übergeordneten Klasse von WMI an eine abgeleitete Klasse weitergegeben, es sei denn, die abgeleitete Klasse stellt eine-Implementierung bereit.</span><span class="sxs-lookup"><span data-stu-id="76496-135">By default, WMI propagates the implementation of the parent class to a derived class unless the derived class provides an implementation.</span></span> <span data-ttu-id="76496-136">Das Weglassen des **implementierten** Qualifizierers gibt an, dass die Methode in dieser Klasse keine Implementierung aufweist.</span><span class="sxs-lookup"><span data-stu-id="76496-136">Omitting the **Implemented** qualifier indicates that the method has no implementation in that class.</span></span> <span data-ttu-id="76496-137">Wenn Sie eine Methode ohne den **implementierten** Qualifizierer erneut deklarieren, geht WMI weiterhin davon aus, dass Sie diese Methode nicht implementieren, und ruft die Implementierung der übergeordneten Klassenmethode auf, wenn aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="76496-137">If you redeclare a method without the **Implemented** qualifier, WMI still assumes that you are not going to implement that method, and invokes the parent class method implementation when called.</span></span> <span data-ttu-id="76496-138">Daher ist es hilfreich, eine Methode in einer abgeleiteten Klasse erneut zu deklarieren, ohne den **implementierten** Qualifizierer anzufügen, wenn Sie der Methode einen Qualifizierer hinzufügen oder daraus entfernen.</span><span class="sxs-lookup"><span data-stu-id="76496-138">As such, redeclaring a method in a derived class without attaching the **Implemented** qualifier is useful only when you add or remove a qualifier to or from the method.</span></span>

</dd> <dt>

<span data-ttu-id="76496-139"><span id="ReturnType"></span><span id="returntype"></span><span id="RETURNTYPE"></span>ReturnType</span><span class="sxs-lookup"><span data-stu-id="76496-139"><span id="ReturnType"></span><span id="returntype"></span><span id="RETURNTYPE"></span>ReturnType</span></span>
</dt> <dd>

<span data-ttu-id="76496-140">Beschreibt den Wert, den die Methode zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="76496-140">Describes what value the method returns.</span></span> <span data-ttu-id="76496-141">Der Rückgabewert einer Methode muss ein boolesches, numerisches, **char**-, **String**-, [DateTime](datetime.md)-oder Schema-Objekt sein.</span><span class="sxs-lookup"><span data-stu-id="76496-141">The return value for a method must be a Boolean, numeric, **CHAR**, **STRING**, [DATETIME](datetime.md), or schema object.</span></span> <span data-ttu-id="76496-142">Sie können den Rückgabetyp auch als [void](void.md)deklarieren, um anzugeben, dass die Methode nichts zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="76496-142">You can also declare the return type as [VOID](void.md), indicating that the method returns nothing.</span></span> <span data-ttu-id="76496-143">Es ist jedoch nicht möglich, ein Array als Rückgabe Werttyp zu deklarieren.</span><span class="sxs-lookup"><span data-stu-id="76496-143">However, you cannot declare an array as a return value type.</span></span>

</dd> <dt>

<span data-ttu-id="76496-144"><span id="MethodName"></span><span id="methodname"></span><span id="METHODNAME"></span>MethodName</span><span class="sxs-lookup"><span data-stu-id="76496-144"><span id="MethodName"></span><span id="methodname"></span><span id="METHODNAME"></span>MethodName</span></span>
</dt> <dd>

<span data-ttu-id="76496-145">Definiert den Namen der Methode.</span><span class="sxs-lookup"><span data-stu-id="76496-145">Defines the name of the method.</span></span> <span data-ttu-id="76496-146">Jede Methode muss einen eindeutigen Namen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="76496-146">Every method must have a unique name.</span></span> <span data-ttu-id="76496-147">WMI lässt nicht zu, dass zwei Methoden mit demselben Namen und unterschiedlichen Signaturen in einer Klasse oder innerhalb einer Klassenhierarchie vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="76496-147">WMI does not allow two methods with the same name and different signatures to exist in one class or within a class hierarchy.</span></span> <span data-ttu-id="76496-148">Daher ist es auch nicht möglich, eine Methode zu überladen.</span><span class="sxs-lookup"><span data-stu-id="76496-148">As such, you also cannot overload a method.</span></span>

</dd> <dt>

<span data-ttu-id="76496-149"><span id="ParameterDirection"></span><span id="parameterdirection"></span><span id="PARAMETERDIRECTION"></span>ParameterDirection</span><span class="sxs-lookup"><span data-stu-id="76496-149"><span id="ParameterDirection"></span><span id="parameterdirection"></span><span id="PARAMETERDIRECTION"></span>ParameterDirection</span></span>
</dt> <dd>

<span data-ttu-id="76496-150">Enthält Qualifizierer, die beschreiben, ob ein Parameter ein Eingabeparameter, ein Ausgabeparameter oder beides ist.</span><span class="sxs-lookup"><span data-stu-id="76496-150">Contains qualifiers that describe if a parameter is an input parameter, output parameter, or both.</span></span> <span data-ttu-id="76496-151">Verwenden Sie nicht denselben Parameternamen mehrmals als Eingabeparameter oder mehr als einen Zeitparameter als Ausgabeparameter.</span><span class="sxs-lookup"><span data-stu-id="76496-151">Do not use the same parameter name more than one time as an input parameter or more than one time as an output parameter.</span></span> <span data-ttu-id="76496-152">Wenn derselbe Parameter Name sowohl [**für den in**](standard-qualifiers.md) -als auch für den **out** -Qualifizierer angezeigt wird, ist die Funktionalität konzeptionell identisch mit der Verwendung der **in**-, **out** -Qualifizierer für einen einzelnen Parameter.</span><span class="sxs-lookup"><span data-stu-id="76496-152">If the same parameter name appears with both the [**In**](standard-qualifiers.md) and an **Out** qualifiers, the functionality is conceptually the same as using the **In**, **Out** qualifiers on a single parameter.</span></span> <span data-ttu-id="76496-153">Wenn jedoch separate Deklarationen verwendet werden, müssen die Eingabe-und Ausgabeparameter in allen anderen Punkten genau übereinstimmen, einschließlich Anzahl und Typ der [**ID**](standard-wmi-qualifiers.md) -Qualifizierer. der Qualifizierer muss gleich sein und explizit für beide deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="76496-153">However, when using separate declarations, the input and output parameters must be exactly the same in all other respects, including the number and type of [**ID**](standard-wmi-qualifiers.md) qualifiers, and the qualifier must be the same and explicitly declared for both.</span></span> <span data-ttu-id="76496-154">Es wird dringend empfohlen, die **in**-, **out** -Qualifizierer innerhalb einer einzelnen Parameter Deklaration zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="76496-154">It is strongly recommended to use the **In**, **Out** qualifiers within a single parameter declaration.</span></span>

</dd> <dt>

<span data-ttu-id="76496-155"><span id="IDQualifier"></span><span id="idqualifier"></span><span id="IDQUALIFIER"></span>**Idqualifizierer**</span><span class="sxs-lookup"><span data-stu-id="76496-155"><span id="IDQualifier"></span><span id="idqualifier"></span><span id="IDQUALIFIER"></span>**IDQualifier**</span></span>
</dt> <dd>

<span data-ttu-id="76496-156">Enthält den [**ID**](standard-wmi-qualifiers.md) -Qualifizierer, der die Position jedes Parameters innerhalb der Sequenz von Parametern in der Methode eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="76496-156">Contains the [**ID**](standard-wmi-qualifiers.md) qualifier that uniquely identifies the position of each parameter within the sequence of parameters in the method.</span></span> <span data-ttu-id="76496-157">Standardmäßig markiert der MOF-Compiler Parameter automatisch mit einem **ID** -Qualifizierer.</span><span class="sxs-lookup"><span data-stu-id="76496-157">By default, the MOF compiler automatically marks parameters with an **ID** qualifier.</span></span> <span data-ttu-id="76496-158">Der Compiler markiert den ersten Parameter mit einem Wert von 0 (null), dem zweiten Parameter dem Wert 1 (eins) usw.</span><span class="sxs-lookup"><span data-stu-id="76496-158">The compiler marks the first parameter with a value of 0 (zero), the second parameter a value of 1 (one), and so on.</span></span> <span data-ttu-id="76496-159">Falls erforderlich, können Sie die ID-Sequenz explizit im MOF-Code angeben.</span><span class="sxs-lookup"><span data-stu-id="76496-159">If necessary, you can explicitly state the ID sequence in your MOF code.</span></span>

</dd> <dt>

<span data-ttu-id="76496-160"><span id="ParameterType"></span><span id="parametertype"></span><span id="PARAMETERTYPE"></span>Parameter Type</span><span class="sxs-lookup"><span data-stu-id="76496-160"><span id="ParameterType"></span><span id="parametertype"></span><span id="PARAMETERTYPE"></span>ParameterType</span></span>
</dt> <dd>

<span data-ttu-id="76496-161">Beschreibt den Datentyp, der von der Methode akzeptiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="76496-161">Describes what data type the method can accept.</span></span> <span data-ttu-id="76496-162">Sie können einen Parametertyp als einen beliebigen MOF-Datenwert definieren, einschließlich eines Arrays, Schema Objekts oder Verweises.</span><span class="sxs-lookup"><span data-stu-id="76496-162">You can define a parameter type as any MOF data value, including an array, schema object, or reference.</span></span> <span data-ttu-id="76496-163">Wenn Sie ein Array als Parameter verwenden, verwenden Sie das Array als ungebunden oder mit einer expliziten Größe.</span><span class="sxs-lookup"><span data-stu-id="76496-163">When using an array as a parameter, use the array as unbound or with an explicit size.</span></span>

</dd> <dt>

<span data-ttu-id="76496-164"><span id="ParameterName"></span><span id="parametername"></span><span id="PARAMETERNAME"></span>Parameter Name</span><span class="sxs-lookup"><span data-stu-id="76496-164"><span id="ParameterName"></span><span id="parametername"></span><span id="PARAMETERNAME"></span>ParameterName</span></span>
</dt> <dd>

<span data-ttu-id="76496-165">Enthält den Namen des Parameters.</span><span class="sxs-lookup"><span data-stu-id="76496-165">Contains the name of the parameter.</span></span> <span data-ttu-id="76496-166">An dieser Stelle können Sie auch den Standardwert des Parameters definieren.</span><span class="sxs-lookup"><span data-stu-id="76496-166">You can also choose to define the default value of the parameter at this point.</span></span> <span data-ttu-id="76496-167">Parameter, die anfängliche Werte fehlen, bleiben nicht zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="76496-167">Parameters lacking initial values remain unassigned.</span></span>

</dd> </dl>

<span data-ttu-id="76496-168">Im folgenden Codebeispiel werden die Parameter Auflistung und die Qualifizierer beschrieben.</span><span class="sxs-lookup"><span data-stu-id="76496-168">The following code example describes parameter listing and qualifiers.</span></span>

``` syntax
[Dynamic, Provider ("ProviderX")]
class MyClass
{
    [Implemented] 
    sint32 MyMethod1 ([in, id(0)] sint32 InParam);
    [Implemented] 
    void MyMethod2 ([in, id(0)] sint32 InParam, 
       [out, id(1)] sint32 OutParam);
    [Implemented] 
    sint32 MyMethod3 ([in, out, id(0)] sint32 InOutParam);
};
```

<span data-ttu-id="76496-169">Im folgenden Codebeispiel wird beschrieben, wie ein Array in einem MOF-Parameter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="76496-169">The following code example describes how to use an array in a MOF parameter.</span></span>

``` syntax
[Dynamic, Provider ("ProviderX")]
class MyClass
{
    [Implemented] 
    sint32 MyMethod1 ([in, id(0)] Win32_LogicalDisk DiskParam[]);
    [Implemented] 
    sint32 MyMethod2 ([in, id(0)] Win32_LogicalDisk DiskParam[32]);
};
```

<span data-ttu-id="76496-170">Im folgenden Codebeispiel wird die Verwendung eines Schema Objekts als Parameter und Rückgabewert beschrieben.</span><span class="sxs-lookup"><span data-stu-id="76496-170">The following code example describes using a schema object as both a parameter and return value.</span></span>

``` syntax
[Dynamic, Provider ("ProviderX")]
class MyClass
{
    [Implemented] sint32 MyMethod1 ([in, id(0)] Win32_LogicalDisk 
        DiskParam);
    [Implemented] 
    Win32_LogicalDisk MyMethod2 ([in, id(0)] string DiskVolLabel);
};
```

<span data-ttu-id="76496-171">Im folgenden Codebeispiel wird beschrieben, wie zwei Verweise eingeschlossen werden: eine für eine Instanz der [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Klasse und die andere für eine Instanz eines unbekannten Objekt Typs.</span><span class="sxs-lookup"><span data-stu-id="76496-171">The following code example describes how to include two references: one to an instance of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class and the other to an instance of an unknown object type.</span></span>

``` syntax
[Dynamic, Provider("ProviderX")]
class MyClass
{
    [Implemented] 
    sint32 MyMethod1 ([in, id(0)] Win32_LogicalDisk ref DiskRef);
    [Implemented] 
    sint32 MyMethod2 ([in, id(0)] object ref AnyObject);
};
```

## <a name="creating-a-wmi-class-method-in-c"></a><span data-ttu-id="76496-172">Erstellen einer WMI-Klassenmethode in C++</span><span class="sxs-lookup"><span data-stu-id="76496-172">Creating a WMI Class Method in C++</span></span>

<span data-ttu-id="76496-173">Im folgenden Verfahren wird beschrieben, wie eine WMI-Klassenmethode Programm gesteuert erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="76496-173">The following procedure describes how to create a WMI class method programmatically.</span></span>

<span data-ttu-id="76496-174">**So erstellen Sie eine WMI-Klassenmethode Programm gesteuert**</span><span class="sxs-lookup"><span data-stu-id="76496-174">**To create a WMI class method programmatically**</span></span>

1.  <span data-ttu-id="76496-175">Erstellen Sie die Klasse, zu der die Methode gehört.</span><span class="sxs-lookup"><span data-stu-id="76496-175">Create the class to which the method will belong.</span></span>

    <span data-ttu-id="76496-176">Bevor Sie die-Methode erstellen, muss zunächst eine-Klasse vorhanden sein, in der die-Methode platziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="76496-176">You must first have a class to place the method in before you create the method.</span></span>

2.  <span data-ttu-id="76496-177">Rufen Sie mithilfe von [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) oder [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)zwei untergeordnete Klassen der [**\_ \_ Parameters**](--parameters.md) -System Klasse ab.</span><span class="sxs-lookup"><span data-stu-id="76496-177">Retrieve two child classes of the [**\_\_PARAMETERS**](--parameters.md) system class using either [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

    <span data-ttu-id="76496-178">Verwenden Sie die erste untergeordnete Klasse, um die in-Parameter zu beschreiben, und die zweite, um die Out-Parameter zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="76496-178">Use the first child class to describe the in-parameters, and the second to describe the out-parameters.</span></span> <span data-ttu-id="76496-179">Falls erforderlich, können Sie einen einzelnen Abruf ausführen, gefolgt von einem-Befehl der [**IWbemClassObject:: Clone**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-clone) -Methode.</span><span class="sxs-lookup"><span data-stu-id="76496-179">If necessary, you can perform a single retrieval followed by a call to the [**IWbemClassObject::Clone**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-clone) method.</span></span>

3.  <span data-ttu-id="76496-180">Schreiben Sie die in-Parameter in die erste Klasse und die Out-Parameter in die zweite Klasse mit einem oder mehreren Aufrufen von [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span><span class="sxs-lookup"><span data-stu-id="76496-180">Write the in-parameters to the first class, and the out-parameters to the second class, using one or more calls to [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span></span>

    <span data-ttu-id="76496-181">Beachten Sie beim Beschreiben von Parametern für eine Methode die folgenden Regeln und Einschränkungen:</span><span class="sxs-lookup"><span data-stu-id="76496-181">When describing parameters to a method, observe the following rules and restrictions:</span></span>

    -   <span data-ttu-id="76496-182">Behandeln \[ Sie die in \] -und out-Parameter als separate Einträge, eine in dem-Objekt, das die in-Parameter enthält, und eines in dem-Objekt, das die Out-Parameter enthält.</span><span class="sxs-lookup"><span data-stu-id="76496-182">Treat the \[in, out\] parameters as separate entries, one in the object that contains the in-parameters and one in the object that contains the out-parameters.</span></span>
    -   <span data-ttu-id="76496-183">Abgesehen von den \[ in-, out- \] Qualifizierern müssen die verbleibenden Qualifizierer exakt identisch sein.</span><span class="sxs-lookup"><span data-stu-id="76496-183">Other than the \[in, out\] qualifiers, the remaining qualifiers must be exactly the same.</span></span>
    -   <span data-ttu-id="76496-184">Geben Sie die [**ID**](standard-wmi-qualifiers.md) -Qualifizierer an, beginnend bei 0 (null), eine für jeden Parameter.</span><span class="sxs-lookup"><span data-stu-id="76496-184">Specify the [**ID**](standard-wmi-qualifiers.md) qualifiers, starting at 0 (zero), one for each parameter.</span></span>

        <span data-ttu-id="76496-185">Die Reihenfolge der Eingabe-oder Ausgabeparameter wird durch den Wert des [**ID**](standard-wmi-qualifiers.md) -Qualifizierers für jeden Parameter festgelegt.</span><span class="sxs-lookup"><span data-stu-id="76496-185">The order of the input or output parameters is established by the value of the [**ID**](standard-wmi-qualifiers.md) qualifier on each parameter.</span></span> <span data-ttu-id="76496-186">Alle Eingabeargumente müssen allen Ausgabe Argumenten vorangestellt sein.</span><span class="sxs-lookup"><span data-stu-id="76496-186">All input arguments must precede any output arguments.</span></span> <span data-ttu-id="76496-187">Wenn Sie die Reihenfolge der Eingabe-und Ausgabeparameter der Methode beim Aktualisieren eines vorhandenen Methoden Anbieters ändern, kann dies dazu führen, dass Anwendungen, die die-Methode aufruft</span><span class="sxs-lookup"><span data-stu-id="76496-187">Changing the order of method input and output parameters when updating an existing method provider can cause applications that call the method to fail.</span></span> <span data-ttu-id="76496-188">Fügen Sie am Ende der vorhandenen Parameter neue Eingabeparameter hinzu, anstatt Sie in die bereits festgelegte Sequenz einzufügen.</span><span class="sxs-lookup"><span data-stu-id="76496-188">Add new input parameters at the end of the existing parameters rather than inserting them in the sequence that is already established.</span></span>

        <span data-ttu-id="76496-189">Stellen Sie sicher, dass keine Lücken in der [**ID**](standard-wmi-qualifiers.md) -qualifizierersequenz bestehen.</span><span class="sxs-lookup"><span data-stu-id="76496-189">Make sure to leave no gaps in the [**ID**](standard-wmi-qualifiers.md) qualifier sequence.</span></span>

    -   <span data-ttu-id="76496-190">Legen Sie den Rückgabewert in der Out-Parameter-Klasse als Eigenschaft mit dem Namen " **ReturnValue**" ab.</span><span class="sxs-lookup"><span data-stu-id="76496-190">Place the return value in the out-parameters class as a property named **ReturnValue**.</span></span>

        <span data-ttu-id="76496-191">Dadurch wird die-Eigenschaft als Rückgabewert der-Methode identifiziert.</span><span class="sxs-lookup"><span data-stu-id="76496-191">This identifies the property as the return value of the method.</span></span> <span data-ttu-id="76496-192">Der CIM-Typ dieser Eigenschaft ist der Rückgabetyp der Methode.</span><span class="sxs-lookup"><span data-stu-id="76496-192">The CIM type of this property is the return type of the method.</span></span> <span data-ttu-id="76496-193">Wenn die Methode den Rückgabetyp "void" aufweist, verfügen Sie nicht über eine **ReturnValue** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="76496-193">If the method has a return type of void, then do not have a **ReturnValue** property at all.</span></span> <span data-ttu-id="76496-194">Außerdem kann die **ReturnValue** -Eigenschaft nicht über einen [**ID**](standard-wmi-qualifiers.md) -Qualifizierer wie die Argumente der Methode verfügen.</span><span class="sxs-lookup"><span data-stu-id="76496-194">Also, the **ReturnValue** property cannot have an [**ID**](standard-wmi-qualifiers.md) qualifier like the arguments of the method.</span></span> <span data-ttu-id="76496-195">Das Zuweisen eines **ID** -Qualifizierers zur **ReturnValue** -Eigenschaft erzeugt einen WMI-Fehler.</span><span class="sxs-lookup"><span data-stu-id="76496-195">Assigning an **ID** qualifier to the **ReturnValue** property produces a WMI error.</span></span>

    -   <span data-ttu-id="76496-196">Ausgedrückt alle Standardparameter Werte für die-Eigenschaft in der-Klasse.</span><span class="sxs-lookup"><span data-stu-id="76496-196">Express any default parameter values for the property in the class.</span></span>

4.  <span data-ttu-id="76496-197">Fügen Sie beide [**\_ \_ Parameter**](--parameters.md) Objekte in die übergeordnete Klasse ein, indem Sie " [**IWbemClassObject::P utmethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod)" aufruft.</span><span class="sxs-lookup"><span data-stu-id="76496-197">Place both [**\_\_PARAMETERS**](--parameters.md) objects into the parent class with a call to [**IWbemClassObject::PutMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).</span></span>

    <span data-ttu-id="76496-198">Mit einem einzelnen [**CALLMETHOD**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod) -Befehl können beide [**\_ \_ Parameter**](--parameters.md) Objekte in die-Klasse platziert werden.</span><span class="sxs-lookup"><span data-stu-id="76496-198">A single call to [**PutMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod) can place both [**\_\_PARAMETERS**](--parameters.md) objects into the class.</span></span>

## <a name="related-topics"></a><span data-ttu-id="76496-199">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="76496-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76496-200">Erstellen einer Klasse</span><span class="sxs-lookup"><span data-stu-id="76496-200">Creating a Class</span></span>](creating-a-class.md)
</dt> </dl>

 

 
