---
description: Das Löschen einer Instanz ist der häufigste DELETE-Befehl, den Sie in WMI wahrscheinlich ausführen.
ms.assetid: 95ba3e9c-1397-41fe-a080-c03a98aafd42
ms.tgt_platform: multiple
title: Löschen einer Instanz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2229889ec4bc21ad234eb1636f264977bb3e25e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345273"
---
# <a name="deleting-an-instance"></a><span data-ttu-id="7b844-103">Löschen einer Instanz</span><span class="sxs-lookup"><span data-stu-id="7b844-103">Deleting an Instance</span></span>

<span data-ttu-id="7b844-104">Das Löschen einer Instanz ist der häufigste DELETE-Befehl, den Sie in WMI wahrscheinlich ausführen.</span><span class="sxs-lookup"><span data-stu-id="7b844-104">Deleting an instance is the most common delete command you are likely to perform in WMI.</span></span> <span data-ttu-id="7b844-105">Wie beim Löschen einer Klasse ist der tatsächliche Befehl recht einfach.</span><span class="sxs-lookup"><span data-stu-id="7b844-105">Like deleting a class, the actual command is fairly simple.</span></span> <span data-ttu-id="7b844-106">WMI unterscheidet sich jedoch je nach dem zu löschenden Instanztyp ganz anders.</span><span class="sxs-lookup"><span data-stu-id="7b844-106">However, WMI performs quite differently depending on the type of instance you are deleting.</span></span> <span data-ttu-id="7b844-107">Wenn die Instanz statisch ist, löscht WMI einfach die Instanz aus dem WMI-Repository.</span><span class="sxs-lookup"><span data-stu-id="7b844-107">If the instance is static, WMI simply deletes the instance from the WMI repository.</span></span> <span data-ttu-id="7b844-108">Weitere Informationen zum Entfernen von Klassen und Instanzen aus dem WMI-Repository finden Sie im [**pragma deleteclass**](pragma-deleteclass.md) -Präprozessorbefehl.</span><span class="sxs-lookup"><span data-stu-id="7b844-108">For information about removing classes and instances from the WMI repository, see the [**pragma deleteclass**](pragma-deleteclass.md) preprocessor command.</span></span>

<span data-ttu-id="7b844-109">Wenn die Instanz dynamisch ist, muss WMI auf den Anbietern, die für die folgenden Klassen zuständig sind, [**IWbemServices::D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) aufrufen:</span><span class="sxs-lookup"><span data-stu-id="7b844-109">If the instance is dynamic, WMI must call [**IWbemServices::DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) on the providers that are responsible for the following classes:</span></span>

-   <span data-ttu-id="7b844-110">Die Klasse, die Besitzer der-Instanz ist.</span><span class="sxs-lookup"><span data-stu-id="7b844-110">The class that owns the instance.</span></span>
-   <span data-ttu-id="7b844-111">Jede übergeordnete Klasse der Klasse, die die Instanz besitzt.</span><span class="sxs-lookup"><span data-stu-id="7b844-111">Every parent class of the class that owns the instance.</span></span>
-   <span data-ttu-id="7b844-112">Jede Unterklasse der-Klasse, die Besitzer der-Instanz ist.</span><span class="sxs-lookup"><span data-stu-id="7b844-112">Every subclass of the class that owns the instance.</span></span>

<span data-ttu-id="7b844-113">Der Erfolg der Löschung hängt von der obersten nicht abstrakten Klasse der ursprünglichen Instanz ab.</span><span class="sxs-lookup"><span data-stu-id="7b844-113">The success of the deletion depends on the topmost nonabstract class for the original instance.</span></span> <span data-ttu-id="7b844-114">Wenn der Anbieter für eine oberste, nicht abstrakte Klasse den Löschvorgang abgeschlossen hat, ist der Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="7b844-114">If the provider for any topmost nonabstract class succeeds in completing the deletion, the operation succeeds.</span></span> <span data-ttu-id="7b844-115">Weitere Informationen finden Sie im Abschnitt "Hinweise" unter [**IWbemServices::D eleteinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance).</span><span class="sxs-lookup"><span data-stu-id="7b844-115">For more information, see the Remarks section of [**IWbemServices::DeleteInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance).</span></span>

<span data-ttu-id="7b844-116">Die [com-API für WMI](com-api-for-wmi.md) verfügt über verschiedene Methoden zum Löschen einer Instanz und zum Löschen eines Objekts.</span><span class="sxs-lookup"><span data-stu-id="7b844-116">The [COM API for WMI](com-api-for-wmi.md) has different methods for deleting an instance and deleting an object.</span></span>

<span data-ttu-id="7b844-117">Im folgenden Verfahren wird beschrieben, wie C++ verwendet wird, um eine Instanz einer Basisklasse oder abgeleiteten Klasse zu löschen.</span><span class="sxs-lookup"><span data-stu-id="7b844-117">The following procedure describes how to use C++ to delete an instance of a base class or derived class.</span></span>

<span data-ttu-id="7b844-118">**So löschen Sie eine Instanz einer Basisklasse oder abgeleiteten Klasse mithilfe von C++**</span><span class="sxs-lookup"><span data-stu-id="7b844-118">**To delete an instance of a base class or derived class using C++**</span></span>

-   <span data-ttu-id="7b844-119">Entweder die [**IWbemServices::D eleteinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance) -oder [**IWbemServices::D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7b844-119">Call either the [**IWbemServices::DeleteInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance) or [**IWbemServices::DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) methods.</span></span>

    <span data-ttu-id="7b844-120">Wie der Name vermuten lässt, löscht " [**Delta einstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) " eine Instanz asynchron, während " [**Delta einstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance) " eine Instanz synchron löscht.</span><span class="sxs-lookup"><span data-stu-id="7b844-120">As the name suggests, [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) deletes an instance asynchronously while [**DeleteInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance) deletes an instance synchronously.</span></span> <span data-ttu-id="7b844-121">Um **Delta einstanceasync** verwenden zu können, müssen Sie auch ein [**IWbemObjectSink**](iwbemobjectsink.md) -Objekt implementieren.</span><span class="sxs-lookup"><span data-stu-id="7b844-121">To use **DeleteInstanceAsync**, you must also implement an [**IWbemObjectSink**](iwbemobjectsink.md) object.</span></span>

> [!Note]  
> <span data-ttu-id="7b844-122">Da der Rückruf für die Senke möglicherweise nicht auf derselben Authentifizierungs Ebene wie der Client zurückgegeben wird, wird empfohlen, semisynchrone anstelle der asynchronen Kommunikation zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="7b844-122">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="7b844-123">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="7b844-123">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="7b844-124">Die [Skript-API für WMI](scripting-api-for-wmi.md) verwendet dieselben Methoden, um entweder ein Klassenobjekt oder eine Instanz zu löschen.</span><span class="sxs-lookup"><span data-stu-id="7b844-124">The [Scripting API for WMI](scripting-api-for-wmi.md) uses the same methods to delete either a class object or an instance.</span></span>

<span data-ttu-id="7b844-125">Im folgenden Verfahren wird die Verwendung von VBScript zum Löschen einer Instanz einer Basisklasse oder abgeleiteten Klasse beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7b844-125">The following procedure describes how to use VBScript to delete an instance of a base class or derived class.</span></span>

<span data-ttu-id="7b844-126">**So löschen Sie eine Instanz einer Basisklasse oder abgeleiteten Klasse mithilfe von VBScript**</span><span class="sxs-lookup"><span data-stu-id="7b844-126">**To delete an instance of a base class or derived class using VBScript**</span></span>

-   <span data-ttu-id="7b844-127">Aufrufen der Methoden " [**errbemjebject \_ . Delete**](swbemobject-delete-.md) " oder " [**errbemubject. \_ deleteasync**](swbemobject-deleteasync-.md) ".</span><span class="sxs-lookup"><span data-stu-id="7b844-127">Call either the [**SWbemObject.Delete\_**](swbemobject-delete-.md) or [**SWbemObject.DeleteAsync\_**](swbemobject-deleteasync-.md) methods.</span></span>

    <span data-ttu-id="7b844-128">Wie der Name vermuten lässt, löscht [**Delete \_**](swbemobject-delete-.md) eine Instanz synchron, während [**deleteasync \_**](swbemobject-deleteasync-.md) eine Instanz asynchron löscht.</span><span class="sxs-lookup"><span data-stu-id="7b844-128">As the name suggests, [**Delete\_**](swbemobject-delete-.md) deletes an instance synchronously while [**DeleteAsync\_**](swbemobject-deleteasync-.md) deletes an instance asynchronously.</span></span> <span data-ttu-id="7b844-129">Weitere Informationen zum asynchronen Löschen einer Instanz finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="7b844-129">For more information about deleting an instance asynchronously, see [Calling a Method](calling-a-method.md).</span></span>

    <span data-ttu-id="7b844-130">Im folgenden Beispiel wird beschrieben, wie eine Instanz mit VBScript gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="7b844-130">The following example describes how to delete an instance using VBScript.</span></span>

    ```VB
    Dim service

    Set service = GetObject("winmgmts:{impersonationLevel=impersonate}") 

    Set objwbemobject= service.get("")

    objwbemobject.Path_.Class = "MyNewClass" 
    objwbemobject.put_
    service.delete  "MyNewClass"
    ```

    

> [!Note]  
> <span data-ttu-id="7b844-131">Da der Rückruf für die Senke möglicherweise nicht auf derselben Authentifizierungs Ebene wie der Client zurückgegeben wird, wird empfohlen, semisynchrone anstelle der asynchronen Kommunikation zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="7b844-131">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="7b844-132">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="7b844-132">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

 

 



