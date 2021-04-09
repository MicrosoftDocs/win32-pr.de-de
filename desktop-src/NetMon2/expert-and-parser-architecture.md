---
description: Die folgende Abbildung zeigt die Beziehung zwischen Experten-und parseranwendungen und anderen Komponenten der Netzwerkmonitor Architektur.
ms.assetid: f943f0e6-5fdc-48f9-ba5d-5effdf8229f3
title: Architektur von Experten und Parsers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caa8477d97604acfb04686170ca6cb5cff8116a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128361"
---
# <a name="expert-and-parser-architecture"></a><span data-ttu-id="47feb-103">Architektur von Experten und Parsers</span><span class="sxs-lookup"><span data-stu-id="47feb-103">Expert and Parser Architecture</span></span>

<span data-ttu-id="47feb-104">Die folgende Abbildung zeigt die Beziehung zwischen [Experten](experts.md) -und [parseranwendungen](parsers.md) und anderen Komponenten der Netzwerkmonitor Architektur.</span><span class="sxs-lookup"><span data-stu-id="47feb-104">The following figure shows the relationship between [expert](experts.md) and [parser](parsers.md) applications and other components of the Network Monitor architecture.</span></span>

![die Beziehung zwischen Experten-und parseranwendungen](images/nm-arch1.png)

<span data-ttu-id="47feb-106">Der Netzwerk Datenverkehr wird als einzelne Frames vom NDIS-Treiber gesammelt.</span><span class="sxs-lookup"><span data-stu-id="47feb-106">The network traffic is collected, as individual frames, from the NDIS driver.</span></span> <span data-ttu-id="47feb-107">Der Netzwerkmonitor Treiber (Nmnt.sys) leitet die Frames dann an einen Netzwerk Paketanbieter (NPP) weiter, der die Daten erfasst und in einer oder mehreren Erfassungs Dateien platziert.</span><span class="sxs-lookup"><span data-stu-id="47feb-107">The Network Monitor driver (Nmnt.sys) then routes the frames to a network packet provider (NPP), which captures the data and places it in one or more capture files.</span></span> <span data-ttu-id="47feb-108">Der npp ist eine Sammlung von COM-Schnittstellen, die zum Erfassen von Daten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="47feb-108">The NPP is a collection of COM interfaces used to capture data.</span></span> <span data-ttu-id="47feb-109">In diesem Fall wird die [**idelta-DC**](idelaydc.md) -Schnittstelle verwendet, um eine verzögerte Erfassung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="47feb-109">In this case, the [**IDelaydC**](idelaydc.md) interface is used to perform a delayed capture.</span></span>

> [!Note]  
> <span data-ttu-id="47feb-110">Der NPP wird für verzögerte und Echt Zeit Erfassungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="47feb-110">The NPP is used for delayed and real-time captures.</span></span> <span data-ttu-id="47feb-111">Für echt Zeit Erfassungen [**wird die-**](irtc.md) Schnittstelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="47feb-111">For real-time captures, the [**IRTC**](irtc.md) interface is used.</span></span>

 

<span data-ttu-id="47feb-112">Wenn die Netzwerk Frames in der Erfassungs Datei gespeichert werden und auf die Datei zugegriffen werden kann, können Experten und Parser die Netzwerkmonitor-Benutzeroberfläche und die Netzwerkmonitor Funktionen verwenden, die in Nmapi.dll zur Analyse der Daten bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="47feb-112">When the network frames are stored in the capture file and the file is accessible, experts and parsers can use the Network Monitor UI and the Network Monitor functions provided in Nmapi.dll to analyze the data.</span></span> <span data-ttu-id="47feb-113">Auf Erfassungs Dateien kann erst dann zugegriffen werden, wenn die Erfassung beendet ist.</span><span class="sxs-lookup"><span data-stu-id="47feb-113">Capture files are not accessible until the capture is complete.</span></span>

 

 



