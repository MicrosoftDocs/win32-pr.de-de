---
description: Das Schreiben eines hochleistungsfähigen WMI-Anbieters zum Erstellen von Leistungsindikatoren ist nicht empfehlenswert.
ms.assetid: 6a22d6f7-d9e2-45fa-876d-921a4bc4f574
ms.tgt_platform: multiple
title: Erstellen eines Instanzanbieters in einen High-Performance-Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10744b110463a3207f76bb55d48a8045ec22783d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363496"
---
# <a name="making-an-instance-provider-into-a-high-performance-provider"></a><span data-ttu-id="1ddbf-103">Erstellen eines Instanzanbieters in einen High-Performance-Anbieter</span><span class="sxs-lookup"><span data-stu-id="1ddbf-103">Making an Instance Provider into a High-Performance Provider</span></span>

<span data-ttu-id="1ddbf-104">Das Schreiben eines hochleistungsfähigen WMI-Anbieters zum Erstellen von Leistungsindikatoren ist nicht empfehlenswert.</span><span class="sxs-lookup"><span data-stu-id="1ddbf-104">Writing a WMI high-performance provider to create performance counters is not recommended.</span></span> <span data-ttu-id="1ddbf-105">Ab Windows Vista werden die WMI- [Leistungs Leistungs](/windows/desktop/CIMWin32Prov/performance-counter-classes) Daten-Klassen nicht mehr vom reverseadapter AutoDiscovery/AUTOPURGE (ADAP) in die Windows-Leistungs Bibliotheken migriert.</span><span class="sxs-lookup"><span data-stu-id="1ddbf-105">Starting with Windows Vista, the WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes) are no longer migrated into the Windows performance libraries by the AutoDiscovery/AutoPurge (ADAP) reverse adapter.</span></span> <span data-ttu-id="1ddbf-106">Verwenden Sie zum Erstellen eines Leistungsindikator Anbieters die [Leistungsindikatoren Version 2,0](/windows/desktop/PerfCtrs/performance-counters-portal).</span><span class="sxs-lookup"><span data-stu-id="1ddbf-106">To create a performance counter provider, use [Performance Counters Version 2.0](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span> <span data-ttu-id="1ddbf-107">Nachdem Leistungs Bibliotheksobjekte erstellt wurden, analysiert der [wmiperfclass-Anbieter](wmiperfclass-provider.md) die Objekte und erstellt oder aktualisiert eine von [**Win32 \_ perf**](/windows/desktop/CIMWin32Prov/win32-perf) abgeleitete WMI-Klasse für jedes Leistungs Objekt.</span><span class="sxs-lookup"><span data-stu-id="1ddbf-107">After performance library objects are created, the [WMIPerfClass Provider](wmiperfclass-provider.md) parses the objects and creates or refreshes a WMI class derived from [**Win32\_Perf**](/windows/desktop/CIMWin32Prov/win32-perf) for each performance object.</span></span> <span data-ttu-id="1ddbf-108">Der [WMIPerfInst-Anbieter](wmiperfinst-provider.md) stellt dann dynamisch Rohdaten und formatierte Leistungsdaten für die WMI-Leistungsklassen bereit.</span><span class="sxs-lookup"><span data-stu-id="1ddbf-108">The [WMIPerfInst Provider](wmiperfinst-provider.md) then dynamically provides raw and formatted performance counter data to the WMI performance classes.</span></span>

<span data-ttu-id="1ddbf-109">Die folgende allgemeine Vorgehensweise enthält die zum Erstellen eines Hochleistungs Anbieters erforderlichen Schritte.</span><span class="sxs-lookup"><span data-stu-id="1ddbf-109">The following high-level procedure provides the steps required to create a high-performance provider.</span></span>

<span data-ttu-id="1ddbf-110">**So erstellen Sie einen Hochleistungs Anbieter**</span><span class="sxs-lookup"><span data-stu-id="1ddbf-110">**To create a high-performance provider**</span></span>

1.  <span data-ttu-id="1ddbf-111">Registrieren Sie Ihren Anbieter bei WMI.</span><span class="sxs-lookup"><span data-stu-id="1ddbf-111">Register your provider with WMI.</span></span> <span data-ttu-id="1ddbf-112">Weitere Informationen finden Sie unter [Registrieren eines High-Performance Anbieters](registering-a-high-performance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="1ddbf-112">For more information, see [Registering a High-Performance Provider](registering-a-high-performance-provider.md).</span></span>
2.  <span data-ttu-id="1ddbf-113">Implementieren Sie Ihren Anbieter.</span><span class="sxs-lookup"><span data-stu-id="1ddbf-113">Implement your provider.</span></span> <span data-ttu-id="1ddbf-114">Weitere Informationen finden Sie unter [Schreiben eines Instanzanbieters](writing-an-instance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="1ddbf-114">For more information, see [Writing an Instance Provider](writing-an-instance-provider.md).</span></span>
3.  <span data-ttu-id="1ddbf-115">Implementieren Sie die Hochleistungs Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="1ddbf-115">Implement the high-performance interface.</span></span> <span data-ttu-id="1ddbf-116">Weitere Informationen finden Sie unter [Implementieren der High-Performance-Schnittstelle](implementing-the-high-performance-interface.md).</span><span class="sxs-lookup"><span data-stu-id="1ddbf-116">For more information, see [Implementing the High-Performance Interface](implementing-the-high-performance-interface.md).</span></span>
4.  <span data-ttu-id="1ddbf-117">Leiten Sie das MOF-Schema (Managed Object Format) ab, und schreiben Sie es, um rohleistungs Daten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1ddbf-117">Derive and write your Managed Object Format (MOF) schema to obtain raw performance data.</span></span> <span data-ttu-id="1ddbf-118">Weitere Informationen finden Sie [unter unterstützen der Win32 \_ perfrawdata-Klasse](supporting-the-win32-perfrawdata-class.md).</span><span class="sxs-lookup"><span data-stu-id="1ddbf-118">For more information, see [Supporting the Win32\_PerfRawData Class](supporting-the-win32-perfrawdata-class.md).</span></span>
5.  <span data-ttu-id="1ddbf-119">Ableiten und schreiben Sie das MOF-Schema, um vorab berechnete Daten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1ddbf-119">Derive and write your MOF schema to obtain precalculated data.</span></span> <span data-ttu-id="1ddbf-120">Wenn diese Klasse unterstützt wird, ist es nicht erforderlich, dass der Anbieter die Berechnungen ausführt.</span><span class="sxs-lookup"><span data-stu-id="1ddbf-120">By supporting this class, the provider is not required to perform the calculations.</span></span> <span data-ttu-id="1ddbf-121">Dabei handelt es sich um die gleichen Daten, die im System Monitor in Perfmon angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="1ddbf-121">This data will be the same that appears in the System Monitor in Perfmon.</span></span> <span data-ttu-id="1ddbf-122">Weitere Informationen finden Sie [unter unterstützen der Win32 \_ perfformatteddata-Klasse](supporting-the-win32-perfformatteddata-class.md).</span><span class="sxs-lookup"><span data-stu-id="1ddbf-122">For more information, see [Supporting the Win32\_PerfFormattedData Class](supporting-the-win32-perfformatteddata-class.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ddbf-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1ddbf-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ddbf-124">Entwickeln eines WMI-Anbieters</span><span class="sxs-lookup"><span data-stu-id="1ddbf-124">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> <dt>

[<span data-ttu-id="1ddbf-125">Leistungs Bibliotheken und WMI</span><span class="sxs-lookup"><span data-stu-id="1ddbf-125">Performance Libraries and WMI</span></span>](performance-libraries-and-wmi.md)
</dt> </dl>

 

 
