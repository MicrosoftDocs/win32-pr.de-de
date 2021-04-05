---
description: Beschreibt die Energierichtlinien Einstellungen, die ein Energie Schema bilden.
ms.assetid: cd515cd6-67f4-45d0-b769-3abc7a56faa8
title: Energierichtlinien Einstellungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f490c758a890faf314be1ddffe9ac7a503bd473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756571"
---
# <a name="power-policy-settings"></a><span data-ttu-id="02b54-103">Energierichtlinien Einstellungen</span><span class="sxs-lookup"><span data-stu-id="02b54-103">Power Policy Settings</span></span>

<span data-ttu-id="02b54-104">Energie Sparpläne und-Schemas bestehen aus Einstellungen und Richtlinien Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="02b54-104">Power plans and schemes consist of preferences and policy settings.</span></span>

<span data-ttu-id="02b54-105">Ein Energie Sparplan besteht aus einer Gruppe von Einstellungen für die Energie Einstellung.</span><span class="sxs-lookup"><span data-stu-id="02b54-105">A power plan consists of a group of power setting preferences.</span></span> <span data-ttu-id="02b54-106">Diese Einstellungen bestehen sowohl aus einem AC-als auch einem DC-Wert für jede der Energie Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="02b54-106">These preferences consist of both an AC and DC value for each of the power settings.</span></span> <span data-ttu-id="02b54-107">Jeder Energie Sparplan wird durch eine eindeutige **GUID** und einen anzeigen Amen identifiziert.</span><span class="sxs-lookup"><span data-stu-id="02b54-107">Each power plan is identified through a unique **GUID** as well as a friendly name.</span></span> <span data-ttu-id="02b54-108">Windows Vista verfügt über drei Standard Energie Sparpläne: Energiesparmodus, ausgeglichen und hohe Leistung.</span><span class="sxs-lookup"><span data-stu-id="02b54-108">Windows Vista has three default power plans: Power Saver, Balanced, and High Performance.</span></span> <span data-ttu-id="02b54-109">Diese Pläne können angepasst werden, und es können weitere Pläne erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="02b54-109">These plans can be customized, and additional plans can be created.</span></span> <span data-ttu-id="02b54-110">Alle Energie Sparpläne verfügen über ein Attribut "Personality", das das Gesamtenergie Einsparungs Verhalten des Plans angibt.</span><span class="sxs-lookup"><span data-stu-id="02b54-110">All power plans have a personality attribute that indicates the overall power savings behavior of the plan.</span></span>

<span data-ttu-id="02b54-111">In der folgenden Tabelle werden die drei Energie Sparplan-Persönlichkeiten aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="02b54-111">The following table shows the three power plan personalities.</span></span> 

| <span data-ttu-id="02b54-112">`Display name`</span><span class="sxs-lookup"><span data-stu-id="02b54-112">Display name</span></span>     | <span data-ttu-id="02b54-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="02b54-113">Description</span></span>                                                                   | <span data-ttu-id="02b54-114">**GUID**</span><span class="sxs-lookup"><span data-stu-id="02b54-114">**GUID**</span></span>                             |
|------------------|-------------------------------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="02b54-115">Energiesparmodus</span><span class="sxs-lookup"><span data-stu-id="02b54-115">Power Saver</span></span>      | <span data-ttu-id="02b54-116">Bietet eine geringere Leistung, wodurch sich der Energiespar Aufwand erhöhen kann.</span><span class="sxs-lookup"><span data-stu-id="02b54-116">Delivers reduced performance which may increase power savings.</span></span>                | <span data-ttu-id="02b54-117">a1841308-3541-4fab-bc81-f71556f20b4a</span><span class="sxs-lookup"><span data-stu-id="02b54-117">a1841308-3541-4fab-bc81-f71556f20b4a</span></span> |
| <span data-ttu-id="02b54-118">Balanced</span><span class="sxs-lookup"><span data-stu-id="02b54-118">Balanced</span></span>         | <span data-ttu-id="02b54-119">Die Leistung und der Stromverbrauch werden von nach Bedarf automatisch ausgeglichen.</span><span class="sxs-lookup"><span data-stu-id="02b54-119">Automatically balances performance and power consumption according to demand.</span></span> | <span data-ttu-id="02b54-120">381b4222-f694-41f0-9685-ff5bb260df2e</span><span class="sxs-lookup"><span data-stu-id="02b54-120">381b4222-f694-41f0-9685-ff5bb260df2e</span></span> |
| <span data-ttu-id="02b54-121">Hohe Leistung</span><span class="sxs-lookup"><span data-stu-id="02b54-121">High Performance</span></span> | <span data-ttu-id="02b54-122">Bietet eine maximale Leistung bei einem höheren Stromverbrauch.</span><span class="sxs-lookup"><span data-stu-id="02b54-122">Delivers maximum performance at the expense of higher power consumption.</span></span>      | <span data-ttu-id="02b54-123">8c5e7lda-e8bf -4a96-9a85-a6e23a8c635c</span><span class="sxs-lookup"><span data-stu-id="02b54-123">8c5e7fda-e8bf-4a96-9a85-a6e23a8c635c</span></span> |



 

> [!Note]  
> <span data-ttu-id="02b54-124">Geräte, die den [modernen Standby](/windows-hardware/design/device-experiences/modern-standby) -Modus unterstützen, ermöglichen nur den **ausgeglichenen** Energie Sparplan.</span><span class="sxs-lookup"><span data-stu-id="02b54-124">Devices that support [Modern Standby](/windows-hardware/design/device-experiences/modern-standby) mode only allow the **Balanced** power plan.</span></span> <span data-ttu-id="02b54-125">**Modern Standby** ist die neuere, optimierte Lösung für die Verwaltung von Energie Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="02b54-125">**Modern Standby** is the newer, more streamlined solution to power settings management.</span></span>

 

<span data-ttu-id="02b54-126">Jeder Computer verfügt über einen einzigen, aktiven Energie Sparplan.</span><span class="sxs-lookup"><span data-stu-id="02b54-126">Each computer has a single, active power plan.</span></span> <span data-ttu-id="02b54-127">Standardmäßig können nicht berechtigte Benutzer auf System Energie Einstellungen zugreifen.</span><span class="sxs-lookup"><span data-stu-id="02b54-127">By default, nonprivileged users are able to access system power settings.</span></span> <span data-ttu-id="02b54-128">Der Zugriff auf alle oder einzelne Energie Einstellungen kann über ACLs in den Energie Einstellungen oder über Gruppenrichtlinie gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="02b54-128">Access to all or individual power settings can be controlled through ACLs on the power settings or through Group Policy.</span></span> <span data-ttu-id="02b54-129">Anwendungen sollten [**powersettingaccesscheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) aufrufen, um zu bestimmen, ob der Benutzer Zugriff auf die Energie Einstellung hat.</span><span class="sxs-lookup"><span data-stu-id="02b54-129">Applications should call [**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) to determine if the user has access to the power setting.</span></span>

<span data-ttu-id="02b54-130">Jede Energie Einstellung wird durch eine eindeutige **GUID** gekennzeichnet und enthält einen anzeigen Amen, eine Beschreibung, zulässige Werte und Standardwerte für die AC-und DC-Werte.</span><span class="sxs-lookup"><span data-stu-id="02b54-130">Each power setting is identified by a unique **GUID** and includes a friendly name, description, allowable values, and default values for AC and DC.</span></span> <span data-ttu-id="02b54-131">Benutzerdefinierte Energie Einstellungen können mithilfe der Funktion " [**Power| ateseing"**](/windows/desktop/api/PowrProf/nf-powrprof-powercreatesetting) erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="02b54-131">Custom power settings can be created using the [**PowerCreateSetting**](/windows/desktop/api/PowrProf/nf-powrprof-powercreatesetting) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="02b54-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="02b54-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02b54-133">Energie Schemas</span><span class="sxs-lookup"><span data-stu-id="02b54-133">Power Schemes</span></span>](power-schemes.md)
</dt> </dl>

 

 
