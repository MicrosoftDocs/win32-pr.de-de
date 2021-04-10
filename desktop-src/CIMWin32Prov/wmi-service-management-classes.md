---
description: WMI-Dienst Verwaltungs Klassen werden verwendet, um den WMI-Dienst selbst und nicht das Computersystem oder Unternehmensnetzwerk zu verwalten. Das Verwalten von WMI umfasst sowohl das Konfigurieren des WMI-dienbes als auch das Verwalten von WMI
ms.assetid: EF58AC04-FE04-4D0C-A5F7-3491C885A0E4
ms.tgt_platform: multiple
title: WMI-Dienst Verwaltungs Klassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b502abebbddfd2ce90562045a8b0d7acd3974171
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126068"
---
# <a name="wmi-service-management-classes"></a><span data-ttu-id="eac08-104">WMI-Dienst Verwaltungs Klassen</span><span class="sxs-lookup"><span data-stu-id="eac08-104">WMI Service Management Classes</span></span>

<span data-ttu-id="eac08-105">WMI-Dienst Verwaltungs Klassen werden verwendet, um den WMI-Dienst selbst und nicht das Computersystem oder Unternehmensnetzwerk zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="eac08-105">WMI service management classes are used to manage the WMI service itself and not the computer system or enterprise network.</span></span> <span data-ttu-id="eac08-106">Das Verwalten von WMI umfasst sowohl das Konfigurieren des WMI-dienbes als auch das Verwalten von WMI</span><span class="sxs-lookup"><span data-stu-id="eac08-106">Managing WMI encompasses both configuring the WMI service and managing WMI operations.</span></span>

<span data-ttu-id="eac08-107">Die Kategorie WMI-Dienst Verwaltung enthält die folgenden Unterkategorien von Klassen:</span><span class="sxs-lookup"><span data-stu-id="eac08-107">The WMI Service Management category includes the following subcategories of classes:</span></span>

-   [<span data-ttu-id="eac08-108">WMI-Konfigurations Klassen</span><span class="sxs-lookup"><span data-stu-id="eac08-108">WMI configuration classes</span></span>](#wmi-configuration-classes)
-   [<span data-ttu-id="eac08-109">WMI-Verwaltungs Klassen</span><span class="sxs-lookup"><span data-stu-id="eac08-109">WMI management classes</span></span>](#wmi-management-classes)

## <a name="wmi-configuration-classes"></a><span data-ttu-id="eac08-110">WMI-Konfigurations Klassen</span><span class="sxs-lookup"><span data-stu-id="eac08-110">WMI Configuration Classes</span></span>

<span data-ttu-id="eac08-111">Die WMI-Konfigurations Klasse leitet Methoden ab, die den WMI-Dienst konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="eac08-111">The WMI Configuration class derives methods that configure the WMI service.</span></span>

<span data-ttu-id="eac08-112">Im folgenden finden Sie eine Tabelle der WMI-Konfigurations Klassen.</span><span class="sxs-lookup"><span data-stu-id="eac08-112">The following is a table of WMI configuration classes.</span></span>



| <span data-ttu-id="eac08-113">Klasse</span><span class="sxs-lookup"><span data-stu-id="eac08-113">Class</span></span>                                                             | <span data-ttu-id="eac08-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eac08-114">Description</span></span>                                                                     |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="eac08-115">**Win32 \_ methodparameterclass**</span><span class="sxs-lookup"><span data-stu-id="eac08-115">**Win32\_MethodParameterClass**</span></span>](win32-methodparameterclass.md) | <span data-ttu-id="eac08-116">Abstrakte Basisklasse, die von dieser Klasse abgeleitete Methoden Parameter implementiert.</span><span class="sxs-lookup"><span data-stu-id="eac08-116">Abstract, base class that implements method parameters derived from this class.</span></span> |



 

## <a name="wmi-management-classes"></a><span data-ttu-id="eac08-117">WMI-Verwaltungs Klassen</span><span class="sxs-lookup"><span data-stu-id="eac08-117">WMI Management Classes</span></span>

<span data-ttu-id="eac08-118">Die WMI-Verwaltungs Klassen stellen Betriebsparameter für den WMI-Dienst dar.</span><span class="sxs-lookup"><span data-stu-id="eac08-118">The WMI management classes represent operational parameters for the WMI service.</span></span>

<span data-ttu-id="eac08-119">Im folgenden finden Sie eine Tabelle der WMI-Verwaltungs Klassen.</span><span class="sxs-lookup"><span data-stu-id="eac08-119">The following is a table of WMI management classes.</span></span>



| <span data-ttu-id="eac08-120">Klasse</span><span class="sxs-lookup"><span data-stu-id="eac08-120">Class</span></span>                                                       | <span data-ttu-id="eac08-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eac08-121">Description</span></span>                                                                                   |
|-------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eac08-122">**Win32- \_ wmisetting**</span><span class="sxs-lookup"><span data-stu-id="eac08-122">**Win32\_WMISetting**</span></span>](win32-wmisetting.md)               | <span data-ttu-id="eac08-123">Enthält die Betriebsparameter für den WMI-Dienst.</span><span class="sxs-lookup"><span data-stu-id="eac08-123">Contains the operational parameters for the WMI service.</span></span>                                      |
| [<span data-ttu-id="eac08-124">**Win32- \_ wmielementsetting**</span><span class="sxs-lookup"><span data-stu-id="eac08-124">**Win32\_WMIElementSetting**</span></span>](win32-wmielementsetting.md) | <span data-ttu-id="eac08-125">Zuordnung zwischen einem Dienst, der im Windows-System ausgeführt wird, und den WMI-Einstellungen, die verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="eac08-125">Association between a service running in the Windows system, and the WMI settings it can use.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="eac08-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="eac08-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eac08-127">Win32-Klassen</span><span class="sxs-lookup"><span data-stu-id="eac08-127">Win32 Classes</span></span>](./win32-provider.md)
</dt> </dl>

 

 
