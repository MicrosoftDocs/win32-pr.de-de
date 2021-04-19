---
description: Windows-Abbild Erfassungsgeräte (WIA) sind Konstanten, die den Typ des Geräts angeben, das dem Computer eines Benutzers zugeordnet ist.
ms.assetid: 569b99ab-628b-4a43-a6e5-0ae81524fcc0
title: WIA-Gerätetyp spezifiker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc18b000d84bec5e5be37a5a5c52f28f6f8325d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357347"
---
# <a name="wia-device-type-specifiers"></a><span data-ttu-id="b5d30-103">WIA-Gerätetyp spezifiker</span><span class="sxs-lookup"><span data-stu-id="b5d30-103">WIA Device Type Specifiers</span></span>

<span data-ttu-id="b5d30-104">Windows-Abbild Erfassungsgeräte (WIA) sind Konstanten, die den Typ des Geräts angeben, das dem Computer eines Benutzers zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b5d30-104">Windows Image Acquisition (WIA) Device Type Specifiers are constants that indicate the type of device attached to a user's computer.</span></span> <span data-ttu-id="b5d30-105">Verwenden Sie das \_ Makro Get stidevice \_ Type, um diese Werte aus der Eigenschaft WIA-Gerätetyp abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b5d30-105">Use the GET\_STIDEVICE\_TYPE macro to obtain these values from the WIA device type property.</span></span> <span data-ttu-id="b5d30-106">Im folgenden sind gültige WIA-Gerätetyp spezifiatoren aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="b5d30-106">The following are valid WIA Device Type Specifiers:</span></span> 

| <span data-ttu-id="b5d30-107">Gerätetyp</span><span class="sxs-lookup"><span data-stu-id="b5d30-107">Device Type</span></span>                 | <span data-ttu-id="b5d30-108">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b5d30-108">Meaning</span></span>                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5d30-109">Stide vicetypeer default</span><span class="sxs-lookup"><span data-stu-id="b5d30-109">StiDeviceTypeDefault</span></span>        | <span data-ttu-id="b5d30-110">Generisches WIA-Gerät.</span><span class="sxs-lookup"><span data-stu-id="b5d30-110">Generic WIA device.</span></span> <span data-ttu-id="b5d30-111">Während der Geräte Enumerationen wird diese Konstante zum Auflisten aller WIA-Geräte verwendet.</span><span class="sxs-lookup"><span data-stu-id="b5d30-111">During device enumerations, this constant is used to enumerate all WIA devices.</span></span>                         |
| <span data-ttu-id="b5d30-112">Stide vicetyetdigitalcamera</span><span class="sxs-lookup"><span data-stu-id="b5d30-112">StiDeviceTypeDigitalCamera</span></span>  | <span data-ttu-id="b5d30-113">Das Gerät ist eine Kamera.</span><span class="sxs-lookup"><span data-stu-id="b5d30-113">The device is a camera.</span></span> <span data-ttu-id="b5d30-114">*Dieser Spezifizierer wird von nicht unterstützt* . Windows Vista *und höher.*</span><span class="sxs-lookup"><span data-stu-id="b5d30-114">*This specifier is not supported by* Windows Vista *and later.*</span></span>                                     |
| <span data-ttu-id="b5d30-115">Stide vicetypescanner</span><span class="sxs-lookup"><span data-stu-id="b5d30-115">StiDeviceTypeScanner</span></span>        | <span data-ttu-id="b5d30-116">Das Gerät ist ein Scanner.</span><span class="sxs-lookup"><span data-stu-id="b5d30-116">The device is a scanner.</span></span>                                                                                                    |
| <span data-ttu-id="b5d30-117">Stientvicetyetstreamingvideo</span><span class="sxs-lookup"><span data-stu-id="b5d30-117">StiDeviceTypeStreamingVideo</span></span> | <span data-ttu-id="b5d30-118">Das Gerät enthält Streaming-Videos.</span><span class="sxs-lookup"><span data-stu-id="b5d30-118">The device contains streaming video.</span></span> <span data-ttu-id="b5d30-119">*Dieser Spezifizierer wird von nicht unterstützt* . Windows Server 2003 *,* Windows Vista *oder höher.*</span><span class="sxs-lookup"><span data-stu-id="b5d30-119">*This specifier is not supported by* Windows Server 2003 *,* Windows Vista, *or later.*</span></span> |



 

 

 



