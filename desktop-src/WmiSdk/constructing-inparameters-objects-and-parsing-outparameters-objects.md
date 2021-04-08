---
description: Normalerweise ist der direkte Zugriff ausreichend, um eine WMI-Anbieter Methode aufzurufen.
ms.assetid: be9332b5-8094-44a2-8632-af9957ecf36b
ms.tgt_platform: multiple
title: Erstellen von InParameters-Objekten und übernehmen von outparameter-Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a291d4fd44e69e87572684856bba587685e1f07b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960221"
---
# <a name="constructing-inparameters-objects-and-parsing-outparameters-objects"></a><span data-ttu-id="0db47-103">Erstellen von InParameters-Objekten und übernehmen von outparameter-Objekten</span><span class="sxs-lookup"><span data-stu-id="0db47-103">Constructing InParameters Objects and Parsing OutParameters Objects</span></span>

<span data-ttu-id="0db47-104">Normalerweise ist der direkte Zugriff ausreichend, um eine WMI- [*Anbieter Methode*](gloss-p.md)aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="0db47-104">Normally, direct access is adequate to call a WMI [*provider method*](gloss-p.md).</span></span> <span data-ttu-id="0db47-105">Direkter Zugriff bedeutet, dass eine Methode mithilfe der *Object. Method* -Syntax ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0db47-105">Direct access means executing a method by using *object.method* syntax.</span></span> <span data-ttu-id="0db47-106">In einigen Fällen kann der direkte Zugriff jedoch nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0db47-106">However, in some cases, direct access cannot be used.</span></span> <span data-ttu-id="0db47-107">Außerdem erfordert der asynchrone Aufruf einer Anbieter Methode aus einem Skript einen [**ExecMethodAsync**](swbemobject-execmethodasync-.md) -Aufgabentyp.</span><span class="sxs-lookup"><span data-stu-id="0db47-107">Also, calling a provider method asynchronously from a script requires an [**ExecMethodAsync**](swbemobject-execmethodasync-.md) type of call.</span></span>

> [!Note]  
> <span data-ttu-id="0db47-108">Da der Rückruf für die Senke möglicherweise nicht auf derselben Authentifizierungs Ebene wie der Client zurückgegeben wird, wird empfohlen, semisynchrone anstelle der asynchronen Kommunikation zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="0db47-108">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="0db47-109">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="0db47-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="0db47-110">Die Reihenfolge der Eingabe-und Ausgabeparameter der Methode wird im MOF-Schema (Managed Object Format) für die Methode definiert.</span><span class="sxs-lookup"><span data-stu-id="0db47-110">The order of method input and output parameters is defined in the Managed Object Format (MOF) schema for the method.</span></span> <span data-ttu-id="0db47-111">WMI verhindert nicht, dass die Parameterreihenfolge geändert wird, wenn die Klasse von " [MUF Comp](mofcomp.md)" neu kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="0db47-111">WMI does not prevent the parameter order from being changed when the class is recompiled by [mofcomp](mofcomp.md).</span></span> <span data-ttu-id="0db47-112">Mit einem [**InParameters**](swbemmethod-inparameters.md) -Objekt können Sie Probleme vermeiden, die sich aus dem geänderten Schema ergeben, da die Eingabeparameter anhand des Namens identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="0db47-112">By using an [**InParameters**](swbemmethod-inparameters.md) object, you can avoid problems that result from changed schema because the input parameters are identified by name.</span></span> <span data-ttu-id="0db47-113">Der richtige Parameter kann angezeigt werden, indem Sie den **ID** -Qualifizierer der einzelnen Eingabeparameter untersuchen.</span><span class="sxs-lookup"><span data-stu-id="0db47-113">The correct parameter can be seen by examining the **ID** qualifier of each input parameter.</span></span> <span data-ttu-id="0db47-114">Der erste Parameter weist den **ID** -Wert 0 (null) auf.</span><span class="sxs-lookup"><span data-stu-id="0db47-114">The first parameter has an **ID** value of 0 (zero).</span></span>

<span data-ttu-id="0db47-115">[**Die Methoden SWbemObject.Exe\_ cmethod**](swbemobject-execmethod-.md), [**SWbemObject.Execmethodasync \_**](swbemobject-execmethodasync-.md), [**SWbemServices.Execmethod**](swbemservices-execmethod.md)und [**SWbemServices.Execmethodasync**](swbemservices-execmethodasync.md) bieten eine alternative Möglichkeit, eine Anbieter Methode auszuführen, wenn es nicht möglich ist, eine Methode direkt auszuführen.</span><span class="sxs-lookup"><span data-stu-id="0db47-115">[**The SWbemObject.ExecMethod\_**](swbemobject-execmethod-.md), [**SWbemObject.ExecMethodAsync\_**](swbemobject-execmethodasync-.md), [**SWbemServices.ExecMethod**](swbemservices-execmethod.md), and [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md) methods provide an alternate way to execute a provider method in cases where it is not possible to execute a method directly.</span></span> <span data-ttu-id="0db47-116">Weitere Informationen finden Sie unter Bearbeiten von [Klassen-und Instanzinformationen](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="0db47-116">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

<span data-ttu-id="0db47-117">Weitere Informationen zu Parametern finden Sie unter [Erstellen von inparameter-Objekten](constructing-inparameters-objects.md) und Auswerten von [outparameter-Objekten](parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="0db47-117">For more information about parameters, see [Constructing InParameters Objects](constructing-inparameters-objects.md) and [Parsing OutParameters Objects](parsing-outparameters-objects.md).</span></span>

 

 



