---
description: Entfernt alle Zertifikat Objekte aus einer Empfänger Auflistung.
ms.assetid: 456fcfbc-4388-40f4-ab58-04508ee2141b
title: Empfängers. Clear-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients.Clear
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 7d9bd711bbc97997045989f2eb4ffdbc51ae3559
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373681"
---
# <a name="recipientsclear-method"></a><span data-ttu-id="defdb-103">Empfängers. Clear-Methode</span><span class="sxs-lookup"><span data-stu-id="defdb-103">Recipients.Clear method</span></span>

<span data-ttu-id="defdb-104">\[Die **Clear** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="defdb-104">\[The **Clear** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="defdb-105">Verwenden Sie stattdessen die [**cmsrecepentcollection-Klasse**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="defdb-105">Instead, use the [**CmsRecipientCollection Class**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="defdb-106">Die **Clear** -Methode entfernt alle [**Zertifikat**](certificate.md) Objekte aus einer [**Empfänger**](recipients.md) Auflistung.</span><span class="sxs-lookup"><span data-stu-id="defdb-106">The **Clear** method removes all [**Certificate**](certificate.md) objects from a [**Recipients**](recipients.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="defdb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="defdb-107">Syntax</span></span>


```VB
Recipients.Clear()
```



## <a name="parameters"></a><span data-ttu-id="defdb-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="defdb-108">Parameters</span></span>

<span data-ttu-id="defdb-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="defdb-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="defdb-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="defdb-110">Return value</span></span>

<span data-ttu-id="defdb-111">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="defdb-111">This method does not return a value.</span></span> <span data-ttu-id="defdb-112">Eine Anwendung, die diese Methode verwendet, muss Code enthalten, um eine Ausnahme zu behandeln, die von dieser Methode ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="defdb-112">An application that uses this method must contain code to handle an exception raised by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="defdb-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="defdb-113">Requirements</span></span>



| <span data-ttu-id="defdb-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="defdb-114">Requirement</span></span> | <span data-ttu-id="defdb-115">Wert</span><span class="sxs-lookup"><span data-stu-id="defdb-115">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="defdb-116">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="defdb-116">Redistributable</span></span><br/> | <span data-ttu-id="defdb-117">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="defdb-117">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="defdb-118">DLL</span><span class="sxs-lookup"><span data-stu-id="defdb-118">DLL</span></span><br/>             | <dl> <span data-ttu-id="defdb-119"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="defdb-119"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="defdb-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="defdb-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="defdb-121">**Kryptografieobjekte**</span><span class="sxs-lookup"><span data-stu-id="defdb-121">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="defdb-122">**Empfänger**</span><span class="sxs-lookup"><span data-stu-id="defdb-122">**Recipients**</span></span>](recipients.md)
</dt> </dl>

 

 
