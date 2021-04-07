---
description: Stellt Informationen zu einem Experiment (Erfassung) dar.
MS-HAID: vspixengine.Experiment
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Experiment Struktur
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 632F1F92-3E32-4B0A-8E38-2613694C267F
api_name:
- Experiment
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e932d2f2b60a72ca167f3f6edd7f4ddae9b68710
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746441"
---
# <a name="span-idvspixengineexperimentspanexperiment-structure"></a><span data-ttu-id="5ca38-103"><span id="vspixengine.experiment"></span>Experiment Struktur</span><span class="sxs-lookup"><span data-stu-id="5ca38-103"><span id="vspixengine.experiment"></span>Experiment structure</span></span>

<span data-ttu-id="5ca38-104">Stellt Informationen zu einem Experiment (Erfassung) dar.</span><span class="sxs-lookup"><span data-stu-id="5ca38-104">Represents information about an experiment (capture).</span></span>

## <a name="syntax"></a><span data-ttu-id="5ca38-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ca38-105">Syntax</span></span>


```C++
} Experiment;
```

## <a name="members"></a><span data-ttu-id="5ca38-106">Member</span><span class="sxs-lookup"><span data-stu-id="5ca38-106">Members</span></span>

<span data-ttu-id="5ca38-107">**ProcessID**</span><span class="sxs-lookup"><span data-stu-id="5ca38-107">**processId**</span></span>  
<span data-ttu-id="5ca38-108">Die zugeordnete Prozess-ID.</span><span class="sxs-lookup"><span data-stu-id="5ca38-108">The associated process ID.</span></span>

<span data-ttu-id="5ca38-109">**applicationName**</span><span class="sxs-lookup"><span data-stu-id="5ca38-109">**applicationName**</span></span>  
<span data-ttu-id="5ca38-110">Eine com-Zeichenfolge mit dem Namen der Anwendung, für die das Experiment ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5ca38-110">A COM string containing the name of the application to run the experiment on.</span></span>

<span data-ttu-id="5ca38-111">**commandLineArguments**</span><span class="sxs-lookup"><span data-stu-id="5ca38-111">**commandLineArguments**</span></span>  
<span data-ttu-id="5ca38-112">Eine com-Zeichenfolge, die die Befehlszeilenargumente enthält.</span><span class="sxs-lookup"><span data-stu-id="5ca38-112">A COM string containing the command line arguments.</span></span>

<span data-ttu-id="5ca38-113">**workingDirectory**</span><span class="sxs-lookup"><span data-stu-id="5ca38-113">**workingDirectory**</span></span>  
<span data-ttu-id="5ca38-114">Eine com-Zeichenfolge, die den Pfad des Arbeitsverzeichnisses enthält.</span><span class="sxs-lookup"><span data-stu-id="5ca38-114">A COM string containing the path of the working directory.</span></span>

<span data-ttu-id="5ca38-115">**temppixrunfile**</span><span class="sxs-lookup"><span data-stu-id="5ca38-115">**tempPixRunFile**</span></span>  
<span data-ttu-id="5ca38-116">Eine com-Zeichenfolge, die den filePath der zum Ausführen des Experiments verwendeten temporären Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="5ca38-116">A COM string containing the filepath of the temporary file used to perform the experiment.</span></span>

<span data-ttu-id="5ca38-117">**Startoption**</span><span class="sxs-lookup"><span data-stu-id="5ca38-117">**startOption**</span></span>  
<span data-ttu-id="5ca38-118">Die dem Experiment zugeordnete Startoption.</span><span class="sxs-lookup"><span data-stu-id="5ca38-118">The start option associated with the experiment.</span></span>

<span data-ttu-id="5ca38-119">**experimentstyp**</span><span class="sxs-lookup"><span data-stu-id="5ca38-119">**experimentType**</span></span>  
<span data-ttu-id="5ca38-120">Die Art des Experiments (Erfassung).</span><span class="sxs-lookup"><span data-stu-id="5ca38-120">The kind of experiment (capture).</span></span>

<span data-ttu-id="5ca38-121">**uilocale**</span><span class="sxs-lookup"><span data-stu-id="5ca38-121">**uiLocale**</span></span>  
<span data-ttu-id="5ca38-122">Die ID des Gebiets Schemas, das während der Überlagerung (Erfassung) für UI-Überlagerungs Elemente verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5ca38-122">The ID of the locale used for UI overlay elements during the experiement (capture).</span></span> <span data-ttu-id="5ca38-123">Diese wird vom Host (z. b. Visual Studio Grafikdiagnose) an die Aufzeichnungs-Engine übermittelt.</span><span class="sxs-lookup"><span data-stu-id="5ca38-123">This is passed from the host (such as Visual Studio Graphics Diagnostics) to the capture engine.</span></span>

<span data-ttu-id="5ca38-124">**registryRoot**</span><span class="sxs-lookup"><span data-stu-id="5ca38-124">**registryRoot**</span></span>  
<span data-ttu-id="5ca38-125">Eine com-Zeichenfolge, die den Registrierungs Stamm enthält.</span><span class="sxs-lookup"><span data-stu-id="5ca38-125">A COM string containing the registry root.</span></span> <span data-ttu-id="5ca38-126">Diese wird vom Host (z. b. Visual Studio Grafikdiagnose) an die Aufzeichnungs-Engine übermittelt.</span><span class="sxs-lookup"><span data-stu-id="5ca38-126">This is passed from the host (such as Visual Studio Graphics Diagnostics) to the capture engine.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ca38-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ca38-127">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="5ca38-128">Header</span><span class="sxs-lookup"><span data-stu-id="5ca38-128">Header</span></span></p></td><td><span data-ttu-id="5ca38-129">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="5ca38-129">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



