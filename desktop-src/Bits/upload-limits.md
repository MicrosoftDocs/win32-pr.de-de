---
title: Uploadlimits
description: Um die Größe der Uploads einzuschränken, legen Sie die IIS-Erweiterungs Eigenschaft bizmaximumuploadsize fest.
ms.assetid: 01ad2f32-18be-43a5-a07f-e6f28f7a471b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 647aeefe82cf9c3ab035bc3e233c4157f471110b
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104472268"
---
# <a name="upload-limits"></a><span data-ttu-id="682c8-103">Uploadlimits</span><span class="sxs-lookup"><span data-stu-id="682c8-103">Upload Limits</span></span>

<span data-ttu-id="682c8-104">Um die Größe der Uploads einzuschränken, legen Sie die IIS-Erweiterungs Eigenschaft [**bizmaximumuploadsize**](bits-iis-extension-properties.md) fest.</span><span class="sxs-lookup"><span data-stu-id="682c8-104">To limit the size of uploads, set the [**BITSMaximumUploadSize**](bits-iis-extension-properties.md) IIS extension property.</span></span> <span data-ttu-id="682c8-105">In IIS 7 müssen Sie möglicherweise auch das Attribut " **maxzuweisung wedcontentlength** " ändern.</span><span class="sxs-lookup"><span data-stu-id="682c8-105">In IIS 7, you may also have to modify the **maxAllowedContentLength** attribute.</span></span> <span data-ttu-id="682c8-106">Der Standardwert für das IIS 7-Uploadlimit beträgt 30 Millionen Bytes.</span><span class="sxs-lookup"><span data-stu-id="682c8-106">By default, the IIS 7 upload limit is 30 million bytes.</span></span> <span data-ttu-id="682c8-107">Weitere Informationen und Informationen zum Ändern der IIS-Standardeinstellungen finden Sie unter [KB942074](https://support.microsoft.com//kb/942074).</span><span class="sxs-lookup"><span data-stu-id="682c8-107">For details and information on changing the IIS default, see [KB942074](https://support.microsoft.com//kb/942074).</span></span>

 

 




