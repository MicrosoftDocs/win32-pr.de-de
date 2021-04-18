---
description: Im folgenden Thema wird beschrieben, wie die API der Windows as a Service (WAAS) Assessment Platform funktioniert.
ms.assetid: B107AAF3-4248-40EF-ABD2-C5B31602AEF7
title: Informationen zur WAAS-Bewertungsplattform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb96dd27fdc5b8838f2e2a26e74f0046eda8f20b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351729"
---
# <a name="about-the-waas-assessment-platform"></a><span data-ttu-id="569bb-103">Informationen zur WAAS-Bewertungsplattform</span><span class="sxs-lookup"><span data-stu-id="569bb-103">About the WaaS Assessment Platform</span></span>

<span data-ttu-id="569bb-104">Im folgenden Thema wird beschrieben, wie die API der Windows as a Service (WAAS) Assessment Platform funktioniert.</span><span class="sxs-lookup"><span data-stu-id="569bb-104">The following topic describes how the Windows as a Service (WaaS) Assessment Platform API works.</span></span>

<span data-ttu-id="569bb-105">Die WAAS-Bewertungs-API bietet dem Aufrufer die folgenden Informationen:</span><span class="sxs-lookup"><span data-stu-id="569bb-105">The WaaS Assessment API offers the caller the following information:</span></span>

-   <span data-ttu-id="569bb-106">Wenn ein Gerät auf den neuesten Microsoft-Updates basiert.</span><span class="sxs-lookup"><span data-stu-id="569bb-106">If a device is on the latest Microsoft updates.</span></span>
-   <span data-ttu-id="569bb-107">Gibt an, ob das Gerät das Ende des Supports erreicht hat.</span><span class="sxs-lookup"><span data-stu-id="569bb-107">Whether the device has reached end of support.</span></span>
-   <span data-ttu-id="569bb-108">Die Releasezeiten für die neuesten anwendbaren Updates für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="569bb-108">The release times for the latest applicable updates for the device.</span></span>
-   <span data-ttu-id="569bb-109">Eine Einschätzung, warum ein Gerät nicht auf dem neuesten Stand ist und welche möglichen Auswirkungen es auf das Gerät haben kann.</span><span class="sxs-lookup"><span data-stu-id="569bb-109">An assessment of why a device is not up-to-date and the potential impact it may have on the device.</span></span>

<span data-ttu-id="569bb-110">Die WAAS Assessment Platform verwendet das com-API-Modell und wird automatisch mindestens einmal pro Tag ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="569bb-110">The WaaS Assessment Platform uses the COM API model and runs automatically at least once a day.</span></span> <span data-ttu-id="569bb-111">Dieser Cycle fängt die anwendbaren Releaseinformationen ab.</span><span class="sxs-lookup"><span data-stu-id="569bb-111">This cycle catches applicable release information.</span></span> <span data-ttu-id="569bb-112">Im zwischengespeicherten Zeitraum werden für die zwischengespeicherten Releaseinformationen Bewertungen durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="569bb-112">During the cached period, assessments are made against the cached release information.</span></span> <span data-ttu-id="569bb-113">Wenn ein aufrufen außerhalb des Cache Ablauf Fensters erfolgt, werden ein neuer Rückruf und eine Bewertung durchgeführt, zwischengespeichert und zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="569bb-113">If a call is made outside of the cache expiration window, a fresh call and assessment is made, cached, and returned.</span></span> <span data-ttu-id="569bb-114">Wenn ein-Befehl durchgeführt wird, kontaktiert der WAAS-Bewertungs Client den WAAS-Bewertungs Dienst mit den Attributen des Geräts und empfängt ein auf das Gerät anwendbares Dossier von Informationen.</span><span class="sxs-lookup"><span data-stu-id="569bb-114">When a call is made, the WaaS Assessment Client contacts the WaaS Assessment Service with the device's attributes, and receives back a dossier of information applicable to the device.</span></span> <span data-ttu-id="569bb-115">Der Client verwendet diese Informationen dann anhand der Informationen, die er über das Gerät zum Durchführen der Bewertung sammelt.</span><span class="sxs-lookup"><span data-stu-id="569bb-115">The client then uses this information against the information it gathers about the device to perform the assessment.</span></span>

> [!NOTE]
> <span data-ttu-id="569bb-116">Der Code muss über Administratorrechte verfügen, um die WAAS-Bewertungs-API aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="569bb-116">Your code must have administrator privileges to call the Waas Assessment API.</span></span> <span data-ttu-id="569bb-117">Weitere Informationen zum Entwickeln von Anwendungen, für die Administratorrechte erforderlich sind, finden Sie in [diesem Artikel](../secauthz/developing-applications-that-require-administrator-privilege.md).</span><span class="sxs-lookup"><span data-stu-id="569bb-117">For more details about developing applications that require administrator privileges, see [this article](../secauthz/developing-applications-that-require-administrator-privilege.md).</span></span>

 
