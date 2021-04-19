---
description: Im Gegensatz zum Löschen einer dynamischen Instanz ist das Löschen einer Klasse eine einfache Prozedur.
ms.assetid: bc0ee1e8-7515-4f35-ace3-6344c2ef0ab8
ms.tgt_platform: multiple
title: Löschen einer Klasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f3d9ce149b5eff0f5202cb25c5f7d16fdf44291
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355293"
---
# <a name="deleting-a-class"></a><span data-ttu-id="fe7ae-103">Löschen einer Klasse</span><span class="sxs-lookup"><span data-stu-id="fe7ae-103">Deleting a Class</span></span>

<span data-ttu-id="fe7ae-104">Im Gegensatz zum Löschen einer dynamischen Instanz ist das Löschen einer Klasse eine einfache Prozedur.</span><span class="sxs-lookup"><span data-stu-id="fe7ae-104">Unlike deleting a dynamic instance, deleting a class is a simple procedure.</span></span> <span data-ttu-id="fe7ae-105">Wie bereits erläutert, werden Basisklassen oder abgeleitete Klassen jedoch nur selten gelöscht.</span><span class="sxs-lookup"><span data-stu-id="fe7ae-105">However, as discussed earlier, base or derived classes are rarely deleted.</span></span> <span data-ttu-id="fe7ae-106">Stattdessen wird eine Instanz häufiger gelöscht.</span><span class="sxs-lookup"><span data-stu-id="fe7ae-106">Instead, an instance is more commonly deleted.</span></span> <span data-ttu-id="fe7ae-107">Die [Skript-API für WMI](scripting-api-for-wmi.md) verwendet dieselben Methoden, um entweder ein Klassenobjekt oder eine Instanz zu löschen.</span><span class="sxs-lookup"><span data-stu-id="fe7ae-107">The [Scripting API for WMI](scripting-api-for-wmi.md) uses the same methods to delete either a class object or an instance.</span></span> <span data-ttu-id="fe7ae-108">Weitere Informationen finden Sie unter [Löschen einer Instanz](deleting-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="fe7ae-108">For more information, see [Deleting an Instance](deleting-an-instance.md).</span></span> <span data-ttu-id="fe7ae-109">Weitere Informationen zum Entfernen von Klassen und Instanzen aus dem WMI-Repository finden Sie im [**pragma deleteclass**](pragma-deleteclass.md) -Präprozessorbefehl.</span><span class="sxs-lookup"><span data-stu-id="fe7ae-109">For information about removing classes and instances from the WMI repository, see the [**pragma deleteclass**](pragma-deleteclass.md) preprocessor command.</span></span>

<span data-ttu-id="fe7ae-110">Die [com-API für WMI](com-api-for-wmi.md) verfügt über verschiedene Methoden zum Löschen einer Instanz und zum Löschen eines Objekts.</span><span class="sxs-lookup"><span data-stu-id="fe7ae-110">The [COM API for WMI](com-api-for-wmi.md) has different methods for deleting an instance and deleting an object.</span></span>

<span data-ttu-id="fe7ae-111">Im folgenden Verfahren wird beschrieben, wie Sie eine Basisklasse oder eine abgeleitete Klasse löschen.</span><span class="sxs-lookup"><span data-stu-id="fe7ae-111">The following procedure describes how to delete a base class or derived class.</span></span>

<span data-ttu-id="fe7ae-112">**So löschen Sie eine Basisklasse oder eine abgeleitete Klasse**</span><span class="sxs-lookup"><span data-stu-id="fe7ae-112">**To delete a base class or derived class**</span></span>

-   <span data-ttu-id="fe7ae-113">Entweder die [**IWbemServices::D eleteclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) -oder [**IWbemServices::D eleteclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="fe7ae-113">Call either the [**IWbemServices::DeleteClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) or [**IWbemServices::DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) method.</span></span>

    <span data-ttu-id="fe7ae-114">Wie der Name vermuten lässt, löscht [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) eine Instanz asynchron, während [**deleteclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) eine Instanz synchron löscht.</span><span class="sxs-lookup"><span data-stu-id="fe7ae-114">As the name suggests, [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) deletes an instance asynchronously while [**DeleteClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) deletes an instance synchronously.</span></span> <span data-ttu-id="fe7ae-115">Um **DeleteClassAsync** verwenden zu können, müssen Sie auch ein [**iwbe"iwbejebjectsink**](iwbemobjectsink.md) "-Objekt implementieren.</span><span class="sxs-lookup"><span data-stu-id="fe7ae-115">To use **DeleteClassAsync**, you must also implement an [**IWbemObjectSink**](iwbemobjectsink.md) object.</span></span>

> [!Note]  
> <span data-ttu-id="fe7ae-116">Da der Rückruf für die Senke möglicherweise nicht auf derselben Authentifizierungs Ebene wie der Client zurückgegeben wird, wird empfohlen, semisynchrone anstelle der asynchronen Kommunikation zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="fe7ae-116">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="fe7ae-117">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="fe7ae-117">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

 

 



