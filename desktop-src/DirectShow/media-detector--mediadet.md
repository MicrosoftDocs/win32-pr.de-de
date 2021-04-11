---
description: Medien Erkennung (mediadet)
ms.assetid: 5cdbb6ca-d2c3-4123-b545-198863fed25f
title: Medien Erkennung (mediadet)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90f34b1dc267480d3d6ea9efe9b9a743623a917b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104132173"
---
# <a name="media-detector-mediadet"></a><span data-ttu-id="5432e-103">Medien Erkennung (mediadet)</span><span class="sxs-lookup"><span data-stu-id="5432e-103">Media Detector (MediaDet)</span></span>

> [!Note]  
> <span data-ttu-id="5432e-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="5432e-104">\[Deprecated.</span></span> <span data-ttu-id="5432e-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="5432e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5432e-106">Das Media Detector-Objekt (mediadet) ruft Formatierungsinformationen ab und gibt weiterhin Frames aus Datei Quellen aus.</span><span class="sxs-lookup"><span data-stu-id="5432e-106">The Media Detector (MediaDet) object retrieves format information and still frames from file sources.</span></span> <span data-ttu-id="5432e-107">Der Filter Graph-Manager muss vom Medien Erkennungs Modul nicht funktionieren.</span><span class="sxs-lookup"><span data-stu-id="5432e-107">The Media Detector does not require the Filter Graph Manager to function.</span></span> <span data-ttu-id="5432e-108">Um dieses Objekt zu erstellen, rufen Sie **cokreateinstance** auf.</span><span class="sxs-lookup"><span data-stu-id="5432e-108">To create this object, call **CoCreateInstance**.</span></span> <span data-ttu-id="5432e-109">Der Klassen Bezeichner ist CLSID \_ mediadet.</span><span class="sxs-lookup"><span data-stu-id="5432e-109">The class identifier is CLSID\_MediaDet.</span></span>

<span data-ttu-id="5432e-110">Um Windows Media™-Dateien zu lesen, muss die Anwendung ein Software Zertifikat bereitstellen, das auch als Schlüssel bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="5432e-110">To read Windows Media™ files, the application must provide a software certificate, also called a key.</span></span> <span data-ttu-id="5432e-111">Registrieren Sie die Anwendung als Schlüssel Anbieter über die **IObjectWithSite** -Schnittstelle des Medien Detektors.</span><span class="sxs-lookup"><span data-stu-id="5432e-111">Register the application as a key provider through the Media Detector's **IObjectWithSite** interface.</span></span> <span data-ttu-id="5432e-112">Weitere Informationen finden Sie unter [Entsperren des Windows Media-Format](unlocking-the-windows-media-format-sdk.md)-SDKs.</span><span class="sxs-lookup"><span data-stu-id="5432e-112">For more information, see [Unlocking the Windows Media Format SDK](unlocking-the-windows-media-format-sdk.md).</span></span>

<span data-ttu-id="5432e-113">Das mediadet-Objekt macht die folgenden Schnittstellen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="5432e-113">The MediaDet object exposes the following interfaces:</span></span>

-   [<span data-ttu-id="5432e-114">**Imediadet**</span><span class="sxs-lookup"><span data-stu-id="5432e-114">**IMediaDet**</span></span>](imediadet.md)
-   <span data-ttu-id="5432e-115">**IObjectWithSite**</span><span class="sxs-lookup"><span data-stu-id="5432e-115">**IObjectWithSite**</span></span>

## <a name="related-topics"></a><span data-ttu-id="5432e-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5432e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5432e-117">Arbeiten mit Quellen</span><span class="sxs-lookup"><span data-stu-id="5432e-117">Working with Sources</span></span>](working-with-sources.md)
</dt> </dl>

 

 



