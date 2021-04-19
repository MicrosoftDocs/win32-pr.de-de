---
description: MF Trace ist ein Tool zum Erstellen von Ablauf Verfolgungs Protokollen für Media Foundation Anwendungen.
ms.assetid: 55b421c8-e87c-4dd2-8649-93832c93f999
title: MF-Ablauf Verfolgung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d4a216f225141ceccf3f1357025dd069afa494d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367569"
---
# <a name="mftrace"></a><span data-ttu-id="d8398-103">MF-Ablauf Verfolgung</span><span class="sxs-lookup"><span data-stu-id="d8398-103">MFTrace</span></span>

<span data-ttu-id="d8398-104">MF Trace ist ein Tool zum Erstellen von Ablauf Verfolgungs Protokollen für Media Foundation Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="d8398-104">MFTrace is a tool for generating trace logs for Media Foundation applications.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d8398-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="d8398-105">In this section</span></span>

-   [<span data-ttu-id="d8398-106">Verwenden von MF Trace</span><span class="sxs-lookup"><span data-stu-id="d8398-106">Using MFTrace</span></span>](using-mftrace.md)
-   [<span data-ttu-id="d8398-107">MF Trace-Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="d8398-107">MFTrace Keywords</span></span>](mftrace-keywords.md)
-   [<span data-ttu-id="d8398-108">MF-Ablauf Verfolgungs Konfigurationsdatei</span><span class="sxs-lookup"><span data-stu-id="d8398-108">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)

## <a name="requirements"></a><span data-ttu-id="d8398-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d8398-109">Requirements</span></span>



| <span data-ttu-id="d8398-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d8398-110">Requirement</span></span> | <span data-ttu-id="d8398-111">Wert</span><span class="sxs-lookup"><span data-stu-id="d8398-111">Value</span></span> |
|--------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d8398-112">Mindestversion des SDK</span><span class="sxs-lookup"><span data-stu-id="d8398-112">Minimum SDK version</span></span>      | <span data-ttu-id="d8398-113">Microsoft Windows Software Development Kit (SDK) für Windows 7 und .NET Framework 4,0</span><span class="sxs-lookup"><span data-stu-id="d8398-113">Microsoft Windows Software Development Kit (SDK) for Windows 7 and .NET Framework 4.0</span></span> |
| <span data-ttu-id="d8398-114">Mindestens Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="d8398-114">Minimum operating system</span></span> | <span data-ttu-id="d8398-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d8398-115">Windows Vista</span></span>                                                                         |



 

<span data-ttu-id="d8398-116">MF-Ablauf Verfolgung erfordert die folgenden DLLs, die ebenfalls im SDK bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d8398-116">MFTrace requires the following DLLs, which are also provided in the SDK.</span></span>

-   <span data-ttu-id="d8398-117">detoured.dll</span><span class="sxs-lookup"><span data-stu-id="d8398-117">detoured.dll</span></span>
-   <span data-ttu-id="d8398-118">mfdetours.dll</span><span class="sxs-lookup"><span data-stu-id="d8398-118">mfdetours.dll</span></span>

<span data-ttu-id="d8398-119">Das SDK bietet sowohl 32-Bit-als auch 64-Bit-Versionen von MF Trace.</span><span class="sxs-lookup"><span data-stu-id="d8398-119">The SDK provides both 32-bit and 64-bit versions of MFTrace.</span></span> <span data-ttu-id="d8398-120">MF unterstützt nicht WOW64; Verwenden Sie zum Nachverfolgen eines 32-Bit-Prozesses, der unter 64-Bit-Windows ausgeführt wird, die 32-Bit-Version von mftrace.</span><span class="sxs-lookup"><span data-stu-id="d8398-120">MFTrace does not support WOW64; to trace a 32-bit process running on 64-bit Windows, use the 32-bit version of MFTrace.</span></span>

<span data-ttu-id="d8398-121">SDK-Root auf 32-Bit-Systemen: \Program Files\Windows kits\10 SDK-Root auf 64 Bit System: \Programme (x86) \Windows kits\10 Sie finden mftrace unter <SDK-Root> \bin \<sdk-version> \<architecture>\mftrace.exe</span><span class="sxs-lookup"><span data-stu-id="d8398-121">sdk-root on 32 bit systems: \Program Files\Windows Kits\10 sdk-root on 64 bit system: \Program Files (x86)\Windows Kits\10 You will find mftrace at <sdk-root>\bin\<sdk-version>\<architecture>\mftrace.exe</span></span>

## <a name="related-topics"></a><span data-ttu-id="d8398-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d8398-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8398-123">Media Foundation Tools</span><span class="sxs-lookup"><span data-stu-id="d8398-123">Media Foundation Tools</span></span>](media-foundation-tools.md)
</dt> </dl>

 

 



