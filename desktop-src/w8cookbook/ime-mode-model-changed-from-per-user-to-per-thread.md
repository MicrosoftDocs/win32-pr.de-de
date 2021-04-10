---
title: IME-modusmodelländerungen
description: IME-modusmodell von pro Benutzer in Thread pro Thread geändert
ms.assetid: C9717AF2-7055-47CA-8F8F-BC0F483B2259
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 781c322949f17d4d3313b6a9b7b5eff9b1e83b06
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316155"
---
# <a name="ime-mode-model-changed-from-per-user-to-per-thread"></a><span data-ttu-id="5ea02-103">IME-modusmodell von pro Benutzer in Thread pro Thread geändert</span><span class="sxs-lookup"><span data-stu-id="5ea02-103">IME mode model changed from per-user to per-thread</span></span>

## <a name="platforms"></a><span data-ttu-id="5ea02-104">Plattformen</span><span class="sxs-lookup"><span data-stu-id="5ea02-104">Platforms</span></span>

<dl> <span data-ttu-id="5ea02-105">Clients-Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="5ea02-105">Clients - Windows 8.1</span></span>  
<span data-ttu-id="5ea02-106">Server-Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="5ea02-106">Servers - Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="5ea02-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5ea02-107">Description</span></span>

<span data-ttu-id="5ea02-108">In Windows 8 basieren der IME-Konvertierungsmodus und der IME-Satz Modus auf dem Benutzer Kontext, und das Ändern des Modus einer Anwendung betraf alle anderen Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="5ea02-108">In Windows 8, the IME Conversion Mode and IME Sentence Mode were based on the User context, and changing the mode of an application affected all other applications.</span></span> <span data-ttu-id="5ea02-109">Dieses Verhalten kann deaktiviert werden, indem Sie im Abschnitt "Erweiterte Einstellungen" der sprach Systemsteuerung die Einstellung "eine andere Eingabemethode für die einzelnen App-Fenster festlegen" verwenden.</span><span class="sxs-lookup"><span data-stu-id="5ea02-109">This behavior could be disabled by using the "Let me set a different input method for each app window" setting in the advanced settings section of the language control panel.</span></span>

<span data-ttu-id="5ea02-110">Um die Kompatibilität zu verbessern, werden die Modi in Windows 8.1 in einem Eingabe Kontext gespeichert, unabhängig davon, wie das Steuerelement "legen Sie eine andere Eingabemethode für jedes App-Fenster festlegen" festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="5ea02-110">In order to improve compatibility, in Windows 8.1 the modes are stored in an Input context regardless of how the "Let me set a different input method for each app window" control is set.</span></span> <span data-ttu-id="5ea02-111">In Windows 8.1 wirkt sich die Einstellung "eine andere Eingabemethode für jedes App-Fenster festlegen" nur auf die Auswahl der Eingabemethode selbst aus.</span><span class="sxs-lookup"><span data-stu-id="5ea02-111">In Windows 8.1, the "Let me set a different input method for each app window" setting affects only the selection of the input method itself.</span></span>

<span data-ttu-id="5ea02-112">Beim Starten der Anwendung wird der IME-Modus auf die folgenden Standardwerte festgelegt:</span><span class="sxs-lookup"><span data-stu-id="5ea02-112">At application start up, the IME mode is set to the following defaults:</span></span>



|          | <span data-ttu-id="5ea02-113">Software Eingabebereich</span><span class="sxs-lookup"><span data-stu-id="5ea02-113">Software input panel</span></span> | <span data-ttu-id="5ea02-114">Hardware Tastatur</span><span class="sxs-lookup"><span data-stu-id="5ea02-114">Hardware keyboard</span></span> |
|----------|----------------------|-------------------|
| <span data-ttu-id="5ea02-115">Kor, jpn</span><span class="sxs-lookup"><span data-stu-id="5ea02-115">KOR, JPN</span></span> | <span data-ttu-id="5ea02-116">Ein</span><span class="sxs-lookup"><span data-stu-id="5ea02-116">On</span></span>                   | <span data-ttu-id="5ea02-117">Aus</span><span class="sxs-lookup"><span data-stu-id="5ea02-117">Off</span></span>               |
| <span data-ttu-id="5ea02-118">CHS, cht</span><span class="sxs-lookup"><span data-stu-id="5ea02-118">CHS,CHT</span></span>  | <span data-ttu-id="5ea02-119">Ein</span><span class="sxs-lookup"><span data-stu-id="5ea02-119">On</span></span>                   | <span data-ttu-id="5ea02-120">Ein</span><span class="sxs-lookup"><span data-stu-id="5ea02-120">On</span></span>                |



 

## <a name="manifestations"></a><span data-ttu-id="5ea02-121">Kundgebungen</span><span class="sxs-lookup"><span data-stu-id="5ea02-121">Manifestations</span></span>

<span data-ttu-id="5ea02-122">Wenn ein Benutzer den IME-Modus für eine Anwendung ändert, wirkt sich die Änderung nicht auf andere Anwendungen aus.</span><span class="sxs-lookup"><span data-stu-id="5ea02-122">When a user changes the IME mode on an application, the change doesn’t affect other applications.</span></span>

## <a name="resources"></a><span data-ttu-id="5ea02-123">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5ea02-123">Resources</span></span>

-   [<span data-ttu-id="5ea02-124">Werte des IME-Konvertierungsmodus</span><span class="sxs-lookup"><span data-stu-id="5ea02-124">IME Conversion Mode Values</span></span>](../intl/ime-conversion-mode-values.md)
-   [<span data-ttu-id="5ea02-125">Werte für den IME-Satzmodus</span><span class="sxs-lookup"><span data-stu-id="5ea02-125">IME Sentence Mode Values</span></span>](../intl/ime-sentence-mode-values.md)

 

 