---
description: Definiert die Eingabe-und Ausgabeparameter für Methoden.
ms.assetid: d973feb5-27c4-4d8e-bf1b-0a455afa4375
ms.tgt_platform: multiple
title: __PARAMETERS-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __PARAMETERS
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: df858445797a45e21a0d54e9aedc2387851ae54f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358952"
---
# <a name="__parameters-class"></a><span data-ttu-id="bd935-103">\_\_Parameters-Klasse</span><span class="sxs-lookup"><span data-stu-id="bd935-103">\_\_PARAMETERS class</span></span>

<span data-ttu-id="bd935-104">Die **\_ \_ Parameters** -System Klasse ist eine abstrakte Klasse, die die Eingabe-und Ausgabeparameter für Methoden definiert.</span><span class="sxs-lookup"><span data-stu-id="bd935-104">The **\_\_PARAMETERS** system class is an abstract class that defines the input and output parameters for methods.</span></span> <span data-ttu-id="bd935-105">Außerdem werden Sie verwendet, um Eingabe-und Ausgabeparameter Werte zwischen einem WMI-Client und einem Methoden Anbieter zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="bd935-105">It is also used to pass input and output parameter values between a WMI client and a method provider.</span></span>

<span data-ttu-id="bd935-106">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="bd935-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="bd935-107">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="bd935-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd935-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd935-108">Syntax</span></span>

``` syntax
[abstract]
class __PARAMETERS
{
};
```

## <a name="members"></a><span data-ttu-id="bd935-109">Member</span><span class="sxs-lookup"><span data-stu-id="bd935-109">Members</span></span>

<span data-ttu-id="bd935-110">Die **\_ \_ Parameters** -Klasse definiert keine Member.</span><span class="sxs-lookup"><span data-stu-id="bd935-110">The **\_\_PARAMETERS** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd935-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bd935-111">Remarks</span></span>

<span data-ttu-id="bd935-112">Zum Definieren einer Methode in einer Benutzerklasse erstellt ein WMI-Client eine Kopie der **\_ \_ para** meters-Klasse und fügt eine Eigenschaft für jeden Eingabeparameter in einer Methode hinzu.</span><span class="sxs-lookup"><span data-stu-id="bd935-112">To define a method in a user class, a WMI client creates a copy of the **\_\_PARAMETERS** class, and adds a property for each input parameter in a method.</span></span> <span data-ttu-id="bd935-113">Wenn die Methode einen Rückgabewert oder Ausgabeparameter enthält, muss eine andere Kopie der **\_ \_ Parameter** erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="bd935-113">If the method contains a return value or output parameters, another copy of **\_\_PARAMETERS** must be created.</span></span> <span data-ttu-id="bd935-114">Wenn die Methode einen Rückgabewert zurückgibt, muss der Client eine Eigenschaft mit dem Namen " **ReturnValue**" hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="bd935-114">If the method returns a return value, the client must add a property named **ReturnValue**.</span></span> <span data-ttu-id="bd935-115">Der Methoden Anbieter speichert dann die Methoden Parameter mit einem-Befehl, der [**IWbemClassObject::P utmethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod)aufruft.</span><span class="sxs-lookup"><span data-stu-id="bd935-115">The method provider then stores the method parameters with a call to [**IWbemClassObject::PutMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).</span></span>

<span data-ttu-id="bd935-116">Um eine Methode aufzurufen, Ruft ein Client die folgenden Reihenfolge auf:</span><span class="sxs-lookup"><span data-stu-id="bd935-116">To invoke a method, a client calls the following in sequence:</span></span>

1.  <span data-ttu-id="bd935-117">[**IWbemClassObject:: GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) zum Abrufen einer Kopie der **\_ \_ Parameters** -Klasse, die von [**IWbemClassObject::P utmethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod)gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="bd935-117">[**IWbemClassObject::GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) to retrieve a copy of the **\_\_PARAMETERS** class that is stored by [**IWbemClassObject::PutMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).</span></span>
2.  <span data-ttu-id="bd935-118">[**IWbemClassObject:: SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance), und legt dann eine Eigenschaft für jeden Eingabeparameter für die Methode fest.</span><span class="sxs-lookup"><span data-stu-id="bd935-118">[**IWbemClassObject::SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance), and then sets one property for each input parameter to the method.</span></span>
3.  <span data-ttu-id="bd935-119">[**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) oder [**IWbemServices:: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) zum Ausführen der Methode.</span><span class="sxs-lookup"><span data-stu-id="bd935-119">[**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) or [**IWbemServices::ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) to execute the method.</span></span>

<span data-ttu-id="bd935-120">Nachdem die Ausführung der Methode abgeschlossen ist, kann eine andere **\_ \_ Parameter** Klasseninstanz zurückgegeben werden, wenn die Methode über Ausgabeparameter oder einen Rückgabewert verfügt.</span><span class="sxs-lookup"><span data-stu-id="bd935-120">After the method is finished executing, another **\_\_PARAMETERS** class instance may be returned if the method has output parameters or a return value.</span></span>

-   <span data-ttu-id="bd935-121">Wenn die Methode mithilfe von [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod)aufgerufen wurde, wird die **\_ \_ Parameter** Instanz als Ausgabe Argument zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bd935-121">If the method was invoked by using [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod), the **\_\_PARAMETERS** instance is returned as an output argument.</span></span>
-   <span data-ttu-id="bd935-122">Wenn die Methode mithilfe von [**IWbemServices:: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)aufgerufen wurde, wird die **\_ \_ Parameter** Instanz als Parameter an [**iwbemubjectsink::**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate)Expression zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bd935-122">If the method was invoked by using [**IWbemServices::ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync), the **\_\_PARAMETERS** instance is returned as a parameter to [**IWbemObjectSink::Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate).</span></span>

## <a name="requirements"></a><span data-ttu-id="bd935-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bd935-123">Requirements</span></span>



| <span data-ttu-id="bd935-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bd935-124">Requirement</span></span> | <span data-ttu-id="bd935-125">Wert</span><span class="sxs-lookup"><span data-stu-id="bd935-125">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="bd935-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bd935-126">Minimum supported client</span></span><br/> | <span data-ttu-id="bd935-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bd935-127">Windows Vista</span></span><br/>       |
| <span data-ttu-id="bd935-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bd935-128">Minimum supported server</span></span><br/> | <span data-ttu-id="bd935-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bd935-129">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="bd935-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="bd935-130">Namespace</span></span><br/>                | <span data-ttu-id="bd935-131">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="bd935-131">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="bd935-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd935-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd935-133">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="bd935-133">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="bd935-134">**IWbemServices:: ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="bd935-134">**IWbemServices::ExecMethodAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
</dt> <dt>

[<span data-ttu-id="bd935-135">Aufrufen einer Methode</span><span class="sxs-lookup"><span data-stu-id="bd935-135">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 




