---
title: Modelländerungen im IME-Modus
description: Das IME-Modusmodell wurde von "Pro Benutzer" in "Pro Thread" geändert.
ms.assetid: C9717AF2-7055-47CA-8F8F-BC0F483B2259
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30404b1a386c4346e7d8900481d8c5198972cdbe
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443247"
---
# <a name="ime-mode-model-changed-from-per-user-to-per-thread"></a><span data-ttu-id="165fc-103">Das IME-Modusmodell wurde von "Pro Benutzer" in "Pro Thread" geändert.</span><span class="sxs-lookup"><span data-stu-id="165fc-103">IME mode model changed from per-user to per-thread</span></span>

## <a name="platforms"></a><span data-ttu-id="165fc-104">Plattformen</span><span class="sxs-lookup"><span data-stu-id="165fc-104">Platforms</span></span>

<dl> <span data-ttu-id="165fc-105">Clients – Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="165fc-105">Clients - Windows 8.1</span></span>  
<span data-ttu-id="165fc-106">Server – Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="165fc-106">Servers - Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="165fc-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="165fc-107">Description</span></span>

<span data-ttu-id="165fc-108">In Windows 8 basierten der IME-Konvertierungsmodus und der IME-Satzmodus auf dem Benutzerkontext, und das Ändern des Modus einer Anwendung hat sich auf alle anderen Anwendungen ausdrungen.</span><span class="sxs-lookup"><span data-stu-id="165fc-108">In Windows 8, the IME Conversion Mode and IME Sentence Mode were based on the User context, and changing the mode of an application affected all other applications.</span></span> <span data-ttu-id="165fc-109">Dieses Verhalten kann mithilfe der Einstellung "Let me set a different input method for each app window" im Abschnitt "Erweiterte Einstellungen" der Sprachsteuerung deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="165fc-109">This behavior could be disabled by using the "Let me set a different input method for each app window" setting in the advanced settings section of the language control panel.</span></span>

<span data-ttu-id="165fc-110">Zur Verbesserung der Kompatibilität werden die Modi in Windows 8.1 in einem Eingabekontext gespeichert, unabhängig davon, wie das Steuerelement "Let me set a different input method for each app window" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="165fc-110">In order to improve compatibility, in Windows 8.1 the modes are stored in an Input context regardless of how the "Let me set a different input method for each app window" control is set.</span></span> <span data-ttu-id="165fc-111">In Windows 8.1 die Einstellung "Let me set a different input method for each app window" (Lass mich eine andere Eingabemethode für jedes App-Fenster festlegen) nur die Auswahl der Eingabemethode selbst.</span><span class="sxs-lookup"><span data-stu-id="165fc-111">In Windows 8.1, the "Let me set a different input method for each app window" setting affects only the selection of the input method itself.</span></span>

<span data-ttu-id="165fc-112">Beim Starten der Anwendung wird der IME-Modus auf die folgenden Standardwerte festgelegt:</span><span class="sxs-lookup"><span data-stu-id="165fc-112">At application start up, the IME mode is set to the following defaults:</span></span>



| &nbsp;   | <span data-ttu-id="165fc-113">Softwareeingabebereich</span><span class="sxs-lookup"><span data-stu-id="165fc-113">Software input panel</span></span> | <span data-ttu-id="165fc-114">Hardwaretastatur</span><span class="sxs-lookup"><span data-stu-id="165fc-114">Hardware keyboard</span></span> |
|----------|----------------------|-------------------|
| <span data-ttu-id="165fc-115">KOR, JPN</span><span class="sxs-lookup"><span data-stu-id="165fc-115">KOR, JPN</span></span> | <span data-ttu-id="165fc-116">Ein</span><span class="sxs-lookup"><span data-stu-id="165fc-116">On</span></span>                   | <span data-ttu-id="165fc-117">Aus</span><span class="sxs-lookup"><span data-stu-id="165fc-117">Off</span></span>               |
| <span data-ttu-id="165fc-118">CHS,CHT</span><span class="sxs-lookup"><span data-stu-id="165fc-118">CHS,CHT</span></span>  | <span data-ttu-id="165fc-119">Ein</span><span class="sxs-lookup"><span data-stu-id="165fc-119">On</span></span>                   | <span data-ttu-id="165fc-120">Ein</span><span class="sxs-lookup"><span data-stu-id="165fc-120">On</span></span>                |



 

## <a name="manifestations"></a><span data-ttu-id="165fc-121">Manifestationen</span><span class="sxs-lookup"><span data-stu-id="165fc-121">Manifestations</span></span>

<span data-ttu-id="165fc-122">Wenn ein Benutzer den IME-Modus für eine Anwendung ändert, wirkt sich die Änderung nicht auf andere Anwendungen aus.</span><span class="sxs-lookup"><span data-stu-id="165fc-122">When a user changes the IME mode on an application, the change doesn’t affect other applications.</span></span>

## <a name="resources"></a><span data-ttu-id="165fc-123">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="165fc-123">Resources</span></span>

-   [<span data-ttu-id="165fc-124">Werte des IME-Konvertierungsmodus</span><span class="sxs-lookup"><span data-stu-id="165fc-124">IME Conversion Mode Values</span></span>](../intl/ime-conversion-mode-values.md)
-   [<span data-ttu-id="165fc-125">IME-Satzmoduswerte</span><span class="sxs-lookup"><span data-stu-id="165fc-125">IME Sentence Mode Values</span></span>](../intl/ime-sentence-mode-values.md)

 

 