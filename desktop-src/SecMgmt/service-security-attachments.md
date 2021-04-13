---
description: Das Microsoft Security Configuration Tool ist ein Satz von Microsoft Management Console (MMC)-Tools, die die Konfiguration und Analyse der Systemsicherheit vereinfachen.
ms.assetid: c6558789-84eb-4998-a2c1-725d8a64d255
title: Dienst Sicherheitsanlagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f47cdd0ca3799615125900a3ae6b0b78c26f4abc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343089"
---
# <a name="service-security-attachments"></a><span data-ttu-id="1ddc3-103">Dienst Sicherheitsanlagen</span><span class="sxs-lookup"><span data-stu-id="1ddc3-103">Service Security Attachments</span></span>

<span data-ttu-id="1ddc3-104">Das Microsoft Security Configuration Tool ist ein Satz von Microsoft Management Console (MMC)-Tools, die die Konfiguration und Analyse der Systemsicherheit vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="1ddc3-104">The Microsoft Security Configuration tool set is a set of Microsoft Management Console (MMC) tools that simplify configuration and analysis of system security.</span></span> <span data-ttu-id="1ddc3-105">Einige Dienste verfügen jedoch über spezielle Konfigurations Anforderungen, die über die vom Standard Toolset bereitgestellten Sicherheitseinstellungen hinausgehen.</span><span class="sxs-lookup"><span data-stu-id="1ddc3-105">Some services, however, have specialized configuration needs that go beyond the security settings provided by the standard tool set.</span></span> <span data-ttu-id="1ddc3-106">Um diese Anforderungen zu erfüllen, können Sie die Funktionalität des Toolsets erweitern, indem Sie eine Anlage schreiben, die die Dienst spezifischen Sicherheitsaufgaben behandelt.</span><span class="sxs-lookup"><span data-stu-id="1ddc3-106">To handle those needs, you can extend the functionality of the tool set by writing an attachment that handles the service-specific security tasks.</span></span>

<span data-ttu-id="1ddc3-107">Spooler ist beispielsweise ein Windows NT-Dienst, der private Objekte definiert, die gesichert werden müssen, z. b. Drucker.</span><span class="sxs-lookup"><span data-stu-id="1ddc3-107">For example, Spooler is a Windows NT service that defines private objects, which need to be secured, for example, printers.</span></span> <span data-ttu-id="1ddc3-108">Diese Funktion wird nicht von der Standard Toolreihe behandelt und erfordert daher eine Anlage zur Handhabung der Konfiguration und Analyse von Drucker Objekten.</span><span class="sxs-lookup"><span data-stu-id="1ddc3-108">This functionality is not handled by the standard tool set and thus requires an attachment to handle configuration and analysis of printer objects.</span></span> <span data-ttu-id="1ddc3-109">Die Konfiguration allgemeiner Sicherheitsparameter, wie z. b. der Dienst Aufruf Richtlinie, wird weiterhin vom Sicherheitskonfigurations-Toolset behandelt.</span><span class="sxs-lookup"><span data-stu-id="1ddc3-109">Configuration of general security parameters, such as the service invocation policy, is still handled by the Security Configuration tool set.</span></span>

<span data-ttu-id="1ddc3-110">Sicherheitsdienst Anlagen erweitern die Funktionalität des Sicherheitskonfigurations Tools, die für die Unterstützung Dienst spezifischer Konfigurationen festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1ddc3-110">Security service attachments extend the functionality of the Security Configuration tool set to support service-specific configurations.</span></span>

<span data-ttu-id="1ddc3-111">Eine Anlage verfügt über zwei Komponenten:</span><span class="sxs-lookup"><span data-stu-id="1ddc3-111">An attachment has two components:</span></span>

-   <span data-ttu-id="1ddc3-112">Eine MMC-Snap-in-Erweiterung, die die Benutzeroberfläche der Anlage implementiert.</span><span class="sxs-lookup"><span data-stu-id="1ddc3-112">An MMC snap-in extension that implements the attachment user interface.</span></span>
-   <span data-ttu-id="1ddc3-113">Eine Anlage-Engine, die Dienst spezifische Sicherheitskonfigurations-und Analyse Tasks verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="1ddc3-113">An attachment engine that processes service-specific security configuration and analysis tasks.</span></span>

<span data-ttu-id="1ddc3-114">Die Erweiterungs-Snap-in-Erweiterung wird von den Snap-Ins "Sicherheitskonfiguration" gehostet. Hierbei handelt es sich um MMC-Snap-Ins, die dem Benutzer Schnittstellen zum Konfigurieren und Analysieren der allgemeinen Sicherheitseinstellungen für einen Dienst bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="1ddc3-114">The attachment snap-in extension is hosted by the Security Configuration snap-ins. These are MMC snap-ins that provide the user with interfaces to configure and analyze the general security settings for a service.</span></span> <span data-ttu-id="1ddc3-115">Dienst spezifische Einstellungen werden mithilfe der Erweiterungs-Snap-in-Erweiterung konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="1ddc3-115">Service-specific settings are configured using the attachment snap-in extension.</span></span>

<span data-ttu-id="1ddc3-116">Wenn der Benutzer eine Konfigurationseinstellung ändert, werden die neuen Informationen in den Snap-Ins "Sicherheitskonfigurations-Snap-Ins" gespeichert, und die Anforderung wird an die Sicherheitskonfigurations-Engine übergeben.</span><span class="sxs-lookup"><span data-stu-id="1ddc3-116">When the user changes a configuration setting, the Security Configuration snap-ins store the new information and then pass the request to the Security Configuration Engine.</span></span> <span data-ttu-id="1ddc3-117">Die Engine verarbeitet die Anforderung und legt den Dienst auf die neue Konfiguration fest.</span><span class="sxs-lookup"><span data-stu-id="1ddc3-117">The Engine processes the request and sets the service to the new configuration.</span></span> <span data-ttu-id="1ddc3-118">Wenn die Anforderung eine Standard Sicherheitseinstellung betrifft, wird Sie von der-Engine behandelt.</span><span class="sxs-lookup"><span data-stu-id="1ddc3-118">If the request affects a standard security setting, it is handled by the Engine.</span></span> <span data-ttu-id="1ddc3-119">Wenn die Anforderung Dienst spezifisch ist, ruft die Engine die entsprechende Anlage-Engine auf, um die Anforderung zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="1ddc3-119">If the request is service-specific, the Engine calls the appropriate attachment engine to handle the request.</span></span>

<span data-ttu-id="1ddc3-120">In der folgenden Abbildung wird gezeigt, wie die Anlagen-Engine und die Snap-in-Erweiterung innerhalb des Frameworks des Sicherheitskonfigurations-Toolsets funktionieren.</span><span class="sxs-lookup"><span data-stu-id="1ddc3-120">The following illustration shows how the attachment engine and snap-in extension work within the framework of the Security Configuration tool set.</span></span>

![Anlagen-Engine und Snap-Ins](images/model1a.png)

<span data-ttu-id="1ddc3-122">Weitere Informationen zur Verwendung des Microsoft Security Configuration Tool Sets finden Sie unter Sicherheitskonfiguration mithilfe Ihrer bevorzugten Suchmaschine.</span><span class="sxs-lookup"><span data-stu-id="1ddc3-122">For more information about using the Microsoft Security Configuration tool set, search for Security Configuration using your preferred search engine.</span></span>

 

 



