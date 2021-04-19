---
description: Fügt einer Empfänger Auflistung ein Zertifikat Objekt hinzu.
ms.assetid: 2a1b9e0f-ccbf-4042-871b-397de6b6fc35
title: Empfängers. Add-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 255d17485e3423d50cd86b092c2120605f0f1106
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357606"
---
# <a name="recipientsadd-method"></a><span data-ttu-id="ee51f-103">Empfängers. Add-Methode</span><span class="sxs-lookup"><span data-stu-id="ee51f-103">Recipients.Add method</span></span>

<span data-ttu-id="ee51f-104">\[Die **Add** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="ee51f-104">\[The **Add** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ee51f-105">Verwenden Sie stattdessen die [**cmsrecepentcollection-Klasse**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="ee51f-105">Instead, use the [**CmsRecipientCollection Class**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="ee51f-106">Mit der **Add** -Methode wird einer [**Empfänger**](recipients.md) Auflistung ein [**Zertifikat**](certificate.md) Objekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ee51f-106">The **Add** method adds a [**Certificate**](certificate.md) object to a [**Recipients**](recipients.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee51f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee51f-107">Syntax</span></span>


```VB
Recipients.Add( _
  ByVal Certificate _
)
```



## <a name="parameters"></a><span data-ttu-id="ee51f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee51f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee51f-109">*Zertifikat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ee51f-109">*Certificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee51f-110">Ausdruck, der in das [**Zertifikat**](certificate.md) Objekt aufgelöst wird, das der Auflistung hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ee51f-110">Expression that resolves to the [**Certificate**](certificate.md) object to be added to the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee51f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ee51f-111">Return value</span></span>

<span data-ttu-id="ee51f-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ee51f-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee51f-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ee51f-113">Requirements</span></span>



| <span data-ttu-id="ee51f-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ee51f-114">Requirement</span></span> | <span data-ttu-id="ee51f-115">Wert</span><span class="sxs-lookup"><span data-stu-id="ee51f-115">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee51f-116">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="ee51f-116">Redistributable</span></span><br/> | <span data-ttu-id="ee51f-117">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="ee51f-117">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ee51f-118">DLL</span><span class="sxs-lookup"><span data-stu-id="ee51f-118">DLL</span></span><br/>             | <dl> <span data-ttu-id="ee51f-119"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee51f-119"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee51f-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee51f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee51f-121">**Kryptografieobjekte**</span><span class="sxs-lookup"><span data-stu-id="ee51f-121">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="ee51f-122">**Empfänger**</span><span class="sxs-lookup"><span data-stu-id="ee51f-122">**Recipients**</span></span>](recipients.md)
</dt> </dl>

 

 
