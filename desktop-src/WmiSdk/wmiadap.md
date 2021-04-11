---
description: Wmiadap ist eine Anwendung, die unter Windows ausgeführt wird und Leistungsinformationen im WMI-Repository aktualisieren kann.
ms.assetid: 459fe19e-3e2e-4a58-b3e7-75fd285f7389
ms.tgt_platform: multiple
title: wmiadap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa5d2de65e8566283b341c5af52048cc79cc0299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218472"
---
# <a name="wmiadap"></a><span data-ttu-id="ccf37-103">wmiadap</span><span class="sxs-lookup"><span data-stu-id="ccf37-103">wmiadap</span></span>

<span data-ttu-id="ccf37-104">Wmiadap ist eine Anwendung, die unter Windows ausgeführt wird und Leistungsinformationen im WMI-Repository aktualisieren kann.</span><span class="sxs-lookup"><span data-stu-id="ccf37-104">Wmiadap is a application that runs on Windows that can update performance information in the WMI repository.</span></span> <span data-ttu-id="ccf37-105">Im Allgemeinen können Entwickler und IT-Administratoren Skripts erstellen, die auf Leistungsinformationen zugreifen, wie z. b. die Menge an Arbeitsspeicher, die von einer Anwendung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ccf37-105">Generally, this allows developers and IT Administrators to create scripts that access performance information, such as the amount of memory used by an application.</span></span> <span data-ttu-id="ccf37-106">Im folgenden Thema wird die Befehlszeilenschnittstelle beschrieben, mit der Sie steuern können, wie wmiadap Informationen abruft.</span><span class="sxs-lookup"><span data-stu-id="ccf37-106">The following topic describes the command-line interface you can use to control how wmiadap retrieves information.</span></span>

<span data-ttu-id="ccf37-107">Wmiadap wird mit dem Betriebssystem auf den meisten Systemen im Verzeichnis "C: \\ Windows \\ system32 \\ WBEM" installiert.</span><span class="sxs-lookup"><span data-stu-id="ccf37-107">Wmiadap is installed with the operating system on most systems, in the C:\\Windows\\System32\\wbem directory.</span></span> <span data-ttu-id="ccf37-108">Wenn Sie Fehlermeldungen zu wmiadap.exe sehen, suchen Sie [Microsoft-Support](https://support.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="ccf37-108">If you are seeing error messages concerning wmiadap.exe, search [Microsoft Support](https://support.microsoft.com/).</span></span> <span data-ttu-id="ccf37-109">Im Allgemeinen sollten Sie wmiadap.exe nicht von Ihrem System löschen, sofern nicht anders beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ccf37-109">Generally, you should not delete wmiadap.exe from your system, unless otherwise instructed.</span></span>

<span data-ttu-id="ccf37-110">Die Übertragung von Daten aus den Leistungs Bibliotheken und die Aktualisierung von Klassen, die von [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) und [**Win32 \_ perfformatteddata**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) abgeleitet werden, erfolgt durch die Anbieter [wmiperfclass](wmi-providers.md) und [wmiperfinst](wmi-providers.md) .</span><span class="sxs-lookup"><span data-stu-id="ccf37-110">The transfer of data from the performance libraries and the refresh of classes derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) is done by the [WmiPerfClass](wmi-providers.md) and [WMIPerfInst](wmi-providers.md) providers.</span></span> <span data-ttu-id="ccf37-111">Der wmiperfclass-Anbieter aktualisiert die WMI- [Leistungs Objektklassen](/windows/desktop/CIMWin32Prov/performance-counter-classes) nur dann, wenn ein neues Leistungs Objekt hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="ccf37-111">The WmiPerfClass provider updates WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes) only when a new performance object is added.</span></span> <span data-ttu-id="ccf37-112">Sie können wmiadap weiterhin mit dem Schalter **/r** ausführen, um die Windows-Treibermodell-Treiber zum Erstellen von Leistungs Objekten zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="ccf37-112">You still can run Wmiadap with the **/r** switch to parse the Windows Driver Model drivers to create performance objects.</span></span> <span data-ttu-id="ccf37-113">Der Schalter **/f** erzwingt weiterhin ein Update der WMI-Klassen aus den Leistungs Bibliotheken.</span><span class="sxs-lookup"><span data-stu-id="ccf37-113">The **/f** switch still forces an update of the WMI classes from the performance libraries.</span></span>

<span data-ttu-id="ccf37-114">Die folgenden Schalter sind an der Eingabeaufforderung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ccf37-114">The following switches are available at the command prompt.</span></span>

<span data-ttu-id="ccf37-115">**wmiadap** \[  \] /f \[ **/r**\]</span><span class="sxs-lookup"><span data-stu-id="ccf37-115">**wmiadap** \[**/f**\]\[**/r**\]</span></span>

## <a name="switches"></a><span data-ttu-id="ccf37-116">Switches</span><span class="sxs-lookup"><span data-stu-id="ccf37-116">Switches</span></span>

<dl> <dt>

<span data-ttu-id="ccf37-117"><span id="_f"></span><span id="_F"></span>**/f**</span><span class="sxs-lookup"><span data-stu-id="ccf37-117"><span id="_f"></span><span id="_F"></span>**/f**</span></span>
</dt> <dd>

<span data-ttu-id="ccf37-118">Analysiert alle Leistungs Bibliotheken auf dem System und aktualisiert die von [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) und [**Win32 \_ perfformatteddata**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)abgeleiteten Klassen.</span><span class="sxs-lookup"><span data-stu-id="ccf37-118">Parses all the performance libraries on the system and refreshes the classes derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span>

</dd> <dt>

<span data-ttu-id="ccf37-119"><span id="_r"></span><span id="_R"></span>**/r**</span><span class="sxs-lookup"><span data-stu-id="ccf37-119"><span id="_r"></span><span id="_R"></span>**/r**</span></span>
</dt> <dd>

<span data-ttu-id="ccf37-120">Analysiert alle Windows-Treibermodell Treiber auf dem System, um Leistungs Objekte zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ccf37-120">Parses all the Windows Driver Model drivers on the system to create performance objects.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="ccf37-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ccf37-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccf37-122">Leistungs Bibliotheken und WMI</span><span class="sxs-lookup"><span data-stu-id="ccf37-122">Performance Libraries and WMI</span></span>](performance-libraries-and-wmi.md)
</dt> <dt>

[<span data-ttu-id="ccf37-123">**WinMgmt**</span><span class="sxs-lookup"><span data-stu-id="ccf37-123">**winmgmt**</span></span>](winmgmt.md)
</dt> </dl>

 

 
