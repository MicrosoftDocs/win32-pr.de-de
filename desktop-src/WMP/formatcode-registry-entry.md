---
title: Registrierungs Eintrag "Formatcode"
description: Registrierungs Eintrag "Formatcode"
ms.assetid: cc444eaa-6898-48ab-9573-9e7d5e25d6db
keywords:
- Windows Media Player, Formatcode-Registrierungseinträge
- Windows Media Player, Dateinamen Erweiterungen
- Windows Media Player, Registrierung
- Registrierung, Dateinamen Erweiterungen
- Registrierung, Formatcode-Einträge
- Registrierung, Einstellungen für Windows-Media Player
- Registrierungs Einstellungen für die Dateinamenerweiterung
- Formatcode-Registrierungseinträge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2318d32e9d7a08a2ae23b24e7acd2674b9eecb2
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104208735"
---
# <a name="formatcode-registry-entry"></a><span data-ttu-id="48014-111">Registrierungs Eintrag "Formatcode"</span><span class="sxs-lookup"><span data-stu-id="48014-111">FormatCode Registry Entry</span></span>

<span data-ttu-id="48014-112">Wenn Windows Media Player auf eine benutzerdefinierte Dateierweiterung trifft, sucht es nach einem Registrierungs Unterschlüssel, der der Erweiterung entspricht.</span><span class="sxs-lookup"><span data-stu-id="48014-112">When Windows Media Player encounters a custom file name extension, it looks for a registry subkey that matches the extension.</span></span> <span data-ttu-id="48014-113">Der Unterschlüssel wird in [Registrierungs Einstellungen für Dateinamen Erweiterungen](file-name-extension-registry-settings.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="48014-113">The subkey is described in [File Name Extension Registry Settings](file-name-extension-registry-settings.md).</span></span> <span data-ttu-id="48014-114">Einer der Registrierungseinträge, der unter dem Unterschlüssel der Erweiterung angezeigt werden kann, ist der **Formatcode** -Eintrag.</span><span class="sxs-lookup"><span data-stu-id="48014-114">One of the registry entries that can appear under the extension's subkey is the **FormatCode** entry.</span></span>

<span data-ttu-id="48014-115">Der Registrierungs Eintrag **Formatcode** gibt den MTP-Format Code (Media Transport Protocol) für Dateien an, die über die benutzerdefinierte Erweiterung verfügen.</span><span class="sxs-lookup"><span data-stu-id="48014-115">The **FormatCode** registry entry specifies the Media Transport Protocol (MTP) format code for files that have the custom extension.</span></span> <span data-ttu-id="48014-116">Der Registrierungs Eintrag " **Formatcode** " weist die folgende Form auf:</span><span class="sxs-lookup"><span data-stu-id="48014-116">The **FormatCode** registry entry has the following form.</span></span>



| <span data-ttu-id="48014-117">Name</span><span class="sxs-lookup"><span data-stu-id="48014-117">Name</span></span>       | <span data-ttu-id="48014-118">type</span><span class="sxs-lookup"><span data-stu-id="48014-118">Type</span></span>           | <span data-ttu-id="48014-119">Wert</span><span class="sxs-lookup"><span data-stu-id="48014-119">Value</span></span>                                                             |
|------------|----------------|-------------------------------------------------------------------|
| <span data-ttu-id="48014-120">Formatcode</span><span class="sxs-lookup"><span data-stu-id="48014-120">FormatCode</span></span> | <span data-ttu-id="48014-121">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="48014-121">**REG\_DWORD**</span></span> | <span data-ttu-id="48014-122">Eine positive 16-Bit-Ganzzahl, die das Format der Datei angibt.</span><span class="sxs-lookup"><span data-stu-id="48014-122">A 16-bit positive integer that identifies the format of the file.</span></span> |



 

<span data-ttu-id="48014-123">Wenn der Benutzer versucht, eine digitale Mediendatei mit einer benutzerdefinierten Dateinamenerweiterung auf ein tragbares Gerät zu kopieren, sucht Windows Media Player in der Registrierung nach einem Format Code, der der benutzerdefinierten Dateinamenerweiterung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="48014-123">When the user attempts to copy a digital media file that has a custom file name extension to a portable device, Windows Media Player looks in the registry to find a format code associated with the custom file name extension.</span></span> <span data-ttu-id="48014-124">Wenn Windows Media Player einen Format Code findet, verwendet er MTP, um zu bestimmen, ob das Gerät das benutzerdefinierte Dateiformat unterstützt.</span><span class="sxs-lookup"><span data-stu-id="48014-124">If Windows Media Player finds a format code, it uses MTP to determine whether the device supports the custom file format.</span></span> <span data-ttu-id="48014-125">Wenn das Gerät das-Format unterstützt, wird die Mediendatei ohne transcoded auf das Gerät kopiert.</span><span class="sxs-lookup"><span data-stu-id="48014-125">If the device supports the format, the media file is copied to the device without being transcoded.</span></span>

<span data-ttu-id="48014-126">Ein Gerät, das MTP unterstützt, kann Windows-Media Player mit einem deviceInfo-DataSet bereitstellen, das unter anderem eine Liste der vom Gerät unterstützten Formatcodes enthält.</span><span class="sxs-lookup"><span data-stu-id="48014-126">A device that supports MTP can supply Windows Media Player with a DeviceInfo dataset, which contains, among other things, a list of format codes supported by the device.</span></span>

<span data-ttu-id="48014-127">Wenn Sie gerade ein benutzerdefiniertes Dateiformat entwickeln, können Sie einen Format Code von Microsoft anfordern.</span><span class="sxs-lookup"><span data-stu-id="48014-127">If you are in the process of developing a custom file format, you can request a format code from Microsoft.</span></span> <span data-ttu-id="48014-128">Informationen zum Anfordern eines Formatierungscodes finden Sie im Microsoft Media Transport Protocol Porting Kit, das im [Microsoft Windows Media Developer Center](https://msdn.microsoft.com/windowsmedia/default.aspx)verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="48014-128">For information about how to request a format code, see the Microsoft Media Transport Protocol Porting Kit, which is available at the [Microsoft Windows Media Developer Center](https://msdn.microsoft.com/windowsmedia/default.aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="48014-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="48014-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48014-130">**Registrierungs Einstellungen für die Dateinamenerweiterung**</span><span class="sxs-lookup"><span data-stu-id="48014-130">**File Name Extension Registry Settings**</span></span>](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




