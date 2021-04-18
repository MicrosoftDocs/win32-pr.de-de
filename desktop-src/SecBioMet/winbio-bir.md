---
title: WINBIO_BIR Struktur (winbio \_ types. h)
description: Stellt einen biometrischen Informationsdaten Satz (BIR) dar.
ms.assetid: 39cfab34-0416-4897-bf95-a1b3c3a6a7a1
keywords:
- WINBIO_BIR Struktur Windows-Biometrieframework-API
topic_type:
- apiref
api_name:
- WINBIO_BIR
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e422bbe59414d75541127b41e5e2cc1829adaaa7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344272"
---
# <a name="winbio_bir-structure"></a><span data-ttu-id="86e4f-104">Winbio- \_ Struktur "Bir"</span><span class="sxs-lookup"><span data-stu-id="86e4f-104">WINBIO\_BIR structure</span></span>

<span data-ttu-id="86e4f-105">Die Struktur von **winbio \_ Bir** stellt einen biometrischen Informationsdaten Satz (BIR) dar.</span><span class="sxs-lookup"><span data-stu-id="86e4f-105">The **WINBIO\_BIR** structure represents a biometric information record (BIR).</span></span> <span data-ttu-id="86e4f-106">Der Informationsdaten Satz enthält Header-, Daten-und Signatur Blöcke.</span><span class="sxs-lookup"><span data-stu-id="86e4f-106">The information record contains header, data, and signature blocks.</span></span>

## <a name="syntax"></a><span data-ttu-id="86e4f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="86e4f-107">Syntax</span></span>


```C++
typedef struct _WINBIO_BIR {
  WINBIO_BIR_DATA HeaderBlock;
  WINBIO_BIR_DATA StandardDataBlock;
  WINBIO_BIR_DATA VendorDataBlock;
  WINBIO_BIR_DATA SignatureBlock;
} WINBIO_BIR;
```



## <a name="members"></a><span data-ttu-id="86e4f-108">Member</span><span class="sxs-lookup"><span data-stu-id="86e4f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="86e4f-109">**Headerblock**</span><span class="sxs-lookup"><span data-stu-id="86e4f-109">**HeaderBlock**</span></span>
</dt> <dd>

<span data-ttu-id="86e4f-110">Eine [**winbio \_ - \_ Daten**](winbio-bir-data.md) Struktur, die die Größe, in Bytes und den Offset des BIR-Headers enthält.</span><span class="sxs-lookup"><span data-stu-id="86e4f-110">A [**WINBIO\_BIR\_DATA**](winbio-bir-data.md) structure that contains the size, in bytes, and offset of the BIR header.</span></span> <span data-ttu-id="86e4f-111">Der-Header enthält Informationen, mit denen der Inhalt des Informationsdaten Satzes beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="86e4f-111">The header contains information that describes the contents of the information record.</span></span>

</dd> <dt>

<span data-ttu-id="86e4f-112">**Standarddatablock**</span><span class="sxs-lookup"><span data-stu-id="86e4f-112">**StandardDataBlock**</span></span>
</dt> <dd>

<span data-ttu-id="86e4f-113">Eine [**winbio \_ - \_ Daten**](winbio-bir-data.md) Struktur, die die Größe, in Bytes und den Offset der verarbeiteten oder nicht verarbeiteten biometrischen Informationen enthält, die vom Windows-Biometrieframework (WBF) erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="86e4f-113">A [**WINBIO\_BIR\_DATA**](winbio-bir-data.md) structure that contains the size, in bytes, and offset of processed or unprocessed biometric information created by the Windows Biometric Framework (WBF).</span></span>

</dd> <dt>

<span data-ttu-id="86e4f-114">**Vendordatablock**</span><span class="sxs-lookup"><span data-stu-id="86e4f-114">**VendorDataBlock**</span></span>
</dt> <dd>

<span data-ttu-id="86e4f-115">Eine [**winbio \_ - \_ Daten**](winbio-bir-data.md) Struktur, die die Größe, in Bytes und den Offset der verarbeiteten oder nicht verarbeiteten biometrischen Informationen von Hersteller Sensoren und Software enthält.</span><span class="sxs-lookup"><span data-stu-id="86e4f-115">A [**WINBIO\_BIR\_DATA**](winbio-bir-data.md) structure that contains the size, in bytes, and offset of processed or unprocessed biometric information provided by vendor sensors and software.</span></span>

</dd> <dt>

<span data-ttu-id="86e4f-116">**Signatureblock**</span><span class="sxs-lookup"><span data-stu-id="86e4f-116">**SignatureBlock**</span></span>
</dt> <dd>

<span data-ttu-id="86e4f-117">Eine optionale [**winbio \_ - \_ Daten**](winbio-bir-data.md) Struktur, die die Größe (in Bytes) und den Offset des Mac (Digital Signature Message Authentication Code) enthält, der zum Überprüfen der Integrität von Bir verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="86e4f-117">An optional [**WINBIO\_BIR\_DATA**](winbio-bir-data.md) structure that contains the size, in bytes, and offset of the digital signature message authentication code (MAC) that can be used to verify the integrity of the BIR.</span></span> <span data-ttu-id="86e4f-118">Falls vorhanden, muss die Signatur oder der Mac den Header und die Datenblöcke abdecken.</span><span class="sxs-lookup"><span data-stu-id="86e4f-118">If present, the signature or MAC must cover the header and data blocks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="86e4f-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="86e4f-119">Remarks</span></span>

<span data-ttu-id="86e4f-120">Die Verwendung von Offsets anstelle von Zeigern ermöglicht die einfache Serialisierung von Bir und für eine weniger komplizierte Übersetzung zwischen 32-und 64-Bit-Umgebungen oder zwischen Benutzer-und Kernel Modus.</span><span class="sxs-lookup"><span data-stu-id="86e4f-120">The use of offsets rather than pointers allows for easy serialization of the BIR and for less complicated translation between 32 and 64-bit environments or between user and kernel mode.</span></span>

<span data-ttu-id="86e4f-121">Der BIR ist mit dem allgemeinen CBEFF (biometrische Exchange Format Framework) kompatibel, das von NIST 6529-A definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="86e4f-121">The BIR is compatible with the Common Biometric Exchange Format Framework (CBEFF) defined by NIST 6529-A.</span></span>

<span data-ttu-id="86e4f-122">Wenn diese Struktur einen *standarddatablock* -Wert enthält, muss der *Typparameter* des Headers, der vom Header *Block* -Parameter angegeben wird, auf den **\_ \_ \_ \_ Formattyp winbio ANSI 381** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="86e4f-122">If this structure contains a *StandardDataBlock* value, the *Type* parameter of the header specified by the *HeaderBlock* parameter must be set to **WINBIO\_ANSI\_381\_FORMAT\_TYPE**.</span></span> <span data-ttu-id="86e4f-123">Dies ist das einzige Standarddatenformat, das von der aktuellen Version der Windows-Biometrieframework unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="86e4f-123">This is the only standard data format supported by the current version of the Windows Biometric Framework.</span></span>

## <a name="requirements"></a><span data-ttu-id="86e4f-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="86e4f-124">Requirements</span></span>



| <span data-ttu-id="86e4f-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="86e4f-125">Requirement</span></span> | <span data-ttu-id="86e4f-126">Wert</span><span class="sxs-lookup"><span data-stu-id="86e4f-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86e4f-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="86e4f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="86e4f-128">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="86e4f-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="86e4f-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="86e4f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="86e4f-130">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="86e4f-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="86e4f-131">Header</span><span class="sxs-lookup"><span data-stu-id="86e4f-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="86e4f-132"><dt>Winbio \_ types. h (Include winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="86e4f-132"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86e4f-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="86e4f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86e4f-134">Client Anwendungs Strukturen</span><span class="sxs-lookup"><span data-stu-id="86e4f-134">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="86e4f-135">**winbio \_ - \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="86e4f-135">**WINBIO\_BIR\_DATA**</span></span>](winbio-bir-data.md)
</dt> <dt>

[<span data-ttu-id="86e4f-136">**winbio- \_ Bir- \_ Header**</span><span class="sxs-lookup"><span data-stu-id="86e4f-136">**WINBIO\_BIR\_HEADER**</span></span>](winbio-bir-header.md)
</dt> </dl>

 

 





