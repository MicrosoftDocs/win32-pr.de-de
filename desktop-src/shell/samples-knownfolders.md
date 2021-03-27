---
description: Veranschaulicht, wie Sie den Pfad für alle bekannten Ordner auf dem aktuellen System definieren, registrieren, aufzählen und suchen.
title: Bekannte Ordner (Beispiel)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 49799A9E-BA86-4977-B5F3-590BE1E5FBF6
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8d3784e64986a338f6554534199852191bd06ca7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959996"
---
# <a name="known-folders-sample"></a><span data-ttu-id="b621b-103">Bekannte Ordner (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="b621b-103">Known Folders Sample</span></span>

<span data-ttu-id="b621b-104">Veranschaulicht, wie Sie den Pfad für alle bekannten Ordner auf dem aktuellen System definieren, registrieren, aufzählen und suchen.</span><span class="sxs-lookup"><span data-stu-id="b621b-104">Demonstrates how to define, register, enumerate and find the path for all known folders on the current system.</span></span>

<span data-ttu-id="b621b-105">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="b621b-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="b621b-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b621b-106">Description</span></span>](#description)
-   [<span data-ttu-id="b621b-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b621b-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="b621b-108">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="b621b-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="b621b-109">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="b621b-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="b621b-110">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="b621b-110">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="b621b-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b621b-111">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="b621b-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b621b-112">Description</span></span>

<span data-ttu-id="b621b-113">Dieses Beispiel enthält eine Registrierungsdatei, die veranschaulicht, wie ein bekannter Ordner registriert wird, indem einige allgemeine Registrierungsschlüssel und-Werte für Entwickler geschrieben werden, die den Registrierungs Zugriff bevorzugen.</span><span class="sxs-lookup"><span data-stu-id="b621b-113">This sample includes a registry file that demonstrates how to register a known folder by writing some common registry keys and values for developers who prefer registry access.</span></span>

## <a name="requirements"></a><span data-ttu-id="b621b-114">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="b621b-114">Requirements</span></span>



| <span data-ttu-id="b621b-115">Produkt</span><span class="sxs-lookup"><span data-stu-id="b621b-115">Product</span></span>                                | <span data-ttu-id="b621b-116">Minimale Produkt Version</span><span class="sxs-lookup"><span data-stu-id="b621b-116">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="b621b-117">Windows</span><span class="sxs-lookup"><span data-stu-id="b621b-117">Windows</span></span>                                | <span data-ttu-id="b621b-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b621b-118">Windows Vista</span></span>           |
| <span data-ttu-id="b621b-119">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="b621b-119">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="b621b-120">6.1</span><span class="sxs-lookup"><span data-stu-id="b621b-120">6.1</span></span>                     |



 

<span data-ttu-id="b621b-121">Weitere Anforderungen finden Sie in der im Beispiel enthaltenen Infodatei.</span><span class="sxs-lookup"><span data-stu-id="b621b-121">For additional requirements, see the Readme file included with the sample.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="b621b-122">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="b621b-122">Downloading the Sample</span></span>

| <span data-ttu-id="b621b-123">Standort</span><span class="sxs-lookup"><span data-stu-id="b621b-123">Location</span></span>      | <span data-ttu-id="b621b-124">Pfad-URL</span><span class="sxs-lookup"><span data-stu-id="b621b-124">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b621b-125">GitHub</span><span class="sxs-lookup"><span data-stu-id="b621b-125">GitHub</span></span>  | [<span data-ttu-id="b621b-126">KnownFolders-Beispiel</span><span class="sxs-lookup"><span data-stu-id="b621b-126">KnownFolders sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/knownfolders) |

## <a name="building-the-sample"></a><span data-ttu-id="b621b-127">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="b621b-127">Building the Sample</span></span>

<span data-ttu-id="b621b-128">Anweisungen zum Erstellen des Beispiels finden Sie in der im Beispiel enthaltenen Infodatei.</span><span class="sxs-lookup"><span data-stu-id="b621b-128">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="b621b-129">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="b621b-129">Running the Sample</span></span>

<span data-ttu-id="b621b-130">Anweisungen zum Erstellen des Beispiels finden Sie in der im Beispiel enthaltenen Infodatei.</span><span class="sxs-lookup"><span data-stu-id="b621b-130">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b621b-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b621b-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b621b-132">Bekannte Ordner</span><span class="sxs-lookup"><span data-stu-id="b621b-132">Known Folders</span></span>](known-folders.md)
</dt> </dl>

 

 



