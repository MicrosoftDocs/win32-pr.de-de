---
title: Vorgehensweise beim aufzurufen einer WMI-Methode
description: Der Hauptzweck von WMI besteht darin, den Zugriff auf Klassen und Instanzen bereitzustellen, die Objekte in Ihrem Netzwerk darstellen.
ms.assetid: 8d559eee-3dbf-4132-b1c0-a6925b8feb56
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 892561785280e78ecf29da1030883994990fc822
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529555"
---
# <a name="how-to-call-a-wmi-method"></a><span data-ttu-id="33c3c-103">Vorgehensweise beim aufzurufen einer WMI-Methode</span><span class="sxs-lookup"><span data-stu-id="33c3c-103">How to call a WMI method</span></span>

<span data-ttu-id="33c3c-104">Der Hauptzweck von WMI besteht darin, den Zugriff auf Klassen und Instanzen bereitzustellen, die Objekte in Ihrem Netzwerk darstellen.</span><span class="sxs-lookup"><span data-stu-id="33c3c-104">The main purpose of WMI is to provide access to classes and instances that represent objects on your network.</span></span> <span data-ttu-id="33c3c-105">Diese Klassen und Instanzen werden von Anbietern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="33c3c-105">These classes and instances are supported by providers.</span></span> <span data-ttu-id="33c3c-106">Beispielsweise werden alle Instanzen, die Standard Hardware Geräte in Ihrem Unternehmen darstellen, wie z. b. [**Win32 \_ PhysicalMemory**](/windows/desktop/CIMWin32Prov/win32-physicalmemory) oder [**Win32- \_ Drucker**](/windows/desktop/CIMWin32Prov/win32-printer), vom Win32-Anbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="33c3c-106">For example, all of the instances that represent standard hardware devices on your enterprise, such as [**Win32\_PhysicalMemory**](/windows/desktop/CIMWin32Prov/win32-physicalmemory) or [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer), are supported by the Win32 provider.</span></span> <span data-ttu-id="33c3c-107">Auf ähnliche Weise können Sie über den Ereignisprotokoll Anbieter und die Registrierung über den Registrierungs Anbieter auf das Ereignisprotokoll zugreifen.</span><span class="sxs-lookup"><span data-stu-id="33c3c-107">Similarly, you can access the event log through the Event Log provider, and the registry through the Registry provider.</span></span>

<span data-ttu-id="33c3c-108">Die von WMI implementierten Methoden, wie z. b. [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) oder Skript Objekte wie z. b. " [**Swap Services**](swbemservices.md)", sind hauptsächlich für die generische Erfassung und Bearbeitung von Daten, die von einem Anbieter bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="33c3c-108">The methods that WMI implements in interfaces such as [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) or scripting objects such as [**SWbemServices**](swbemservices.md), are primarily for generically obtaining and manipulating data supplied by any provider.</span></span> <span data-ttu-id="33c3c-109">Verwenden Sie z. b. " [**Swap Services. InstancesOf**](swbemservices-instancesof.md) ", um alle Instanzen des [**Win32- \_ Prozesses**](/windows/desktop/CIMWin32Prov/win32-process) in einer Teilmenge von Unternehmens Computern abzurufen.</span><span class="sxs-lookup"><span data-stu-id="33c3c-109">For example, use [**SWbemServices.InstancesOf**](swbemservices-instancesof.md) to obtain all the instances of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) in a subset of enterprise computers.</span></span> <span data-ttu-id="33c3c-110">Sie können dann die Win32-Anbieter Methode " [**GetOwnerSID**](/windows/desktop/CIMWin32Prov/getownersid-method-in-class-win32-process) " für jedes **Win32- \_ Prozess** Objekt aufrufen.</span><span class="sxs-lookup"><span data-stu-id="33c3c-110">You can then call the Win32 provider method [**GetOwnerSid**](/windows/desktop/CIMWin32Prov/getownersid-method-in-class-win32-process) on each **Win32\_Process** object.</span></span>

<span data-ttu-id="33c3c-111">Im folgenden Beispiel wird die [**GetOwnerSID**](/windows/desktop/CIMWin32Prov/getownersid-method-in-class-win32-process) -Methode als Automatisierungs Methode für das Process-Objekt aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="33c3c-111">In the following example, the [**GetOwnerSid**](/windows/desktop/CIMWin32Prov/getownersid-method-in-class-win32-process) method is called as an automation method on the Process object.</span></span> <span data-ttu-id="33c3c-112">Eine WMI-Methode, z. b. die für " [**Swap**](swbemobject.md) " definierte [**Pfad \_**](swbemobject-path-.md) Methode, kann auch für das **Prozess** Objekt aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="33c3c-112">A WMI method, such as the [**Path\_**](swbemobject-path-.md) method defined for [**SWbemObject**](swbemobject.md) could also be called on the **Process** object.</span></span>


```VB
Set ProcessCollection = _
    GetObject("WinMgmts:").InstancesOf("Win32_Process")

For Each Process In ProcessCollection
    SID = Process.GetOwnerSid
Next
```



<span data-ttu-id="33c3c-113">Der tatsächliche Prozess der Verwendung der WMI-Methoden ist identisch mit der Verwendung anderer Windows com-oder Automatisierungs Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="33c3c-113">The actual process of using the WMI methods is identical to using any other Windows COM or automation interface.</span></span> <span data-ttu-id="33c3c-114">Weitere Informationen finden Sie unter [com](../cossdk/component-services-portal.md) und [Erstellen einer WMI-Anwendung oder eines Skripts](creating-a-wmi-application-or-script.md).</span><span class="sxs-lookup"><span data-stu-id="33c3c-114">For more information, see [COM](../cossdk/component-services-portal.md) and [Creating a WMI Application or Script](creating-a-wmi-application-or-script.md).</span></span> <span data-ttu-id="33c3c-115">Weitere Informationen zu den Schnittstellen, die von WMI unterstützt werden, finden Sie unter [com-API für WMI](com-api-for-wmi.md) und [Skript-API für WMI](scripting-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="33c3c-115">For more information about the interfaces that WMI supports, see [COM API for WMI](com-api-for-wmi.md) and [Scripting API for WMI](scripting-api-for-wmi.md).</span></span>

<span data-ttu-id="33c3c-116">Weitere Informationen finden Sie unter Bearbeiten von [Klassen-und Instanzinformationen](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="33c3c-116">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="33c3c-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="33c3c-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33c3c-118">Aufrufen einer Methode</span><span class="sxs-lookup"><span data-stu-id="33c3c-118">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 
