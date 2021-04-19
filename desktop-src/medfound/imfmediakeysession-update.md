---
description: Übergibt einen Schlüsselwert mit allen zugeordneten Daten, die vom Modul für die Inhalts Entschlüsselung für das angegebene Schlüsselsystem benötigt werden.
ms.assetid: 29e66037-5f18-4724-b6f2-d85555e6af69
title: 'IMF mediakeysession:: Update-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.Update
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 15bc06523f0cf9a7dc433381dd596cea89608ce7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106366375"
---
# <a name="imfmediakeysessionupdate-method"></a><span data-ttu-id="fba3e-103">IMF mediakeysession:: Update-Methode</span><span class="sxs-lookup"><span data-stu-id="fba3e-103">IMFMediaKeySession::Update method</span></span>

<span data-ttu-id="fba3e-104">Übergibt einen Schlüsselwert mit allen zugeordneten Daten, die vom Modul für die Inhalts Entschlüsselung für das angegebene Schlüsselsystem benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="fba3e-104">Passes in a key value with any associated data required by the Content Decryption Module for the given key system.</span></span>

## <a name="syntax"></a><span data-ttu-id="fba3e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fba3e-105">Syntax</span></span>


```C++
HRESULT Update(
   const BYTE  *key,
         DWORD cb
);
```



## <a name="parameters"></a><span data-ttu-id="fba3e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fba3e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fba3e-107">*key*</span><span class="sxs-lookup"><span data-stu-id="fba3e-107">*key*</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="fba3e-108">*betrieben*</span><span class="sxs-lookup"><span data-stu-id="fba3e-108">*cb*</span></span> 
</dt> <dd>

<span data-ttu-id="fba3e-109">Die Anzahl in Bytes des *Schlüssels*.</span><span class="sxs-lookup"><span data-stu-id="fba3e-109">The count in bytes of *key*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fba3e-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fba3e-110">Return value</span></span>

<span data-ttu-id="fba3e-111">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="fba3e-111">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fba3e-112">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fba3e-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fba3e-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fba3e-113">Requirements</span></span>



| <span data-ttu-id="fba3e-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fba3e-114">Requirement</span></span> | <span data-ttu-id="fba3e-115">Wert</span><span class="sxs-lookup"><span data-stu-id="fba3e-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fba3e-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fba3e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fba3e-117">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="fba3e-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="fba3e-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fba3e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fba3e-119">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fba3e-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="fba3e-120">IDL</span><span class="sxs-lookup"><span data-stu-id="fba3e-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fba3e-121"><dt>MF mediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fba3e-121"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fba3e-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fba3e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fba3e-123">**IMF mediakeysession**</span><span class="sxs-lookup"><span data-stu-id="fba3e-123">**IMFMediaKeySession**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 




