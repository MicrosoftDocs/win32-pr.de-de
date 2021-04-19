---
description: Ruft die Schlüssel Spezifikation ab.
ms.assetid: 93c909cb-b1d1-4c2b-a66c-9d3f6dd9b340
title: PrivateKey. KeySpec-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.KeySpec
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f9d0ba55ca48d5257a038845f84374544b7615b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361377"
---
# <a name="privatekeykeyspec-property"></a><span data-ttu-id="56650-103">PrivateKey. KeySpec-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="56650-103">PrivateKey.KeySpec property</span></span>

<span data-ttu-id="56650-104">\[Die **KeySpec** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="56650-104">\[The **KeySpec** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="56650-105">Verwenden Sie stattdessen die [**X509Certificate2. PrivateKey-Eigenschaft**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="56650-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="56650-106">Die **KeySpec** -Eigenschaft ruft die Schlüssel Spezifikation ab.</span><span class="sxs-lookup"><span data-stu-id="56650-106">The **KeySpec** property retrieves the key specification.</span></span>

## <a name="syntax"></a><span data-ttu-id="56650-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="56650-107">Syntax</span></span>


```VB
PrivateKey.KeySpec As CAPICOM_KEY_SPEC
```



## <a name="property-value"></a><span data-ttu-id="56650-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="56650-108">Property value</span></span>

<span data-ttu-id="56650-109">Ein Wert der [**CAPICOM- \_ schlüsselspezifikations \_**](capicom-key-spec.md) Enumeration, der die Schlüssel Spezifikation angibt.</span><span class="sxs-lookup"><span data-stu-id="56650-109">A value of the [**CAPICOM\_KEY\_SPEC**](capicom-key-spec.md) enumeration that indicates the key specification.</span></span> <span data-ttu-id="56650-110">In der folgenden Tabelle sind die möglichen Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="56650-110">The following table shows the possible values.</span></span>



| <span data-ttu-id="56650-111">Wert</span><span class="sxs-lookup"><span data-stu-id="56650-111">Value</span></span>                                                                                                                                                                                                        | <span data-ttu-id="56650-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="56650-112">Meaning</span></span>                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="CAPICOM_KEY_SPEC_KEYEXCHANGE"></span><span id="capicom_key_spec_keyexchange"></span><dl> <span data-ttu-id="56650-113"><dt>**CAPICOM- \_ Schlüssel \_ Spezifikation \_ keyexchange**</dt></span><span class="sxs-lookup"><span data-stu-id="56650-113"><dt>**CAPICOM\_KEY\_SPEC\_KEYEXCHANGE**</dt></span></span> </dl> | <span data-ttu-id="56650-114">Der Schlüssel kann für die Verschlüsselung und Signierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="56650-114">The key can be used for encryption and signing.</span></span><br/> |
| <span id="CAPICOM_KEY_SPEC_SIGNATURE"></span><span id="capicom_key_spec_signature"></span><dl> <span data-ttu-id="56650-115"><dt>**CAPICOM \_ Key \_ spec- \_ Signatur**</dt></span><span class="sxs-lookup"><span data-stu-id="56650-115"><dt>**CAPICOM\_KEY\_SPEC\_SIGNATURE**</dt></span></span> </dl>       | <span data-ttu-id="56650-116">Der Schlüssel kann nur für die Signierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="56650-116">The key can be used only for signing.</span></span><br/>           |



 

## <a name="requirements"></a><span data-ttu-id="56650-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="56650-117">Requirements</span></span>



| <span data-ttu-id="56650-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="56650-118">Requirement</span></span> | <span data-ttu-id="56650-119">Wert</span><span class="sxs-lookup"><span data-stu-id="56650-119">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="56650-120">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="56650-120">Redistributable</span></span><br/> | <span data-ttu-id="56650-121">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="56650-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="56650-122">DLL</span><span class="sxs-lookup"><span data-stu-id="56650-122">DLL</span></span><br/>             | <dl> <span data-ttu-id="56650-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56650-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56650-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56650-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56650-125">**PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="56650-125">**PrivateKey**</span></span>](privatekey.md)
</dt> </dl>

 

 
