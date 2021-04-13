---
description: Das wsfromscript-Codebeispiel veranschaulicht die Abfrage von Windows Search von einem Microsoft Visual Basic-Skript mithilfe von Microsoft ActiveX Data Objects (ADO).
ms.assetid: 93ee63f2-ab05-478a-99d0-4f4d09c11506
title: Wsfromscript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 99f505872571eeea4c16c0edde5059eafd301ac7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342969"
---
# <a name="wsfromscript"></a><span data-ttu-id="32938-103">Wsfromscript</span><span class="sxs-lookup"><span data-stu-id="32938-103">WSFromScript</span></span>

<span data-ttu-id="32938-104">Das wsfromscript-Codebeispiel veranschaulicht die Abfrage von Windows Search von einem Microsoft Visual Basic-Skript mithilfe von Microsoft ActiveX Data Objects (ADO).</span><span class="sxs-lookup"><span data-stu-id="32938-104">The WSFromScript code sample demonstrates how to query Windows Search from a Microsoft Visual Basic script using Microsoft ActiveX Data Objects (ADO).</span></span>

<span data-ttu-id="32938-105">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="32938-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="32938-106">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="32938-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="32938-107">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="32938-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="32938-108">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="32938-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="32938-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="32938-109">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="32938-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="32938-110">Requirements</span></span>

| <span data-ttu-id="32938-111">Produkt</span><span class="sxs-lookup"><span data-stu-id="32938-111">Product</span></span>     | <span data-ttu-id="32938-112">Produktversion</span><span class="sxs-lookup"><span data-stu-id="32938-112">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="32938-113">Windows</span><span class="sxs-lookup"><span data-stu-id="32938-113">Windows</span></span>     | <span data-ttu-id="32938-114">Windows 7, 8.1 oder 10</span><span class="sxs-lookup"><span data-stu-id="32938-114">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="32938-115">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="32938-115">Windows SDK</span></span> | <span data-ttu-id="32938-116">7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="32938-116">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="32938-117">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="32938-117">Downloading the Sample</span></span>

<span data-ttu-id="32938-118">Dieses Beispiel ist im folgenden Speicherort verfügbar.</span><span class="sxs-lookup"><span data-stu-id="32938-118">This sample is available in the following location.</span></span>

| <span data-ttu-id="32938-119">Standort</span><span class="sxs-lookup"><span data-stu-id="32938-119">Location</span></span>      | <span data-ttu-id="32938-120">Pfad-URL</span><span class="sxs-lookup"><span data-stu-id="32938-120">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="32938-121">GitHub</span><span class="sxs-lookup"><span data-stu-id="32938-121">GitHub</span></span>  | [<span data-ttu-id="32938-122">Wsfromscript-Beispiel</span><span class="sxs-lookup"><span data-stu-id="32938-122">WSFromScript sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/WSFromScript)    |

> [!NOTE]  
> <span data-ttu-id="32938-123">Für alle Versionen von Windows, einschließlich Windows 7, empfiehlt es sich, die Beispiele direkt von GitHub für die aktuellste Version herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="32938-123">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="32938-124">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="32938-124">Building the Sample</span></span>

<span data-ttu-id="32938-125">So erstellen Sie das Beispiel über das Eingabe Aufforderungs Fenster:</span><span class="sxs-lookup"><span data-stu-id="32938-125">To build the sample from the Command Prompt window:</span></span>

1. <span data-ttu-id="32938-126">Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum Projektverzeichnis **queryeverything** .</span><span class="sxs-lookup"><span data-stu-id="32938-126">Open the Command Prompt window and navigate to the **QueryEverything** project directory.</span></span> <span data-ttu-id="32938-127">Der vollständige Standard Installationspfad des Windows 7 SDK lautet beispielsweise `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\WindowsSearch\WSFromScript` .</span><span class="sxs-lookup"><span data-stu-id="32938-127">For example, the full default installation path of the Windows 7 SDK is `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\WindowsSearch\WSFromScript`.</span></span>
2. <span data-ttu-id="32938-128">Geben Sie `cscript QueryEverything.vbs` ein.</span><span class="sxs-lookup"><span data-stu-id="32938-128">Enter `cscript QueryEverything.vbs`.</span></span>

## <a name="related-topics"></a><span data-ttu-id="32938-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="32938-129">Related topics</span></span>

### <a name="conceptual"></a><span data-ttu-id="32938-130">Konzept</span><span class="sxs-lookup"><span data-stu-id="32938-130">Conceptual</span></span>

<span data-ttu-id="32938-131">[**VBScript-Sprachreferenz**](/previous-versions/d1wf56tt(v=vs.71))</span><span class="sxs-lookup"><span data-stu-id="32938-131">[**VBScript Language Reference**](/previous-versions/d1wf56tt(v=vs.71))</span></span>

### <a name="other-samples"></a><span data-ttu-id="32938-132">Weitere Beispiele</span><span class="sxs-lookup"><span data-stu-id="32938-132">Other Samples</span></span>

[<span data-ttu-id="32938-133">Code Beispiele durchsuchen</span><span class="sxs-lookup"><span data-stu-id="32938-133">Search Code Samples</span></span>](-search-samples-ovw.md)
