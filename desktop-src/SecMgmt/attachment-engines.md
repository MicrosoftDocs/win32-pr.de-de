---
description: Eine Anlage-Engine ist eine DLL, die Dienst spezifische Konfigurations-und Analyseanforderungen verarbeitet.
ms.assetid: bbca486a-9eec-4510-b5fd-435972182a69
title: Anlagen-Engines
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9af0711caa5ceada7c16ae11b6470568a76d16ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866963"
---
# <a name="attachment-engines"></a><span data-ttu-id="cd980-103">Anlagen-Engines</span><span class="sxs-lookup"><span data-stu-id="cd980-103">Attachment Engines</span></span>

<span data-ttu-id="cd980-104">Eine Anlage-Engine ist eine DLL, die Dienst spezifische Konfigurations-und Analyseanforderungen verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="cd980-104">An attachment engine is a DLL that handles service-specific configuration and analysis requests.</span></span>

<span data-ttu-id="cd980-105">Der Benutzer stellt eine Dienst spezifische Konfigurations-und Analyse Anforderung mithilfe der Erweiterungs-Snap-in-Erweiterung her.</span><span class="sxs-lookup"><span data-stu-id="cd980-105">The user makes a service-specific configuration and analysis request using the attachment snap-in extension.</span></span> <span data-ttu-id="cd980-106">Diese Anforderung wird dann über die Sicherheitskonfigurations-Snap-Ins an die allgemeine Sicherheitskonfigurations-Engine weitergeleitet, die wiederum die Dienst spezifische Verarbeitung an die entsprechende Anlage-Engine übergibt.</span><span class="sxs-lookup"><span data-stu-id="cd980-106">This request is then passed through the Security Configuration snap-ins to the general Security Configuration Engine, which in turn passes the service-specific processing to the appropriate attachment engine.</span></span> <span data-ttu-id="cd980-107">Die Anlagen-Engine stellt dann eine Verbindung mit dem Dienst her und ändert seine Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="cd980-107">The attachment engine then connects to the service and changes its configuration.</span></span> <span data-ttu-id="cd980-108">Mit anderen Worten: die Anlagen-Engine stellt die Back-End-Verarbeitung bereit, die die Erweiterungs-Snap-in-Erweiterung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cd980-108">In other words, the attachment engine provides the back-end processing that supports the attachment snap-in extension.</span></span>

<span data-ttu-id="cd980-109">Eine Anlage-Engine muss die folgenden drei Funktionen implementieren:</span><span class="sxs-lookup"><span data-stu-id="cd980-109">An attachment engine must implement the following three functions:</span></span>

-   <span data-ttu-id="cd980-110">[**Scesvstreamtachmentanalysis**](scesvcattachmentanalyze.md): berechnet den Unterschied zwischen der Konfiguration des Diensts und der Konfiguration, die in der Sicherheitsdatenbank gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="cd980-110">[**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md), which computes the difference between the service's configuration and the configuration stored in the security database.</span></span> <span data-ttu-id="cd980-111">Die Unterschiede werden in die Sicherheitsdatenbank geschrieben.</span><span class="sxs-lookup"><span data-stu-id="cd980-111">The differences are written to the security database.</span></span>
-   <span data-ttu-id="cd980-112">[**Scesvtortachmentconfig**](scesvcattachmentconfig.md): Hiermit wird der Dienst entsprechend der Angabe in der Snap-in-Benutzeroberfläche konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="cd980-112">[**SceSvcAttachmentConfig**](scesvcattachmentconfig.md), which configures the service as specified in the snap-in user interface.</span></span>
-   <span data-ttu-id="cd980-113">[**Scesvsintachmentupdate**](scesvcattachmentupdate.md), das die Basiskonfiguration und Konfigurations Analyse für den Dienst in der Sicherheitsdatenbank aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="cd980-113">[**SceSvcAttachmentUpdate**](scesvcattachmentupdate.md), which updates the base configuration and configuration analysis for the service in the security database.</span></span>

<span data-ttu-id="cd980-114">Um die Implementierung der vorangehenden Funktionen zu vereinfachen, stellt das Sicherheitskonfigurations-Toolset Unterstützungsfunktionen und-Strukturen bereit, die Ihre Anwendung zum Abfragen und Festlegen von Informationen in der Sicherheitsdatenbank verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="cd980-114">To simplify implementation of the preceding functions, the Security Configuration tool set provides support functions and structures that your application can use to query and set information in the security database.</span></span> <span data-ttu-id="cd980-115">Weitere Informationen finden Sie unter [Anlage Rückruf Funktionen](management-functions.md).</span><span class="sxs-lookup"><span data-stu-id="cd980-115">For more information, see [Attachment Callback Functions](management-functions.md).</span></span>

<span data-ttu-id="cd980-116">Wenn Sie eine Anlagen-Engine-dll erstellen, müssen Sie Sie installieren und anschließend bei der Sicherheitskonfigurations-Engine registrieren.</span><span class="sxs-lookup"><span data-stu-id="cd980-116">When you create an attachment engine DLL, you must install it and then register it with the Security Configuration Engine.</span></span> <span data-ttu-id="cd980-117">Um die dll zu registrieren, fügen Sie der Registrierung einen bestimmten Schlüssel hinzu.</span><span class="sxs-lookup"><span data-stu-id="cd980-117">To register the DLL, you add a specific key to the registry.</span></span> <span data-ttu-id="cd980-118">Beim Start der Sicherheitskonfigurations-Engine wird die Registrierung überprüft und alle registrierten Anlagen-Engine-DLLs geladen.</span><span class="sxs-lookup"><span data-stu-id="cd980-118">When the Security Configuration Engine starts, it checks the registry and loads all registered attachment engine DLLs.</span></span> <span data-ttu-id="cd980-119">Anschließend werden Dienst spezifische Konfigurations-und Analyseanforderungen an die entsprechende Anlage-Engine weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="cd980-119">It then passes service-specific configuration and analysis requests to the appropriate attachment engine.</span></span> <span data-ttu-id="cd980-120">Standard Konfigurations-und Analyseanforderungen, die nicht Dienst spezifisch sind, werden von der Sicherheitskonfigurations-Engine verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="cd980-120">Standard configuration and analysis requests, those that are not service-specific, are handled by the Security Configuration Engine.</span></span>

 

 



