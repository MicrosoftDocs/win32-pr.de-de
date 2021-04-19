---
description: Allgemeine Registrierungseinträge
ms.assetid: 6a140c7f-df8c-4a8e-9e4d-dbb38901e14f
title: Allgemeine Registrierungseinträge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d7c3514adcc0aeaaf9adadd2b71dfdffcd8d408
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373147"
---
# <a name="general-registry-entries"></a><span data-ttu-id="9ff2a-103">Allgemeine Registrierungseinträge</span><span class="sxs-lookup"><span data-stu-id="9ff2a-103">General Registry Entries</span></span>


<span data-ttu-id="9ff2a-104">Die folgenden Registrierungseinträge müssen für den Decoder und den Encoder separat erstellt werden:</span><span class="sxs-lookup"><span data-stu-id="9ff2a-104">The following registry entries must be made separately for both the decoder and the encoder:</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Encoder/Decoder CLSID}
         Author = Author's Name
         Description = Your Codec Description
         DeviceManufacturer = Manufacturer's Name
         DeviceModels = Device,Device
         FriendlyName = Codec Friendly Name
         Date = mm-dd-yyyy
         Vendor = {GUID_Vendor}
         ContainerFormat = {GUID_ContainerFormat}
         Version = Major.Minor.Build.Number
         SpecVersion = Major.Minor.Build.Number
         MimeTypes = Your Mime Type
         SupportAnimation = 0|1
         SupportChromakey = 0|1
         SupportLossless = 0|1
         SupportMultiframe = 0|1
         Formats
            {Supported PixelFormat GUID 1}
            {Supported PixelFormat GUID ...}
            {Supported PixelFormat GUID N}
         ArbitrationPriority  = 0-10
```

<span data-ttu-id="9ff2a-105">Die Einträge FriendlyName, VendorGUID, Containerformat, mimeTypes, File Extensions und Formats sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9ff2a-105">The FriendlyName, VendorGUID, ContainerFormat, MimeTypes, FileExtensions, and Formats entries are required.</span></span> <span data-ttu-id="9ff2a-106">Alle anderen sind optional.</span><span class="sxs-lookup"><span data-stu-id="9ff2a-106">All of the others are optional.</span></span>

<span data-ttu-id="9ff2a-107">Beachten Sie, dass die Einträge "de vicemanufakturer" und "DeviceModels" spezifisch für Rohdaten-Codecs sind und sich auf den Kamerahersteller und die Kameramodelle beziehen, auf die der Codec anwendbar ist.</span><span class="sxs-lookup"><span data-stu-id="9ff2a-107">Note that the DeviceManufacturer and DeviceModels entries are specific to raw codecs and refer to the camera manufacturer and camera models that the codec is applicable to.</span></span> <span data-ttu-id="9ff2a-108">Die spec-Version ist die Version der Abbild Format Spezifikation, der der Codec entspricht.</span><span class="sxs-lookup"><span data-stu-id="9ff2a-108">The spec version is the version of the image format specification with which the codec complies.</span></span> <span data-ttu-id="9ff2a-109">Der-Format Eintrag gibt die Pixel Formate an, die vom Codec unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="9ff2a-109">The Formats entry specifies the pixel formats supported by the codec.</span></span> <span data-ttu-id="9ff2a-110">Ein Codec unterstützt möglicherweise mehr als ein Pixel Format.</span><span class="sxs-lookup"><span data-stu-id="9ff2a-110">A codec may support more than one pixel format.</span></span> <span data-ttu-id="9ff2a-111">In diesem Fall würden Sie mehrere Schlüssel unter HKEY \_ Classes \_ root \\ CLSID \\ {Encoder/Decoder CLSID} Formats eingeben \\ .</span><span class="sxs-lookup"><span data-stu-id="9ff2a-111">In that case, you would enter multiple keys under HKEY\_CLASSES\_ROOT\\CLSID\\{Encoder/Decoder CLSID}\\Formats.</span></span>

## <a name="arbitrationpriority"></a><span data-ttu-id="9ff2a-112">Arbitrationpriority</span><span class="sxs-lookup"><span data-stu-id="9ff2a-112">ArbitrationPriority</span></span>

<span data-ttu-id="9ff2a-113">Ab Windows 8 ist arbitrationpriority ein neuer Registrierungs Eintrag.</span><span class="sxs-lookup"><span data-stu-id="9ff2a-113">Starting in Windows 8, ArbitrationPriority is a new registry entry.</span></span> <span data-ttu-id="9ff2a-114">Gültige Werte sind 0 bis 10.</span><span class="sxs-lookup"><span data-stu-id="9ff2a-114">Valid values are 0 through 10.</span></span> <span data-ttu-id="9ff2a-115">Wenn der Schlüssel arbitrationpriority vorhanden ist, weist der Wert dieses Schlüssels WIC an, den zugeordneten Codec hinter allen anderen Codecs mit einem niedrigeren arbitrationpriority-Wert zu priorisieren.</span><span class="sxs-lookup"><span data-stu-id="9ff2a-115">When the ArbitrationPriority key is present, the value of this key will instruct WIC to prioritize the associated codec behind any other codecs with a lower ArbitrationPriority value.</span></span> <span data-ttu-id="9ff2a-116">Diese Auswertung erfolgt vor dem Auftreten der vorhandenen WIC-Codec-Schiedsgerichtsbarkeit und stellt sicher, dass der zugehörige Codec unter jedem konkurrierenden Codec priorisiert wird, auch wenn er als oder besser geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="9ff2a-116">This evaluation occurs before the existing WIC codec arbitration occurs, and ensures the associated codec is prioritized below any competing codec, even if it is as or more capable.</span></span> <span data-ttu-id="9ff2a-117">Jeder Codec, der keinen expliziten arbitrationpriority-Wert besitzt, der in der Registrierung definiert ist, erhält standardmäßig die Priorität 0.</span><span class="sxs-lookup"><span data-stu-id="9ff2a-117">Any codec that doesn’t have an explicit ArbitrationPriority value defined in the registry will default to Priority 0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9ff2a-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9ff2a-118">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="9ff2a-119">**Licher**</span><span class="sxs-lookup"><span data-stu-id="9ff2a-119">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9ff2a-120">Codec-Installation und-Registrierung</span><span class="sxs-lookup"><span data-stu-id="9ff2a-120">CODEC Installation and Registration</span></span>](-wic-codecinstallandreg.md)
</dt> <dt>

[<span data-ttu-id="9ff2a-121">Codierungs spezifische Registrierungseinträge</span><span class="sxs-lookup"><span data-stu-id="9ff2a-121">Encoder-Specific Registry Entries</span></span>](-wic-encoderregentries.md)
</dt> <dt>

[<span data-ttu-id="9ff2a-122">Schreiben eines WIC-Enabled Codecs</span><span class="sxs-lookup"><span data-stu-id="9ff2a-122">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="9ff2a-123">Übersicht über die Windows Imaging-Komponente</span><span class="sxs-lookup"><span data-stu-id="9ff2a-123">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="9ff2a-124">**Funktionsweise der Windows Imaging-Komponente: Codec-Ermittlung und-Vermittlung**</span><span class="sxs-lookup"><span data-stu-id="9ff2a-124">**How the Windows Imaging Component Works: Codec Discovery and Arbitration**</span></span>](-wic-howwicworks.md)
</dt> </dl>

 

 



