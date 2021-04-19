---
description: Das Tool MF Trace kann eine XML-Konfigurationsdatei lesen, die einen oder mehrere Ablauf Verfolgungs Anbieter angibt.
ms.assetid: 70d11a55-041e-4eb5-96a9-238e7ecdd906
title: MF-Ablauf Verfolgungs Konfigurationsdatei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6598bcfdde16291fb744783b2f12be414ae997b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355630"
---
# <a name="mftrace-configuration-file"></a><span data-ttu-id="0d31a-103">MF-Ablauf Verfolgungs Konfigurationsdatei</span><span class="sxs-lookup"><span data-stu-id="0d31a-103">MFTrace Configuration File</span></span>

<span data-ttu-id="0d31a-104">Das Tool [MF Trace](mftrace.md) kann eine XML-Konfigurationsdatei lesen, die einen oder mehrere Ablauf Verfolgungs Anbieter angibt.</span><span class="sxs-lookup"><span data-stu-id="0d31a-104">The [MFTrace](mftrace.md) tool can read an XML configuration file that specifies one or more trace providers.</span></span>

<span data-ttu-id="0d31a-105">Das [**Providers**](providers.md) -Element ist das Stamm Element in der Konfigurationsdatei.</span><span class="sxs-lookup"><span data-stu-id="0d31a-105">The [**providers**](providers.md) element is the root element in the configuration file.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0d31a-106">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="0d31a-106">In this section</span></span>

-   [<span data-ttu-id="0d31a-107">**Schlüsselwort**</span><span class="sxs-lookup"><span data-stu-id="0d31a-107">**keyword**</span></span>](keyword.md)
-   [<span data-ttu-id="0d31a-108">**MF-Umleitungen**</span><span class="sxs-lookup"><span data-stu-id="0d31a-108">**mfdetours**</span></span>](mfdetours.md)
-   [<span data-ttu-id="0d31a-109">**ab**</span><span class="sxs-lookup"><span data-stu-id="0d31a-109">**provider**</span></span>](provider.md)
-   [<span data-ttu-id="0d31a-110">**providers**</span><span class="sxs-lookup"><span data-stu-id="0d31a-110">**providers**</span></span>](providers.md)

## <a name="example"></a><span data-ttu-id="0d31a-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0d31a-111">Example</span></span>

``` syntax
<?xml version='1.0' encoding='utf-8'?>
<providers>
  <mfdetours level="info"> 
    <keyword ID="MFPlatExport" />
  </mfdetours>
  
  <!-- Manifest-based traces -->

  <provider level="verbose" ID="Microsoft-Windows-MediaFoundation-MFReadWrite">
    <keyword ID="0x0000000000000000" />
  </provider>

</providers>
```

## <a name="related-topics"></a><span data-ttu-id="0d31a-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0d31a-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d31a-113">MF-Ablauf Verfolgung</span><span class="sxs-lookup"><span data-stu-id="0d31a-113">MFTrace</span></span>](mftrace.md)
</dt> </dl>

 

 



