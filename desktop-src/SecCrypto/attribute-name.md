---
description: Legt den CAPICOM-Namen des Attributs fest oder ruft ihn ab. Dies ist die Standard Eigenschaft.
ms.assetid: 082f286e-f2ac-4e45-94b9-abdaa3f4c926
title: Attribute.Name-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attribute.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f71bb231941765dd073d44abd11c56152ea2d975
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352849"
---
# <a name="attributename-property"></a><span data-ttu-id="2c8bb-104">Attribute.Name-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2c8bb-104">Attribute.Name property</span></span>

<span data-ttu-id="2c8bb-105">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2c8bb-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="2c8bb-106">Verwenden Sie stattdessen die [**cryptographiertributeobject-Klasse**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography**](/previous-versions/windows/) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="2c8bb-106">Instead, use the [**CryptographicAttributeObject Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="2c8bb-107">Die **Name** -Eigenschaft legt den CAPICOM-Namen des Attributs fest oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="2c8bb-107">The **Name** property sets or retrieves the CAPICOM name of the attribute.</span></span> <span data-ttu-id="2c8bb-108">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="2c8bb-108">This is the default property.</span></span>

<span data-ttu-id="2c8bb-109">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="2c8bb-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c8bb-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c8bb-110">Syntax</span></span>


```VB
Attribute.Name As CAPICOM_ATTRIBUTE
```



## <a name="property-value"></a><span data-ttu-id="2c8bb-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="2c8bb-111">Property value</span></span>

<span data-ttu-id="2c8bb-112">Ein Wert der [**CAPICOM- \_ Attribut**](capicom-attribute.md) Enumeration, der den CAPICOM-Namen des Attributs angibt.</span><span class="sxs-lookup"><span data-stu-id="2c8bb-112">A value of the [**CAPICOM\_ATTRIBUTE**](capicom-attribute.md) enumeration that specifies the CAPICOM name of the attribute.</span></span> <span data-ttu-id="2c8bb-113">In der folgenden Tabelle sind die möglichen Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="2c8bb-113">The following table shows the possible values.</span></span>



| <span data-ttu-id="2c8bb-114">Wert</span><span class="sxs-lookup"><span data-stu-id="2c8bb-114">Value</span></span>                                                                                                                                                                                                                                                                                 | <span data-ttu-id="2c8bb-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="2c8bb-115">Meaning</span></span>                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME"></span><span id="capicom_authenticated_attribute_signing_time"></span><dl> <span data-ttu-id="2c8bb-116"><dt>**\_Signatur Zeit des authentifizierten CAPICOM- \_ Attributs \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2c8bb-116"><dt>**CAPICOM\_AUTHENTICATED\_ATTRIBUTE\_SIGNING\_TIME**</dt></span></span> </dl>                         | <span data-ttu-id="2c8bb-117">Das-Attribut enthält den Zeitpunkt, zu dem die Signatur erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="2c8bb-117">The attribute contains the time that the signature was created.</span></span><br/> |
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_NAME"></span><span id="capicom_authenticated_attribute_document_name"></span><dl> <span data-ttu-id="2c8bb-118"><dt>**Name des von CAPICOM \_ authentifizierten \_ Attribut \_ Dokuments \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2c8bb-118"><dt>**CAPICOM\_AUTHENTICATED\_ATTRIBUTE\_DOCUMENT\_NAME**</dt></span></span> </dl>                      | <span data-ttu-id="2c8bb-119">Das-Attribut enthält den Namen des signierten Dokuments.</span><span class="sxs-lookup"><span data-stu-id="2c8bb-119">The attribute contains the name of the signed document.</span></span><br/>         |
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_DESCRIPTION"></span><span id="capicom_authenticated_attribute_document_description"></span><dl> <span data-ttu-id="2c8bb-120"><dt>**Beschreibung des \_ authentifizierten CAPICOM- \_ Attribut \_ Dokuments \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2c8bb-120"><dt>**CAPICOM\_AUTHENTICATED\_ATTRIBUTE\_DOCUMENT\_DESCRIPTION**</dt></span></span> </dl> | <span data-ttu-id="2c8bb-121">Das-Attribut enthält eine Beschreibung des signierten Dokuments.</span><span class="sxs-lookup"><span data-stu-id="2c8bb-121">The attribute contains a description of the signed document.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="2c8bb-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2c8bb-122">Remarks</span></span>

<span data-ttu-id="2c8bb-123">Wenn der Wert dieser Eigenschaft direkt oder indirekt zurückgesetzt wird, wird der gesamte Status des Objekts zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="2c8bb-123">When the value of this property is reset, directly or indirectly, the whole state of the object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c8bb-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2c8bb-124">Requirements</span></span>



| <span data-ttu-id="2c8bb-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2c8bb-125">Requirement</span></span> | <span data-ttu-id="2c8bb-126">Wert</span><span class="sxs-lookup"><span data-stu-id="2c8bb-126">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c8bb-127">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="2c8bb-127">End of client support</span></span><br/> | <span data-ttu-id="2c8bb-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2c8bb-128">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="2c8bb-129">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="2c8bb-129">End of server support</span></span><br/> | <span data-ttu-id="2c8bb-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2c8bb-130">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="2c8bb-131">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="2c8bb-131">Redistributable</span></span><br/>       | <span data-ttu-id="2c8bb-132">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="2c8bb-132">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="2c8bb-133">DLL</span><span class="sxs-lookup"><span data-stu-id="2c8bb-133">DLL</span></span><br/>                   | <dl> <span data-ttu-id="2c8bb-134"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c8bb-134"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c8bb-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c8bb-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c8bb-136">**Versehen**</span><span class="sxs-lookup"><span data-stu-id="2c8bb-136">**Attribute**</span></span>](attribute.md)
</dt> </dl>

 

 
