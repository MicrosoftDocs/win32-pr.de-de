---
description: Die itformatcontrol-Schnittstelle macht Methoden verfügbar, mit denen eine Anwendung Informationen über das Format eines Empfangs-oder Übertragungsdaten Stroms für einen-Abruf abrufen kann.
ms.assetid: a3d15561-229e-4eb6-a0ac-2d69f170bced
title: Itformatcontrol-Schnittstelle (ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0735e7bfaf5222948cef5e047530a35cb19a125
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365764"
---
# <a name="itformatcontrol-interface"></a><span data-ttu-id="c63cf-103">Itformatcontrol-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="c63cf-103">ITFormatControl interface</span></span>

<span data-ttu-id="c63cf-104">\[ Diese Schnittstelle ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c63cf-104">\[ This interface is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c63cf-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="c63cf-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="c63cf-106">Die **itformatcontrol** -Schnittstelle macht Methoden verfügbar, mit denen eine Anwendung Informationen über das Format eines Empfangs-oder Übertragungsdaten Stroms für einen-Abruf abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="c63cf-106">The **ITFormatControl** interface exposes methods that allow an application to retrieve information concerning the format of a receive or transmit stream for a call.</span></span>

<span data-ttu-id="c63cf-107">Diese Schnittstelle wird vom [h323-MSP](h323-msp.md) implementiert und wird nur verfügbar gemacht, wenn ein-Rückruf diesen Dienstanbieter verwendet.</span><span class="sxs-lookup"><span data-stu-id="c63cf-107">This interface is implemented by the [H323 MSP](h323-msp.md) and is exposed only when a call uses this service provider.</span></span>

## <a name="members"></a><span data-ttu-id="c63cf-108">Member</span><span class="sxs-lookup"><span data-stu-id="c63cf-108">Members</span></span>

<span data-ttu-id="c63cf-109">Die **itformatcontrol** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="c63cf-109">The **ITFormatControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c63cf-110">**Itformatcontrol** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c63cf-110">**ITFormatControl** also has these types of members:</span></span>

-   [<span data-ttu-id="c63cf-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="c63cf-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c63cf-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="c63cf-112">Methods</span></span>

<span data-ttu-id="c63cf-113">Die **itformatcontrol** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="c63cf-113">The **ITFormatControl** interface has these methods.</span></span>



| <span data-ttu-id="c63cf-114">Methode</span><span class="sxs-lookup"><span data-stu-id="c63cf-114">Method</span></span>                                                                     | <span data-ttu-id="c63cf-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c63cf-115">Description</span></span>                                                                    |
|:---------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="c63cf-116">**Getcurrentformat**</span><span class="sxs-lookup"><span data-stu-id="c63cf-116">**GetCurrentFormat**</span></span>](itformatcontrol-getcurrentformat.md)               | <span data-ttu-id="c63cf-117">Ruft das Medienformat des aktuellen Streams ab.</span><span class="sxs-lookup"><span data-stu-id="c63cf-117">Gets the media format of the current stream.</span></span><br/>                        |
| [<span data-ttu-id="c63cf-118">**Getnumof-Funktionen**</span><span class="sxs-lookup"><span data-stu-id="c63cf-118">**GetNumberOfCapabilities**</span></span>](itformatcontrol-getnumberofcapabilities.md) | <span data-ttu-id="c63cf-119">Ruft die Anzahl der Funktionen ab, die dem aktuellen Format zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c63cf-119">Gets the number of capabilities associated with the current format.</span></span><br/> |
| [<span data-ttu-id="c63cf-120">**Getstreamcaps**</span><span class="sxs-lookup"><span data-stu-id="c63cf-120">**GetStreamCaps**</span></span>](itformatcontrol-getstreamcaps.md)                     | <span data-ttu-id="c63cf-121">Ruft die Funktionen ab, die einem angegebenen Format Index zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c63cf-121">Gets the capabilities associated with a given format index.</span></span><br/>         |
| [<span data-ttu-id="c63cf-122">**Releaseformat**</span><span class="sxs-lookup"><span data-stu-id="c63cf-122">**ReleaseFormat**</span></span>](itformatcontrol-releaseformat.md)                     | <span data-ttu-id="c63cf-123">Gibt die Struktur frei, die dem Format zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c63cf-123">Releases the structure associated with the format.</span></span><br/>                  |
| [<span data-ttu-id="c63cf-124">**Reorderfunktionen**</span><span class="sxs-lookup"><span data-stu-id="c63cf-124">**ReOrderCapabilities**</span></span>](itformatcontrol-reordercapabilities.md)         | <span data-ttu-id="c63cf-125">Legt eine neue Reihenfolge für Formatierungsfunktionen fest.</span><span class="sxs-lookup"><span data-stu-id="c63cf-125">Sets a new order for format capabilities.</span></span><br/>                           |



 

## <a name="requirements"></a><span data-ttu-id="c63cf-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c63cf-126">Requirements</span></span>



| <span data-ttu-id="c63cf-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c63cf-127">Requirement</span></span> | <span data-ttu-id="c63cf-128">Wert</span><span class="sxs-lookup"><span data-stu-id="c63cf-128">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c63cf-129">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="c63cf-129">TAPI version</span></span><br/> | <span data-ttu-id="c63cf-130">Erfordert TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="c63cf-130">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="c63cf-131">Header</span><span class="sxs-lookup"><span data-stu-id="c63cf-131">Header</span></span><br/>       | <dl> <span data-ttu-id="c63cf-132"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c63cf-132"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c63cf-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c63cf-133">Library</span></span><br/>      | <dl> <span data-ttu-id="c63cf-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c63cf-134"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="c63cf-135">DLL</span><span class="sxs-lookup"><span data-stu-id="c63cf-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="c63cf-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c63cf-136"><dt>Tapi3.dll</dt></span></span> </dl> |



 

