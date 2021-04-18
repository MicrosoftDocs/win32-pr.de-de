---
description: Schließt ein HCERTSTORE-handle, das über die StoreHandle-Eigenschaft abgerufen wurde.
ms.assetid: 1b0d3d9b-09e0-4035-88ac-2887b3ab60c9
title: 'Icertstore:: CloseHandle-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore.CloseHandle
- CertStore.CloseHandle
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: bb1e9ab032b76b8ef02de786d1fc39af0b0d54b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361080"
---
# <a name="icertstoreclosehandle-method"></a><span data-ttu-id="5aead-103">Icertstore:: CloseHandle-Methode</span><span class="sxs-lookup"><span data-stu-id="5aead-103">ICertStore::CloseHandle method</span></span>

<span data-ttu-id="5aead-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="5aead-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="5aead-105">Die **CloseHandle** -Methode schließt ein HCERTSTORE-handle, das über die [**storeHandle**](icertstore-storehandle.md) -Eigenschaft abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="5aead-105">The **CloseHandle** method closes an HCERTSTORE handle acquired through the [**StoreHandle**](icertstore-storehandle.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="5aead-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5aead-106">Syntax</span></span>


```VB
CertStore.CloseHandle( _
  ByVal hCertStore _
)
```



## <a name="parameters"></a><span data-ttu-id="5aead-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="5aead-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5aead-108">*HCERTSTORE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5aead-108">*hCertStore* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5aead-109">Das zu schließende HCERTSTORE-handle.</span><span class="sxs-lookup"><span data-stu-id="5aead-109">The HCERTSTORE handle to be closed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5aead-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5aead-110">Return value</span></span>

<span data-ttu-id="5aead-111">Der Rückgabewert ist ein **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="5aead-111">The return value is an **HRESULT**.</span></span> <span data-ttu-id="5aead-112">Der Wert **S \_ OK** weist auf Erfolg hin.</span><span class="sxs-lookup"><span data-stu-id="5aead-112">A value of **S\_OK** indicates success.</span></span> <span data-ttu-id="5aead-113">Jeder andere Wert gibt an, dass der Vorgang fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="5aead-113">Any other value indicates that the operation failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="5aead-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5aead-114">Remarks</span></span>

<span data-ttu-id="5aead-115">Mit dieser Methode wird das in einem [**Speicher**](store.md) Objekt enthaltene HCERTSTORE-Handle nicht freigegeben.</span><span class="sxs-lookup"><span data-stu-id="5aead-115">This method does not release the HCERTSTORE handle contained within a [**Store**](store.md) object.</span></span> <span data-ttu-id="5aead-116">Es sollte nur verwendet werden, um ein HCERTSTORE-Handle freizugeben, das über die [**storeHandle**](icertstore-storehandle.md) -Eigenschaft abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="5aead-116">It should be used only to release a HCERTSTORE handle acquired through the [**StoreHandle**](icertstore-storehandle.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="5aead-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5aead-117">Requirements</span></span>



| <span data-ttu-id="5aead-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5aead-118">Requirement</span></span> | <span data-ttu-id="5aead-119">Wert</span><span class="sxs-lookup"><span data-stu-id="5aead-119">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5aead-120">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="5aead-120">Redistributable</span></span><br/> | <span data-ttu-id="5aead-121">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="5aead-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="5aead-122">DLL</span><span class="sxs-lookup"><span data-stu-id="5aead-122">DLL</span></span><br/>             | <dl> <span data-ttu-id="5aead-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5aead-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5aead-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5aead-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5aead-125">**Icertstore**</span><span class="sxs-lookup"><span data-stu-id="5aead-125">**ICertStore**</span></span>](icertstore.md)
</dt> </dl>

 

 




