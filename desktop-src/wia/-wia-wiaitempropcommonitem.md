---
description: Die folgenden Geräteeigenschaften Konstanten müssen von allen iwiaitem-, IWiaItem2-und iwiadrvitem-Schnittstellen Schnittstellen unterstützt werden, sofern in ihren Beschreibungen nichts anderes angegeben ist.
ms.assetid: ef48313e-4df4-4ccd-a085-f714100885a7
title: Allgemeine WIA-Element Eigenschaften Konstanten (wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_IPA_ACCESS_RIGHTS
- WIA_IPA_APP_COLOR_MAPPING
- WIA_IPA_BITS_PER_CHANNEL
- WIA_IPA_BUFFER_SIZE
- WIA_IPA_BYTES_PER_LINE
- WIA_IPA_CHANNELS_PER_PIXEL
- WIA_IPA_COLOR_PROFILE
- WIA_IPA_COMPRESSION
- WIA_IPA_DATATYPE
- WIA_IPA_DEPTH
- WIA_IPA_FILENAME_EXTENSION
- WIA_IPA_FORMAT
- WIA_IPA_FULL_ITEM_NAME
- WIA_IPA_GAMMA_CURVES
- WIA_IPA_ICM_PROFILE_NAME
- WIA_IPA_ITEM_CATEGORY
- WIA_IPA_ITEM_FLAGS
- WIA_IPA_ITEM_NAME
- WIA_IPA_ITEM_SIZE
- WIA_IPA_ITEM_TIME
- WIA_IPA_ITEMS_STORED
- WIA_IPA_MIN_BUFFER_SIZE
- WIA_IPA_NUMBER_OF_LINES
- WIA_IPA_PIXELS_PER_LINE
- WIA_IPA_PLANAR
- WIA_IPA_PREFERRED_FORMAT
- WIA_IPA_PROP_STREAM_COMPAT_ID
- WIA_IPA_RAW_BITS_PER_CHANNEL
- WIA_IPA_REGION_TYPE
- WIA_IPA_SUPPRESS_PROPERTY_PAGE
- WIA_IPA_TYMED
- WIA_IPA_UPLOAD_ITEM_SIZE
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: d36a390256c6a9d183caa0f9231d2a92035d83da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344453"
---
# <a name="common-wia-item-property-constants"></a><span data-ttu-id="db91f-103">Allgemeine WIA-Element Eigenschaften Konstanten</span><span class="sxs-lookup"><span data-stu-id="db91f-103">Common WIA Item Property Constants</span></span>

<span data-ttu-id="db91f-104">Die folgenden Geräteeigenschaften Konstanten müssen von allen [**iwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)-, [**IWiaItem2**](-wia-iwiaitem2.md) -und [iwiadrvitem-Schnittstellen](https://msdn.microsoft.com/library/ms793976.aspx) Schnittstellen unterstützt werden, sofern in ihren Beschreibungen nichts anderes angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="db91f-104">The following device property constants must be supported by all [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem), [**IWiaItem2**](-wia-iwiaitem2.md) and [IWiaDrvItem Interface](https://msdn.microsoft.com/library/ms793976.aspx) interfaces unless otherwise noted in their descriptions.</span></span>

<span data-ttu-id="db91f-105">Das Präfix "WIA \_ IPA \_ " gibt eine Element Eigenschaft für alle Geräte an und ist die Benennungs Konvention, die in C/C++ verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="db91f-105">The prefix "WIA\_IPA\_" indicates an item property for all devices and is the naming convention used in C/C++.</span></span> <span data-ttu-id="db91f-106">Bei der Skripterstellung verwenden diese Konstanten das Präfix "Bild" und sind Teil des enumerierten Typs " [wiaitempropertyid](-wia-wiaitempropertyid.md) ".</span><span class="sxs-lookup"><span data-stu-id="db91f-106">For scripting purposes these constants use the prefix "Picture" and are part of the [WiaItemPropertyId](-wia-wiaitempropertyid.md) enumerated type.</span></span> <span data-ttu-id="db91f-107">Der entsprechende Elementname aus dieser Skript Enumeration wird in Klammern neben dem Konstanten Namen C/C++ in der folgenden Liste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="db91f-107">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="db91f-108">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="db91f-108">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="db91f-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="db91f-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ACCESS_RIGHTS"></span><span id="wia_ipa_access_rights"></span><dl> <span data-ttu-id="db91f-110"><dt><strong>WIA_IPA_ACCESS_RIGHTS</strong></dt> <dt>pictureaccessrights</dt> </span><span class="sxs-lookup"><span data-stu-id="db91f-110"><dt><strong>WIA_IPA_ACCESS_RIGHTS</strong></dt> <dt>PictureAccessRights</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="db91f-111">Dieses Flag steuert den Zugriff auf das Element und gibt an, ob das Element gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="db91f-111">This flag controls access to the item as well as whether the item is deleted.</span></span><br/> <span data-ttu-id="db91f-112">Erforderlich für alle WIA 2,0-Elemente.</span><span class="sxs-lookup"><span data-stu-id="db91f-112">Required for all WIA 2.0 items.</span></span><br/> <span data-ttu-id="db91f-113">Typ: <strong>VT_I4</strong>; Lese-/Schreibzugriff oder schreibgeschützt, abhängig von der Fähigkeit des Elements, die Zugriffsrechte zu ändern; Gültige Werte: WIA_PROP_FLAG</span><span class="sxs-lookup"><span data-stu-id="db91f-113">Type: <strong>VT_I4</strong>; Read/Write or Read Only, depending on the item's ability to have its access rights changed; Valid values: WIA_PROP_FLAG</span></span><br/> <span data-ttu-id="db91f-114">Die folgende Tabelle enthält die fünf Flags, die mit dieser Eigenschaft gültig sind.</span><span class="sxs-lookup"><span data-stu-id="db91f-114">The following table has the five flags that are valid with this property.</span></span><br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="db91f-115">Zugriffsrecht</span><span class="sxs-lookup"><span data-stu-id="db91f-115">Access Right</span></span></th>
<th><span data-ttu-id="db91f-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="db91f-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="db91f-117">WIA_ITEM_READ</span><span class="sxs-lookup"><span data-stu-id="db91f-117">WIA_ITEM_READ</span></span></td>
<td><span data-ttu-id="db91f-118">Das Element hat schreibgeschützten Zugriff.</span><span class="sxs-lookup"><span data-stu-id="db91f-118">Item has read-only access.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-119">WIA_ITEM_WRITE</span><span class="sxs-lookup"><span data-stu-id="db91f-119">WIA_ITEM_WRITE</span></span></td>
<td><span data-ttu-id="db91f-120">Das Element hat schreibgeschützten Zugriff.</span><span class="sxs-lookup"><span data-stu-id="db91f-120">Item has write-only access.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db91f-121">WIA_ITEM_CAN_BE_DELETED</span><span class="sxs-lookup"><span data-stu-id="db91f-121">WIA_ITEM_CAN_BE_DELETED</span></span></td>
<td><span data-ttu-id="db91f-122">Das Element hat nur den Lösch Zugriff.</span><span class="sxs-lookup"><span data-stu-id="db91f-122">Item has delete-only access.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-123">WIA_ITEM_RD</span><span class="sxs-lookup"><span data-stu-id="db91f-123">WIA_ITEM_RD</span></span></td>
<td><span data-ttu-id="db91f-124">WIA_ITEM_READ | WIA_ITEM_CAN_BE_DELETED</span><span class="sxs-lookup"><span data-stu-id="db91f-124">WIA_ITEM_READ | WIA_ITEM_CAN_BE_DELETED</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db91f-125">WIA_ITEM_RWD</span><span class="sxs-lookup"><span data-stu-id="db91f-125">WIA_ITEM_RWD</span></span></td>
<td><span data-ttu-id="db91f-126">WIA_ITEM_READ | WIA_ITEM_WRITE | WIA_ITEM_CAN_BE_DELETED</span><span class="sxs-lookup"><span data-stu-id="db91f-126">WIA_ITEM_READ | WIA_ITEM_WRITE | WIA_ITEM_CAN_BE_DELETED</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_APP_COLOR_MAPPING"></span><span id="wia_ipa_app_color_mapping"></span><dl> <span data-ttu-id="db91f-127"><dt><strong>WIA_IPA_APP_COLOR_MAPPING</strong></dt> <dt>pictureappcolormapping</dt> </span><span class="sxs-lookup"><span data-stu-id="db91f-127"><dt><strong>WIA_IPA_APP_COLOR_MAPPING</strong></dt> <dt>PictureAppColorMapping</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="db91f-128">Diese Eigenschaft ist für die zukünftige Verwendung reserviert und wird zu diesem Zeitpunkt nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="db91f-128">This property is reserved by for future use and is not implemented at this time.</span></span></p>
<p><span data-ttu-id="db91f-129">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="db91f-129">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_BITS_PER_CHANNEL"></span><span id="wia_ipa_bits_per_channel"></span><dl> <span data-ttu-id="db91f-130"><dt><strong>WIA_IPA_BITS_PER_CHANNEL</strong></dt> <dt>picturebitsperchannel</dt> </span><span class="sxs-lookup"><span data-stu-id="db91f-130"><dt><strong>WIA_IPA_BITS_PER_CHANNEL</strong></dt> <dt>PictureBitsPerChannel</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="db91f-131">Enthält die Anzahl der Bits pro Kanal für das Bild.</span><span class="sxs-lookup"><span data-stu-id="db91f-131">Contains the number of bits per channel for the image.</span></span> <span data-ttu-id="db91f-132">Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="db91f-132">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="db91f-133">Erforderlich für alle Erfassungs fähigen oder gespeicherten Bildelemente von WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="db91f-133">Required for all WIA 2.0 acquisition-enabled or stored image items.</span></span></p>
<p><span data-ttu-id="db91f-134">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="db91f-134">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_BUFFER_SIZE"></span><span id="wia_ipa_buffer_size"></span><dl> <span data-ttu-id="db91f-135"><dt><strong>WIA_IPA_BUFFER_SIZE</strong></dt> <dt>picturebuffersize</dt> </span><span class="sxs-lookup"><span data-stu-id="db91f-135"><dt><strong>WIA_IPA_BUFFER_SIZE</strong></dt> <dt>PictureBufferSize</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="db91f-136">Enthält die Größe des Puffers in Bytes, der während einer Datenübertragung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="db91f-136">Contains the size of the buffer, in bytes, used during a data transfer.</span></span> <span data-ttu-id="db91f-137">Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="db91f-137">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="db91f-138">Eine Anwendung kann diese Eigenschaft lesen, um die vom Treiber angegebene Puffergröße für Datenübertragungen zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="db91f-138">An application can read this property to determine the driver-specified buffer size for data transfers.</span></span> <span data-ttu-id="db91f-139">Der WIA-Dienst liest auch diese Eigenschaft, um während der Datenübertragung Arbeitsspeicher für den Mini Treiber zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="db91f-139">The WIA service also reads this property to allocate memory for the minidriver during the data transfer</span></span></p>
<p><span data-ttu-id="db91f-140">Optional für alle für die Übertragung aktivierten WIA 2,0-Elemente.</span><span class="sxs-lookup"><span data-stu-id="db91f-140">Optional for all transfer-enabled WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="db91f-141">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="db91f-141">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="db91f-142">Die <strong>WIA_IPA_BUFFER_SIZE</strong> -Eigenschaft enthält die minimale Datenmenge, die von einer Anwendung zu einem beliebigen Zeitpunkt angefordert werden kann.</span><span class="sxs-lookup"><span data-stu-id="db91f-142">The <strong>WIA_IPA_BUFFER_SIZE</strong> property contains is the minimum amount of data an application can request at any given time.</span></span> <span data-ttu-id="db91f-143">Je größer die Puffergröße ist, desto größer sind die Anforderungen an das Gerät.</span><span class="sxs-lookup"><span data-stu-id="db91f-143">The larger the buffer size, the larger the requests to the device will be.</span></span> <span data-ttu-id="db91f-144">Dies kann dazu führen, dass das Gerät langsam und nicht mehr reagiert, die Gesamtleistung des Systems verlangsamt und übermäßige Ressourcen beanspruchen kann.</span><span class="sxs-lookup"><span data-stu-id="db91f-144">This can make the device seem slow and unresponsive, can slow the overall system performance, and can consume excessive resources.</span></span> <span data-ttu-id="db91f-145">Puffergrößen, die zu klein sind, können die Leistung der Datenübertragung beeinträchtigen, da viele kleinere Anforderungen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="db91f-145">Buffer sizes that are too small can slow performance of the data transfer by requiring many smaller requests.</span></span> <span data-ttu-id="db91f-146">Wählen Sie eine angemessene Puffergröße aus, indem Sie die typische Größe einer Daten Anforderung an Ihr Gerät berücksichtigen und die Anzahl der Anforderungen mit der Größe dieser Anforderungen ausgleichen.</span><span class="sxs-lookup"><span data-stu-id="db91f-146">Choose a reasonable buffer size by considering the typical size of a data request to your device and balancing the number of requests against the size of those requests.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_BYTES_PER_LINE"></span><span id="wia_ipa_bytes_per_line"></span><dl> <span data-ttu-id="db91f-147"><dt><strong>WIA_IPA_BYTES_PER_LINE</strong></dt> <dt>picturebytesperline</dt> </span><span class="sxs-lookup"><span data-stu-id="db91f-147"><dt><strong>WIA_IPA_BYTES_PER_LINE</strong></dt> <dt>PictureBytesPerLine</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="db91f-148">Enthält die Anzahl der Bytes in einer Scan Zeile des Bilds.</span><span class="sxs-lookup"><span data-stu-id="db91f-148">Contains the number of bytes in one scan line of the image.</span></span> <span data-ttu-id="db91f-149">Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="db91f-149">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="db91f-150">Optional für alle WIA 2,0-Elemente.</span><span class="sxs-lookup"><span data-stu-id="db91f-150">Optional for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="db91f-151">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="db91f-151">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_CHANNELS_PER_PIXEL"></span><span id="wia_ipa_channels_per_pixel"></span><dl> <span data-ttu-id="db91f-152"><dt><strong>WIA_IPA_CHANNELS_PER_PIXEL</strong></dt> <dt>picturechannelsperpixel</dt> </span><span class="sxs-lookup"><span data-stu-id="db91f-152"><dt><strong>WIA_IPA_CHANNELS_PER_PIXEL</strong></dt> <dt>PictureChannelsPerPixel</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="db91f-153">Enthält die Anzahl der Kanäle pro Pixel für das Bild.</span><span class="sxs-lookup"><span data-stu-id="db91f-153">Contains the number of channels per pixel for the image.</span></span> <span data-ttu-id="db91f-154">Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="db91f-154">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="db91f-155">Erforderlich für alle Erfassungs fähigen oder gespeicherten Bildelemente von WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="db91f-155">Required for all WIA 2.0 acquisition-enabled or stored image items.</span></span></p>
<p><span data-ttu-id="db91f-156">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="db91f-156">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_COLOR_PROFILE"></span><span id="wia_ipa_color_profile"></span><dl> <span data-ttu-id="db91f-157"><dt><strong>WIA_IPA_COLOR_PROFILE</strong></dt> von " <dt>picturecolorprofile</dt> " </span><span class="sxs-lookup"><span data-stu-id="db91f-157"><dt><strong>WIA_IPA_COLOR_PROFILE</strong></dt> <dt>PictureColorProfile</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="db91f-158">Diese Eigenschaft ist für die zukünftige Verwendung reserviert und wird zu diesem Zeitpunkt nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="db91f-158">This property is reserved by for future use and is not implemented at this time.</span></span></p>
<p><span data-ttu-id="db91f-159">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="db91f-159">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_COMPRESSION"></span><span id="wia_ipa_compression"></span><dl> <span data-ttu-id="db91f-160"><dt><strong>WIA_IPA_COMPRESSION</strong></dt> <dt>picturecompression</dt> </span><span class="sxs-lookup"><span data-stu-id="db91f-160"><dt><strong>WIA_IPA_COMPRESSION</strong></dt> <dt>PictureCompression</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="db91f-161">Enthält den verwendeten aktuellen Komprimierungstyp.</span><span class="sxs-lookup"><span data-stu-id="db91f-161">Contains the current compression type used.</span></span> <span data-ttu-id="db91f-162">Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="db91f-162">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="db91f-163">Eine Anwendung liest diese Eigenschaft, um den Bild Komprimierungstyp zu bestimmen, oder legt diese Eigenschaft fest, um die Komprimierungs Einstellung zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="db91f-163">An application reads this property to determine the image compression type or sets this property to configure the compression setting.</span></span></p>
<p><span data-ttu-id="db91f-164">Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="db91f-164">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="db91f-165">Die folgende Tabelle enthält die Konstanten, die mit dieser Eigenschaft gültig sind.</span><span class="sxs-lookup"><span data-stu-id="db91f-165">The following table has the constants that are valid with this property.</span></span> <span data-ttu-id="db91f-166">Das Symbol <strong>V</strong> gibt an, dass die Konstante nur in Windows Vista und höher unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="db91f-166">The <strong>V</strong> symbol indicates that the constant is supported only in Windows Vista and later.</span></span> <span data-ttu-id="db91f-167">(Er ist nur über die <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> -Schnittstelle verfügbar.)</span><span class="sxs-lookup"><span data-stu-id="db91f-167">(It is only available through the <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> interface.)</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="db91f-168">Komprimierungstyp</span><span class="sxs-lookup"><span data-stu-id="db91f-168">Compression Type</span></span></th>
<th><span data-ttu-id="db91f-169">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="db91f-169">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="db91f-170">WIA_COMPRESSION_NONE</span><span class="sxs-lookup"><span data-stu-id="db91f-170">WIA_COMPRESSION_NONE</span></span></td>
<td><span data-ttu-id="db91f-171">Keine Komprimierung.</span><span class="sxs-lookup"><span data-stu-id="db91f-171">No compression.</span></span> <span data-ttu-id="db91f-172">Weitere Informationen finden <strong>Sie unter Hinweis</strong> .</span><span class="sxs-lookup"><span data-stu-id="db91f-172">See <strong>Note</strong> for more information.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-173">WIA_COMPRESSION_AUTO</span><span class="sxs-lookup"><span data-stu-id="db91f-173">WIA_COMPRESSION_AUTO</span></span></td>
<td><span data-ttu-id="db91f-174">Automatischer Komprimierungs Modus.</span><span class="sxs-lookup"><span data-stu-id="db91f-174">Automatic compression mode.</span></span> <span data-ttu-id="db91f-175">Weitere Informationen finden <strong>Sie unter Hinweis</strong> .</span><span class="sxs-lookup"><span data-stu-id="db91f-175">See <strong>Note</strong> for more information.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db91f-176">WIA_COMPRESSION_BI_RLE4</span><span class="sxs-lookup"><span data-stu-id="db91f-176">WIA_COMPRESSION_BI_RLE4</span></span></td>
<td><span data-ttu-id="db91f-177">RLE4-Komprimierung</span><span class="sxs-lookup"><span data-stu-id="db91f-177">RLE4 compression</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-178">WIA_COMPRESSION_BI_RLE8</span><span class="sxs-lookup"><span data-stu-id="db91f-178">WIA_COMPRESSION_BI_RLE8</span></span></td>
<td><span data-ttu-id="db91f-179">RLE8-Komprimierung</span><span class="sxs-lookup"><span data-stu-id="db91f-179">RLE8 compression</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db91f-180">WIA_COMPRESSION_G3</span><span class="sxs-lookup"><span data-stu-id="db91f-180">WIA_COMPRESSION_G3</span></span></td>
<td><span data-ttu-id="db91f-181">Komprimierung in Gruppe 3</span><span class="sxs-lookup"><span data-stu-id="db91f-181">Group 3 compression</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-182">WIA_COMPRESSION_G4</span><span class="sxs-lookup"><span data-stu-id="db91f-182">WIA_COMPRESSION_G4</span></span></td>
<td><span data-ttu-id="db91f-183">Komprimierung in Gruppe 4</span><span class="sxs-lookup"><span data-stu-id="db91f-183">Group 4 compression</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db91f-184">WIA_COMPRESSION_JPEG</span><span class="sxs-lookup"><span data-stu-id="db91f-184">WIA_COMPRESSION_JPEG</span></span></td>
<td><span data-ttu-id="db91f-185">JPEG-Komprimierung.</span><span class="sxs-lookup"><span data-stu-id="db91f-185">JPEG compression.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-186">WIA_COMPRESSION_JBIG<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="db91f-186">WIA_COMPRESSION_JBIG<strong>V</strong></span></span></td>
<td><span data-ttu-id="db91f-187">JBIG-Komprimierung.</span><span class="sxs-lookup"><span data-stu-id="db91f-187">JBIG compression.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db91f-188">WIA_COMPRESSION_JPEG2K<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="db91f-188">WIA_COMPRESSION_JPEG2K<strong>V</strong></span></span></td>
<td><span data-ttu-id="db91f-189">JPEG 2000-Komprimierung.</span><span class="sxs-lookup"><span data-stu-id="db91f-189">JPEG 2000 compression.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-190">WIA_COMPRESSION_PNG<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="db91f-190">WIA_COMPRESSION_PNG<strong>V</strong></span></span></td>
<td><span data-ttu-id="db91f-191">PNG-Komprimierung.</span><span class="sxs-lookup"><span data-stu-id="db91f-191">PNG compression.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
<p>[!Note]</p>
<p><span data-ttu-id="db91f-192">Wenn diese Eigenschaft WIA_COMPRESSION_NONE ist und WIA_IPA_FORMAT entweder WiaImgFmt_PDFA oder WiaImgFmt_XPS ist; WIA_COMPRESSION_NONE bedeutet dann, dass der Komprimierungs Modus nicht definiert ist und der Scanner einen Modus treffen muss.</span><span class="sxs-lookup"><span data-stu-id="db91f-192">When this property is WIA_COMPRESSION_NONE, and WIA_IPA_FORMAT is either WiaImgFmt_PDFA or WiaImgFmt_XPS; then WIA_COMPRESSION_NONE means that the compression mode is undefined and the scanner must decide on a mode.</span></span></p>
<p><span data-ttu-id="db91f-193">WIA_COMPRESSION_AUTO ist ein neuer Eigenschafts Wert, der für die WIA_IPA_COMPRESSION-Eigenschaft definiert ist.</span><span class="sxs-lookup"><span data-stu-id="db91f-193">WIA_COMPRESSION_AUTO is a new property value defined for the WIA_IPA_COMPRESSION property.</span></span> <span data-ttu-id="db91f-194">Dieser Wert gilt für alle programmierbaren Image-Datenquellen Elemente, einschließlich des Flatbed und des Feeds.</span><span class="sxs-lookup"><span data-stu-id="db91f-194">This value is valid for all programmable image data source items, including the Flatbed and Feeder.</span></span> <span data-ttu-id="db91f-195">Wenn dieser Wert vom WIA-Mini Treiber unterstützt wird, kann der WIA-Anwendungs Client WIA_IPA_COMPRESSION festlegen, um die automatische Komprimierung des Komprimierungs Modus auf dem Gerät zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="db91f-195">When this value is supported by the WIA mini-driver, the WIA application client can set WIA_IPA_COMPRESSION in order to enable automatic compression mode detection at the device.</span></span> <span data-ttu-id="db91f-196">WIA_COMPRESSION_AUTO kann mit und ohne vollständige automatische Farbe unterstützt oder aktiviert werden (WIA_DATA_AUTO und WIA_DEPTH_AUTO).</span><span class="sxs-lookup"><span data-stu-id="db91f-196">WIA_COMPRESSION_AUTO can work with and without full auto-color being supported or enabled (WIA_DATA_AUTO and WIA_DEPTH_AUTO).</span></span></p>
<p><span data-ttu-id="db91f-197">WIA_COMPRESSION_AUTO ist besonders nützlich bei Übertragungs Dateiformaten, die mehrere Datentypen und Bitraten unterstützen, z. b. WiaImgFmt_RAW.</span><span class="sxs-lookup"><span data-stu-id="db91f-197">WIA_COMPRESSION_AUTO is most useful with transfer file formats that support multiple data types and bit depths, such as WiaImgFmt_RAW.</span></span> <span data-ttu-id="db91f-198">Weitere Informationen zu Übertragungs Dateiformaten finden Sie unter WIA_IPA_FORMAT in dieser Tabelle.</span><span class="sxs-lookup"><span data-stu-id="db91f-198">For more information about transfer file formats, see WIA_IPA_FORMAT in this table.</span></span></p>
<p><span data-ttu-id="db91f-199">Es ist opitonale, wenn der WIA-Mini Treiber WIA_COMPRESSION_AUTO unterstützt.</span><span class="sxs-lookup"><span data-stu-id="db91f-199">It is opitonal for the WIA mini-driver to suport WIA_COMPRESSION_AUTO.</span></span> <span data-ttu-id="db91f-200">Wenn es unterstützt wird, darf der WIA-Mini Treiber ihn nie als Standardwert für WIA_IPA_COMPRESSION festlegen. Dieser Wert kann nur von der WIA-Anwendung festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="db91f-200">When it is supported, the WIA mini-driver must never set it as the default value for WIA_IPA_COMPRESSION; only the WIA application can set this value.</span></span></p>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_DATATYPE"></span><span id="wia_ipa_datatype"></span><dl> <span data-ttu-id="db91f-201"><dt><strong>WIA_IPA_DATATYPE</strong></dt> <dt>picturedatatype</dt> </span><span class="sxs-lookup"><span data-stu-id="db91f-201"><dt><strong>WIA_IPA_DATATYPE</strong></dt> <dt>PictureDatatype</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="db91f-202">Enthält die aktuelle Datentyp Einstellung für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="db91f-202">Contains the current data type setting for the device.</span></span> <span data-ttu-id="db91f-203">Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="db91f-203">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="db91f-204">Eine Anwendung liest diese Eigenschaft, um den Datentyp des Bilds zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="db91f-204">An application reads this property to determine the data type of the image.</span></span> <span data-ttu-id="db91f-205">Diese Eigenschaft wird von einer Anwendung geschrieben, um den aktuellen Datentyp des zu übertragenden Bilds festzulegen.</span><span class="sxs-lookup"><span data-stu-id="db91f-205">An application writes this property to set the current data type of the image about to be transferred.</span></span></p>
<p><span data-ttu-id="db91f-206">Diese Eigenschaft ist für alle WIA 2,0-Elemente erforderlich.</span><span class="sxs-lookup"><span data-stu-id="db91f-206">This property is required for all WIA 2.0 items.</span></span> <span data-ttu-id="db91f-207">Der Lese-/Schreibzugriff muss für alle für WIA 2,0 Erwerbs aktivierten Elemente und für WIA 2,0-Speicherelemente schreibgeschützt sein.</span><span class="sxs-lookup"><span data-stu-id="db91f-207">It must be Read/Write for all WIA 2.0 acquisition enabled items and Read Only for WIA 2.0 storage items.</span></span></p>
<p><span data-ttu-id="db91f-208">Typ: <strong>VT_I4</strong>; Zugriff für Windows Vista-Betriebssysteme vor Windows Vista: Diese Eigenschaft ist für Kameras und Lese-/Schreibzugriff auf Scanner schreibgeschützt. Access für Windows Vista und höher: Diese Eigenschaft ist nur für WIA_CATEGORY_FOLDER-und WIA_CATEGORY_FINISHED_FILE Elemente und Lese-/Schreibzugriff für alle anderen WIA 2,0-Element Kategorien schreibgeschützt. Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="db91f-208">Type: <strong>VT_I4</strong>; Access for pre-Windows Vista operating systems: This property is Read Only for cameras and Read/Write for scanners; Access for Windows Vista and later: This property is Read Only for WIA_CATEGORY_FOLDER and WIA_CATEGORY_FINISHED_FILE items, and Read/Write for all other WIA 2.0 item categories; Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="db91f-209">Die folgende Tabelle enthält die sechs Konstanten, die mit gültig sind, wenn <strong>WIA_IPA_FORMAT</strong> nicht auf WiaImgFmt_RAW festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="db91f-209">The following table has the six constants that are valid with when <strong>WIA_IPA_FORMAT</strong> is not set to WiaImgFmt_RAW.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="db91f-210">Datentyp</span><span class="sxs-lookup"><span data-stu-id="db91f-210">Data Type</span></span></th>
<th><span data-ttu-id="db91f-211">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="db91f-211">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="db91f-212">WIA_DATA_AUTO</span><span class="sxs-lookup"><span data-stu-id="db91f-212">WIA_DATA_AUTO</span></span></td>
<td><span data-ttu-id="db91f-213">Gültig für alle programmierbaren Image-Datenquellen Elemente, einschließlich des Flatbed und des Feeds.</span><span class="sxs-lookup"><span data-stu-id="db91f-213">Valid for all programmable image data source items, including the Flatbed and Feeder.</span></span> <span data-ttu-id="db91f-214">Wenn dieser Wert vom WIA-Mini Treiber unterstützt wird, kann der WIA-Anwendungs Client WIA_IPA_DATATYPE festlegen, um die automatische Farberkennung auf dem Gerät zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="db91f-214">When this value is supported by the WIA mini-driver, the WIA application client can set WIA_IPA_DATATYPE in order to enable automatic color detection at the device.</span></span> <span data-ttu-id="db91f-215">Wenn WIA_DATA_AUTO festgelegt ist, muss der WIA-Mini Treiber WIA_IPA_DEPTH auf demselben Element auf WIA_DEPTH_AUTO aktualisieren (Dies muss ein unterstützter Wert sein, wenn das Gerät automatische Farbe unterstützt).</span><span class="sxs-lookup"><span data-stu-id="db91f-215">When WIA_DATA_AUTO is set, the WIA mini-driver must update WIA_IPA_DEPTH on the same item to WIA_DEPTH_AUTO (which must be a supported value if the device supports automatic color).</span></span><br/> <span data-ttu-id="db91f-216">Dies ist ein optionaler Wert, der jedoch erforderlich ist, wenn WIA_DEPTH_AUTO für WIA_IPA_DEPTH unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="db91f-216">This is an optional value, but it is required when WIA_DEPTH_AUTO is supported for WIA_IPA_DEPTH.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-217">WIA_DATA_COLOR</span><span class="sxs-lookup"><span data-stu-id="db91f-217">WIA_DATA_COLOR</span></span></td>
<td><span data-ttu-id="db91f-218">Scan Daten sind rot, grün, blau (RGB).</span><span class="sxs-lookup"><span data-stu-id="db91f-218">Scan data is red, green, blue (RGB) color.</span></span> <span data-ttu-id="db91f-219">Das vollständige Farb Format wird mit den folgenden WIA-Eigenschaften beschrieben: <strong>WIA_IPA_CHANNELS_PER_PIXEL</strong></span><span class="sxs-lookup"><span data-stu-id="db91f-219">The full color format is described using the following WIA properties: <strong>WIA_IPA_CHANNELS_PER_PIXEL</strong></span></span><br/> <span data-ttu-id="db91f-220"><strong>WIA_IPA_BITS_PER_CHANNEL</strong></span><span class="sxs-lookup"><span data-stu-id="db91f-220"><strong>WIA_IPA_BITS_PER_CHANNEL</strong></span></span><br/> <span data-ttu-id="db91f-221"><strong>WIA_IPA_PLANAR</strong></span><span class="sxs-lookup"><span data-stu-id="db91f-221"><strong>WIA_IPA_PLANAR</strong></span></span><br/> <span data-ttu-id="db91f-222"><strong>WIA_IPA_PIXELS_PER_LINE</strong></span><span class="sxs-lookup"><span data-stu-id="db91f-222"><strong>WIA_IPA_PIXELS_PER_LINE</strong></span></span><br/> <span data-ttu-id="db91f-223"><strong>WIA_IPA_BYTES_PER_LINE</strong></span><span class="sxs-lookup"><span data-stu-id="db91f-223"><strong>WIA_IPA_BYTES_PER_LINE</strong></span></span><br/> <span data-ttu-id="db91f-224"><strong>WIA_IPA_NUMBER_OF_LINES</strong></span><span class="sxs-lookup"><span data-stu-id="db91f-224"><strong>WIA_IPA_NUMBER_OF_LINES</strong></span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db91f-225">WIA_DATA_COLOR_DITHER</span><span class="sxs-lookup"><span data-stu-id="db91f-225">WIA_DATA_COLOR_DITHER</span></span></td>
<td><span data-ttu-id="db91f-226">Identisch mit WIA_DATA_COLOR, mit dem Unterschied, dass die Daten mit dem aktuell ausgewählten Dithering-Muster ausgeblendet werden.</span><span class="sxs-lookup"><span data-stu-id="db91f-226">Same as WIA_DATA_COLOR except that the data is dithered using the currently selected dither pattern.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-227">WIA_DATA_COLOR_THRESHOLD</span><span class="sxs-lookup"><span data-stu-id="db91f-227">WIA_DATA_COLOR_THRESHOLD</span></span></td>
<td><span data-ttu-id="db91f-228">Identisch mit WIA_DATA_COLOR, mit dem Unterschied, dass der Schwellenwert beim Scannen der Daten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="db91f-228">Same as WIA_DATA_COLOR except that the threshold value is used when scanning the data.</span></span> <span data-ttu-id="db91f-229">Farbwerte für den <a href="https://msdn.microsoft.com/library/ms796233.aspx">WIA_IPS_THRESHOLD</a> Wert werden in vollständige Helligkeit konvertiert. Farben unter diesem Wert werden in schwarz konvertiert.</span><span class="sxs-lookup"><span data-stu-id="db91f-229">Color values over the <a href="https://msdn.microsoft.com/library/ms796233.aspx">WIA_IPS_THRESHOLD</a> value are converted to full brightness; colors under this value are converted to black.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db91f-230">WIA_DATA_DITHER</span><span class="sxs-lookup"><span data-stu-id="db91f-230">WIA_DATA_DITHER</span></span></td>
<td><span data-ttu-id="db91f-231">Scandaten werden mit dem aktuell ausgewählten Dithering-Muster ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="db91f-231">Scan data is dithered using the currently selected dither pattern.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-232">WIA_DATA_GRAYSCALE</span><span class="sxs-lookup"><span data-stu-id="db91f-232">WIA_DATA_GRAYSCALE</span></span></td>
<td><span data-ttu-id="db91f-233">Scan Daten repräsentieren die Intensität.</span><span class="sxs-lookup"><span data-stu-id="db91f-233">Scan data represents intensity.</span></span> <span data-ttu-id="db91f-234">Die Palette ist eine festgelegte, gleichmäßig entfernte graue Größe mit einer Tiefe, die durch <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> -Eigenschaft angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="db91f-234">The palette is a fixed, equally-spaced gray scale with a depth specified by <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> property.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db91f-235">WIA_DATA_THRESHOLD</span><span class="sxs-lookup"><span data-stu-id="db91f-235">WIA_DATA_THRESHOLD</span></span></td>
<td><span data-ttu-id="db91f-236">Der Schwellenwert ist ein Bit pro Pixel von schwarzen und weißen Daten.</span><span class="sxs-lookup"><span data-stu-id="db91f-236">The threshold is one bit per pixel of black-and-white data.</span></span> <span data-ttu-id="db91f-237">Daten über den aktuellen Wert <a href="https://msdn.microsoft.com/library/ms796233.aspx">WIA_IPS_THRESHOLD</a> werden in weiß konvertiert. Daten unter diesem Wert werden in schwarz konvertiert.</span><span class="sxs-lookup"><span data-stu-id="db91f-237">Data over the current value of <a href="https://msdn.microsoft.com/library/ms796233.aspx">WIA_IPS_THRESHOLD</a> is converted to white; data under this value is converted to black.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="db91f-238">Die <strong>WIA_IPA_DATATYPE</strong> -Eigenschaft wird auch verwendet, um den Typ der zu verwendenden rohdatenübertragung zu beschreiben, wenn die Anwendung WiaImgFmt_RAW festlegt.</span><span class="sxs-lookup"><span data-stu-id="db91f-238">The <strong>WIA_IPA_DATATYPE</strong> property is also used to describe the type of RAW data transfer to be used when the application sets WiaImgFmt_RAW.</span></span> <span data-ttu-id="db91f-239">Der Treiber sollte die <strong>WIA_IPA_DATATYPE</strong> -Eigenschaft auf eine Liste zulässiger Werte festlegen, von denen die Anwendung eine Auswahl treffen kann.</span><span class="sxs-lookup"><span data-stu-id="db91f-239">The driver should set the <strong>WIA_IPA_DATATYPE</strong> property to a list of allowed values from which the application can pick one.</span></span></p>
<p><span data-ttu-id="db91f-240">Wenn das Gerät nur auf einen einzelnen Wert festgelegt werden kann, erstellen Sie einen <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> Typ, und platzieren Sie den gültigen Wert darin.</span><span class="sxs-lookup"><span data-stu-id="db91f-240">If the device can be set to only a single value, create a <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> type, and place the valid value in it.</span></span></p>
<p><span data-ttu-id="db91f-241">Überprüfen Sie die <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> -Eigenschaft, um die Bittiefe zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="db91f-241">Check the <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> property to determine the bit depth.</span></span> <span data-ttu-id="db91f-242">Diese Eigenschaft enthält in der Regel einen einzelnen Wert für Kameras.</span><span class="sxs-lookup"><span data-stu-id="db91f-242">This property usually contains a single value for cameras.</span></span></p>
<p><span data-ttu-id="db91f-243">In der folgenden Tabelle werden die Konstanten aufgelistet, die mit <strong>WIA_IPA_DATATYPE</strong> gültig sind, wenn <strong>WIA_IPA_FORMAT</strong> auf WiaImgFmt_RAW festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="db91f-243">The following table lists the constants that are valid with <strong>WIA_IPA_DATATYPE</strong> when <strong>WIA_IPA_FORMAT</strong> is set to WiaImgFmt_RAW.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="db91f-244">Datentyp</span><span class="sxs-lookup"><span data-stu-id="db91f-244">Data Type</span></span></th>
<th><span data-ttu-id="db91f-245">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="db91f-245">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="db91f-246">WIA_DATA_GRAYSCALE</span><span class="sxs-lookup"><span data-stu-id="db91f-246">WIA_DATA_GRAYSCALE</span></span></td>
<td><span data-ttu-id="db91f-247">Scan Daten repräsentieren die Intensität.</span><span class="sxs-lookup"><span data-stu-id="db91f-247">Scan data represents intensity.</span></span> <span data-ttu-id="db91f-248">Die Palette ist eine festgelegte, gleichmäßig entfernte Graustufen mit einer Tiefe, die durch die <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> -Eigenschaft angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="db91f-248">The palette is a fixed, equally spaced grayscale with a depth specified by the <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> property.</span></span> <span data-ttu-id="db91f-249"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> muss auf 1 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="db91f-249"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-250">WIA_DATA_RAW_BGR</span><span class="sxs-lookup"><span data-stu-id="db91f-250">WIA_DATA_RAW_BGR</span></span></td>
<td><span data-ttu-id="db91f-251">Scandaten befinden sich im BGR-colorspace (blau-grün-rot).</span><span class="sxs-lookup"><span data-stu-id="db91f-251">Scan data is in the BGR (blue-green-red) colorspace.</span></span> <span data-ttu-id="db91f-252">Das vollständige Farb Format wird mithilfe der folgenden Eigenschaften beschrieben: <a href="https://msdn.microsoft.com/library/ms796163.aspx">WIA_IPA_CHANNELS_PER_PIXEL</a></span><span class="sxs-lookup"><span data-stu-id="db91f-252">The full color format is described using the followingWIAproperties: <a href="https://msdn.microsoft.com/library/ms796163.aspx">WIA_IPA_CHANNELS_PER_PIXEL</a></span></span><br/> <span data-ttu-id="db91f-253"><a href="https://msdn.microsoft.com/library/ms795997.aspx">WIA_IPA_BITS_PER_CHANNEL</a></span><span class="sxs-lookup"><span data-stu-id="db91f-253"><a href="https://msdn.microsoft.com/library/ms795997.aspx">WIA_IPA_BITS_PER_CHANNEL</a></span></span><br/> <span data-ttu-id="db91f-254"><a href="https://msdn.microsoft.com/library/ms796567.aspx">WIA_IPA_PIXELS_PER_LINE</a></span><span class="sxs-lookup"><span data-stu-id="db91f-254"><a href="https://msdn.microsoft.com/library/ms796567.aspx">WIA_IPA_PIXELS_PER_LINE</a></span></span><br/> <span data-ttu-id="db91f-255"><a href="https://msdn.microsoft.com/library/ms796404.aspx">WIA_IPA_BYTES_PER_LINE</a></span><span class="sxs-lookup"><span data-stu-id="db91f-255"><a href="https://msdn.microsoft.com/library/ms796404.aspx">WIA_IPA_BYTES_PER_LINE</a></span></span><br/> <span data-ttu-id="db91f-256"><a href="https://msdn.microsoft.com/library/ms795916.aspx">WIA_IPA_NUMBER_OF_LINES</a></span><span class="sxs-lookup"><span data-stu-id="db91f-256"><a href="https://msdn.microsoft.com/library/ms795916.aspx">WIA_IPA_NUMBER_OF_LINES</a></span></span><br/> <span data-ttu-id="db91f-257"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> muss auf 3 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="db91f-257"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 3.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db91f-258">WIA_DATA_RAW_CMY</span><span class="sxs-lookup"><span data-stu-id="db91f-258">WIA_DATA_RAW_CMY</span></span></td>
<td><span data-ttu-id="db91f-259">Scandaten befinden sich in der "Cyan-Magenta-Yellow (CMY)"-colorspace.</span><span class="sxs-lookup"><span data-stu-id="db91f-259">Scan data is in the cyan-magenta-yellow (CMY) colorspace.</span></span> <span data-ttu-id="db91f-260">Das vollständige Farb Format wird mit denselben WIA-Eigenschaften wie in WIA_DATA_RAW_BGR beschrieben.</span><span class="sxs-lookup"><span data-stu-id="db91f-260">The full color format is described using the same WIA properties as in WIA_DATA_RAW_BGR.</span></span> <span data-ttu-id="db91f-261"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> muss auf 3 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="db91f-261"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 3.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-262">WIA_DATA_RAW_CMYK</span><span class="sxs-lookup"><span data-stu-id="db91f-262">WIA_DATA_RAW_CMYK</span></span></td>
<td><span data-ttu-id="db91f-263">Scandaten befinden sich im "Cyan-Magenta-Yellow-Black (CMYK) ColorSpace".</span><span class="sxs-lookup"><span data-stu-id="db91f-263">Scan data is in the cyan-magenta-yellow-black (CMYK) colorspace.</span></span> <span data-ttu-id="db91f-264">Das vollständige Farb Format wird mit denselben WIA-Eigenschaften wie in WIA_DATA_RAW_BGR beschrieben.</span><span class="sxs-lookup"><span data-stu-id="db91f-264">The full color format is described using the same WIA properties as in WIA_DATA_RAW_BGR.</span></span> <span data-ttu-id="db91f-265"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> muss auf 4 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="db91f-265"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 4.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db91f-266">WIA_DATA_RAW_RGB</span><span class="sxs-lookup"><span data-stu-id="db91f-266">WIA_DATA_RAW_RGB</span></span></td>
<td><span data-ttu-id="db91f-267">Überprüfungs Daten befinden sich in der Farbe Rot-Grün-Blau (RGB).</span><span class="sxs-lookup"><span data-stu-id="db91f-267">Scan data is in the red-green-blue (RGB) colorspace.</span></span> <span data-ttu-id="db91f-268">Das vollständige Farb Format wird mit denselben WIA-Eigenschaften wie in WIA_DATA_RAW_BGR beschrieben.</span><span class="sxs-lookup"><span data-stu-id="db91f-268">The full color format is described using the same WIA properties as in WIA_DATA_RAW_BGR.</span></span> <span data-ttu-id="db91f-269"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> muss auf 3 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="db91f-269"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 3.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-270">WIA_DATA_RAW_YUV</span><span class="sxs-lookup"><span data-stu-id="db91f-270">WIA_DATA_RAW_YUV</span></span></td>
<td><span data-ttu-id="db91f-271">Die Überprüfungs Daten befinden sich im YUV-colorspace (Leuchtkraft-Blue Difference-Red Difference).</span><span class="sxs-lookup"><span data-stu-id="db91f-271">Scan data is in the luminance-blue difference-red difference (YUV) colorspace.</span></span> <span data-ttu-id="db91f-272">Das vollständige Farb Format wird mit denselben WIA-Eigenschaften wie in WIA_DATA_RAW_BGR beschrieben.</span><span class="sxs-lookup"><span data-stu-id="db91f-272">The full color format is described using the same WIA properties as in WIA_DATA_RAW_BGR.</span></span> <span data-ttu-id="db91f-273"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> muss auf 3 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="db91f-273"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 3.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db91f-274">WIA_DATA_RAW_YUVK</span><span class="sxs-lookup"><span data-stu-id="db91f-274">WIA_DATA_RAW_YUVK</span></span></td>
<td><span data-ttu-id="db91f-275">Scandaten befinden sich in der "Leuchtkraft-Blue Difference-Red Difference-Black (yuvk) ColorSpace".</span><span class="sxs-lookup"><span data-stu-id="db91f-275">Scan data is in the luminance-blue difference-red difference-black (YUVK) colorspace.</span></span> <span data-ttu-id="db91f-276">Das vollständige Farb Format wird mit denselben WIA-Eigenschaften wie in WIA_DATA_RAW_BGR beschrieben.</span><span class="sxs-lookup"><span data-stu-id="db91f-276">The full color format is described using the same WIA properties as in WIA_DATA_RAW_BGR.</span></span> <span data-ttu-id="db91f-277"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> muss auf 4 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="db91f-277"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 4.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_DEPTH"></span><span id="wia_ipa_depth"></span><dl> <span data-ttu-id="db91f-278"><dt><strong>WIA_IPA_DEPTH</strong></dt> <dt>picturetiefe</dt> </span><span class="sxs-lookup"><span data-stu-id="db91f-278"><dt><strong>WIA_IPA_DEPTH</strong></dt> <dt>PictureDepth</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="db91f-279">WIA_IPA_DEPTH enthält die Bittiefe-Einstellung eines Bilds.</span><span class="sxs-lookup"><span data-stu-id="db91f-279">WIA_IPA_DEPTH Contains the bit depth setting of an image.</span></span> <span data-ttu-id="db91f-280">Der Mini Treiber erstellt und verwaltet diese Eigenschaft. Eine Anwendung liest diese Eigenschaft, um die Bittiefe-Einstellung des Bilds zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="db91f-280">The minidriver creates and maintains this property.An application reads this property to determine the bit depth setting of the image.</span></span> <span data-ttu-id="db91f-281">Die Anwendung kann diesen Wert möglicherweise auch auf die gewünschte Bittiefe festlegen.</span><span class="sxs-lookup"><span data-stu-id="db91f-281">The application might also be able to set this value to the desired bit depth.</span></span></p>
<p><span data-ttu-id="db91f-282">Wenn das Gerät nur auf einen einzelnen Wert festgelegt werden kann, erstellen Sie einen <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> Typ, und platzieren Sie den gültigen Wert darin.</span><span class="sxs-lookup"><span data-stu-id="db91f-282">If the device can be set to only a single value, create a <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> type and place the valid value in it.</span></span></p>
<p><span data-ttu-id="db91f-283">Diese Eigenschaft ist für alle WIA 2,0-Elemente erforderlich.</span><span class="sxs-lookup"><span data-stu-id="db91f-283">This property is required for all WIA 2.0 items.</span></span> <span data-ttu-id="db91f-284">Der Lese-/Schreibzugriff muss für alle für WIA 2,0 Erwerbs aktivierten Elemente und für WIA 2,0-Speicherelemente schreibgeschützt sein.</span><span class="sxs-lookup"><span data-stu-id="db91f-284">It must be Read/Write for all WIA 2.0 acquisition enabled items and Read Only for WIA 2.0 storage items.</span></span></p>
<p><span data-ttu-id="db91f-285">Typ: <strong>VT_I4</strong>; Zugriff für Windows Vista-Betriebssysteme vor Windows Vista: Lesen/Schreiben; Access für Windows Vista und höher: Diese Eigenschaft ist nur für WIA_CATEGORY_FOLDER-und WIA_CATEGORY_FINISHED_FILE Elemente und Lese-/Schreibzugriff für alle anderen WIA 2,0-Element Kategorien schreibgeschützt. Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="db91f-285">Type: <strong>VT_I4</strong>; Access for pre-Windows Vista operating systems: Read/Write; Access for Windows Vista and later: This property is Read Only for WIA_CATEGORY_FOLDER and WIA_CATEGORY_FINISHED_FILE items, and Read/Write for all other WIA 2.0 item categories; Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="db91f-286">WIA_DEPTH_AUTO ist als 0 Bits pro Pixel definiert, und es handelt sich um einen neuen Eigenschafts Wert, der für die WIA_IPA_DEPTH definiert ist.</span><span class="sxs-lookup"><span data-stu-id="db91f-286">WIA_DEPTH_AUTO is defined as 0 bits per pixel, and it is a new property value defined for the WIA_IPA_DEPTH.</span></span> <span data-ttu-id="db91f-287">Dieser Wert gilt für alle programmierbaren Image-Datenquellen Elemente, einschließlich des Flatbed und des Feeds.</span><span class="sxs-lookup"><span data-stu-id="db91f-287">This value is valid for all programmable image data source items, including the Flatbed and Feeder.</span></span> <span data-ttu-id="db91f-288">Wenn WIA_DEPTH_AUTO vom WIA-Mini Treiber unterstützt wird, kann der WIA-Anwendungs Client WIA_IPA_DEPTH auf diesen Wert festlegen, um die automatische Erkennung von Farben auf dem Gerät zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="db91f-288">When WIA_DEPTH_AUTO is supported by the WIA mini-driver, the WIA application client can set WIA_IPA_DEPTH to this value, to enable automatic color detection at the device.</span></span> <span data-ttu-id="db91f-289">Wenn WIA_DEPTH_AUTO festgelegt ist, muss der WIA-Mini Treiber WIA_IPA_DATATYPE auf demselben Element auf WIA_DATA_AUTO aktualisieren (Dies muss ein unterstützter Wert sein, wenn das Gerät automatische Farbe unterstützt).</span><span class="sxs-lookup"><span data-stu-id="db91f-289">When WIA_DEPTH_AUTO is set, the WIA mini-driver must update WIA_IPA_DATATYPE on the same item to WIA_DATA_AUTO (which must be a supported value, if the device supports automatic color).</span></span></p>
<p><span data-ttu-id="db91f-290">WIA_DEPTH_AUTO ist ein optionaler Wert, wird jedoch benötigt, wenn WIA_DATA_AUTO für WIA_IPA_DATATYPE unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="db91f-290">WIA_DEPTH_AUTO is an optional value, but it becomes required when WIA_DATA_AUTO is supported for WIA_IPA_DATATYPE.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_FILENAME_EXTENSION"></span><span id="wia_ipa_filename_extension"></span><dl> <span data-ttu-id="db91f-291"><dt><strong>WIA_IPA_FILENAME_EXTENSION</strong></dt> <dt>picturedateinameextension</dt> </span><span class="sxs-lookup"><span data-stu-id="db91f-291"><dt><strong>WIA_IPA_FILENAME_EXTENSION</strong></dt> <dt>PictureFilenameExtension</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="db91f-292">Enthält die Dateinamenerweiterung für ein bestimmtes Dateiformat.</span><span class="sxs-lookup"><span data-stu-id="db91f-292">Contains the file name extension for a particular file format.</span></span> <span data-ttu-id="db91f-293">Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="db91f-293">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="db91f-294">Optional für alle für die Übertragung aktivierten WIA 2,0-Elemente.</span><span class="sxs-lookup"><span data-stu-id="db91f-294">Optional for all transfer-enabled WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="db91f-295">Typ: <strong>VT_BSTR</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="db91f-295">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="db91f-296">Der Treiber aktualisiert diese Eigenschaft, um den aktuellen Wert der <a href="https://msdn.microsoft.com/library/ms796440.aspx">WIA_IPA_FORMAT</a> -Eigenschaft widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="db91f-296">The driver updates this property to reflect the current value of the <a href="https://msdn.microsoft.com/library/ms796440.aspx">WIA_IPA_FORMAT</a> property.</span></span></p>
<p><span data-ttu-id="db91f-297">Wenn <strong>WIA_IPA_FORMAT</strong> z. b. WiaImgFmt_JPEG ist, sollte <a href="-wia-property-attributes.md">WIA_IPA_FILENAME_EXTENSION</a> <strong>JPG</strong>lauten.</span><span class="sxs-lookup"><span data-stu-id="db91f-297">For example, if <strong>WIA_IPA_FORMAT</strong> is WiaImgFmt_JPEG, then <a href="-wia-property-attributes.md">WIA_IPA_FILENAME_EXTENSION</a> should be <strong>jpg</strong>.</span></span> <span data-ttu-id="db91f-298">Wenn <strong>WIA_IPA_FORMAT</strong> WiaImgFmt_BMP ist, sollte WIA_IPA_FILENAME_EXTENSION BMP lauten.</span><span class="sxs-lookup"><span data-stu-id="db91f-298">If <strong>WIA_IPA_FORMAT</strong> is WiaImgFmt_BMP, then WIA_IPA_FILENAME_EXTENSION should be BMP.</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="db91f-299">Die Dateinamenerweiterung enthält nicht den Punkt.</span><span class="sxs-lookup"><span data-stu-id="db91f-299">The file name extension does not include the dot.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="db91f-300">Diese Eigenschaft wird für Treiber empfohlen, die Standardformate unterstützen und für Treiber erforderlich sind, die benutzerdefinierte Formate implementieren.</span><span class="sxs-lookup"><span data-stu-id="db91f-300">This property is recommended for drivers that support standard formats and is required for drivers that implement custom-defined formats.</span></span> <span data-ttu-id="db91f-301">Er informiert die Anwendung über die richtige Dateierweiterung, die während der Übertragung privat formatierter Dateien verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="db91f-301">It informs the application of the correct file name extension to use during the transfer of privately formatted files.</span></span> <span data-ttu-id="db91f-302">Wenn z. b. der a. Datum Corporation einen WIA-Treiber erstellt hat, der eine Datei in einem neuen Format übertragen hat, könnte das Unternehmen eine Erweiterung von &quot; ADC angeben &quot; .</span><span class="sxs-lookup"><span data-stu-id="db91f-302">For example, if the A. Datum Corporation created a WIA driver that transferred a file in a new format, the company could specify an extension of &quot;adc&quot;.</span></span> <span data-ttu-id="db91f-303">Dies ermöglicht es Anwendungen, Daten in diesem Format in eine Datei zu übertragen und einen Dateinamen zu erstellen, z <em>. b. MyFile. ADC</em>, was für andere nützlich ist, die die neue Erweiterung verstanden haben.</span><span class="sxs-lookup"><span data-stu-id="db91f-303">This allows applications to transfer data in that format to a file and to create a file name such as <em>myfile.adc</em>,which is useful to others who understand the new extension.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_FORMAT"></span><span id="wia_ipa_format"></span><dl> <span data-ttu-id="db91f-304"><dt><strong>WIA_IPA_FORMAT</strong></dt> <dt>PictureFormat</dt> </span><span class="sxs-lookup"><span data-stu-id="db91f-304"><dt><strong>WIA_IPA_FORMAT</strong></dt> <dt>PictureFormat</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="db91f-305">Enthält das aktuelle Format des zu übertragenden Bilds.</span><span class="sxs-lookup"><span data-stu-id="db91f-305">Contains the current format of the image about to be transferred.</span></span></p>
<p><span data-ttu-id="db91f-306">Eine Anwendung liest diese Eigenschaft, um das Format des Abbilds zu ermitteln, das Sie erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="db91f-306">An application reads this property to determine the format of the image that it is about to receive.</span></span> <span data-ttu-id="db91f-307">Diese Eigenschaft wird von einer Anwendung geschrieben, um das Format festzulegen.</span><span class="sxs-lookup"><span data-stu-id="db91f-307">An application writes this property to set the format.</span></span> <span data-ttu-id="db91f-308">Diese Eigenschaft hängt von der <a href="https://msdn.microsoft.com/library/ms795488.aspx">WIA_IPA_TYMED</a> -Eigenschaft ab.</span><span class="sxs-lookup"><span data-stu-id="db91f-308">This property depends on the <a href="https://msdn.microsoft.com/library/ms795488.aspx">WIA_IPA_TYMED</a> property.</span></span> <span data-ttu-id="db91f-309">Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="db91f-309">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="db91f-310">Wenn das Gerät nur auf einen einzelnen Wert festgelegt werden kann, erstellen Sie einen <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> Typ, und platzieren Sie den gültigen Wert darin.</span><span class="sxs-lookup"><span data-stu-id="db91f-310">If the device can be set to only a single value, create a <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> type, and place the valid value in it.</span></span></p>
<p><span data-ttu-id="db91f-311">Typ: <strong>CLSID</strong>, Access: Read/Write, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="db91f-311">Type: <strong>CLSID</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="db91f-312">In der folgenden Tabelle werden die Konstanten aufgelistet, die mit dieser Eigenschaft gültig sind.</span><span class="sxs-lookup"><span data-stu-id="db91f-312">The following table lists the constants that are valid with this property.</span></span> <span data-ttu-id="db91f-313">Das Sternchen \* gibt an, dass die Konstante in Windows Vista nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="db91f-313">The asterisk \* indicates that the constant is not supported in Windows Vista.</span></span> <span data-ttu-id="db91f-314">(Er ist nur über die <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>iwiaitem</strong></a> -Schnittstelle verfügbar.) Das doppelte Sternchen \* \* gibt an, dass die Konstante weder in Windows Server 2003 noch in Windows Vista unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="db91f-314">(It is only available through the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> interface.) The double asterisk \*\* indicates that the constant is not supported in either Windows Server 2003 or Windows Vista.</span></span> <span data-ttu-id="db91f-315">Das Symbol <strong>V</strong> gibt an, dass die Konstante nur in Windows Vista und höher unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="db91f-315">The <strong>V</strong> symbol indicates that the constant is supported only in Windows Vista and later.</span></span> <span data-ttu-id="db91f-316">(Er ist nur über die <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> -Schnittstelle verfügbar.)</span><span class="sxs-lookup"><span data-stu-id="db91f-316">(It is only available through the <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> interface.)</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="db91f-317">Format</span><span class="sxs-lookup"><span data-stu-id="db91f-317">Format</span></span></th>
<th><span data-ttu-id="db91f-318">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="db91f-318">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="db91f-319">WiaAudFmt_AIFF</span><span class="sxs-lookup"><span data-stu-id="db91f-319">WiaAudFmt_AIFF</span></span></td>
<td><span data-ttu-id="db91f-320">AIFF-Audioformat</span><span class="sxs-lookup"><span data-stu-id="db91f-320">AIFF audio format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-321">WiaAudFmt_MP3</span><span class="sxs-lookup"><span data-stu-id="db91f-321">WiaAudFmt_MP3</span></span></td>
<td><span data-ttu-id="db91f-322">MP3-Audioformat</span><span class="sxs-lookup"><span data-stu-id="db91f-322">MP3 audio format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db91f-323">WiaAudFmt_WAV</span><span class="sxs-lookup"><span data-stu-id="db91f-323">WiaAudFmt_WAV</span></span></td>
<td><span data-ttu-id="db91f-324">WAV-Audioformat</span><span class="sxs-lookup"><span data-stu-id="db91f-324">WAV audio format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-325">WiaAudFmt_WMA</span><span class="sxs-lookup"><span data-stu-id="db91f-325">WiaAudFmt_WMA</span></span></td>
<td><span data-ttu-id="db91f-326">WMA-Audioformat</span><span class="sxs-lookup"><span data-stu-id="db91f-326">WMA audio format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db91f-327">WiaImgFmt_ASF \* \*</span><span class="sxs-lookup"><span data-stu-id="db91f-327">WiaImgFmt_ASF\*\*</span></span></td>
<td><span data-ttu-id="db91f-328">ASF-Videoformat</span><span class="sxs-lookup"><span data-stu-id="db91f-328">ASF video format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-329">WiaImgFmt_AVI \* \*</span><span class="sxs-lookup"><span data-stu-id="db91f-329">WiaImgFmt_AVI\*\*</span></span></td>
<td><span data-ttu-id="db91f-330">AVI-Videoformat</span><span class="sxs-lookup"><span data-stu-id="db91f-330">AVI video format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db91f-331">WiaImgFmt_BMP</span><span class="sxs-lookup"><span data-stu-id="db91f-331">WiaImgFmt_BMP</span></span></td>
<td><span data-ttu-id="db91f-332">Windows-Bitmap mit einer Header Datei</span><span class="sxs-lookup"><span data-stu-id="db91f-332">Windows bitmap with a header file</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-333">WiaImgFmt_CIFF \*</span><span class="sxs-lookup"><span data-stu-id="db91f-333">WiaImgFmt_CIFF\*</span></span></td>
<td><span data-ttu-id="db91f-334">Kamerabild-Dateiformat</span><span class="sxs-lookup"><span data-stu-id="db91f-334">Camera Image File format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db91f-335">WiaImgFmt_DPOF</span><span class="sxs-lookup"><span data-stu-id="db91f-335">WiaImgFmt_DPOF</span></span></td>
<td><span data-ttu-id="db91f-336">DPOF-Druckformat</span><span class="sxs-lookup"><span data-stu-id="db91f-336">DPOF printing format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-337">WiaImgFmt_EMF</span><span class="sxs-lookup"><span data-stu-id="db91f-337">WiaImgFmt_EMF</span></span></td>
<td><span data-ttu-id="db91f-338">Erweiterte Windows-Metadatendatei</span><span class="sxs-lookup"><span data-stu-id="db91f-338">Extended Windows metafile</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db91f-339">WiaImgFmt_EXEC</span><span class="sxs-lookup"><span data-stu-id="db91f-339">WiaImgFmt_EXEC</span></span></td>
<td><span data-ttu-id="db91f-340">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="db91f-340">Executable file</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-341">WiaImgFmt_EXIF</span><span class="sxs-lookup"><span data-stu-id="db91f-341">WiaImgFmt_EXIF</span></span></td>
<td><span data-ttu-id="db91f-342">Austauschbares Datei Format</span><span class="sxs-lookup"><span data-stu-id="db91f-342">Exchangeable File Format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db91f-343">WiaImgFmt_FLASHPIX</span><span class="sxs-lookup"><span data-stu-id="db91f-343">WiaImgFmt_FLASHPIX</span></span></td>
<td><span data-ttu-id="db91f-344">Format von Flash pix</span><span class="sxs-lookup"><span data-stu-id="db91f-344">FlashPix format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-345">WiaImgFmt_GIF</span><span class="sxs-lookup"><span data-stu-id="db91f-345">WiaImgFmt_GIF</span></span></td>
<td><span data-ttu-id="db91f-346">GIF-Bildformat</span><span class="sxs-lookup"><span data-stu-id="db91f-346">GIF image format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db91f-347">WiaImgFmt_HTML</span><span class="sxs-lookup"><span data-stu-id="db91f-347">WiaImgFmt_HTML</span></span></td>
<td><span data-ttu-id="db91f-348">HTML-Format</span><span class="sxs-lookup"><span data-stu-id="db91f-348">HTML format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-349">WiaImgFmt_ICO</span><span class="sxs-lookup"><span data-stu-id="db91f-349">WiaImgFmt_ICO</span></span></td>
<td><span data-ttu-id="db91f-350">Windows-Symbol Dateiformat</span><span class="sxs-lookup"><span data-stu-id="db91f-350">Windows icon file format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db91f-351">WiaImgFmt_JBIG<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="db91f-351">WiaImgFmt_JBIG<strong>V</strong></span></span></td>
<td><span data-ttu-id="db91f-352">Das gemeinsame Format der Abbildung Experts Group (JBIG) der bidirektionalen Ebene.</span><span class="sxs-lookup"><span data-stu-id="db91f-352">The Joint Bi-level Image Experts Group (JBIG) format.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-353">WiaImgFmt_JPEG</span><span class="sxs-lookup"><span data-stu-id="db91f-353">WiaImgFmt_JPEG</span></span></td>
<td><span data-ttu-id="db91f-354">Komprimiertes JPEG-Format</span><span class="sxs-lookup"><span data-stu-id="db91f-354">JPEG compressed format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db91f-355">WiaImgFmt_JPEG2K</span><span class="sxs-lookup"><span data-stu-id="db91f-355">WiaImgFmt_JPEG2K</span></span></td>
<td><span data-ttu-id="db91f-356">JPEG 2000 komprimiertes Format</span><span class="sxs-lookup"><span data-stu-id="db91f-356">JPEG 2000 compressed format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-357">WiaImgFmt_JPEG2KX</span><span class="sxs-lookup"><span data-stu-id="db91f-357">WiaImgFmt_JPEG2KX</span></span></td>
<td><span data-ttu-id="db91f-358">JPEG 2000 komprimiertes Format</span><span class="sxs-lookup"><span data-stu-id="db91f-358">JPEG 2000 compressed format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db91f-359">WiaImgFmt_MEMORYBMP</span><span class="sxs-lookup"><span data-stu-id="db91f-359">WiaImgFmt_MEMORYBMP</span></span></td>
<td><span data-ttu-id="db91f-360">Windows-Bitmap ohne Header Datei</span><span class="sxs-lookup"><span data-stu-id="db91f-360">Windows bitmap without a header file</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-361">WiaImgFmt_PDFA<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="db91f-361">WiaImgFmt_PDFA<strong>V</strong></span></span></td>
<td><span data-ttu-id="db91f-362">Das Format PDF/A (ISO/CD 19005-1).</span><span class="sxs-lookup"><span data-stu-id="db91f-362">The PDF/A (ISO/CD 19005-1) format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db91f-363">WiaImgFmt_MPG \* \*</span><span class="sxs-lookup"><span data-stu-id="db91f-363">WiaImgFmt_MPG\*\*</span></span></td>
<td><span data-ttu-id="db91f-364">MPEG-Videoformat</span><span class="sxs-lookup"><span data-stu-id="db91f-364">MPEG video format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-365">WiaImgFmt_PHOTOCD</span><span class="sxs-lookup"><span data-stu-id="db91f-365">WiaImgFmt_PHOTOCD</span></span></td>
<td><span data-ttu-id="db91f-366">Eastman-Dateiformat von Kodak</span><span class="sxs-lookup"><span data-stu-id="db91f-366">Eastman Kodak file format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db91f-367">WiaImgFmt_PICT</span><span class="sxs-lookup"><span data-stu-id="db91f-367">WiaImgFmt_PICT</span></span></td>
<td><span data-ttu-id="db91f-368">Apple-Dateiformat</span><span class="sxs-lookup"><span data-stu-id="db91f-368">Apple file format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-369">WiaImgFmt_PNG</span><span class="sxs-lookup"><span data-stu-id="db91f-369">WiaImgFmt_PNG</span></span></td>
<td><span data-ttu-id="db91f-370">W3C-PNG-Format</span><span class="sxs-lookup"><span data-stu-id="db91f-370">W3C PNG format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db91f-371">WiaImgFmt_RAW</span><span class="sxs-lookup"><span data-stu-id="db91f-371">WiaImgFmt_RAW</span></span></td>
<td><span data-ttu-id="db91f-372">Rohdaten Format nur für Datenübertragungen</span><span class="sxs-lookup"><span data-stu-id="db91f-372">Raw format for data transfers only</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-373">WiaImgFmt_RAWRGB</span><span class="sxs-lookup"><span data-stu-id="db91f-373">WiaImgFmt_RAWRGB</span></span></td>
<td><span data-ttu-id="db91f-374">Formatierte RGB-Format</span><span class="sxs-lookup"><span data-stu-id="db91f-374">Raw RGB format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db91f-375">WiaImgFmt_RTF</span><span class="sxs-lookup"><span data-stu-id="db91f-375">WiaImgFmt_RTF</span></span></td>
<td><span data-ttu-id="db91f-376">Rich-Text-Dateiformat</span><span class="sxs-lookup"><span data-stu-id="db91f-376">Rich Text File format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-377">WiaImgFmt_SCRIPT</span><span class="sxs-lookup"><span data-stu-id="db91f-377">WiaImgFmt_SCRIPT</span></span></td>
<td><span data-ttu-id="db91f-378">Skriptdatei</span><span class="sxs-lookup"><span data-stu-id="db91f-378">Script file</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db91f-379">WiaImgFmt_TIFF</span><span class="sxs-lookup"><span data-stu-id="db91f-379">WiaImgFmt_TIFF</span></span></td>
<td><span data-ttu-id="db91f-380">Tag Image File Format</span><span class="sxs-lookup"><span data-stu-id="db91f-380">Tag Image File Format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-381">WiaImgFmt_TXT</span><span class="sxs-lookup"><span data-stu-id="db91f-381">WiaImgFmt_TXT</span></span></td>
<td><span data-ttu-id="db91f-382">Textdatei</span><span class="sxs-lookup"><span data-stu-id="db91f-382">Text file</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db91f-383">WiaImgFmt_UNICODE16</span><span class="sxs-lookup"><span data-stu-id="db91f-383">WiaImgFmt_UNICODE16</span></span></td>
<td><span data-ttu-id="db91f-384">Unicode-16-Bit-Codierung</span><span class="sxs-lookup"><span data-stu-id="db91f-384">UNICODE 16-bit encoding</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-385">WiaImgFmt_WMF</span><span class="sxs-lookup"><span data-stu-id="db91f-385">WiaImgFmt_WMF</span></span></td>
<td><span data-ttu-id="db91f-386">Windows-Metadatendatei</span><span class="sxs-lookup"><span data-stu-id="db91f-386">Windows metafile</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db91f-387">WiaImgFmt_XML</span><span class="sxs-lookup"><span data-stu-id="db91f-387">WiaImgFmt_XML</span></span></td>
<td><span data-ttu-id="db91f-388">XML-Datei:</span><span class="sxs-lookup"><span data-stu-id="db91f-388">XML file</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-389">WiaImgFmt_XPS<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="db91f-389">WiaImgFmt_XPS<strong>V</strong></span></span></td>
<td><span data-ttu-id="db91f-390">XPS-Paketformat</span><span class="sxs-lookup"><span data-stu-id="db91f-390">XPS Package format</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="db91f-391">Wenn diese Eigenschaft entweder WiaImgFmt_PDFA oder WiaImgFmt_XPS ist und WIA_IPA_COMPRESSION WIA_COMPRESSION_NONE ist. der letztere Wert bedeutet, dass der Komprimierungs Modus nicht definiert ist und der Scanner einen Modus treffen muss.</span><span class="sxs-lookup"><span data-stu-id="db91f-391">When this property is either WiaImgFmt_PDFA or WiaImgFmt_XPS, and WIA_IPA_COMPRESSION is WIA_COMPRESSION_NONE; then the latter value means that the compression mode is undefined and the scanner must decide on a mode.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_FULL_ITEM_NAME"></span><span id="wia_ipa_full_item_name"></span><dl> <span data-ttu-id="db91f-392"><dt><strong>WIA_IPA_FULL_ITEM_NAME</strong></dt> <dt>picturefullitemname</dt> </span><span class="sxs-lookup"><span data-stu-id="db91f-392"><dt><strong>WIA_IPA_FULL_ITEM_NAME</strong></dt> <dt>PictureFullItemName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="db91f-393">Enthält den vollständigen Elementnamen (der Elementname und die Pfadinformationen).</span><span class="sxs-lookup"><span data-stu-id="db91f-393">Contains the full item name (the item name together with path information).</span></span> <span data-ttu-id="db91f-394">Der vollständige Elementname ist identisch mit dem <em>bstraufullitemname</em> -Parameter der Dienstprogramm Funktion <a href="https://msdn.microsoft.com/library/ms794649.aspx">wiaskreatedrvitem</a> .</span><span class="sxs-lookup"><span data-stu-id="db91f-394">The full item name is the same as the <em>bstrFullItemName</em> parameter of the <a href="https://msdn.microsoft.com/library/ms794649.aspx">wiasCreateDrvItem</a> service utility function.</span></span> <span data-ttu-id="db91f-395">Eine Anwendung liest diese Eigenschaft, um zu bestimmen, welches Element aktuell verwendet wird und wo sich dieses Element in der Elementstruktur befindet.</span><span class="sxs-lookup"><span data-stu-id="db91f-395">An application reads this property to determine which item it is currently using and where that item is located in the item tree.</span></span> <span data-ttu-id="db91f-396">Jedes Element muss einen eindeutigen Namen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="db91f-396">Each item should have a unique name.</span></span> <span data-ttu-id="db91f-397">Anwendungen verwenden häufig den vollständigen Elementnamen, um nach Elementen in der Elementstruktur zu suchen.</span><span class="sxs-lookup"><span data-stu-id="db91f-397">Applications commonly use the full item name to search for items in the item tree.</span></span> <span data-ttu-id="db91f-398">Der WIA-Dienst erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="db91f-398">The WIA service creates and maintains this property.</span></span></p>
<p><span data-ttu-id="db91f-399">Erforderlich für alle WIA 2,0-Elemente.</span><span class="sxs-lookup"><span data-stu-id="db91f-399">Required for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="db91f-400">Typ: <strong>VT_BSTR</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="db91f-400">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_GAMMA_CURVES"></span><span id="wia_ipa_gamma_curves"></span><dl> <span data-ttu-id="db91f-401"><dt><strong>WIA_IPA_GAMMA_CURVES</strong></dt> von " <dt>picturegammacurves</dt> " </span><span class="sxs-lookup"><span data-stu-id="db91f-401"><dt><strong>WIA_IPA_GAMMA_CURVES</strong></dt> <dt>PictureGammaCurves</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="db91f-402">Diese Eigenschaft ist für die zukünftige Verwendung reserviert und wird zurzeit nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="db91f-402">This property is reserved for future use and is not implemented at this time.</span></span></p>
<p><span data-ttu-id="db91f-403">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="db91f-403">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ICM_PROFILE_NAME"></span><span id="wia_ipa_icm_profile_name"></span><dl> <span data-ttu-id="db91f-404"><dt><strong>WIA_IPA_ICM_PROFILE_NAME</strong></dt> <dt>pictureicmprofilename</dt> </span><span class="sxs-lookup"><span data-stu-id="db91f-404"><dt><strong>WIA_IPA_ICM_PROFILE_NAME</strong></dt> <dt>PictureIcmProfileName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="db91f-405">Enthält den Namen des ICM-Profils, der zum ordnungsgemäßen Decodieren des Bilds erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="db91f-405">Contains the ICM profile name that is needed to properly decode the image.</span></span> <span data-ttu-id="db91f-406">Eine Anwendung liest diese Eigenschaft, um das bei der Verarbeitung des Abbilds zu verwendende ICM-Profil zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="db91f-406">An application reads this property to determine the ICM profile to use when processing the image.</span></span> <span data-ttu-id="db91f-407">Der WIA-Dienst erstellt und verwaltet diese Eigenschaft basierend auf dem Eintrag icmprofiles in der Treiber Installationsdatei.</span><span class="sxs-lookup"><span data-stu-id="db91f-407">The WIA service creates and maintains this property based on the ICMProfiles entry in the driver installation file.</span></span></p>
<p><span data-ttu-id="db91f-408">Typ: <strong>VT_BSTR</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="db91f-408">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_CATEGORY"></span><span id="wia_ipa_item_category"></span><dl> <span data-ttu-id="db91f-409"><dt><strong>WIA_IPA_ITEM_CATEGORY</strong></dt> <dt>pictureitemcategory</dt> </span><span class="sxs-lookup"><span data-stu-id="db91f-409"><dt><strong>WIA_IPA_ITEM_CATEGORY</strong></dt> <dt>PictureItemCategory</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="db91f-410">Wird nur in Windows Vista und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="db91f-410">Supported only in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="db91f-411">WIA 2,0-Elemente sind in Kategorien unterteilt, die definieren, wie ein <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> behandelt oder verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="db91f-411">WIA 2.0 items are grouped into categories that define how a <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> is to be treated or used.</span></span> <span data-ttu-id="db91f-412">Wenn das Element z. b. einen feedvorgang darstellt, sollte die Anwendung erwarten, dass Sie die erforderlichen Eigenschaften für die Dokument feederstellung enthält und wie ein Dokument-feedvorgang funktioniert.</span><span class="sxs-lookup"><span data-stu-id="db91f-412">For example, If the item represents a feeder, then the application should expect it to contain the required document feeder properties and operate like a document feeder.</span></span> <span data-ttu-id="db91f-413">Wenn das Element eine fertige Datei darstellt, sollte eine WIA 2,0-Anwendung diese auf diese Weise behandeln, wobei angenommen wird, dass die Daten statisch sind und sich auf dem Gerät befinden.</span><span class="sxs-lookup"><span data-stu-id="db91f-413">If the item represents a finished file, then a WIA 2.0 application should treat it that way, assuming that the data is static and located on the device.</span></span> <span data-ttu-id="db91f-414">(Die Regeln für jedes Element werden in den einzelnen Spezifikations Dokumenten definiert.)</span><span class="sxs-lookup"><span data-stu-id="db91f-414">(The rules for each item will be defined in their individual specification documents.)</span></span></p>
<p><span data-ttu-id="db91f-415">Erforderlich für alle WIA 2,0-Elemente.</span><span class="sxs-lookup"><span data-stu-id="db91f-415">Required for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="db91f-416">Typ: <strong>VT_CLSID</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-wia2-itemcategoryguids.md"><strong>Element Kategorie-GUIDs</strong></a></span><span class="sxs-lookup"><span data-stu-id="db91f-416">Type: <strong>VT_CLSID</strong>, Access: Read Only, Valid values: <a href="-wia-wia2-itemcategoryguids.md"><strong>Item Category GUIDs</strong></a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_FLAGS"></span><span id="wia_ipa_item_flags"></span><dl> <span data-ttu-id="db91f-417"><dt><strong>WIA_IPA_ITEM_FLAGS</strong></dt> <dt>pictureitemflags</dt> </span><span class="sxs-lookup"><span data-stu-id="db91f-417"><dt><strong>WIA_IPA_ITEM_FLAGS</strong></dt> <dt>PictureItemFlags</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="db91f-418">Enthält die beschreibenden Flags für ein WIA-Element.</span><span class="sxs-lookup"><span data-stu-id="db91f-418">Contains the descriptive flags for a WIA item.</span></span> <span data-ttu-id="db91f-419">Die elementflags sind identisch mit denen im <em>lobjectflags</em> -Parameter der Dienstprogramm Funktion <a href="https://msdn.microsoft.com/library/ms794649.aspx">wiaskreatedrvitem</a> .</span><span class="sxs-lookup"><span data-stu-id="db91f-419">The item flags are the same as those in the <em>lObjectFlags</em> parameter of the <a href="https://msdn.microsoft.com/library/ms794649.aspx">wiasCreateDrvItem</a> service utility function.</span></span> <span data-ttu-id="db91f-420">Der WIA-Dienst erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="db91f-420">The WIA service creates and maintains this property.</span></span></p>
<p><span data-ttu-id="db91f-421">Eine Anwendung liest diese Eigenschaft, um die beschreibenden Flagwerte des Elements zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="db91f-421">An application reads this property to determine the item's descriptive flag values.</span></span></p>
<p><span data-ttu-id="db91f-422">Typ: <strong>VT_I4</strong> Access: Read Only, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="db91f-422">Type: <strong>VT_I4</strong> Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="db91f-423">Die folgende Tabelle enthält die Flags, die mit dieser Eigenschaft gültig sind.</span><span class="sxs-lookup"><span data-stu-id="db91f-423">The following table has the flags that are valid with this property.</span></span> <span data-ttu-id="db91f-424">Ein Sternchen \* gibt an, dass das Flag in Windows Vista oder höher nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="db91f-424">An asterisk \* indicates that the flag is not supported in Windows Vista or later.</span></span> <span data-ttu-id="db91f-425">(Er ist nur über die <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>iwiaitem</strong></a> -Schnittstelle verfügbar.) Ein doppeltes Sternchen \* \* gibt an, dass das Flag weder in Windows Server 2003 noch in Windows Vista oder höher unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="db91f-425">(It is only available through the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> interface.) An double asterisk \*\* indicates that the flag is not supported in either Windows Server 2003 or Windows Vista or later.</span></span> <span data-ttu-id="db91f-426">Das Symbol <strong>V</strong> gibt an, dass das Flag nur in Windows Vista und höher unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="db91f-426">The <strong>V</strong> symbol indicates that the flag is supported only in Windows Vista and later.</span></span> <span data-ttu-id="db91f-427">(Er ist nur über die <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> -Schnittstelle verfügbar.)</span><span class="sxs-lookup"><span data-stu-id="db91f-427">(It is only available through the <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> interface.)</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="db91f-428">Flag</span><span class="sxs-lookup"><span data-stu-id="db91f-428">Flag</span></span></th>
<th><span data-ttu-id="db91f-429">Definition</span><span class="sxs-lookup"><span data-stu-id="db91f-429">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="db91f-430">Wiaitemtypeanalysis \*</span><span class="sxs-lookup"><span data-stu-id="db91f-430">WiaItemTypeAnalyze\*</span></span></td>
<td><span data-ttu-id="db91f-431">Dieses Element unterstützt die <strong>iwiaitem:: analyzeitem</strong> -Methode (beschrieben in der Platform SDK-Dokumentation).</span><span class="sxs-lookup"><span data-stu-id="db91f-431">This item supports the <strong>IWiaItem::AnalyzeItem</strong> method (described in the Platform SDK documentation).</span></span> <span data-ttu-id="db91f-432">Dieses Element unterstützt auch die automatische Generierung von untergeordneten Elementen.</span><span class="sxs-lookup"><span data-stu-id="db91f-432">This item also supports automatic child item generation.</span></span> <span data-ttu-id="db91f-433">Diese Funktion ist nützlich für die Bereichs Erkennung oder die Seiten Zerlegung.</span><span class="sxs-lookup"><span data-stu-id="db91f-433">This capability is useful for region detection or page decomposition.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-434">Wiaitemtypeaudiodatei</span><span class="sxs-lookup"><span data-stu-id="db91f-434">WiaItemTypeAudio</span></span></td>
<td><span data-ttu-id="db91f-435">Dieses Element unterstützt Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="db91f-435">This item supports audio.</span></span> <span data-ttu-id="db91f-436">Dieses Flag ist nur für Elemente gültig, für die das <strong>wiaitemtypefile</strong> -Flag ebenfalls festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="db91f-436">This flag is valid only for items that also have the <strong>WiaItemTypeFile</strong> flag set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db91f-437">Wiaitemtypeburst \*</span><span class="sxs-lookup"><span data-stu-id="db91f-437">WiaItemTypeBurst\*</span></span></td>
<td><span data-ttu-id="db91f-438">Nur für Ordner.</span><span class="sxs-lookup"><span data-stu-id="db91f-438">For folders only.</span></span> <span data-ttu-id="db91f-439">Dieses Flag gibt an, dass die Bilder in diesem Ordner in einer kontinuierlichen Zeitsequenz erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="db91f-439">This flag indicates that the images in this folder were taken in a continuous time sequence.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-440">Wiaitemtypedeleted</span><span class="sxs-lookup"><span data-stu-id="db91f-440">WiaItemTypeDeleted</span></span></td>
<td><span data-ttu-id="db91f-441">Dieses Element ist zum Löschen markiert, dieses Element wurde gelöscht, dieses Element ist nicht vorhanden, oder der Inhalt dieses Elements ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="db91f-441">This item is marked for deletion, this item has been deleted, this item does not exist, or the contents of this item are invalid.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db91f-442">Wiaitemtypedocument<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="db91f-442">WiaItemTypeDocument<strong>V</strong></span></span></td>
<td><span data-ttu-id="db91f-443">Bei diesem Element handelt es sich um eine Dokument Datei in einem Dokumentformat, das in der <strong>WIA_IPA_FORMAT</strong> -Eigenschaft enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="db91f-443">This item is a document file in one of the document formats that the <strong>WIA_IPA_FORMAT</strong> property contains.</span></span> <span data-ttu-id="db91f-444">(Zu diesen Formaten gehören die Dateien für nicht Bilddateien, z. b. txt-, htm-und doc-Dateien.)</span><span class="sxs-lookup"><span data-stu-id="db91f-444">(These formats include those for nonimage files, such as .txt, .htm, and .doc files.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-445">Wiaitemtypedevice</span><span class="sxs-lookup"><span data-stu-id="db91f-445">WiaItemTypeDevice</span></span></td>
<td><span data-ttu-id="db91f-446">Dieses Element stellt ein verbundenes Gerät dar.</span><span class="sxs-lookup"><span data-stu-id="db91f-446">This item represents a connected device.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db91f-447">Wiaitemtypegetrennte</span><span class="sxs-lookup"><span data-stu-id="db91f-447">WiaItemTypeDisconnected</span></span></td>
<td><span data-ttu-id="db91f-448">Dieses Element stellt ein nicht verbundenes Gerät dar.</span><span class="sxs-lookup"><span data-stu-id="db91f-448">This item represents a disconnected device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-449">Wiaitemtypefile</span><span class="sxs-lookup"><span data-stu-id="db91f-449">WiaItemTypeFile</span></span></td>
<td><span data-ttu-id="db91f-450">Das Element unterstützt Dateiübertragungen.</span><span class="sxs-lookup"><span data-stu-id="db91f-450">The item supports file transfers.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db91f-451">Wiaitemtypefolder</span><span class="sxs-lookup"><span data-stu-id="db91f-451">WiaItemTypeFolder</span></span></td>
<td><span data-ttu-id="db91f-452">Das Element ist ein Ordner.</span><span class="sxs-lookup"><span data-stu-id="db91f-452">The item is a folder.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-453">Wiaitemtypefree</span><span class="sxs-lookup"><span data-stu-id="db91f-453">WiaItemTypeFree</span></span></td>
<td><span data-ttu-id="db91f-454">Das Element ist nicht initialisiert oder wurde gelöscht.</span><span class="sxs-lookup"><span data-stu-id="db91f-454">The item is uninitialized or has been deleted.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db91f-455">Wiaitemtypegenerated</span><span class="sxs-lookup"><span data-stu-id="db91f-455">WiaItemTypeGenerated</span></span></td>
<td><span data-ttu-id="db91f-456">Dieses Element wurde von einer Anwendung oder vom Treiber generiert.</span><span class="sxs-lookup"><span data-stu-id="db91f-456">This item has been generated by an application or by the driver.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-457">Wiaitemtypehasattachments \*</span><span class="sxs-lookup"><span data-stu-id="db91f-457">WiaItemTypeHasAttachments\*</span></span></td>
<td><span data-ttu-id="db91f-458">Dieses Element unterstützt Anlagen und enthält zurzeit Anlagen.</span><span class="sxs-lookup"><span data-stu-id="db91f-458">This item supports attachments and currently contains attachments.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db91f-459">Wiaitemtypehpanorama \*</span><span class="sxs-lookup"><span data-stu-id="db91f-459">WiaItemTypeHPanorama\*</span></span></td>
<td><span data-ttu-id="db91f-460">Dieses Element stellt ein horizontales Panoramabild dar.</span><span class="sxs-lookup"><span data-stu-id="db91f-460">This item represents a horizontal panoramic image.</span></span> <span data-ttu-id="db91f-461">Dieses Flag ist nur für Elemente gültig, für die das <strong>wiaitemtypefolder</strong> -Flag ebenfalls festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="db91f-461">This flag is valid only for items that also have the <strong>WiaItemTypeFolder</strong> flag set.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-462">Wiaitemtypeimage</span><span class="sxs-lookup"><span data-stu-id="db91f-462">WiaItemTypeImage</span></span></td>
<td><span data-ttu-id="db91f-463">Das Element ist eine Bilddatei.</span><span class="sxs-lookup"><span data-stu-id="db91f-463">The item is an image file.</span></span> <span data-ttu-id="db91f-464">Dieses Flag ist nur für Elemente gültig, für die das <strong>wiaitemtypefile</strong> -Flag ebenfalls festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="db91f-464">This flag is valid only for items that also have the <strong>WiaItemTypeFile</strong> flag set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db91f-465">Wiaitemtypeprogrammiabledatasource<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="db91f-465">WiaItemTypeProgrammableDataSource<strong>V</strong></span></span></td>
<td><span data-ttu-id="db91f-466">Das Element ist eine programmierbare Datenquelle und folgt einem Satz vordefinierter Konfigurations Regeln, die auf <strong>WIA_IPA_ITEM_CATEGORY</strong>basieren.</span><span class="sxs-lookup"><span data-stu-id="db91f-466">The item is a programmable data source and follows a set of predefined configuration rules, which are based on <strong>WIA_IPA_ITEM_CATEGORY</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-467">Wiaitemtyperoot<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="db91f-467">WiaItemTypeRoot<strong>V</strong></span></span></td>
<td><span data-ttu-id="db91f-468">Dieses Element ist das Stamm Element, das allen Funktions Elementen übergeordnet ist, die das Gerät unterstützt.</span><span class="sxs-lookup"><span data-stu-id="db91f-468">This item is the root item, which is the parent to all the feature items that the device supports.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db91f-469">Wiaitemtypestorage</span><span class="sxs-lookup"><span data-stu-id="db91f-469">WiaItemTypeStorage</span></span></td>
<td><span data-ttu-id="db91f-470">Dieses Flag gibt zusätzlichen Speicher für Ordner Elemente an.</span><span class="sxs-lookup"><span data-stu-id="db91f-470">This flag indicates additional storage for folders items.</span></span> <span data-ttu-id="db91f-471">WIA-Treiber geben ihre Elemente in Form von Bildern und Ordnern an.</span><span class="sxs-lookup"><span data-stu-id="db91f-471">WIA drivers specify their items in terms of images and folders.</span></span> <span data-ttu-id="db91f-472">Es sind keine WIA-Eigenschaften vorhanden, die die Merkmale eines Speicher Elements beschreiben (z. b. den verbleibenden Speicherplatz, die Schreibgeschwindigkeit oder den Medientyp).</span><span class="sxs-lookup"><span data-stu-id="db91f-472">No WIA properties exist that describe the characteristics of a storage item (such as remaining storage space, write speed, or type of media.</span></span> <span data-ttu-id="db91f-473">Anbieterspezifische Eigenschaften, die diese Informationen verfügbar machen, können hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="db91f-473">Vendor-specific properties that expose this information can be added.</span></span> <span data-ttu-id="db91f-474">Diese Eigenschaften sind nur für Anwendungen oder Erweiterungen zugänglich, die geschrieben wurden, um Sie zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="db91f-474">These properties are accessible only to applications or extensions that are written to recognize them.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-475">Wiaitemtypetransfer</span><span class="sxs-lookup"><span data-stu-id="db91f-475">WiaItemTypeTransfer</span></span></td>
<td><span data-ttu-id="db91f-476">Dieses Element kann zum Übertragen von Daten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="db91f-476">This item can be used to transfer data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db91f-477">Wiaitemtypetwaincapabilitypassthrough</span><span class="sxs-lookup"><span data-stu-id="db91f-477">WiaItemTypeTwainCapabilityPassThrough</span></span></td>
<td><span data-ttu-id="db91f-478">Dieser Typ gibt an, dass das WIA-Gerät die TWAIN-Funktionsdaten von der TWAIN-Kompatibilitätsschicht empfangen kann.</span><span class="sxs-lookup"><span data-stu-id="db91f-478">This type indicates that the WIA device is able to receive TWAIN capability data from the TWAIN compatibility layer.</span></span> <span data-ttu-id="db91f-479">Wenn dieser Typ festgelegt ist, wird jede TWAIN-Funktion, die nicht von der TWAIN-Kompatibilitätsschicht verstanden wird, an den WIA-Treiber übermittelt.</span><span class="sxs-lookup"><span data-stu-id="db91f-479">If this type is set, any TWAIN capability that is not understood by the TWAIN compatibility layer will be passed to theWIA driver.</span></span> <span data-ttu-id="db91f-480">Dies gilt nur für das Stamm Element.</span><span class="sxs-lookup"><span data-stu-id="db91f-480">This is valid only for the root item.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-481">Wiaitemtypevideo \* \*</span><span class="sxs-lookup"><span data-stu-id="db91f-481">WiaItemTypeVideo\*\*</span></span></td>
<td><span data-ttu-id="db91f-482">Dieses Element unterstützt Streaming-Videos.</span><span class="sxs-lookup"><span data-stu-id="db91f-482">This item supports streaming video.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db91f-483">Wiaitemtypevpanorama \*</span><span class="sxs-lookup"><span data-stu-id="db91f-483">WiaItemTypeVPanorama\*</span></span></td>
<td><span data-ttu-id="db91f-484">Dieses Element stellt ein vertikales Panoramabild dar.</span><span class="sxs-lookup"><span data-stu-id="db91f-484">This item represents a vertical panoramic image.</span></span> <span data-ttu-id="db91f-485">Dieses Flag ist nur für Elemente gültig, für die das <strong>wiaitemtypefolder</strong> -Flag ebenfalls festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="db91f-485">This flag is valid only for items that also have the <strong>WiaItemTypeFolder</strong> flag set.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="db91f-486">Einige dieser Flags sind gemäß der Kategorie des Elements, wie in dieser Tabelle dargestellt, für WIA 2,0-Elemente erforderlich oder optional.</span><span class="sxs-lookup"><span data-stu-id="db91f-486">Some of these flags are required or optional for WIA 2.0 items, according to the category of the item, as shown in this table.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="db91f-487">Kategorie des Elements</span><span class="sxs-lookup"><span data-stu-id="db91f-487">Category of Item</span></span></th>
<th><span data-ttu-id="db91f-488">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="db91f-488">Required</span></span></th>
<th><span data-ttu-id="db91f-489">Optional</span><span class="sxs-lookup"><span data-stu-id="db91f-489">Optional</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="db91f-490">WIA_CATEGORY_ROOT</span><span class="sxs-lookup"><span data-stu-id="db91f-490">WIA_CATEGORY_ROOT</span></span></td>
<td><span data-ttu-id="db91f-491">Wiaitemtyperoot wiaitemtypefolder</span><span class="sxs-lookup"><span data-stu-id="db91f-491">WiaItemTypeRoot WiaItemTypeFolder</span></span></td>
<td><span data-ttu-id="db91f-492">Wiaitemtypedevice wiaitemtypegetrennte</span><span class="sxs-lookup"><span data-stu-id="db91f-492">WiaItemTypeDevice WiaItemTypeDisconnected</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-493">WIA_CATEGORY_FLATBED</span><span class="sxs-lookup"><span data-stu-id="db91f-493">WIA_CATEGORY_FLATBED</span></span></td>
<td><span data-ttu-id="db91f-494">Wiaitemtypeprogrammiabledatasource wiaitemtypetransfer wiaitemtypeimage wiaitemtypefile</span><span class="sxs-lookup"><span data-stu-id="db91f-494">WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</span></span></td>
<td><span data-ttu-id="db91f-495">Wiaitemtypefolder (wenn mehrere Scan Regions Elemente unterstützt werden, ist dieses Flag nur für das Stamm Element WIA_CATEGORY_FLATBED optional.)</span><span class="sxs-lookup"><span data-stu-id="db91f-495">WiaItemTypeFolder (If multiple scan regions items are supported, this flag is optional only for the WIA_CATEGORY_FLATBED root item.)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db91f-496">WIA_CATEGORY_FEEDER WIA_CATEGORY_FEEDER_FRONT WIA_CATEGORY_FEEDER_BACK</span><span class="sxs-lookup"><span data-stu-id="db91f-496">WIA_CATEGORY_FEEDER WIA_CATEGORY_FEEDER_FRONT WIA_CATEGORY_FEEDER_BACK</span></span></td>
<td><span data-ttu-id="db91f-497">Wiaitemtypeprogrammiabledatasource wiaitemtypetransfer wiaitemtypeimage wiaitemtypefile</span><span class="sxs-lookup"><span data-stu-id="db91f-497">WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</span></span></td>
<td><span data-ttu-id="db91f-498">Wiaitemtypefolder (wenn WIA_CATEGORY_FEEDER_FRONT und WIA_CATEGORY_FEEDER_BACK Elemente vorhanden sind, ist dieses Flag nur für das Stamm Element WIA_CATEGORY_FEEDER optional.)</span><span class="sxs-lookup"><span data-stu-id="db91f-498">WiaItemTypeFolder (If WIA_CATEGORY_FEEDER_FRONT and WIA_CATEGORY_FEEDER_BACK items are present, then this flag is optional only for the WIA_CATEGORY_FEEDER root item.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-499">WIA_CATEGORY_FILM (root)</span><span class="sxs-lookup"><span data-stu-id="db91f-499">WIA_CATEGORY_FILM (root)</span></span></td>
<td><span data-ttu-id="db91f-500">Wiaitemtypeprogrammiabledatasource wiaitemtypetransfer wiaitemtypeimage wiaitemtypefile wiaitemtypefolder</span><span class="sxs-lookup"><span data-stu-id="db91f-500">WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile WiaItemTypeFolder</span></span></td>
<td><span data-ttu-id="db91f-501">Keine</span><span class="sxs-lookup"><span data-stu-id="db91f-501">None</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db91f-502">WIA_CATEGORY_FILM (untergeordnete Elemente)</span><span class="sxs-lookup"><span data-stu-id="db91f-502">WIA_CATEGORY_FILM (children)</span></span></td>
<td><span data-ttu-id="db91f-503">Wiaitemtypeprogrammiabledatasource wiaitemtypetransfer wiaitemtypeimage wiaitemtypefile</span><span class="sxs-lookup"><span data-stu-id="db91f-503">WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</span></span></td>
<td><span data-ttu-id="db91f-504">Keine</span><span class="sxs-lookup"><span data-stu-id="db91f-504">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-505">WIA_CATEGORY_FOLDER</span><span class="sxs-lookup"><span data-stu-id="db91f-505">WIA_CATEGORY_FOLDER</span></span></td>
<td><span data-ttu-id="db91f-506">Wiaitemtypestorage wiaitemtypefolder</span><span class="sxs-lookup"><span data-stu-id="db91f-506">WiaItemTypeStorage WiaItemTypeFolder</span></span></td>
<td><span data-ttu-id="db91f-507">Wiaitemtypedeleted</span><span class="sxs-lookup"><span data-stu-id="db91f-507">WiaItemTypeDeleted</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db91f-508">WIA_CATEGORY_FINISHED_FILE</span><span class="sxs-lookup"><span data-stu-id="db91f-508">WIA_CATEGORY_FINISHED_FILE</span></span></td>
<td><span data-ttu-id="db91f-509">Wiaitemtypefile wiaitemtypetransfer</span><span class="sxs-lookup"><span data-stu-id="db91f-509">WiaItemTypeFile WiaItemTypeTransfer</span></span></td>
<td><span data-ttu-id="db91f-510">Wiaitemtypeimage wiaitemtypeaudiowiaitemtypedeleted</span><span class="sxs-lookup"><span data-stu-id="db91f-510">WiaItemTypeImage WiaItemTypeAudio WiaItemTypeDeleted</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_NAME"></span><span id="wia_ipa_item_name"></span><dl> <span data-ttu-id="db91f-511"><dt><strong>WIA_IPA_ITEM_NAME</strong></dt> <dt>pictureitemname</dt> </span><span class="sxs-lookup"><span data-stu-id="db91f-511"><dt><strong>WIA_IPA_ITEM_NAME</strong></dt> <dt>PictureItemName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="db91f-512">Enthält den Elementnamen.</span><span class="sxs-lookup"><span data-stu-id="db91f-512">Contains the item name.</span></span> <span data-ttu-id="db91f-513">Diese Eigenschaft wird von einer Anwendung gelesen, um zu bestimmen, welches Element zurzeit verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="db91f-513">An application reads this property to determine which item it is currently using.</span></span> <span data-ttu-id="db91f-514">Jedes Element hat einen eindeutigen Namen.</span><span class="sxs-lookup"><span data-stu-id="db91f-514">Each item has a unique name.</span></span> <span data-ttu-id="db91f-515">Der WIA-Dienst erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="db91f-515">The WIA service creates and maintains this property.</span></span></p>
<p><span data-ttu-id="db91f-516">Erforderlich für alle WIA 2,0-Elemente.</span><span class="sxs-lookup"><span data-stu-id="db91f-516">Required for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="db91f-517">Typ: <strong>VT_BSTR</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="db91f-517">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_SIZE"></span><span id="wia_ipa_item_size"></span><dl> <span data-ttu-id="db91f-518"><dt><strong>WIA_IPA_ITEM_SIZE</strong></dt> <dt>pictureitemsize</dt> </span><span class="sxs-lookup"><span data-stu-id="db91f-518"><dt><strong>WIA_IPA_ITEM_SIZE</strong></dt> <dt>PictureItemSize</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="db91f-519">Enthält die aktuelle Größe (in Bytes) der Daten, die dem Element zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="db91f-519">Contains the current size, in bytes, of the data that is associated with the item.</span></span> <span data-ttu-id="db91f-520">Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="db91f-520">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="db91f-521">Enthält die Gesamtgröße der übertragenen Daten.</span><span class="sxs-lookup"><span data-stu-id="db91f-521">Contains is the total size of the data being transferred.</span></span> <span data-ttu-id="db91f-522">Wenn dieser Wert 0 (null) ist, bedeutet dies, dass der Mini Treiber keine Informationen über die genaue Größe der Daten hat.</span><span class="sxs-lookup"><span data-stu-id="db91f-522">If this value is zero, it means that the minidriver has no information about the exact size of the data.</span></span> <span data-ttu-id="db91f-523">(Dies ist häufig bei komprimierten Daten der gibt.) Eine Anwendung liest diesen Wert, um die Größe des Erwerbs zu ermitteln, bevor Sie stattfindet.</span><span class="sxs-lookup"><span data-stu-id="db91f-523">(This is common for compressed data.) An application reads this value to determine the size of the acquisition before it takes place.</span></span> <span data-ttu-id="db91f-524">Der WIA-Dienst liest diese Eigenschaft, um die Zuweisung von Speicher für Datenübertragungen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="db91f-524">The WIA service reads this property to assist in allocating memory for data transfers.</span></span> <span data-ttu-id="db91f-525">Weitere Informationen finden Sie unter über <a href="https://msdn.microsoft.com/library/ms792198.aspx">tragen von Daten an eine WIA-Anwendung</a> , wenn die-Eigenschaft auf NULL festgelegt ist und TYMED für eine Dateiübertragung konfiguriert ist. der WIA-Dienst ordnet keinen Arbeitsspeicher für den WIA-Mini Treiber zu.</span><span class="sxs-lookup"><span data-stu-id="db91f-525">For further information, see <a href="https://msdn.microsoft.com/library/ms792198.aspx">Transferring Data to a WIA Application</a> if the property is set to zero and TYMED is configured for a file transfer, the WIA service does not allocate any memory for the WIA minidriver.</span></span></p>
<p><span data-ttu-id="db91f-526">Erforderlich für alle für die Übertragung aktivierten WIA 2,0-Elemente.</span><span class="sxs-lookup"><span data-stu-id="db91f-526">Required for all transfer-enabled WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="db91f-527">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="db91f-527">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_TIME"></span><span id="wia_ipa_item_time"></span><dl> <span data-ttu-id="db91f-528"><dt><strong>WIA_IPA_ITEM_TIME</strong></dt> <dt>pictureitemtime</dt> </span><span class="sxs-lookup"><span data-stu-id="db91f-528"><dt><strong>WIA_IPA_ITEM_TIME</strong></dt> <dt>PictureItemTime</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="db91f-529">Enthält die Uhrzeit, zu der das Image ursprünglich aufgezeichnet wurde.</span><span class="sxs-lookup"><span data-stu-id="db91f-529">Contains the time that the image was originally captured.</span></span> <span data-ttu-id="db91f-530">Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="db91f-530">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="db91f-531">Diese Eigenschaft sollte als Vektor von acht <strong>Wort</strong> Werten in Form einer SYSTEMTIME-Struktur (beschrieben in der Platform SDK-Dokumentation) gemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="db91f-531">This property should be reported as a vector of eight <strong>WORD</strong> values in the form of a SYSTEMTIME structure (described in the Platform SDK documentation).</span></span></p>
<p><span data-ttu-id="db91f-532">Optional für alle WIA 2,0-Elemente.</span><span class="sxs-lookup"><span data-stu-id="db91f-532">Optional for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="db91f-533">Typ: <strong>VT_UI2</strong>  |  <strong>VT_VECTOR</strong> Access: Lese-/Schreibzugriff oder schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="db91f-533">Type: <strong>VT_UI2</strong> | <strong>VT_VECTOR</strong> Access: Read/Write or Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEMS_STORED"></span><span id="wia_ipa_items_stored"></span><dl> <span data-ttu-id="db91f-534"><dt><strong>WIA_IPA_ITEMS_STORED</strong></dt> <dt>pictureitemitemsgespeicherter</dt> </span><span class="sxs-lookup"><span data-stu-id="db91f-534"><dt><strong>WIA_IPA_ITEMS_STORED</strong></dt> <dt>PictureItemItemsStored</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="db91f-535">Wird nur in Windows Vista und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="db91f-535">Supported only in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="db91f-536">Gibt an, wie viele Elemente im WIA_CATEGORY_FOLDER Element gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="db91f-536">Specifies how many items are stored in the WIA_CATEGORY_FOLDER item.</span></span></p>
<p><span data-ttu-id="db91f-537">Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="db91f-537">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_MIN_BUFFER_SIZE"></span><span id="wia_ipa_min_buffer_size"></span><dl> <span data-ttu-id="db91f-538"><dt><strong>WIA_IPA_MIN_BUFFER_SIZE</strong></dt> von " <dt>pictureminbuffersize</dt> " </span><span class="sxs-lookup"><span data-stu-id="db91f-538"><dt><strong>WIA_IPA_MIN_BUFFER_SIZE</strong></dt> <dt>PictureMinBufferSize</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="db91f-539">Gibt die minimale Puffergröße an, die für Datenübertragungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="db91f-539">Specifies the minimum buffer size that is used in data transfers.</span></span> <span data-ttu-id="db91f-540">Wenn die Datenübertragung über einen Rückrufmechanismus durchgeführt wird, kann der Eigenschafts Wert bis zu 64 KB betragen.</span><span class="sxs-lookup"><span data-stu-id="db91f-540">If the data transfer is performed through a callback mechanism, the property value can be as small as 64KB.</span></span> <span data-ttu-id="db91f-541">Wenn die Übertragung jedoch in eine Datei erfolgt, ist der Eigenschafts Wert die Anzahl von Bytes, die zum Übertragen einer Datenseite gleichzeitig benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="db91f-541">However, if the transfer is to file, the property value is the number of bytes that are needed to transfer one page of data at a time.</span></span> <span data-ttu-id="db91f-542">Der Mini Treiber erstellt und verwaltet diese WIA-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="db91f-542">The minidriver creates and maintains this WIA property.</span></span></p>
<p><span data-ttu-id="db91f-543">Optional für alle für die Übertragung aktivierten WIA 2,0-Elemente.</span><span class="sxs-lookup"><span data-stu-id="db91f-543">Optional for all transfer-enabled WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="db91f-544">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="db91f-544">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_NUMBER_OF_LINES"></span><span id="wia_ipa_number_of_lines"></span><dl> <span data-ttu-id="db91f-545"><dt><strong>WIA_IPA_NUMBER_OF_LINES</strong></dt> <dt>picturenumberoflines</dt> </span><span class="sxs-lookup"><span data-stu-id="db91f-545"><dt><strong>WIA_IPA_NUMBER_OF_LINES</strong></dt> <dt>PictureNumberOfLines</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="db91f-546">Enthält die Anzahl der im Bild enthaltenen Zeilen (die vertikale Höhe des Bilds in Pixel).</span><span class="sxs-lookup"><span data-stu-id="db91f-546">Contains the number of lines contained in the image (the vertical height of the image in pixels).</span></span> <span data-ttu-id="db91f-547">Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="db91f-547">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="db91f-548">Optional für alle WIA 2,0-Elemente.</span><span class="sxs-lookup"><span data-stu-id="db91f-548">Optional for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="db91f-549">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="db91f-549">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_PIXELS_PER_LINE"></span><span id="wia_ipa_pixels_per_line"></span><dl> <span data-ttu-id="db91f-550"><dt><strong>WIA_IPA_PIXELS_PER_LINE</strong></dt> <dt>picturepixelsperline</dt> </span><span class="sxs-lookup"><span data-stu-id="db91f-550"><dt><strong>WIA_IPA_PIXELS_PER_LINE</strong></dt> <dt>PicturePixelsPerLine</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="db91f-551">Enthält die Anzahl der Pixel in jeder Zeile des Bilds (die Breite des Bilds in Pixel).</span><span class="sxs-lookup"><span data-stu-id="db91f-551">Contains the number of pixels in each line of the image (the width of the image in pixels).</span></span> <span data-ttu-id="db91f-552">Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="db91f-552">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="db91f-553">Optional für alle WIA 2,0-Elemente.</span><span class="sxs-lookup"><span data-stu-id="db91f-553">Optional for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="db91f-554">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="db91f-554">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_PLANAR"></span><span id="wia_ipa_planar"></span><dl> <span data-ttu-id="db91f-555"><dt><strong>WIA_IPA_PLANAR</strong></dt> <dt>pictureplanar</dt> </span><span class="sxs-lookup"><span data-stu-id="db91f-555"><dt><strong>WIA_IPA_PLANAR</strong></dt> <dt>PicturePlanar</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="db91f-556">Diese Eigenschaft wird in Windows Vista und höher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="db91f-556">This property is not supported in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="db91f-557">Enthält Optionen für das Packen von Bild Daten.</span><span class="sxs-lookup"><span data-stu-id="db91f-557">Contains image data packing options.</span></span> <span data-ttu-id="db91f-558">Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="db91f-558">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="db91f-559">Eine Anwendung liest diese Eigenschaft, um die Bild Verpackungs Optionen zu bestimmen, oder legt die aktuellen Bild Verpackungs Optionen fest.</span><span class="sxs-lookup"><span data-stu-id="db91f-559">An application reads this property to determine the image packing options or sets the current image packing options.</span></span></p>
<p><span data-ttu-id="db91f-560">Typ: <strong>VT_I4</strong>; Zugriff: Lesen/Schreiben; Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a>.</span><span class="sxs-lookup"><span data-stu-id="db91f-560">Type: <strong>VT_I4</strong>; Access: Read/Write; Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a>.</span></span> <span data-ttu-id="db91f-561">Wenn das Gerät nur auf einen einzelnen Wert festgelegt werden kann, erstellen Sie einen WIA_PROP_LIST Typ, und platzieren Sie den gültigen Wert darin.</span><span class="sxs-lookup"><span data-stu-id="db91f-561">If the device can be set to only a single value, create a WIA_PROP_LIST type and place the valid value in it.</span></span></p>
<p><span data-ttu-id="db91f-562">Die folgende Tabelle enthält die beiden Konstanten, die mit dieser Eigenschaft gültig sind.</span><span class="sxs-lookup"><span data-stu-id="db91f-562">The following table has the two constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="db91f-563">Wert</span><span class="sxs-lookup"><span data-stu-id="db91f-563">Value</span></span></th>
<th><span data-ttu-id="db91f-564">Definition</span><span class="sxs-lookup"><span data-stu-id="db91f-564">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="db91f-565">WIA_PACKED_PIXEL</span><span class="sxs-lookup"><span data-stu-id="db91f-565">WIA_PACKED_PIXEL</span></span></td>
<td><span data-ttu-id="db91f-566">Bilddaten verfügen über ein gepacktes Pixel Format.</span><span class="sxs-lookup"><span data-stu-id="db91f-566">Image data is in packed-pixel format.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-567">WIA_PLANAR</span><span class="sxs-lookup"><span data-stu-id="db91f-567">WIA_PLANAR</span></span></td>
<td><span data-ttu-id="db91f-568">Bilddaten liegen im planaren Format vor.</span><span class="sxs-lookup"><span data-stu-id="db91f-568">Image data is in planar format.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_PREFERRED_FORMAT"></span><span id="wia_ipa_preferred_format"></span><dl> <span data-ttu-id="db91f-569"><dt><strong>WIA_IPA_PREFERRED_FORMAT</strong></dt> <dt>picturepreferredformat</dt> </span><span class="sxs-lookup"><span data-stu-id="db91f-569"><dt><strong>WIA_IPA_PREFERRED_FORMAT</strong></dt> <dt>PicturePreferredFormat</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="db91f-570">Enthält das bevorzugte Format für Images, die dieser Mini Treiber überträgt.</span><span class="sxs-lookup"><span data-stu-id="db91f-570">Contains the preferred format for images that this minidriver transfers.</span></span> <span data-ttu-id="db91f-571">Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="db91f-571">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="db91f-572">Erforderlich für alle für die Übertragung aktivierten WIA 2,0-Elemente.</span><span class="sxs-lookup"><span data-stu-id="db91f-572">Required for all transfer-enabled WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="db91f-573">Typ: <strong>CLSID</strong>, Access: Read Only, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="db91f-573">Type: <strong>CLSID</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_PROP_STREAM_COMPAT_ID"></span><span id="wia_ipa_prop_stream_compat_id"></span><dl> <span data-ttu-id="db91f-574"><dt><strong>WIA_IPA_PROP_STREAM_COMPAT_ID</strong></dt> <dt>picturepropstreamcompatid</dt> </span><span class="sxs-lookup"><span data-stu-id="db91f-574"><dt><strong>WIA_IPA_PROP_STREAM_COMPAT_ID</strong></dt> <dt>PicturePropStreamCompatId</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="db91f-575">Gibt eine CLSID an, die einen Satz von Geräte Eigenschafts Werten darstellt.</span><span class="sxs-lookup"><span data-stu-id="db91f-575">Specifies a CLSID that represents a set of device property values.</span></span> <span data-ttu-id="db91f-576">Wenn ein Gerätetreiber diese Funktion implementiert, verwenden Anwendungen diese Eigenschaft, um zu bestimmen, ob das Gerät eine Reihe von Werten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="db91f-576">If a device driver implements this feature, applications use this property to determine if the device supports a set of values.</span></span></p>
<p><span data-ttu-id="db91f-577">Typ: <strong>CLSID</strong>, Access: Read Only, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="db91f-577">Type: <strong>CLSID</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="db91f-578">Die folgende Tabelle enthält die 12 Konstanten, die mit dieser Eigenschaft gültig sind.</span><span class="sxs-lookup"><span data-stu-id="db91f-578">The following table has the 12 constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="db91f-579">Wert</span><span class="sxs-lookup"><span data-stu-id="db91f-579">Value</span></span></th>
<th><span data-ttu-id="db91f-580">Definition</span><span class="sxs-lookup"><span data-stu-id="db91f-580">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="db91f-581">WiaImgFmt_BMP</span><span class="sxs-lookup"><span data-stu-id="db91f-581">WiaImgFmt_BMP</span></span></td>
<td><span data-ttu-id="db91f-582">MicrosoftWindows-Bitmap mit einer Header Datei</span><span class="sxs-lookup"><span data-stu-id="db91f-582">MicrosoftWindows bitmap with a header file</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-583">WiaImgFmt_EMF</span><span class="sxs-lookup"><span data-stu-id="db91f-583">WiaImgFmt_EMF</span></span></td>
<td><span data-ttu-id="db91f-584">Erweiterte Windows-Metadatendatei</span><span class="sxs-lookup"><span data-stu-id="db91f-584">Extended Windows metafile</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db91f-585">WiaImgFmt_EXIF</span><span class="sxs-lookup"><span data-stu-id="db91f-585">WiaImgFmt_EXIF</span></span></td>
<td><span data-ttu-id="db91f-586">Austauschbares Datei Format</span><span class="sxs-lookup"><span data-stu-id="db91f-586">Exchangeable File Format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-587">WiaImgFmt_FLASHPIX</span><span class="sxs-lookup"><span data-stu-id="db91f-587">WiaImgFmt_FLASHPIX</span></span></td>
<td><span data-ttu-id="db91f-588">Format von Flash pix</span><span class="sxs-lookup"><span data-stu-id="db91f-588">FlashPix format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db91f-589">WiaImgFmt_GIF</span><span class="sxs-lookup"><span data-stu-id="db91f-589">WiaImgFmt_GIF</span></span></td>
<td><span data-ttu-id="db91f-590">GIF-Bildformat</span><span class="sxs-lookup"><span data-stu-id="db91f-590">GIF image format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-591">WiaImgFmt_ICO</span><span class="sxs-lookup"><span data-stu-id="db91f-591">WiaImgFmt_ICO</span></span></td>
<td><span data-ttu-id="db91f-592">Windows-Symbol Dateiformat</span><span class="sxs-lookup"><span data-stu-id="db91f-592">Windows icon file format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db91f-593">WiaImgFmt_JPEG</span><span class="sxs-lookup"><span data-stu-id="db91f-593">WiaImgFmt_JPEG</span></span></td>
<td><span data-ttu-id="db91f-594">Komprimiertes JPEG-Format</span><span class="sxs-lookup"><span data-stu-id="db91f-594">JPEG compressed format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-595">WiaImgFmt_PHOTOCD</span><span class="sxs-lookup"><span data-stu-id="db91f-595">WiaImgFmt_PHOTOCD</span></span></td>
<td><span data-ttu-id="db91f-596">Eastman-Dateiformat von Kodak</span><span class="sxs-lookup"><span data-stu-id="db91f-596">Eastman Kodak file format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db91f-597">WiaImgFmt_PNG</span><span class="sxs-lookup"><span data-stu-id="db91f-597">WiaImgFmt_PNG</span></span></td>
<td><span data-ttu-id="db91f-598">W3C-PNG-Format</span><span class="sxs-lookup"><span data-stu-id="db91f-598">W3C PNG format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-599">WiaImgFmt_MEMORYBMP</span><span class="sxs-lookup"><span data-stu-id="db91f-599">WiaImgFmt_MEMORYBMP</span></span></td>
<td><span data-ttu-id="db91f-600">Windows-Bitmap ohne Header Datei</span><span class="sxs-lookup"><span data-stu-id="db91f-600">Windows bitmap without a header file</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db91f-601">WiaImgFmt_TIFF</span><span class="sxs-lookup"><span data-stu-id="db91f-601">WiaImgFmt_TIFF</span></span></td>
<td><span data-ttu-id="db91f-602">Tag Image File Format</span><span class="sxs-lookup"><span data-stu-id="db91f-602">Tag Image File Format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-603">WiaImgFmt_WMF</span><span class="sxs-lookup"><span data-stu-id="db91f-603">WiaImgFmt_WMF</span></span></td>
<td><span data-ttu-id="db91f-604">Windows-Metadatendatei</span><span class="sxs-lookup"><span data-stu-id="db91f-604">Windows metafile</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_RAW_BITS_PER_CHANNEL"></span><span id="wia_ipa_raw_bits_per_channel"></span><dl> <span data-ttu-id="db91f-605"><dt><strong>WIA_IPA_RAW_BITS_PER_CHANNEL</strong></dt> <dt>picturerawbitsperchannel</dt> </span><span class="sxs-lookup"><span data-stu-id="db91f-605"><dt><strong>WIA_IPA_RAW_BITS_PER_CHANNEL</strong></dt> <dt>PictureRawBitsPerChannel</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="db91f-606">Wird nur in Windows Vista und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="db91f-606">Supported only in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="db91f-607">Enthält die Anzahl der Bits in jedem Kanal.</span><span class="sxs-lookup"><span data-stu-id="db91f-607">Contains the number of bits in each channel.</span></span> <span data-ttu-id="db91f-608">Diese Eigenschaft sollte als Vektor von so vielen Byte Werten als Channels gemeldet werden, wobei das erste Byte der Anzahl von Bits im ersten Kanal entspricht, dem zweiten Byte der Anzahl von Bits im zweiten Kanal usw.</span><span class="sxs-lookup"><span data-stu-id="db91f-608">This property should be reported as a vector of as many BYTE values as there are channels, where the first BYTE corresponds to the number of bits in the first channel, the second byte to the number of bits in the second channel and so on.</span></span> <span data-ttu-id="db91f-609">Es müssen beliebig viele Einträge vorhanden sein, da Kanäle gemäß WIA_IPA_CHANNELS_PER_PIXEL vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="db91f-609">There need to be as many entries as there are channels according to WIA_IPA_CHANNELS_PER_PIXEL.</span></span> <span data-ttu-id="db91f-610">Der Treiber legt diese Eigenschaft fest, wenn die Anwendung zu WiaImgFmt_RAW wechselt.</span><span class="sxs-lookup"><span data-stu-id="db91f-610">The driver sets that property when the application switches to WiaImgFmt_RAW.</span></span> <span data-ttu-id="db91f-611">Bei den bekannten Untertypen sind in der Tabelle unter WIA_IPA_RAW_SUBTYPE beliebig viele Einträge aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="db91f-611">For the well-known subtypes, there are as many entries as listed in the table under WIA_IPA_RAW_SUBTYPE.</span></span></p>
<p><span data-ttu-id="db91f-612">Typ: <strong>VT_UI1</strong> | <strong>VT_VECTOR</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="db91f-612">Type: <strong>VT_UI1</strong>|<strong>VT_VECTOR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_REGION_TYPE"></span><span id="wia_ipa_region_type"></span><dl> <span data-ttu-id="db91f-613"><dt><strong>WIA_IPA_REGION_TYPE</strong></dt> <dt>pictureregiontype</dt> </span><span class="sxs-lookup"><span data-stu-id="db91f-613"><dt><strong>WIA_IPA_REGION_TYPE</strong></dt> <dt>PictureRegionType</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="db91f-614">Diese Eigenschaft ist für die zukünftige Verwendung reserviert und wird zu diesem Zeitpunkt nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="db91f-614">This property is reserved by for future use and is not implemented at this time.</span></span></p>
<p><span data-ttu-id="db91f-615">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="db91f-615">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_SUPPRESS_PROPERTY_PAGE"></span><span id="wia_ipa_suppress_property_page"></span><dl> <span data-ttu-id="db91f-616"><dt><strong>WIA_IPA_SUPPRESS_PROPERTY_PAGE</strong></dt> <dt>picturesuppresspropertypage</dt> </span><span class="sxs-lookup"><span data-stu-id="db91f-616"><dt><strong>WIA_IPA_SUPPRESS_PROPERTY_PAGE</strong></dt> <dt>PictureSuppressPropertyPage</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="db91f-617">Gibt an, ob die allgemeinen Eigenschaften Seiten für Elemente auf dem Gerät unterdrückt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="db91f-617">Specifies whether to suppress the general property pages for items on the device.</span></span></p>
<p><span data-ttu-id="db91f-618">Diese Eigenschaft ist unter Windows XP und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="db91f-618">This property is available on Windows XP and later.</span></span></p>
<p><span data-ttu-id="db91f-619">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="db91f-619">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="db91f-620">Die folgende Tabelle enthält die Konstanten, die mit dieser Eigenschaft gültig sind.</span><span class="sxs-lookup"><span data-stu-id="db91f-620">The following table has the constants that are valid with this property.</span></span> <span data-ttu-id="db91f-621">Das Sternchen \* gibt an, dass die Konstante mit Windows Vista und höher nicht gültig ist.</span><span class="sxs-lookup"><span data-stu-id="db91f-621">The asterisk \* indicates that the constant is not valid with Windows Vista and later.</span></span> <span data-ttu-id="db91f-622">(Er ist nur über die <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>iwiaitem</strong></a> -Schnittstelle verfügbar.)</span><span class="sxs-lookup"><span data-stu-id="db91f-622">(It is only available through the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> interface.)</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="db91f-623">Konstante</span><span class="sxs-lookup"><span data-stu-id="db91f-623">Constant</span></span></th>
<th><span data-ttu-id="db91f-624">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="db91f-624">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="db91f-625">WIA_PROPPAGE_CAMERA_ITEM_GENERAL \*</span><span class="sxs-lookup"><span data-stu-id="db91f-625">WIA_PROPPAGE_CAMERA_ITEM_GENERAL\*</span></span></td>
<td><span data-ttu-id="db91f-626">Unterdrücken Sie die Eigenschaften Seite für allgemeine Elemente für eine Kamera.</span><span class="sxs-lookup"><span data-stu-id="db91f-626">Suppress the general item property page for a camera.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-627">WIA_PROPPAGE_SCANNER_ITEM_GENERAL</span><span class="sxs-lookup"><span data-stu-id="db91f-627">WIA_PROPPAGE_SCANNER_ITEM_GENERAL</span></span></td>
<td><span data-ttu-id="db91f-628">Unterdrücken Sie die Eigenschaften Seite für allgemeine Elemente für einen Scanner.</span><span class="sxs-lookup"><span data-stu-id="db91f-628">Suppress the general item property page for a scanner.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_TYMED"></span><span id="wia_ipa_tymed"></span><dl> <span data-ttu-id="db91f-629"><dt><strong>WIA_IPA_TYMED</strong></dt> <dt>picturetymed</dt> </span><span class="sxs-lookup"><span data-stu-id="db91f-629"><dt><strong>WIA_IPA_TYMED</strong></dt> <dt>PictureTymed</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="db91f-630">Diese Eigenschaft enthält die Übertragungsmethoden Einstellung.</span><span class="sxs-lookup"><span data-stu-id="db91f-630">This property contains the transfer method setting.</span></span> <span data-ttu-id="db91f-631">Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="db91f-631">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="db91f-632">Eine Anwendung liest diese Eigenschaft, um die Methode der Minidriver-Methode für die Datenübertragung zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="db91f-632">An application reads this property to determine the minidriver's method of data transfer.</span></span></p>
<p><span data-ttu-id="db91f-633">Erforderlich für alle für die Übertragung aktivierten WIA 2,0-Elemente.</span><span class="sxs-lookup"><span data-stu-id="db91f-633">Required for all transfer-enabled WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="db91f-634">Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="db91f-634">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="db91f-635">Die folgende Tabelle enthält die Konstanten, die mit dieser Eigenschaft gültig sind.</span><span class="sxs-lookup"><span data-stu-id="db91f-635">The following table has the constants that are valid with this property.</span></span> <span data-ttu-id="db91f-636">Das Sternchen \* gibt Konstanten an, die mit Windows Vista und höher nicht gültig sind.</span><span class="sxs-lookup"><span data-stu-id="db91f-636">The asterisk \* indicates constants that are not valid with Windows Vista and later.</span></span> <span data-ttu-id="db91f-637">(Sie sind nur über die <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>iwiaitem</strong></a> -Schnittstelle verfügbar.)</span><span class="sxs-lookup"><span data-stu-id="db91f-637">(They are only available through the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> interface.)</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="db91f-638">Transfertyp</span><span class="sxs-lookup"><span data-stu-id="db91f-638">Transfer Type</span></span></th>
<th><span data-ttu-id="db91f-639">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="db91f-639">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="db91f-640">TYMED_CALLBACK \*</span><span class="sxs-lookup"><span data-stu-id="db91f-640">TYMED_CALLBACK\*</span></span></td>
<td><span data-ttu-id="db91f-641">Übertragen Sie ein Bild in Bänder in den Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="db91f-641">Transfer an image to memory, in bands.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-642">TYMED_MULTIPAGE_CALLBACK \*</span><span class="sxs-lookup"><span data-stu-id="db91f-642">TYMED_MULTIPAGE_CALLBACK\*</span></span></td>
<td><span data-ttu-id="db91f-643">Übertragen Sie mehrere Abbilder in Bänder in den Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="db91f-643">Transfer multiple images to memory, in bands.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db91f-644">TYMED_FILE</span><span class="sxs-lookup"><span data-stu-id="db91f-644">TYMED_FILE</span></span></td>
<td><span data-ttu-id="db91f-645">Übertragen eines Bilds in eine Datei.</span><span class="sxs-lookup"><span data-stu-id="db91f-645">Transfer an image to a file.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db91f-646">TYMED_MULTIPAGE_FILE</span><span class="sxs-lookup"><span data-stu-id="db91f-646">TYMED_MULTIPAGE_FILE</span></span></td>
<td><span data-ttu-id="db91f-647">Übertragen eines Bilds in eine Datei.</span><span class="sxs-lookup"><span data-stu-id="db91f-647">Transfer an image to a file.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_UPLOAD_ITEM_SIZE"></span><span id="wia_ipa_upload_item_size"></span><dl> <span data-ttu-id="db91f-648"><dt><strong>WIA_IPA_UPLOAD_ITEM_SIZE</strong></dt> <dt>pictureitemuploaditemsize</dt> </span><span class="sxs-lookup"><span data-stu-id="db91f-648"><dt><strong>WIA_IPA_UPLOAD_ITEM_SIZE</strong></dt> <dt>PictureItemUploadItemSize</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="db91f-649">Wird nur in Windows Vista und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="db91f-649">Supported only in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="db91f-650">Gibt die Anzahl der Bytes an, die für ein Element hochgeladen werden.</span><span class="sxs-lookup"><span data-stu-id="db91f-650">Specifies the number of bytes to upload for an item.</span></span></p>
<p><span data-ttu-id="db91f-651">Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="db91f-651">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="db91f-652">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="db91f-652">Requirements</span></span>



| <span data-ttu-id="db91f-653">Anforderung</span><span class="sxs-lookup"><span data-stu-id="db91f-653">Requirement</span></span> | <span data-ttu-id="db91f-654">Wert</span><span class="sxs-lookup"><span data-stu-id="db91f-654">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="db91f-655">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="db91f-655">Minimum supported client</span></span><br/> | <span data-ttu-id="db91f-656">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="db91f-656">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="db91f-657">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="db91f-657">Minimum supported server</span></span><br/> | <span data-ttu-id="db91f-658">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="db91f-658">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="db91f-659">Header</span><span class="sxs-lookup"><span data-stu-id="db91f-659">Header</span></span><br/>                   | <dl> <span data-ttu-id="db91f-660"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="db91f-660"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




