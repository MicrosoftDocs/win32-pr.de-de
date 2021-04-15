---
description: Auf SNMP-Geräte können Sie zugreifen, indem Sie im WMI-SMIR (SNMP-modulinformationenrepository) aus der entsprechenden Klasseninstanz lesen oder in ihr schreiben.
ms.assetid: af5e1321-b552-447e-a217-eecbebe1f203
ms.tgt_platform: multiple
title: Lesen und Schreiben von SNMP-Geräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8fc25f384d499e16e19c5e909f7d091ea34f9a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528604"
---
# <a name="reading-from-and-writing-to-snmp-devices"></a><span data-ttu-id="65eeb-103">Lesen und Schreiben von SNMP-Geräten</span><span class="sxs-lookup"><span data-stu-id="65eeb-103">Reading from and Writing to SNMP Devices</span></span>

<span data-ttu-id="65eeb-104">Auf SNMP-Geräte können Sie zugreifen, indem Sie im WMI-SMIR (SNMP-modulinformationenrepository) aus der entsprechenden Klasseninstanz lesen oder in ihr schreiben.</span><span class="sxs-lookup"><span data-stu-id="65eeb-104">SNMP devices can be accessed by reading from or writing to their corresponding class instance in the WMI SMIR (SNMP Module Information Repository).</span></span> <span data-ttu-id="65eeb-105">Wenn Sie mit mehreren Geräten desselben Typs arbeiten, laden Sie aus Effizienzgründen die MIB-Daten für einen SNMP-Gerätetyp in SMIR.</span><span class="sxs-lookup"><span data-stu-id="65eeb-105">When you are working with multiple devices of the same type, for efficiency, load the MIBs for one SNMP device type into the SMIR.</span></span>

> [!Note]  
> <span data-ttu-id="65eeb-106">Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="65eeb-106">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="65eeb-107">Wählen Sie eine der folgenden Optionen aus, um jeden SNMP-Gerätetyp zu lesen oder zu schreiben, indem Sie die Kontextinformationen der Instanz aktualisieren, bevor Sie miteinander kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="65eeb-107">Select one of the following options to read to or write from each SNMP device type by updating the context information of the instance before communicating with each one.</span></span>

-   <span data-ttu-id="65eeb-108">Verwenden Sie beim Verweisen auf ein bestimmtes Gerät einen DNS-Namen anstelle der IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="65eeb-108">Use a DNS name instead of the IP address when referencing a specific device.</span></span>

    <span data-ttu-id="65eeb-109">Im folgenden Beispiel wird gezeigt, wie Sie den DNS-Namen für ein bestimmtes Gerät verwenden.</span><span class="sxs-lookup"><span data-stu-id="65eeb-109">The following example shows how to use the DNS name for a specific device.</span></span>

    ```VB
    strNamedValue = Context.Add("AgentAddress", "Router1" )
    ```

    

-   <span data-ttu-id="65eeb-110">Erstellen Sie einen separaten Namespace, und ordnen Sie dem Namespace Objekt mithilfe des AgentAddress-instanzqualifizierers eine Geräteadresse zu, sodass der Namespace dauerhaft an das Gerät gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="65eeb-110">Create a separate namespace and associate a device address to the namespace object using the AgentAddress instance qualifier so that the namespace is permanently bound to the device.</span></span> <span data-ttu-id="65eeb-111">In diesem Fall müssen Sie die Kontext Objektinformationen nicht angeben.</span><span class="sxs-lookup"><span data-stu-id="65eeb-111">In this case, you need not specify the context object information.</span></span>
-   <span data-ttu-id="65eeb-112">Lesen von einem SNMP-Gerät</span><span class="sxs-lookup"><span data-stu-id="65eeb-112">Read from an SNMP device.</span></span>

    <span data-ttu-id="65eeb-113">Im folgenden Beispiel wird ein Get-Vorgang für eine Geräteklasse durchführt.</span><span class="sxs-lookup"><span data-stu-id="65eeb-113">The following example performs a Get operation on a device class.</span></span>

    ```VB
    Set objLocator = CreateObject("wbemscripting.swbemlocator")
    Set objServices = objLocator.ConnectServer(, "root\snmp\mngd_hub")
    objServices.security_.privileges.AddAsString("SeSecurityPrivilege")
    Set objSet = objServices.ExecQuery _
        ("SELECT * FROM SNMP_NET_DEVICE_123 WHERE hdwr_idx>1",, _
          wbemFlagReturnWhenComplete)
    for each obj in objset 
      'do whatever 
    next
    ```

    

-   <span data-ttu-id="65eeb-114">Schreiben Sie auf ein SNMP-Gerät.</span><span class="sxs-lookup"><span data-stu-id="65eeb-114">Write to an SNMP device.</span></span>

    <span data-ttu-id="65eeb-115">Im folgenden Beispiel wird ein Set-Vorgang für eine Geräteklasse durchführt.</span><span class="sxs-lookup"><span data-stu-id="65eeb-115">The following example performs a Set operation on a device class.</span></span>

    ```VB
    Set objLocator = CreateObject("wbemscripting.swbemlocator")
    Set objServices = objLocator.ConnectServer(, "root\snmp\mngd_hub")
    objServices.security_.privileges.AddAsString("SeSecurityPrivilege")
    Set obj= objServices.Get("SNMP_NET_DEVICE_123=@")
    obj.deviceLocation = "40/5073"
    obj.put_
    ```

    

<span data-ttu-id="65eeb-116">Korrelierte Klassen sind solche, die ein bestimmtes SNMP-Gerät unterstützt, wenn eine Enumeration auftritt.</span><span class="sxs-lookup"><span data-stu-id="65eeb-116">Correlated classes are those that a given SNMP device is known to support when enumeration occurs.</span></span> <span data-ttu-id="65eeb-117">Korrelation wirkt sich auf den Satz von Klassen aus, die von SMIR zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="65eeb-117">Correlation affects the set of classes returned from the SMIR.</span></span> <span data-ttu-id="65eeb-118">Nicht korrelierte Enumeration gibt alle innerhalb des SMIR vorhandenen Klassen zurück, unabhängig davon, ob Sie vom Gerät unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="65eeb-118">Noncorrelated enumeration returns all classes present within the SMIR, regardless of whether the device supports them.</span></span> <span data-ttu-id="65eeb-119">Weitere Informationen zur Verwendung von WMI-Korrelations Techniken finden Sie unter [WMI-SNMP-Klassen Korrelation](wmi-snmp-class-correlation.md).</span><span class="sxs-lookup"><span data-stu-id="65eeb-119">For more information about using WMI correlation techniques, see [WMI SNMP Class Correlation](wmi-snmp-class-correlation.md).</span></span>

 

 



