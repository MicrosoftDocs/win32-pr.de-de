---
description: Gibt den PnP-X-Hardware Bezeichner des Dienstanbieter an.
ms.assetid: aa4c935f-0d60-4603-ae96-d5cabdf9af00
title: Pnpxhardwareid-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55e5e38b669a289545225df96fad05e55069b474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347910"
---
# <a name="pnpxhardwareid-element"></a><span data-ttu-id="04dca-103">Pnpxhardwareid-Element</span><span class="sxs-lookup"><span data-stu-id="04dca-103">PnPXHardwareId element</span></span>

<span data-ttu-id="04dca-104">Gibt den PnP-X-Hardware Bezeichner des Dienstanbieter an.</span><span class="sxs-lookup"><span data-stu-id="04dca-104">Specifies the PnP-X Hardware Identifier of the service.</span></span> <span data-ttu-id="04dca-105">PNP stimmt mit diesem Element mit den Hardware Beschreibungen überein, die im \[ Abschnitt "pnpxdevice" \] der INF-Datei des Geräts bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="04dca-105">PnP matches this element with the hardware description(s) provided in the \[PnpxDevice\] section of the device's INF file.</span></span> <span data-ttu-id="04dca-106">Basierend auf diesen Informationen wählt der PnP-Dienst den am besten geeigneten Gerätetreiber aus und lädt ihn.</span><span class="sxs-lookup"><span data-stu-id="04dca-106">Based on this information, the PnP service selects and loads the most appropriate device driver.</span></span>

## <a name="usage"></a><span data-ttu-id="04dca-107">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="04dca-107">Usage</span></span>

``` syntax
<PnPXHardwareId/>
```

## <a name="attributes"></a><span data-ttu-id="04dca-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="04dca-108">Attributes</span></span>

<span data-ttu-id="04dca-109">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="04dca-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="04dca-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="04dca-110">Child elements</span></span>

<span data-ttu-id="04dca-111">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="04dca-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="04dca-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="04dca-112">Parent elements</span></span>



| <span data-ttu-id="04dca-113">Element</span><span class="sxs-lookup"><span data-stu-id="04dca-113">Element</span></span>                             | <span data-ttu-id="04dca-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="04dca-114">Description</span></span>                                                                            |
|-------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="04dca-115">**gehostet**</span><span class="sxs-lookup"><span data-stu-id="04dca-115">**hosted**</span></span>](hosted.md)<br/> | <span data-ttu-id="04dca-116">Definiert die Elemente für die Dienste, die vom Dienst Host definiert werden.</span><span class="sxs-lookup"><span data-stu-id="04dca-116">Defines elements for the services defined by the service host.</span></span> <br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="04dca-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="04dca-117">Remarks</span></span>

<span data-ttu-id="04dca-118">Wenn Sie mehr als eine Hardware-ID angeben möchten, trennen Sie die Bezeichner durch ein Leerzeichen, z. b. "PnPX \_ SampleService \_ HWID \_ 1 PnPX \_ SampleService \_ HWID \_ 2 PnPX \_ SampleService1 \_ HWID \_ 3".</span><span class="sxs-lookup"><span data-stu-id="04dca-118">To specify more than one hardware ID, separate the identifiers with a space character, for example, "PnPX\_SampleService\_HWID\_1 PnPX\_SampleService\_HWID\_2 PnPX\_SampleService1\_HWID\_3".</span></span>

## <a name="element-information"></a><span data-ttu-id="04dca-119">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="04dca-119">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="04dca-120">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="04dca-120">Minimum supported system</span></span><br/> | <span data-ttu-id="04dca-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="04dca-121">Windows Vista</span></span> |
| <span data-ttu-id="04dca-122">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="04dca-122">Can be empty</span></span>                        | <span data-ttu-id="04dca-123">Ja</span><span class="sxs-lookup"><span data-stu-id="04dca-123">Yes</span></span>           |



 

 




