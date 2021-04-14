---
title: Sohattributevalue-Union (napprotocol. h)
description: Definiert den Inhalt des Typmembers in einer sohattribute-Struktur.
ms.assetid: 53b30455-33a5-4cf5-8d4e-f0fa8e4e1a12
keywords:
- Sohattributevalue Union NAP
topic_type:
- apiref
api_name:
- SoHAttributeValue
api_location:
- NapProtocol.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36660e4e360ff0df31bb3a76d06c50e5d366c894
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478441"
---
# <a name="sohattributevalue-union"></a><span data-ttu-id="0178d-104">Sohattributevalue-Union</span><span class="sxs-lookup"><span data-stu-id="0178d-104">SoHAttributeValue union</span></span>

> [!Note]  
> <span data-ttu-id="0178d-105">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0178d-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="0178d-106">Die **sohattributevalue** -Union definiert den Inhalt des **Typmembers** in einer [**sohattribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="0178d-106">The **SoHAttributeValue** union defines the contents of the **type** member in a [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) structure.</span></span> <span data-ttu-id="0178d-107">Die Struktur der **sohattributevalue** -Union wird durch den [**sohattributetype**](sohattributetype-enum.md) bestimmt, der im **Typmember** der [**sohattribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) -Struktur angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="0178d-107">The structure of the **SoHAttributeValue** union is determined by the [**SoHAttributeType**](sohattributetype-enum.md) specified in the **type** member of the [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="0178d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0178d-108">Syntax</span></span>


```C++
typedef union tagSoHAttributeValue {
  SystemHealthEntityId     idVal;
  struct tagIpv4Addresses {
    UINT16      count;
    Ipv4Address *addresses;
  } v4AddressesVal;
  struct tagIpv6Addresses {
    UINT16      count;
    Ipv6Address *addresses;
  } v6AddressesVal;
  ResultCodes              codesVal;
  FILETIME                 dateTimeVal;
  struct tagVendorSpecific {
    UINT32 vendorId;
    UINT16 size;
    BYTE   *vendorSpecificData;
  } vendorSpecificVal;
  UINT8                    uint8Val;
  struct tagOctetString {
    UINT16 size;
    BYTE   *data;
  } octetStringVal;
} SoHAttributeValue;
```



## <a name="members"></a><span data-ttu-id="0178d-109">Member</span><span class="sxs-lookup"><span data-stu-id="0178d-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="0178d-110">**idval**</span><span class="sxs-lookup"><span data-stu-id="0178d-110">**idVal**</span></span>
</dt> <dd>

<span data-ttu-id="0178d-111">**Case (sohattributetypesystemhealthid)**</span><span class="sxs-lookup"><span data-stu-id="0178d-111">**case(sohAttributeTypeSystemHealthId)**</span></span>

<span data-ttu-id="0178d-112">Eine eindeutige [systemhealthentityid](nap-datatypes.md) , die die ID des Systemintegritäts-Agents (SHA) oder der System Integritätsprüfung (SHV) enthält, von der dieses [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) -Paket erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="0178d-112">A unique [SystemHealthEntityId](nap-datatypes.md) that contains the ID of the System Health Agent (SHA) or System Health Validator (SHV) that constructed this [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>

</dd> <dt>

<span data-ttu-id="0178d-113">**v4AddressesVal**</span><span class="sxs-lookup"><span data-stu-id="0178d-113">**v4AddressesVal**</span></span>
</dt> <dd>

<span data-ttu-id="0178d-114">**Case (sohAttributeTypeIpv4FixupServers)**</span><span class="sxs-lookup"><span data-stu-id="0178d-114">**case(sohAttributeTypeIpv4FixupServers)**</span></span>

<span data-ttu-id="0178d-115">Die IPv4-Adressen der fixupserver, die vom NAP-System verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0178d-115">The IPv4 addresses of the fix-up servers in use by the NAP system.</span></span>

<dl> <dt>

<span data-ttu-id="0178d-116">**count**</span><span class="sxs-lookup"><span data-stu-id="0178d-116">**count**</span></span>
</dt> <dd>

<span data-ttu-id="0178d-117">Die Anzahl der IPv4-Adressen im **Adress** Element im Bereich von 1 bis [**maxIpv4CountPerSoHAttribute**](nap-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="0178d-117">The number of IPv4 addresses in the **addresses** member in the range 1 to [**maxIpv4CountPerSoHAttribute**](nap-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="0178d-118">**addresses**</span><span class="sxs-lookup"><span data-stu-id="0178d-118">**addresses**</span></span>
</dt> <dd>

<span data-ttu-id="0178d-119">Ein Array von [**Ipv4Address**](/windows/win32/api/naptypes/ns-naptypes-ipv4address) -Strukturen, die die IPv4-Adressen enthalten.</span><span class="sxs-lookup"><span data-stu-id="0178d-119">An array of [**Ipv4Address**](/windows/win32/api/naptypes/ns-naptypes-ipv4address) structures that contain the IPv4 addresses.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="0178d-120">**v6AddressesVal**</span><span class="sxs-lookup"><span data-stu-id="0178d-120">**v6AddressesVal**</span></span>
</dt> <dd>

<span data-ttu-id="0178d-121">**Case (sohAttributeTypeIpv6FixupServers)**</span><span class="sxs-lookup"><span data-stu-id="0178d-121">**case(sohAttributeTypeIpv6FixupServers)**</span></span>

<span data-ttu-id="0178d-122">Die IPv6-Adressen der fixupserver, die vom NAP-System verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0178d-122">The IPv6 addresses of the fix-up servers in use by the NAP system.</span></span>

<dl> <dt>

<span data-ttu-id="0178d-123">**count**</span><span class="sxs-lookup"><span data-stu-id="0178d-123">**count**</span></span>
</dt> <dd>

<span data-ttu-id="0178d-124">Die Anzahl der IPv4-Adressen im **Adress** Element im Bereich von 1 bis [**maxIpv6CountPerSoHAttribute**](nap-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="0178d-124">The number of IPv4 addresses in the **addresses** member in the range 1 to [**maxIpv6CountPerSoHAttribute**](nap-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="0178d-125">**addresses**</span><span class="sxs-lookup"><span data-stu-id="0178d-125">**addresses**</span></span>
</dt> <dd>

<span data-ttu-id="0178d-126">Ein Array von [**Ipv6Address**](/windows/win32/api/naptypes/ns-naptypes-ipv6address) -Strukturen, die die IPv4-Adressen enthalten.</span><span class="sxs-lookup"><span data-stu-id="0178d-126">An array of [**Ipv6Address**](/windows/win32/api/naptypes/ns-naptypes-ipv6address) structures that contain the IPv4 addresses.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="0178d-127">**codesval**</span><span class="sxs-lookup"><span data-stu-id="0178d-127">**codesVal**</span></span>
</dt> <dd>

<span data-ttu-id="0178d-128">**Case (sohattributetypecomplianceresultcodes, sohattributetypeerrorcodes)**</span><span class="sxs-lookup"><span data-stu-id="0178d-128">**case(sohAttributeTypeComplianceResultCodes, sohAttributeTypeErrorCodes)**</span></span>

<span data-ttu-id="0178d-129">Eine [**ResultCodes**](/windows/win32/api/naptypes/ns-naptypes-resultcodes) -Struktur, die entweder die von der Anwendung definierten Kompatibilitäts Ergebnis Codes der Client-oder [**NAP-Fehler Konstanten**](nap-error-constants.md)enthält.</span><span class="sxs-lookup"><span data-stu-id="0178d-129">A [**ResultCodes**](/windows/win32/api/naptypes/ns-naptypes-resultcodes) structure that contains either the application defined compliance result codes of the client or [**NAP error constants**](nap-error-constants.md).</span></span> <span data-ttu-id="0178d-130">Ein [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) -Paket muss dieses TLV oder **sohattributetypefailurecategory** TLV enthalten.</span><span class="sxs-lookup"><span data-stu-id="0178d-130">An [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet must contain this TLV or the **sohAttributeTypeFailureCategory** TLV.</span></span>

</dd> <dt>

<span data-ttu-id="0178d-131">**datetimeval**</span><span class="sxs-lookup"><span data-stu-id="0178d-131">**dateTimeVal**</span></span>
</dt> <dd>

<span data-ttu-id="0178d-132">**Case (sohattributetypetimeoflatstupdate, sohattributetypesohgenerationtime)**</span><span class="sxs-lookup"><span data-stu-id="0178d-132">**case(sohAttributeTypeTimeOfLastUpdate, sohAttributeTypeSoHGenerationTime)**</span></span>

<span data-ttu-id="0178d-133">Eine [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) -Struktur, die die Uhrzeit des letzten [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) -Updates oder der **SoH** -Generierungs Zeit enthält.</span><span class="sxs-lookup"><span data-stu-id="0178d-133">A [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure that contains the time of the last [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) update or the **SoH** generation time.</span></span>

</dd> <dt>

<span data-ttu-id="0178d-134">**vendorspecificval**</span><span class="sxs-lookup"><span data-stu-id="0178d-134">**vendorSpecificVal**</span></span>
</dt> <dd>

<span data-ttu-id="0178d-135">**Case (sohattributetypevendorspecific)**</span><span class="sxs-lookup"><span data-stu-id="0178d-135">**case(sohAttributeTypeVendorSpecific)**</span></span>

<span data-ttu-id="0178d-136">Anwendungsspezifische Daten, die vom Hersteller definiert werden.</span><span class="sxs-lookup"><span data-stu-id="0178d-136">Application-specific data that is defined by the vendor.</span></span>

<dl> <dt>

<span data-ttu-id="0178d-137">**vendorId**</span><span class="sxs-lookup"><span data-stu-id="0178d-137">**vendorId**</span></span>
</dt> <dd>

<span data-ttu-id="0178d-138">Ein 4-Byte-Bezeichner, der die SHA/SHV-paar-ID definiert.</span><span class="sxs-lookup"><span data-stu-id="0178d-138">A 4-byte identifier that defines the SHA/SHV pair ID.</span></span> <span data-ttu-id="0178d-139">Die ersten 3 Bytes sind der durch IETF zugewiesene SMI-Code des Anbieters, und das letzte Byte identifiziert die Komponente selbst.</span><span class="sxs-lookup"><span data-stu-id="0178d-139">The first 3 bytes are the IETF-assigned SMI code of the vendor, and the last byte identifies the component itself.</span></span> <span data-ttu-id="0178d-140">Verwenden Sie bei der Implementierung eines SHA-oder SHV-Dienstanbieters nicht die ID-Werte, die internen Microsoft-System Integritäts Komponenten von [**NAP-Anbieter Konstanten**](nap-vendor-constants.md)</span><span class="sxs-lookup"><span data-stu-id="0178d-140">When implementing a SHA or SHV, do not use the ID values assigned to internal Microsoft system health components on [**NAP vendor constants**](nap-vendor-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="0178d-141">**size**</span><span class="sxs-lookup"><span data-stu-id="0178d-141">**size**</span></span>
</dt> <dd>

<span data-ttu-id="0178d-142">Die Größe (in Bytes) der Herstellerdaten im Bereich von 0 bis ([**maxsohattributesize**](nap-type-constants.md) -4).</span><span class="sxs-lookup"><span data-stu-id="0178d-142">The size, in bytes, of the vendor data in the range 0 to ([**maxSoHAttributeSize**](nap-type-constants.md) - 4).</span></span>

</dd> <dt>

<span data-ttu-id="0178d-143">**vendorSpecificData**</span><span class="sxs-lookup"><span data-stu-id="0178d-143">**vendorSpecificData**</span></span>
</dt> <dd>

<span data-ttu-id="0178d-144">Ein Zeiger auf die herstellerspezifischen Daten in der Netzwerk-Byte Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="0178d-144">A pointer to the vendor specific data in network byte order.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="0178d-145">**uint8Val**</span><span class="sxs-lookup"><span data-stu-id="0178d-145">**uint8Val**</span></span>
</dt> <dd>

<span data-ttu-id="0178d-146">**Case (sohattributetypehealthclass, sohattributetypefailurecategory, sohattributetypeextendedisolationstate)**</span><span class="sxs-lookup"><span data-stu-id="0178d-146">**case(sohAttributeTypeHealthClass, sohAttributeTypeFailureCategory,sohAttributeTypeExtendedIsolationState)**</span></span>

<span data-ttu-id="0178d-147">Die Integritäts Klasse, Fehler Kategorie oder der erweiterte Isolations Status einer NAP-Komponente als [**healthclassvalue**](healthclassvalue-enum.md) -Wert oder [**failurecategory**](/windows/win32/api/naptypes/ne-naptypes-failurecategory) -Wert oder in einer [**isolationinfoex**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="0178d-147">The health class, failure category, or extended isolation state of a NAP component as either a [**HealthClassValue**](healthclassvalue-enum.md) or [**FailureCategory**](/windows/win32/api/naptypes/ne-naptypes-failurecategory) value, or a [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0178d-148">**octetstringval**</span><span class="sxs-lookup"><span data-stu-id="0178d-148">**octetStringVal**</span></span>
</dt> <dd>

<span data-ttu-id="0178d-149">**default**</span><span class="sxs-lookup"><span data-stu-id="0178d-149">**default**</span></span>

<span data-ttu-id="0178d-150">Die folgenden Attributwerte sind Oktett-Zeichen folgen:</span><span class="sxs-lookup"><span data-stu-id="0178d-150">The following attributes' values are octet strings:</span></span>

-   <span data-ttu-id="0178d-151">sohattributetypesoftwareversion</span><span class="sxs-lookup"><span data-stu-id="0178d-151">sohAttributeTypeSoftwareVersion</span></span>
-   <span data-ttu-id="0178d-152">sohattributetypeclientid</span><span class="sxs-lookup"><span data-stu-id="0178d-152">sohAttributeTypeClientId</span></span>
-   <span data-ttu-id="0178d-153">sohattributetypeproductname</span><span class="sxs-lookup"><span data-stu-id="0178d-153">sohAttributeTypeProductName</span></span>
-   <span data-ttu-id="0178d-154">sohattributetypehealthclassstatus</span><span class="sxs-lookup"><span data-stu-id="0178d-154">sohAttributeTypeHealthClassStatus</span></span>

<span data-ttu-id="0178d-155">Für die Vorwärtskompatibilität werden alle nicht erkannten Attribute als Oktett-Zeichen folgen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0178d-155">For forward compatibility, all unrecognized attributes are returned as octet strings.</span></span> <span data-ttu-id="0178d-156">die **Daten** müssen in der Reihenfolge der Netzwerk Bytes vorliegen.</span><span class="sxs-lookup"><span data-stu-id="0178d-156">**data** must be in network byte order.</span></span>

<dl> <dt>

<span data-ttu-id="0178d-157">**size**</span><span class="sxs-lookup"><span data-stu-id="0178d-157">**size**</span></span>
</dt> <dd>

<span data-ttu-id="0178d-158">Die Größe (in Bytes) der **Daten** im Bereich von 0 bis [**maxsohattributesize**](nap-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="0178d-158">The size, in bytes, of **data** in the range 0 to [**maxSoHAttributeSize**](nap-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="0178d-159">**data**</span><span class="sxs-lookup"><span data-stu-id="0178d-159">**data**</span></span>
</dt> <dd>

<span data-ttu-id="0178d-160">Ein Zeiger auf den Oktett-Zeichen folgen Wert.</span><span class="sxs-lookup"><span data-stu-id="0178d-160">A pointer to the octet string value.</span></span>

</dd> </dl> </dd> </dl>

## <a name="actual-data-layout"></a><span data-ttu-id="0178d-161">Tatsächliches Datenlayout</span><span class="sxs-lookup"><span data-stu-id="0178d-161">Actual data layout</span></span>

<span data-ttu-id="0178d-162">Aufgrund der Art der SDK-Veröffentlichungs Umgebung werden Unions nicht eindeutig in Syntax Blöcken dargestellt.</span><span class="sxs-lookup"><span data-stu-id="0178d-162">Due to the nature of the SDK publishing environment, unions are not clearly represented in syntax blocks.</span></span> <span data-ttu-id="0178d-163">Dies ist die tatsächliche Syntax aus der Header Datei "napprotocol. h".</span><span class="sxs-lookup"><span data-stu-id="0178d-163">Here is the actual syntax from the NapProtocol.h header file.</span></span>


```C++
#include <windows.h>

typedef [switch_type(SoHAttributeType)] 
   union tagSoHAttributeValue
   {
      [case(sohAttributeTypeSystemHealthId)]
         SystemHealthEntityId idVal;
   
      [case(sohAttributeTypeIpv4FixupServers)]
         struct tagIpv4Addresses
         {
            [range(1, maxIpv4CountPerSoHAttribute)] 
               UINT16 count;
            [size_is(count)] Ipv4Address* addresses;
         } v4AddressesVal;

      [case(sohAttributeTypeIpv6FixupServers)]
         struct tagIpv6Addresses
         {
            [range(1, maxIpv6CountPerSoHAttribute)]
               UINT16 count;
            [size_is(count)] Ipv6Address* addresses;
         } v6AddressesVal;

      [case(sohAttributeTypeComplianceResultCodes, 
            sohAttributeTypeErrorCodes)]
         ResultCodes codesVal;

      [case(sohAttributeTypeTimeOfLastUpdate, 
            sohAttributeTypeSoHGenerationTime)]
         FILETIME dateTimeVal;

      [case(sohAttributeTypeVendorSpecific)]
         struct tagVendorSpecific
         {
            UINT32 vendorId;
            [range(0, maxSoHAttributeSize - 4)] 
               UINT16 size;
            [size_is(size)] BYTE* vendorSpecificData;
         } vendorSpecificVal;

      [case(sohAttributeTypeHealthClass, 
            sohAttributeTypeFailureCategory,
            sohAttributeTypeExtendedIsolationState)]
         UINT8 uint8Val;

      [default]
         struct tagOctetString
         {
            [range(0, maxSoHAttributeSize)] UINT16 size;
            [size_is(size)] BYTE* data;
         } octetStringVal;

   } SoHAttributeValue;
};
```



## <a name="remarks"></a><span data-ttu-id="0178d-164">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0178d-164">Remarks</span></span>

<span data-ttu-id="0178d-165">Diese Attributtypen werden vom NAP-System verwendet:</span><span class="sxs-lookup"><span data-stu-id="0178d-165">These attribute types are consumed by the NAP system:</span></span>

-   <span data-ttu-id="0178d-166">sohattributetypesystemhealthid</span><span class="sxs-lookup"><span data-stu-id="0178d-166">sohAttributeTypeSystemHealthId</span></span>
-   <span data-ttu-id="0178d-167">sohAttributeTypeIpv4FixupServers</span><span class="sxs-lookup"><span data-stu-id="0178d-167">sohAttributeTypeIpv4FixupServers</span></span>
-   <span data-ttu-id="0178d-168">sohAttributeTypeIpv6FixupServers</span><span class="sxs-lookup"><span data-stu-id="0178d-168">sohAttributeTypeIpv6FixupServers</span></span>
-   <span data-ttu-id="0178d-169">sohattributetypecomplianceresultcodes</span><span class="sxs-lookup"><span data-stu-id="0178d-169">sohAttributeTypeComplianceResultCodes</span></span>
-   <span data-ttu-id="0178d-170">sohattributetypefailurecategory</span><span class="sxs-lookup"><span data-stu-id="0178d-170">sohAttributeTypeFailureCategory</span></span>

<span data-ttu-id="0178d-171">Der Rest der [**sohattributetypes**](sohattributetype-enum.md) ist ausschließlich als ausführliche Anleitung für die Verwendung durch SHAs und SHVs gedacht.</span><span class="sxs-lookup"><span data-stu-id="0178d-171">The rest of the [**SoHAttributeTypes**](sohattributetype-enum.md) are meant purely as prescriptive guidance for usage by SHAs and SHVs.</span></span>

## <a name="requirements"></a><span data-ttu-id="0178d-172">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0178d-172">Requirements</span></span>



| <span data-ttu-id="0178d-173">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0178d-173">Requirement</span></span> | <span data-ttu-id="0178d-174">Wert</span><span class="sxs-lookup"><span data-stu-id="0178d-174">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="0178d-175">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0178d-175">Minimum supported client</span></span><br/> | <span data-ttu-id="0178d-176">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0178d-176">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="0178d-177">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0178d-177">Minimum supported server</span></span><br/> | <span data-ttu-id="0178d-178">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0178d-178">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="0178d-179">Header</span><span class="sxs-lookup"><span data-stu-id="0178d-179">Header</span></span><br/>                   | <dl> <span data-ttu-id="0178d-180"><dt>Napprotocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="0178d-180"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="0178d-181">IDL</span><span class="sxs-lookup"><span data-stu-id="0178d-181">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0178d-182"><dt>Napprotocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0178d-182"><dt>NapProtocol.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0178d-183">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0178d-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0178d-184">NAP-Referenz</span><span class="sxs-lookup"><span data-stu-id="0178d-184">NAP Reference</span></span>](nap-reference.md)
</dt> <dt>

[<span data-ttu-id="0178d-185">NAP-Strukturen</span><span class="sxs-lookup"><span data-stu-id="0178d-185">NAP Structures</span></span>](nap-structures.md)
</dt> </dl>

 

