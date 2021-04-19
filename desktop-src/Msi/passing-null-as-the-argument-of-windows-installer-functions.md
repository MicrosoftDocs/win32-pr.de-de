---
description: Windows Installer Funktionen, die Daten in einem vom Benutzer bereitgestellten –-Speicherort zurückgeben, dürfen nicht mit NULL als Wert für den Zeiger aufgerufen werden.
ms.assetid: f566c4a4-b90c-4d73-9d7f-f5b836630636
title: Übergeben von NULL an Windows Installer Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eb09ceb3982695792614a3c226af9ab276aa3a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348274"
---
# <a name="passing-null-as-the-argument-of-windows-installer-functions"></a><span data-ttu-id="505df-103">Übergeben von NULL als Argument Windows Installer Funktionen</span><span class="sxs-lookup"><span data-stu-id="505df-103">Passing null as the Argument of Windows Installer Functions</span></span>

<span data-ttu-id="505df-104">Windows Installer Funktionen, die Daten in einem vom Benutzer bereitgestellten –-Speicherort zurückgeben, dürfen nicht mit NULL als Wert für den Zeiger aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="505df-104">Windows Installer functions that return data in a user provided–memory location should not be called with null as the value for the pointer.</span></span> <span data-ttu-id="505df-105">Diese Funktionen geben eine Zeichenfolge oder Rückgabe Daten als ganzzahlige Zeiger zurück, geben jedoch inkonsistente Werte zurück, wenn NULL als Wert für das Output-Argument übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="505df-105">These functions return a string or return data as integer pointers, but return inconsistent values when passing null as the value for the output argument.</span></span>

<span data-ttu-id="505df-106">Übergeben Sie NULL nicht als Wert des Output-Arguments für eine der folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="505df-106">Do not pass Null as the value of the output argument for any of the following functions:</span></span>

[<span data-ttu-id="505df-107">**MsiGetProperty**</span><span class="sxs-lookup"><span data-stu-id="505df-107">**MsiGetProperty**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya)

[<span data-ttu-id="505df-108">**Msirecordgetstring**</span><span class="sxs-lookup"><span data-stu-id="505df-108">**MsiRecordGetString**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetstringa)

[<span data-ttu-id="505df-109">**Msiformatrecord**</span><span class="sxs-lookup"><span data-stu-id="505df-109">**MsiFormatRecord**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)

[<span data-ttu-id="505df-110">**Msigetsourcepath**</span><span class="sxs-lookup"><span data-stu-id="505df-110">**MsiGetSourcePath**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetsourcepatha)

[<span data-ttu-id="505df-111">**Msigettargetpath**</span><span class="sxs-lookup"><span data-stu-id="505df-111">**MsiGetTargetPath**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha)

[<span data-ttu-id="505df-112">**MsiGetFeatureState**</span><span class="sxs-lookup"><span data-stu-id="505df-112">**MsiGetFeatureState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)

[<span data-ttu-id="505df-113">**Msiviewgeterror**</span><span class="sxs-lookup"><span data-stu-id="505df-113">**MsiViewGetError**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora)

[<span data-ttu-id="505df-114">**Msisummaryinfogetproperty**</span><span class="sxs-lookup"><span data-stu-id="505df-114">**MsiSummaryInfoGetProperty**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya)

[<span data-ttu-id="505df-115">**Msievaluatecondition**</span><span class="sxs-lookup"><span data-stu-id="505df-115">**MsiEvaluateCondition**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona)

[<span data-ttu-id="505df-116">**Msigetfeaturecost**</span><span class="sxs-lookup"><span data-stu-id="505df-116">**MsiGetFeatureCost**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)

[<span data-ttu-id="505df-117">**MsiGetFeatureState**</span><span class="sxs-lookup"><span data-stu-id="505df-117">**MsiGetFeatureState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)

[<span data-ttu-id="505df-118">**MsiGetComponentState**</span><span class="sxs-lookup"><span data-stu-id="505df-118">**MsiGetComponentState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)

[<span data-ttu-id="505df-119">**Msigetfeaturecost**</span><span class="sxs-lookup"><span data-stu-id="505df-119">**MsiGetFeatureCost**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)

[<span data-ttu-id="505df-120">**Msigetfeaturevalidstates**</span><span class="sxs-lookup"><span data-stu-id="505df-120">**MsiGetFeatureValidStates**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa)

 

 



