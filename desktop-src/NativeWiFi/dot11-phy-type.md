---
description: Definiert einen 802,11-PHY-und Medientyp.
ms.assetid: f3804e57-c633-4288-9749-2b267b1353ae
title: DOT11_PHY_TYPE-Enumeration (Windot11. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_PHY_TYPE
api_type:
- HeaderDef
api_location:
- windot11.h
ms.openlocfilehash: 4e8fc4a1154b9f95fad5024607435861b9e98ae1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866036"
---
# <a name="dot11_phy_type-enumeration"></a><span data-ttu-id="0a376-103">DOT11 \_ PHY- \_ Typenumeration</span><span class="sxs-lookup"><span data-stu-id="0a376-103">DOT11\_PHY\_TYPE enumeration</span></span>

<span data-ttu-id="0a376-104">Die **DOT11 \_ PHY- \_ Typenumeration** definiert einen 802,11-PHY-und Medientyp.</span><span class="sxs-lookup"><span data-stu-id="0a376-104">The **DOT11\_PHY\_TYPE** enumeration defines an 802.11 PHY and media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a376-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a376-105">Syntax</span></span>


```C++
typedef enum _DOT11_PHY_TYPE { 
  dot11_phy_type_unknown     = 0,
  dot11_phy_type_any         = 0,
  dot11_phy_type_fhss        = 1,
  dot11_phy_type_dsss        = 2,
  dot11_phy_type_irbaseband  = 3,
  dot11_phy_type_ofdm        = 4,
  dot11_phy_type_hrdsss      = 5,
  dot11_phy_type_erp         = 6,
  dot11_phy_type_ht          = 7,
  dot11_phy_type_vht         = 8,
  dot11_phy_type_IHV_start   = 0x80000000,
  dot11_phy_type_IHV_end     = 0xffffffff
} DOT11_PHY_TYPE, *PDOT11_PHY_TYPE;
```



## <a name="constants"></a><span data-ttu-id="0a376-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="0a376-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0a376-107"><span id="dot11_phy_type_unknown"></span><span id="DOT11_PHY_TYPE_UNKNOWN"></span>**Dot11 \_ PHY- \_ Typ \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="0a376-107"><span id="dot11_phy_type_unknown"></span><span id="DOT11_PHY_TYPE_UNKNOWN"></span>**dot11\_phy\_type\_unknown**</span></span>
</dt> <dd>

<span data-ttu-id="0a376-108">Gibt einen unbekannten oder nicht initialisierten phiertyp an.</span><span class="sxs-lookup"><span data-stu-id="0a376-108">Specifies an unknown or uninitialized PHY type.</span></span>

</dd> <dt>

<span data-ttu-id="0a376-109"><span id="dot11_phy_type_any"></span><span id="DOT11_PHY_TYPE_ANY"></span>**Dot11 \_ PHY \_ Typ \_ beliebig**</span><span class="sxs-lookup"><span data-stu-id="0a376-109"><span id="dot11_phy_type_any"></span><span id="DOT11_PHY_TYPE_ANY"></span>**dot11\_phy\_type\_any**</span></span>
</dt> <dd>

<span data-ttu-id="0a376-110">Gibt einen beliebigen PHY-Typ an.</span><span class="sxs-lookup"><span data-stu-id="0a376-110">Specifies any PHY type.</span></span>

</dd> <dt>

<span data-ttu-id="0a376-111"><span id="dot11_phy_type_fhss"></span><span id="DOT11_PHY_TYPE_FHSS"></span>**Dot11- \_ PHY- \_ Typ ( \_ SSS)**</span><span class="sxs-lookup"><span data-stu-id="0a376-111"><span id="dot11_phy_type_fhss"></span><span id="DOT11_PHY_TYPE_FHSS"></span>**dot11\_phy\_type\_fhss**</span></span>
</dt> <dd>

<span data-ttu-id="0a376-112">Gibt eine "Frequency-Spring"-e/a-Rate (SHSS) an.</span><span class="sxs-lookup"><span data-stu-id="0a376-112">Specifies a frequency-hopping spread-spectrum (FHSS) PHY.</span></span> <span data-ttu-id="0a376-113">Für Bluetooth-Geräte können Sie den Einsatz von SSS oder eine Anpassung von SHSS verwenden.</span><span class="sxs-lookup"><span data-stu-id="0a376-113">Bluetooth devices can use FHSS or an adaptation of FHSS.</span></span>

</dd> <dt>

<span data-ttu-id="0a376-114"><span id="dot11_phy_type_dsss"></span><span id="DOT11_PHY_TYPE_DSSS"></span>**Dot11 \_ PHY- \_ Typ \_ DSSS**</span><span class="sxs-lookup"><span data-stu-id="0a376-114"><span id="dot11_phy_type_dsss"></span><span id="DOT11_PHY_TYPE_DSSS"></span>**dot11\_phy\_type\_dsss**</span></span>
</dt> <dd>

<span data-ttu-id="0a376-115">Gibt einen DSSS (Direct Sequence Spread)-PHY-Typ an.</span><span class="sxs-lookup"><span data-stu-id="0a376-115">Specifies a direct sequence spread spectrum (DSSS) PHY type.</span></span>

</dd> <dt>

<span data-ttu-id="0a376-116"><span id="dot11_phy_type_irbaseband"></span><span id="DOT11_PHY_TYPE_IRBASEBAND"></span>**Dot11 \_ PHY- \_ Typ " \_ unbaseband"**</span><span class="sxs-lookup"><span data-stu-id="0a376-116"><span id="dot11_phy_type_irbaseband"></span><span id="DOT11_PHY_TYPE_IRBASEBAND"></span>**dot11\_phy\_type\_irbaseband**</span></span>
</dt> <dd>

<span data-ttu-id="0a376-117">Gibt einen Infrarot-Baseband-phikentyp (IR) an.</span><span class="sxs-lookup"><span data-stu-id="0a376-117">Specifies an infrared (IR) baseband PHY type.</span></span>

</dd> <dt>

<span data-ttu-id="0a376-118"><span id="dot11_phy_type_ofdm"></span><span id="DOT11_PHY_TYPE_OFDM"></span>**Dot11 \_ PHY \_ Typ von \_ DM**</span><span class="sxs-lookup"><span data-stu-id="0a376-118"><span id="dot11_phy_type_ofdm"></span><span id="DOT11_PHY_TYPE_OFDM"></span>**dot11\_phy\_type\_ofdm**</span></span>
</dt> <dd>

<span data-ttu-id="0a376-119">Gibt einen Multiplexing (OFDM)-PHY-Typ der orthogonalen Frequenz Division an.</span><span class="sxs-lookup"><span data-stu-id="0a376-119">Specifies an orthogonal frequency division multiplexing (OFDM) PHY type.</span></span> <span data-ttu-id="0a376-120">802.11 a-Geräte können OFDM verwenden.</span><span class="sxs-lookup"><span data-stu-id="0a376-120">802.11a devices can use OFDM.</span></span>

</dd> <dt>

<span data-ttu-id="0a376-121"><span id="dot11_phy_type_hrdsss"></span><span id="DOT11_PHY_TYPE_HRDSSS"></span>**Dot11 \_ PHY \_ Type \_ hrdsss**</span><span class="sxs-lookup"><span data-stu-id="0a376-121"><span id="dot11_phy_type_hrdsss"></span><span id="DOT11_PHY_TYPE_HRDSSS"></span>**dot11\_phy\_type\_hrdsss**</span></span>
</dt> <dd>

<span data-ttu-id="0a376-122">Gibt einen höchst wertigen DSSS (hrdsss)-PHY-Typ an.</span><span class="sxs-lookup"><span data-stu-id="0a376-122">Specifies a high-rate DSSS (HRDSSS) PHY type.</span></span>

</dd> <dt>

<span data-ttu-id="0a376-123"><span id="dot11_phy_type_erp"></span><span id="DOT11_PHY_TYPE_ERP"></span>**Dot11 \_ PHY- \_ Typ \_ ERP**</span><span class="sxs-lookup"><span data-stu-id="0a376-123"><span id="dot11_phy_type_erp"></span><span id="DOT11_PHY_TYPE_ERP"></span>**dot11\_phy\_type\_erp**</span></span>
</dt> <dd>

<span data-ttu-id="0a376-124">Gibt den Typ des erweiterten Raten-PHY (ERP) an.</span><span class="sxs-lookup"><span data-stu-id="0a376-124">Specifies an extended rate PHY type (ERP).</span></span> <span data-ttu-id="0a376-125">802.11 g-Geräte können ERP verwenden.</span><span class="sxs-lookup"><span data-stu-id="0a376-125">802.11g devices can use ERP.</span></span>

</dd> <dt>

<span data-ttu-id="0a376-126"><span id="dot11_phy_type_ht"></span><span id="DOT11_PHY_TYPE_HT"></span>**Dot11 \_ PHY \_ Typ \_ HT**</span><span class="sxs-lookup"><span data-stu-id="0a376-126"><span id="dot11_phy_type_ht"></span><span id="DOT11_PHY_TYPE_HT"></span>**dot11\_phy\_type\_ht**</span></span>
</dt> <dd>

<span data-ttu-id="0a376-127">Gibt den 802.11 n-PHY-Typ an.</span><span class="sxs-lookup"><span data-stu-id="0a376-127">Specifies the 802.11n PHY type.</span></span>

</dd> <dt>

<span data-ttu-id="0a376-128"><span id="dot11_phy_type_vht"></span><span id="DOT11_PHY_TYPE_VHT"></span>**Dot11 \_ PHY \_ Typ \_ VHT**</span><span class="sxs-lookup"><span data-stu-id="0a376-128"><span id="dot11_phy_type_vht"></span><span id="DOT11_PHY_TYPE_VHT"></span>**dot11\_phy\_type\_vht**</span></span>
</dt> <dd>

<span data-ttu-id="0a376-129">Gibt den 802.11-AC-phikentyp an.</span><span class="sxs-lookup"><span data-stu-id="0a376-129">Specifies the 802.11ac PHY type.</span></span> <span data-ttu-id="0a376-130">Dies ist der in IEEE 802.11 AC angegebene extrem hohe Durchsatz-PHY-Typ.</span><span class="sxs-lookup"><span data-stu-id="0a376-130">This is the very high throughput PHY type specified in IEEE 802.11ac.</span></span>

<span data-ttu-id="0a376-131">Dieser Wert wird auf Windows 8.1, Windows Server 2012 R2 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0a376-131">This value is supported on Windows 8.1, Windows Server 2012 R2, and later.</span></span>

</dd> <dt>

<span data-ttu-id="0a376-132"><span id="dot11_phy_type_IHV_start"></span><span id="dot11_phy_type_ihv_start"></span><span id="DOT11_PHY_TYPE_IHV_START"></span>**Dot11 \_ PHY \_ Type \_ IHV \_ Start**</span><span class="sxs-lookup"><span data-stu-id="0a376-132"><span id="dot11_phy_type_IHV_start"></span><span id="dot11_phy_type_ihv_start"></span><span id="DOT11_PHY_TYPE_IHV_START"></span>**dot11\_phy\_type\_IHV\_start**</span></span>
</dt> <dd>

<span data-ttu-id="0a376-133">Gibt den Anfang des Bereichs an, der zum Definieren von PHY-Typen verwendet wird, die von einem unabhängigen Hardwarehersteller (IHV) entwickelt wurden.</span><span class="sxs-lookup"><span data-stu-id="0a376-133">Specifies the start of the range that is used to define PHY types that are developed by an independent hardware vendor (IHV).</span></span>

</dd> <dt>

<span data-ttu-id="0a376-134"><span id="dot11_phy_type_IHV_end"></span><span id="dot11_phy_type_ihv_end"></span><span id="DOT11_PHY_TYPE_IHV_END"></span>**Dot11 \_ PHY \_ Typ \_ IHV \_ Ende**</span><span class="sxs-lookup"><span data-stu-id="0a376-134"><span id="dot11_phy_type_IHV_end"></span><span id="dot11_phy_type_ihv_end"></span><span id="DOT11_PHY_TYPE_IHV_END"></span>**dot11\_phy\_type\_IHV\_end**</span></span>
</dt> <dd>

<span data-ttu-id="0a376-135">Gibt den Anfang des Bereichs an, der zum Definieren von PHY-Typen verwendet wird, die von einem unabhängigen Hardwarehersteller (IHV) entwickelt wurden.</span><span class="sxs-lookup"><span data-stu-id="0a376-135">Specifies the start of the range that is used to define PHY types that are developed by an independent hardware vendor (IHV).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0a376-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0a376-136">Remarks</span></span>

<span data-ttu-id="0a376-137">Ein IHV kann einen Wert für seine proprietären PHY-Typen vom **Dot11 \_ PHY \_ Type \_ IHV \_ Start** through **Dot11 \_ PHY \_ Type \_ IHV \_ End** zuweisen.</span><span class="sxs-lookup"><span data-stu-id="0a376-137">An IHV can assign a value for its proprietary PHY types from **dot11\_phy\_type\_IHV\_start** through **dot11\_phy\_type\_IHV\_end**.</span></span> <span data-ttu-id="0a376-138">Der IHV muss eine eindeutige Zahl aus diesem Bereich für jeden seiner eigenen eigenen PHY-Typen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="0a376-138">The IHV must assign a unique number from this range for each of its proprietary PHY types.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a376-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0a376-139">Requirements</span></span>



| <span data-ttu-id="0a376-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0a376-140">Requirement</span></span> | <span data-ttu-id="0a376-141">Wert</span><span class="sxs-lookup"><span data-stu-id="0a376-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0a376-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0a376-142">Minimum supported client</span></span><br/> | <span data-ttu-id="0a376-143">Windows Vista, Windows XP mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0a376-143">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="0a376-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0a376-144">Minimum supported server</span></span><br/> | <span data-ttu-id="0a376-145">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0a376-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0a376-146">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="0a376-146">Redistributable</span></span><br/>          | <span data-ttu-id="0a376-147">Drahtlose LAN-API für Windows XP mit SP2</span><span class="sxs-lookup"><span data-stu-id="0a376-147">Wireless LAN API for Windows XP with SP2</span></span><br/>                                   |
| <span data-ttu-id="0a376-148">Header</span><span class="sxs-lookup"><span data-stu-id="0a376-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a376-149"><dt>Windot11. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a376-149"><dt>Windot11.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a376-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0a376-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a376-151">**WLAN-Zuordnungs \_ \_ Attribute**</span><span class="sxs-lookup"><span data-stu-id="0a376-151">**WLAN\_ASSOCIATION\_ATTRIBUTES**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_association_attributes)
</dt> <dt>

[<span data-ttu-id="0a376-152">**WLAN- \_ Schnittstellen \_ Funktion**</span><span class="sxs-lookup"><span data-stu-id="0a376-152">**WLAN\_INTERFACE\_CAPABILITY**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_interface_capability)
</dt> </dl>

 

 




