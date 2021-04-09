---
description: HKCU- \\ Systemsteuerung \\ International.
ms.assetid: e2925d92-19df-42e5-9893-2820f437d3a5
title: Addhijridate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22a1c4a721af18e0a8994efdd7641581aa01c133
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860808"
---
# <a name="addhijridate"></a><span data-ttu-id="5b98f-103">Addhijridate</span><span class="sxs-lookup"><span data-stu-id="5b98f-103">AddHijriDate</span></span>

<span data-ttu-id="5b98f-104">**HKCU- \\ Systemsteuerung \\ International**</span><span class="sxs-lookup"><span data-stu-id="5b98f-104">**HKCU\\Control Panel\\International**</span></span>



| <span data-ttu-id="5b98f-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5b98f-105">Data type</span></span> | <span data-ttu-id="5b98f-106">Range</span><span class="sxs-lookup"><span data-stu-id="5b98f-106">Range</span></span>                      | <span data-ttu-id="5b98f-107">Standardwert</span><span class="sxs-lookup"><span data-stu-id="5b98f-107">Default value</span></span> |
|-----------|----------------------------|---------------|
| <span data-ttu-id="5b98f-108">REG- \_ SZ</span><span class="sxs-lookup"><span data-stu-id="5b98f-108">REG\_SZ</span></span>   | <span data-ttu-id="5b98f-109">*Ein gültiger Anpassungswert*</span><span class="sxs-lookup"><span data-stu-id="5b98f-109">*A valid adjustment value*</span></span> | <span data-ttu-id="5b98f-110">(Keine)</span><span class="sxs-lookup"><span data-stu-id="5b98f-110">(None)</span></span>        |



 

## <a name="description"></a><span data-ttu-id="5b98f-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5b98f-111">Description</span></span>

<span data-ttu-id="5b98f-112">Gibt Anpassungen für das Datum innerhalb des Hijri-Kalenders an.</span><span class="sxs-lookup"><span data-stu-id="5b98f-112">Specifies adjustments to the date within the Hijri calendar.</span></span>

<span data-ttu-id="5b98f-113">Der Hijri-Kalender ist ein Mondkalender, der in der islamischen Welt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5b98f-113">The Hijri calendar is a lunar calendar used in the Islamic world.</span></span> <span data-ttu-id="5b98f-114">Die Monate beginnen und enden gemäß einem Dekret, das auf der Beobachtung des neuen Mond basiert.</span><span class="sxs-lookup"><span data-stu-id="5b98f-114">The months begin and end according to a decree that is based on the observation of the new moon.</span></span> <span data-ttu-id="5b98f-115">Es ist schwierig, den Beginn und die Enden der Monate genau vorherzusagen, und es gibt regionale Variationen, sodass zwischen 0 und zwei Tagen eine Anpassung an den Kalender erfolgt.</span><span class="sxs-lookup"><span data-stu-id="5b98f-115">It is difficult to accurately predict the beginnings and endings of the months, and there are regional variations, so an adjustment of between zero and two days is made to the calendar.</span></span>

<span data-ttu-id="5b98f-116">Der Registrierungs Wert **addhijridate** speichert diesen Anpassungswert wie folgt.</span><span class="sxs-lookup"><span data-stu-id="5b98f-116">The **AddHijriDate** registry value stores this adjustment value as follows.</span></span>



| <span data-ttu-id="5b98f-117">Wert</span><span class="sxs-lookup"><span data-stu-id="5b98f-117">Value</span></span>          | <span data-ttu-id="5b98f-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="5b98f-118">Meaning</span></span>                                                                                                                                                                                                                               |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b98f-119">Addhijridate-2</span><span class="sxs-lookup"><span data-stu-id="5b98f-119">AddHijriDate-2</span></span> | <span data-ttu-id="5b98f-120">Subtrahieren Sie zwei Tage.</span><span class="sxs-lookup"><span data-stu-id="5b98f-120">Subtract two days.</span></span>                                                                                                                                                                                                                    |
| <span data-ttu-id="5b98f-121">Addhijridate</span><span class="sxs-lookup"><span data-stu-id="5b98f-121">AddHijriDate</span></span>   | <span data-ttu-id="5b98f-122">Subtrahieren Sie einen Tag.</span><span class="sxs-lookup"><span data-stu-id="5b98f-122">Subtract one day.</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="5b98f-123">(leer)</span><span class="sxs-lookup"><span data-stu-id="5b98f-123">(blank)</span></span>        | <span data-ttu-id="5b98f-124">Es ist keine Anpassung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5b98f-124">No adjustment is necessary.</span></span> <span data-ttu-id="5b98f-125">(Wenn das Datum nicht angepasst wurde, wird dieser Eintrag nicht in der Registrierung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5b98f-125">(If the date has not been adjusted, this entry does not appear in the registry.</span></span> <span data-ttu-id="5b98f-126">Wenn das Datum angepasst und dann auf den ursprünglichen Wert wieder hergestellt wurde, wird dieser Eintrag in der Registrierung ohne Wert angezeigt.)</span><span class="sxs-lookup"><span data-stu-id="5b98f-126">If the date has been adjusted and then restored to its original value, this entry appears in the registry with no value.)</span></span> |
| <span data-ttu-id="5b98f-127">Addhijridate + 1</span><span class="sxs-lookup"><span data-stu-id="5b98f-127">AddHijriDate+1</span></span> | <span data-ttu-id="5b98f-128">Fügen Sie einen Tag hinzu.</span><span class="sxs-lookup"><span data-stu-id="5b98f-128">Add one day.</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="5b98f-129">Addhijridate + 2</span><span class="sxs-lookup"><span data-stu-id="5b98f-129">AddHijriDate+2</span></span> | <span data-ttu-id="5b98f-130">Fügen Sie zwei Tage hinzu.</span><span class="sxs-lookup"><span data-stu-id="5b98f-130">Add two days.</span></span>                                                                                                                                                                                                                         |



 

<span data-ttu-id="5b98f-131">Dieser Eintrag ist nicht standardmäßig in der Registrierung vorhanden.</span><span class="sxs-lookup"><span data-stu-id="5b98f-131">This entry does not exist in the registry by default.</span></span> <span data-ttu-id="5b98f-132">Sie können ihn mithilfe des Registrierungs-Editors Regedit.exe oder mithilfe der unten beschriebenen Änderungs Methode hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5b98f-132">You can add it by using the registry editor Regedit.exe or by using the change method described below.</span></span>

## <a name="change-method"></a><span data-ttu-id="5b98f-133">Methode ändern</span><span class="sxs-lookup"><span data-stu-id="5b98f-133">Change Method</span></span>

<span data-ttu-id="5b98f-134">Um den Wert dieses Eintrags zu ändern oder ihn der Registrierung hinzuzufügen, installieren Sie zunächst die Dateien für das komplexe Skript und die Sprachen von rechts nach links.</span><span class="sxs-lookup"><span data-stu-id="5b98f-134">To change the value of this entry, or to add it to the registry, first install the files for complex script and right-to-left languages.</span></span> <span data-ttu-id="5b98f-135">Klicken Sie in der Systemsteuerung auf Regions **-und Sprachoptionen, und** klicken Sie dann auf die Registerkarte **Sprachen** . Aktivieren Sie unter **zusätzliche Sprachunterstützung** das Kontrollkästchen zum **Installieren von Dateien für komplexe Skripts und Sprachen von rechts nach links (einschließlich Thai)**.</span><span class="sxs-lookup"><span data-stu-id="5b98f-135">In Control Panel, click **Regional and Language Options**, then click the **Languages** tab. Under **Supplemental language support**, select the checkbox to **Install files for complex script and right-to-left languages (including Thai)**.</span></span> <span data-ttu-id="5b98f-136">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b98f-136">Click **OK**.</span></span>

<span data-ttu-id="5b98f-137">Um den Wert dieses Eintrags zu ändern oder ihn der Registrierung hinzuzufügen, klicken Sie in der Systemsteuerung auf Regions **-und Sprachoptionen**.</span><span class="sxs-lookup"><span data-stu-id="5b98f-137">To change the value of this entry, or to add it to the registry, from Control Panel, click **Regional and Language Options**.</span></span> <span data-ttu-id="5b98f-138">Wählen Sie im Feld **Standards und Formate** ein Gebiets Schema aus, das den Hijri-Kalender verwendet.</span><span class="sxs-lookup"><span data-stu-id="5b98f-138">In the **Standards and Formats** field, select a locale that uses the Hijri calendar.</span></span> <span data-ttu-id="5b98f-139">Klicken Sie auf die Schaltfläche **Anpassen** und dann auf die Registerkarte **Datum** . Wählen Sie in der Dropdown Liste **Hijri-Datum anpassen an:** den entsprechenden Wert aus.</span><span class="sxs-lookup"><span data-stu-id="5b98f-139">Click the **Customize** button, then click the **Date** tab. In the **Adjust Hijri date to:** drop-down list, select the appropriate value.</span></span> <span data-ttu-id="5b98f-140">Klicken Sie auf **OK** und dann erneut auf **OK** .</span><span class="sxs-lookup"><span data-stu-id="5b98f-140">Click **OK**, then click **OK** again.</span></span>

## <a name="activation-method"></a><span data-ttu-id="5b98f-141">Aktivierungsmethoden</span><span class="sxs-lookup"><span data-stu-id="5b98f-141">Activation Method</span></span>

<span data-ttu-id="5b98f-142">Änderungen an diesem Eintrag, die über die Systemsteuerung vorgenommen werden, treten sofort in Kraft.</span><span class="sxs-lookup"><span data-stu-id="5b98f-142">Changes to this entry made through Control Panel take effect immediately.</span></span>

 

 



