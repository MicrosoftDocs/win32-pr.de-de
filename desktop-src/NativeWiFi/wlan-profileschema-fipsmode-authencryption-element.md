---
description: Gibt an, ob der Federal Information Processing Standards (fps)-Modus aktiviert ist.
ms.assetid: 4c62c96c-82e7-4174-b833-95ee10b29344
title: Mepsmode-Element (authencryption)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FIPSMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 62a60670622084e3179e9720022c68ad5909ab4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752304"
---
# <a name="fipsmode-authencryption-element"></a><span data-ttu-id="01e10-103">Mepsmode-Element (authencryption)</span><span class="sxs-lookup"><span data-stu-id="01e10-103">FIPSMode (authEncryption) Element</span></span>

<span data-ttu-id="01e10-104">Das Element " **fpsmode** (authencryption)" gibt an, ob der Modus "Federal Information Processing Standards (fps)" aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="01e10-104">The **FIPSMode** (authEncryption) element indicates whether Federal Information Processing Standards (FIPS) mode is enabled.</span></span> <span data-ttu-id="01e10-105">Wenn eine drahtlose Verbindung im PPS-Modus betrieben wird, entspricht die Sicherheitsstufe der Verbindung 140-2 dem Standard-Standard von Standard.</span><span class="sxs-lookup"><span data-stu-id="01e10-105">When a wireless connection is operating in FIPS mode, the security level of the connection complies with the FIPS 140-2 standard.</span></span> <span data-ttu-id="01e10-106">Weitere Informationen zu "fps" finden Sie auf der [Startseite](https://www.itl.nist.gov/fipspubs/)von "Fi".</span><span class="sxs-lookup"><span data-stu-id="01e10-106">For more information about FIPS, see the [FIPS Home Page](https://www.itl.nist.gov/fipspubs/).</span></span>

<span data-ttu-id="01e10-107">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="01e10-107">This element is optional.</span></span> <span data-ttu-id="01e10-108">Wenn dieses Element nicht in einem Profil angegeben wird, ist der Modus "PPS" nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="01e10-108">If this element is not specified in a profile, then FIPS mode is not enabled.</span></span>

<span data-ttu-id="01e10-109">" **Fpsmode** " kann nur auf "true" festgelegt werden, wenn die folgenden Bedingungen erfüllt sind:</span><span class="sxs-lookup"><span data-stu-id="01e10-109">**FIPSMode** can be set to TRUE only when the following conditions are met:</span></span>

-   <span data-ttu-id="01e10-110">Das [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) -Element hat den Wert `ESS` (d. h. die Verbindung ist eine infrastrukturverbindung).</span><span class="sxs-lookup"><span data-stu-id="01e10-110">The [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) element has a value of `ESS` (that is, the connection is an infrastructure connection).</span></span>
-   <span data-ttu-id="01e10-111">Das [**Authentifizierungs**](wlan-profileschema-authentication-authencryption-element.md) Element hat den Wert `WPA2` oder `WPA2PSK` .</span><span class="sxs-lookup"><span data-stu-id="01e10-111">The [**authentication**](wlan-profileschema-authentication-authencryption-element.md) element has a value of `WPA2` or `WPA2PSK`.</span></span>
-   <span data-ttu-id="01e10-112">Das [**Verschlüsselungs**](wlan-profileschema-encryption-authencryption-element.md) Element weist den Wert auf `AES` .</span><span class="sxs-lookup"><span data-stu-id="01e10-112">The [**encryption**](wlan-profileschema-encryption-authencryption-element.md) element has a value of `AES`.</span></span>

<span data-ttu-id="01e10-113">Anders als die meisten Elemente im WLAN- \_ Profil Schema befindet sich dieses Element im- `https://www.microsoft.com/networking/WLAN/profile/v2` Namespace.</span><span class="sxs-lookup"><span data-stu-id="01e10-113">Unlike most elements in the WLAN\_profile schema, this element is in the `https://www.microsoft.com/networking/WLAN/profile/v2` namespace.</span></span>

<span data-ttu-id="01e10-114">**Der Wert des Elements "** -Element" wird ignoriert, wenn der Mini Port-Treiber für die drahtlos Schnittstelle den PPS-Modus nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="01e10-114">The value of the **FIPSMode** element is ignored if the miniport driver for the wireless interface does not support FIPS mode.</span></span>

<span data-ttu-id="01e10-115">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="01e10-115">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span> <span data-ttu-id="01e10-116">Wenn " **fpsmode** " in einem Profil vorhanden ist, wird das-Element ignoriert.</span><span class="sxs-lookup"><span data-stu-id="01e10-116">If **FIPSMode** is present in a profile, the element is ignored.</span></span>

``` syntax
<xs:element name="FIPSMode"
    type="boolean"
 />
```

<span data-ttu-id="01e10-117">Das-Element wird durch das [**authencryption**](wlan-profileschema-authencryption-security-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="01e10-117">The element is defined by the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="01e10-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="01e10-118">Remarks</span></span>

<span data-ttu-id="01e10-119">Dieser Parameter kann über die Befehlszeile mit dem **Netsh WLAN Set ProfileParameter** -Befehl festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="01e10-119">This parameter can be set at the command line using the **netsh wlan set profileparameter** command.</span></span> <span data-ttu-id="01e10-120">Weitere Informationen finden Sie unter [Netsh Commands for Wireless Local Area Network (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="01e10-120">For more information, see [Netsh Commands for Wireless Local Area Network (wlan)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span></span>

## <a name="examples"></a><span data-ttu-id="01e10-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="01e10-121">Examples</span></span>

<span data-ttu-id="01e10-122">Ein Beispiel Profil, das das-Element in der-Datei verwendet, finden Sie unter Beispiel für das **PPS** - [Profil](fips-profile-sample.md).</span><span class="sxs-lookup"><span data-stu-id="01e10-122">To view a sample profile that uses the **FIPSMode** element, see [FIPS Profile Sample](fips-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="01e10-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="01e10-123">Requirements</span></span>



| <span data-ttu-id="01e10-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="01e10-124">Requirement</span></span> | <span data-ttu-id="01e10-125">Wert</span><span class="sxs-lookup"><span data-stu-id="01e10-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="01e10-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="01e10-126">Minimum supported client</span></span><br/> | <span data-ttu-id="01e10-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="01e10-127">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="01e10-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="01e10-128">Minimum supported server</span></span><br/> | <span data-ttu-id="01e10-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="01e10-129">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="01e10-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="01e10-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="01e10-131">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="01e10-131">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="01e10-132">**authEncryption**</span><span class="sxs-lookup"><span data-stu-id="01e10-132">**authEncryption**</span></span>](wlan-profileschema-authencryption-security-element.md)
</dt> <dt>

<span data-ttu-id="01e10-133">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="01e10-133">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="01e10-134">**authencryption (Sicherheit)**</span><span class="sxs-lookup"><span data-stu-id="01e10-134">**authEncryption (security)**</span></span>](wlan-profileschema-authencryption-security-element.md)
</dt> </dl>

 

 
