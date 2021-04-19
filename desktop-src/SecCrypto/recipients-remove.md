---
description: Entfernt ein Zertifikat Objekt aus einer Empfänger Auflistung.
ms.assetid: bb75f6d0-4bab-40dd-9d0c-f0431da9c5f3
title: Empfängers. Remove-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 06d276e2d8e75e8822cee3503a7e8342a94a6b0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351251"
---
# <a name="recipientsremove-method"></a><span data-ttu-id="11e1f-103">Empfängers. Remove-Methode</span><span class="sxs-lookup"><span data-stu-id="11e1f-103">Recipients.Remove method</span></span>

<span data-ttu-id="11e1f-104">\[Die **Remove** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="11e1f-104">\[The **Remove** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="11e1f-105">Verwenden Sie stattdessen die [**cmsrecepentcollection-Klasse**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="11e1f-105">Instead, use the [**CmsRecipientCollection Class**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="11e1f-106">Die **Remove** -Methode entfernt ein [**Zertifikat**](certificate.md) Objekt aus einer [**Empfänger**](recipients.md) Auflistung.</span><span class="sxs-lookup"><span data-stu-id="11e1f-106">The **Remove** method removes a [**Certificate**](certificate.md) object from a [**Recipients**](recipients.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="11e1f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="11e1f-107">Syntax</span></span>


```VB
Recipients.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a><span data-ttu-id="11e1f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="11e1f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11e1f-109">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11e1f-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11e1f-110">Der Index des [**Zertifikat**](certificate.md) Objekts, das aus der Auflistung entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="11e1f-110">Index of the [**Certificate**](certificate.md) object to be removed from the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11e1f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="11e1f-111">Return value</span></span>

<span data-ttu-id="11e1f-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="11e1f-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="11e1f-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11e1f-113">Requirements</span></span>



| <span data-ttu-id="11e1f-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11e1f-114">Requirement</span></span> | <span data-ttu-id="11e1f-115">Wert</span><span class="sxs-lookup"><span data-stu-id="11e1f-115">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="11e1f-116">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="11e1f-116">Redistributable</span></span><br/> | <span data-ttu-id="11e1f-117">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="11e1f-117">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="11e1f-118">DLL</span><span class="sxs-lookup"><span data-stu-id="11e1f-118">DLL</span></span><br/>             | <dl> <span data-ttu-id="11e1f-119"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11e1f-119"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11e1f-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11e1f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11e1f-121">**Kryptografieobjekte**</span><span class="sxs-lookup"><span data-stu-id="11e1f-121">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="11e1f-122">**Empfänger**</span><span class="sxs-lookup"><span data-stu-id="11e1f-122">**Recipients**</span></span>](recipients.md)
</dt> </dl>

 

 
