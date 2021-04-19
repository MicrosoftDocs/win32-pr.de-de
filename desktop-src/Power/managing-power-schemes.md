---
description: Energie Schema Verwaltung
ms.assetid: b79e7b64-be56-4165-af59-a8251284d029
title: Energie Schema Verwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 867d7509e9a04e948818ff7a3a13638a5c9933b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353458"
---
# <a name="power-scheme-management"></a><span data-ttu-id="35c23-103">Energie Schema Verwaltung</span><span class="sxs-lookup"><span data-stu-id="35c23-103">Power Scheme Management</span></span>

<span data-ttu-id="35c23-104">Jedes Energie Schema wird durch eine **GUID** eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="35c23-104">Each power scheme is uniquely identified by a **GUID**.</span></span> <span data-ttu-id="35c23-105">Verwenden Sie zum Auflisten aller verfügbaren Energie Schemas die [**powerenumerate**](/windows/desktop/api/PowrProf/nf-powrprof-powerenumerate) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="35c23-105">To enumerate all available power schemes, use the [**PowerEnumerate**](/windows/desktop/api/PowrProf/nf-powrprof-powerenumerate) function.</span></span> <span data-ttu-id="35c23-106">**Powerenumerate** kann auch verwendet werden, um alle Energie Einstellungen für ein angegebenes Schema abzurufen.</span><span class="sxs-lookup"><span data-stu-id="35c23-106">**PowerEnumerate** can also be used to retrieve all of the power settings for a specified scheme.</span></span>

<span data-ttu-id="35c23-107">Das Energie Schema, das zurzeit auf dem System verwendet wird, wird als aktives Energie Schema oder Plan bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="35c23-107">The power scheme that is currently in use on the system is called the active power scheme or plan.</span></span> <span data-ttu-id="35c23-108">Um die **GUID** des aktiven Plans abzurufen, rufen Sie die [**powergetactivescheme**](/windows/desktop/api/Powersetting/nf-powersetting-powergetactivescheme) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="35c23-108">To retrieve the **GUID** of the active plan, call the [**PowerGetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powergetactivescheme) function.</span></span> <span data-ttu-id="35c23-109">Um den aktiven Energie Sparplan zu ändern, müssen Sie die Funktion " [**powersettactivescheme**](/windows/desktop/api/Powersetting/nf-powersetting-powersetactivescheme) " aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="35c23-109">To change the active power plan, call the [**PowerSetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powersetactivescheme) function.</span></span>

<span data-ttu-id="35c23-110">Um ein Energie Schema zu erstellen, müssen Sie zuerst ein vorhandenes Schema duplizieren, indem Sie die [**powerduplicatescheme**](/windows/desktop/api/PowrProf/nf-powrprof-powerduplicatescheme) -Funktion verwenden und die **GUID** des Schemas angeben, auf dem das neue Schema basieren soll.</span><span class="sxs-lookup"><span data-stu-id="35c23-110">To create a power scheme, you need to first duplicate an existing scheme by using the [**PowerDuplicateScheme**](/windows/desktop/api/PowrProf/nf-powrprof-powerduplicatescheme) function, specifying the **GUID** of the scheme you wish to base your new scheme upon.</span></span> <span data-ttu-id="35c23-111">Sie sollten eines der integrierten Schemas kopieren und die Energie Einstellungen entsprechend Ihren Anforderungen ändern.</span><span class="sxs-lookup"><span data-stu-id="35c23-111">You should copy one of the built-in schemes and modify the power settings to your needs.</span></span> <span data-ttu-id="35c23-112">Beachten Sie, dass durch das Erstellen eines Energie Sparplans der aktive Energie Sparplan nicht automatisch aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="35c23-112">Note that creating a power plan does not automatically update the active power plan.</span></span> <span data-ttu-id="35c23-113">Zum Aktualisieren des aktiven Energie Sparplans müssen Sie immer [**Power-tactivescheme**](/windows/desktop/api/Powersetting/nf-powersetting-powersetactivescheme) aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="35c23-113">You must always call [**PowerSetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powersetactivescheme) to update the active power plan.</span></span> <span data-ttu-id="35c23-114">Vorhandene Energie Sparpläne können geändert und dann auf die gleiche Weise angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="35c23-114">Existing power plans can be modified and then applied in the same manner.</span></span>

<span data-ttu-id="35c23-115">Um einen Energie Sparplan zu entfernen, müssen Sie die [**powerdeletescheme**](/windows/desktop/api/PowrProf/nf-powrprof-powerdeletescheme) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="35c23-115">To remove a power plan, call the [**PowerDeleteScheme**](/windows/desktop/api/PowrProf/nf-powrprof-powerdeletescheme) function.</span></span>

> [!Note]  
> <span data-ttu-id="35c23-116">Rufen Sie die [**callntpowerinformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation) -Funktion auf, um zusätzliche Informationen zum Energiezustand des Systems abzurufen.</span><span class="sxs-lookup"><span data-stu-id="35c23-116">To retrieve additional information about the system power state, call the [**CallNtPowerInformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation) function.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="35c23-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="35c23-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35c23-118">Energie Schemas</span><span class="sxs-lookup"><span data-stu-id="35c23-118">Power Schemes</span></span>](power-schemes.md)
</dt> </dl>

 

 



