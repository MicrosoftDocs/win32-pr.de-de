---
description: Gibt den PnP-X-Hardwarebezeichner des Diensts an.
ms.assetid: aa4c935f-0d60-4603-ae96-d5cabdf9af00
title: PnPXHardwareId-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0ffc389ca6df363439dd6463b3f86ca756359e8
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996527"
---
# <a name="pnpxhardwareid-element"></a><span data-ttu-id="030d3-103">PnPXHardwareId-Element</span><span class="sxs-lookup"><span data-stu-id="030d3-103">PnPXHardwareId element</span></span>

<span data-ttu-id="030d3-104">Gibt den PnP-X-Hardwarebezeichner des Diensts an.</span><span class="sxs-lookup"><span data-stu-id="030d3-104">Specifies the PnP-X Hardware Identifier of the service.</span></span> <span data-ttu-id="030d3-105">PnP gleicht dieses Element mit den Hardwarebeschreibungen ab, die im \[ Abschnitt PnpxDevice \] der INF-Datei des Geräts angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="030d3-105">PnP matches this element with the hardware description(s) provided in the \[PnpxDevice\] section of the device's INF file.</span></span> <span data-ttu-id="030d3-106">Basierend auf diesen Informationen wählt der PnP-Dienst den am besten geeigneten Gerätetreiber aus und lädt diesen.</span><span class="sxs-lookup"><span data-stu-id="030d3-106">Based on this information, the PnP service selects and loads the most appropriate device driver.</span></span>

## <a name="usage"></a><span data-ttu-id="030d3-107">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="030d3-107">Usage</span></span>

``` syntax
<PnPXHardwareId/>
```

## <a name="attributes"></a><span data-ttu-id="030d3-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="030d3-108">Attributes</span></span>

<span data-ttu-id="030d3-109">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="030d3-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="030d3-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="030d3-110">Child elements</span></span>

<span data-ttu-id="030d3-111">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="030d3-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="030d3-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="030d3-112">Parent elements</span></span>



| <span data-ttu-id="030d3-113">Element</span><span class="sxs-lookup"><span data-stu-id="030d3-113">Element</span></span>                             | <span data-ttu-id="030d3-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="030d3-114">Description</span></span>                                                                            |
|-------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="030d3-115">**Gehostet**</span><span class="sxs-lookup"><span data-stu-id="030d3-115">**hosted**</span></span>](hosted.md)<br/> | <span data-ttu-id="030d3-116">Definiert Elemente für die vom Diensthost definierten Dienste.</span><span class="sxs-lookup"><span data-stu-id="030d3-116">Defines elements for the services defined by the service host.</span></span> <br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="030d3-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="030d3-117">Remarks</span></span>

<span data-ttu-id="030d3-118">Um mehr als eine Hardware-ID anzugeben, trennen Sie die Bezeichner durch ein Leerzeichen, z.B. "PnPX \_ SampleService \_ HWID \_ 1 PnPX \_ SampleService \_ HWID \_ 2 PnPX \_ SampleService1 \_ HWID \_ 3".</span><span class="sxs-lookup"><span data-stu-id="030d3-118">To specify more than one hardware ID, separate the identifiers with a space character, for example, "PnPX\_SampleService\_HWID\_1 PnPX\_SampleService\_HWID\_2 PnPX\_SampleService1\_HWID\_3".</span></span>

## <a name="element-information"></a><span data-ttu-id="030d3-119">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="030d3-119">Element information</span></span>



| <span data-ttu-id="030d3-120">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="030d3-120">Label</span></span> | <span data-ttu-id="030d3-121">Wert</span><span class="sxs-lookup"><span data-stu-id="030d3-121">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="030d3-122">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="030d3-122">Minimum supported system</span></span><br/> | <span data-ttu-id="030d3-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="030d3-123">Windows Vista</span></span> |
| <span data-ttu-id="030d3-124">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="030d3-124">Can be empty</span></span>                        | <span data-ttu-id="030d3-125">Ja</span><span class="sxs-lookup"><span data-stu-id="030d3-125">Yes</span></span>           |



 

 




