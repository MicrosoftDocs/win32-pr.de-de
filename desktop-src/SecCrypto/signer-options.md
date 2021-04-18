---
description: Legt die Zertifikat Option des Signatur Gebers fest oder ruft Sie ab.
ms.assetid: 2362b9d4-d4d8-46fb-8791-7e856827fb31
title: Signer. Options (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer.Options
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c22cf7b9d9ebe7e98e534d62b0a2771391c6cacb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365683"
---
# <a name="signeroptions-property"></a><span data-ttu-id="d54e9-103">Signer. Options (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d54e9-103">Signer.Options property</span></span>

<span data-ttu-id="d54e9-104">\[Die **options** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="d54e9-104">\[The **Options** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d54e9-105">Verwenden Sie stattdessen die [**CmsSigner-Klasse**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="d54e9-105">Instead, use the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="d54e9-106">Die **options** -Eigenschaft legt die Zertifikat Option des Signatur Gebers fest oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="d54e9-106">The **Options** property sets or retrieves the signer's certificate option.</span></span>

<span data-ttu-id="d54e9-107">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="d54e9-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d54e9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d54e9-108">Syntax</span></span>


```VB
Signer.Options As CAPICOM_CERTIFICATE_INCLUDE_OPTION
```



## <a name="property-value"></a><span data-ttu-id="d54e9-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="d54e9-109">Property value</span></span>

<span data-ttu-id="d54e9-110">Ein Wert der [**CAPICOM \_ Certificate \_ include- \_ Option**](capicom-certificate-include-option.md) -Enumeration, die die Zertifikat Option des Signatur Gebers angibt.</span><span class="sxs-lookup"><span data-stu-id="d54e9-110">A value of the [**CAPICOM\_CERTIFICATE\_INCLUDE\_OPTION**](capicom-certificate-include-option.md) enumeration that specifies the signer's certificate option.</span></span> <span data-ttu-id="d54e9-111">Der Standardwert ist CAPICOM \_ Certificate \_ include \_ Chain, \_ ausgenommen \_ root.</span><span class="sxs-lookup"><span data-stu-id="d54e9-111">The default value is CAPICOM\_CERTIFICATE\_INCLUDE\_CHAIN\_EXCEPT\_ROOT.</span></span> <span data-ttu-id="d54e9-112">In der folgenden Tabelle sind die möglichen Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="d54e9-112">The following table shows the possible values.</span></span>



| <span data-ttu-id="d54e9-113">Wert</span><span class="sxs-lookup"><span data-stu-id="d54e9-113">Value</span></span>                                                                                                                                                                                                                                                             | <span data-ttu-id="d54e9-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d54e9-114">Meaning</span></span>                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_INCLUDE_CHAIN_EXCEPT_ROOT"></span><span id="capicom_certificate_include_chain_except_root"></span><dl> <span data-ttu-id="d54e9-115"><dt>**CAPICOM- \_ Zertifikats \_ include- \_ Kette \_ mit Ausnahme von \_ root**</dt></span><span class="sxs-lookup"><span data-stu-id="d54e9-115"><dt>**CAPICOM\_CERTIFICATE\_INCLUDE\_CHAIN\_EXCEPT\_ROOT**</dt></span></span> </dl> | <span data-ttu-id="d54e9-116">Speichert alle Zertifikate in der Kette mit Ausnahme der Stamm Entität.</span><span class="sxs-lookup"><span data-stu-id="d54e9-116">Saves all certificates in the chain with the exception of the root entity.</span></span><br/> |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_WHOLE_CHAIN"></span><span id="capicom_certificate_include_whole_chain"></span><dl> <span data-ttu-id="d54e9-117"><dt>**CAPICOM- \_ Zertifikat \_ einschließlich \_ ganzer \_ Kette**</dt></span><span class="sxs-lookup"><span data-stu-id="d54e9-117"><dt>**CAPICOM\_CERTIFICATE\_INCLUDE\_WHOLE\_CHAIN**</dt></span></span> </dl>                    | <span data-ttu-id="d54e9-118">Speichert die komplette Zertifikatskette.</span><span class="sxs-lookup"><span data-stu-id="d54e9-118">Saves the complete certificate chain.</span></span><br/>                                      |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_END_ENTITY_ONLY"></span><span id="capicom_certificate_include_end_entity_only"></span><dl> <span data-ttu-id="d54e9-119"><dt>**CAPICOM- \_ Zertifikat \_ schließt \_ nur End- \_ Entität \_ ein.**</dt></span><span class="sxs-lookup"><span data-stu-id="d54e9-119"><dt>**CAPICOM\_CERTIFICATE\_INCLUDE\_END\_ENTITY\_ONLY**</dt></span></span> </dl>       | <span data-ttu-id="d54e9-120">Speichert nur das Endentitäts Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="d54e9-120">Saves only the end entity certificate.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="d54e9-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d54e9-121">Requirements</span></span>



| <span data-ttu-id="d54e9-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d54e9-122">Requirement</span></span> | <span data-ttu-id="d54e9-123">Wert</span><span class="sxs-lookup"><span data-stu-id="d54e9-123">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d54e9-124">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="d54e9-124">Redistributable</span></span><br/> | <span data-ttu-id="d54e9-125">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="d54e9-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d54e9-126">DLL</span><span class="sxs-lookup"><span data-stu-id="d54e9-126">DLL</span></span><br/>             | <dl> <span data-ttu-id="d54e9-127"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d54e9-127"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d54e9-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d54e9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d54e9-129">**Signatur Geber**</span><span class="sxs-lookup"><span data-stu-id="d54e9-129">**Signer**</span></span>](signer.md)
</dt> </dl>

 

 
