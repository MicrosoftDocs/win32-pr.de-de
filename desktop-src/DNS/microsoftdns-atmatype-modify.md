---
title: Modify-Methode der MicrosoftDNS_ATMAType-Klasse
description: Die Modify-Methode aktualisiert einen Atma-Ressourcen Eintrag (ATM-Adresse).
ms.assetid: 202fc38d-fb8f-4044-bb7d-9e041cbde8ec
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_ATMAType-Klasse
- DNS-MicrosoftDNS_ATMAType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_ATMAType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48d784e9421641dc53d64bb39a2e97b0d9ef257b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040620"
---
# <a name="modify-method-of-the-microsoftdns_atmatype-class"></a><span data-ttu-id="cd6ff-106">Modify-Methode der MicrosoftDNS \_ atmatype-Klasse</span><span class="sxs-lookup"><span data-stu-id="cd6ff-106">Modify method of the MicrosoftDNS\_ATMAType class</span></span>

<span data-ttu-id="cd6ff-107">Die **Modify** -Methode aktualisiert einen Atma-Ressourcen Eintrag (ATM-Adresse).</span><span class="sxs-lookup"><span data-stu-id="cd6ff-107">The **Modify** method updates an ATM Address to Name (ATMA) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd6ff-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd6ff-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] uint16                Format,
  [in, optional] string                ATMAddress,
  [out, ref]     MicrosoftDNS_ATMAType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="cd6ff-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="cd6ff-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd6ff-110">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="cd6ff-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cd6ff-111">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="cd6ff-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="cd6ff-112">*Format* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="cd6ff-112">*Format* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cd6ff-113">ATM-Adressformat.</span><span class="sxs-lookup"><span data-stu-id="cd6ff-113">ATM address format.</span></span> <span data-ttu-id="cd6ff-114">Zwei mögliche Werte für das Format sind: 0, was das AESA-Format (ATM End System Address) angibt, und 1 gibt das E. 164-Format an.</span><span class="sxs-lookup"><span data-stu-id="cd6ff-114">Two possible values for FORMAT are: 0 indicating ATM End System Address (AESA) format and 1 indicating E.164 format.</span></span>

</dd> <dt>

<span data-ttu-id="cd6ff-115">*Atmaddress* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="cd6ff-115">*ATMAddress* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cd6ff-116">Zeichenfolge mit variabler Länge von Oktetten, die die ATM-Adresse des Knotens bzw. Besitzers enthält, auf den sich diese RR bezieht.</span><span class="sxs-lookup"><span data-stu-id="cd6ff-116">Variable length string of octets containing the ATM address of the node/owner to which this RR pertains.</span></span> <span data-ttu-id="cd6ff-117">Die ersten vier Bytes des Arrays werden verwendet, um die Größe der Oktett-Zeichenfolge zu speichern.</span><span class="sxs-lookup"><span data-stu-id="cd6ff-117">The first four bytes of the array are used to store the size of the octet string.</span></span> <span data-ttu-id="cd6ff-118">Das signifikanteste Byte wird in Byte 0 gespeichert.</span><span class="sxs-lookup"><span data-stu-id="cd6ff-118">The most significant byte is stored in byte 0.</span></span>

</dd> <dt>

<span data-ttu-id="cd6ff-119">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="cd6ff-119">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="cd6ff-120">Verweis auf das neue-Objekt.</span><span class="sxs-lookup"><span data-stu-id="cd6ff-120">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd6ff-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cd6ff-121">Return value</span></span>

<span data-ttu-id="cd6ff-122">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="cd6ff-122">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd6ff-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cd6ff-123">Remarks</span></span>

<span data-ttu-id="cd6ff-124">Alle Parameter, die nicht angegeben sind, bleiben im geänderten Datensatz unverändert.</span><span class="sxs-lookup"><span data-stu-id="cd6ff-124">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd6ff-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cd6ff-125">Requirements</span></span>



| <span data-ttu-id="cd6ff-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cd6ff-126">Requirement</span></span> | <span data-ttu-id="cd6ff-127">Wert</span><span class="sxs-lookup"><span data-stu-id="cd6ff-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd6ff-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cd6ff-128">Minimum supported client</span></span><br/> | <span data-ttu-id="cd6ff-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="cd6ff-129">None supported</span></span><br/>                                                              |
| <span data-ttu-id="cd6ff-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cd6ff-130">Minimum supported server</span></span><br/> | <span data-ttu-id="cd6ff-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cd6ff-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="cd6ff-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="cd6ff-132">Namespace</span></span><br/>                | <span data-ttu-id="cd6ff-133">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="cd6ff-133">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="cd6ff-134">MOF</span><span class="sxs-lookup"><span data-stu-id="cd6ff-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cd6ff-135"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="cd6ff-135"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd6ff-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd6ff-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd6ff-137">**MicrosoftDNS- \_ atmatype**</span><span class="sxs-lookup"><span data-stu-id="cd6ff-137">**MicrosoftDNS\_ATMAType**</span></span>](microsoftdns-atmatype.md)
</dt> <dt>

[<span data-ttu-id="cd6ff-138">**Methode "kreateinzustancefrompropertydata" der MicrosoftDNS \_ atmatype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="cd6ff-138">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_ATMAType Class**</span></span>](microsoftdns-atmatype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="cd6ff-139">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="cd6ff-139">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





