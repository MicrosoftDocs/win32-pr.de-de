---
description: Diese Funktion nimmt das Ursprungs Attribut an, wenn es aus dem Ursprungs Token vorhanden ist, und legt Sie auf ein Duplikat des vererbenden Tokens fest und gibt das doppelte Token zurück.
ms.assetid: ED1FAEA1-0665-49FA-BD8B-232254B4C883
title: srpinvereroriginclaim-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- srpInheritOriginClaim
api_type:
- DllExport
api_location:
- srpapi.dll
ms.openlocfilehash: 3edf274622bc1a2611bc49d710a809bd80bd501a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348760"
---
# <a name="srpinheritoriginclaim-function"></a><span data-ttu-id="456a1-103">srpinvereroriginclaim-Funktion</span><span class="sxs-lookup"><span data-stu-id="456a1-103">srpInheritOriginClaim function</span></span>

<span data-ttu-id="456a1-104">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="456a1-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="456a1-105">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="456a1-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="456a1-106">Diese Funktion nimmt das Ursprungs Attribut an, wenn es aus dem Ursprungs Token vorhanden ist, und legt Sie auf ein Duplikat des vererbenden Tokens fest und gibt das doppelte Token zurück.</span><span class="sxs-lookup"><span data-stu-id="456a1-106">This function takes the origin attribute if present from the origin token and sets them on a duplicate of the inheriting token, and returns the duplicate token.</span></span> <span data-ttu-id="456a1-107">Der Aufrufer kann dann die Identität des zurückgegebenen Tokens annehmen.</span><span class="sxs-lookup"><span data-stu-id="456a1-107">The caller can then impersonate the returned token.</span></span> <span data-ttu-id="456a1-108">Diese Funktion verfügt über keine zugeordnete Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="456a1-108">This function has no associated import library.</span></span> <span data-ttu-id="456a1-109">Sie müssen die [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit srpapi.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="456a1-109">You must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to srpapi.dll.</span></span>

## <a name="syntax"></a><span data-ttu-id="456a1-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="456a1-110">Syntax</span></span>


```C++
HRESULT WINAPI srpInheritOriginClaim(
  _In_ Handle OriginToken,
  _In_ Handle InheritingToken,
       Handle ResultToken
);
```



## <a name="parameters"></a><span data-ttu-id="456a1-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="456a1-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="456a1-112">*Origintoken* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="456a1-112">*OriginToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="456a1-113">Handle für das Token, das dupliziert wird und das geerbte Ursprungs Attribut empfängt.</span><span class="sxs-lookup"><span data-stu-id="456a1-113">Handle to the token which is duplicated and receives the inherited origin attribute.</span></span> <span data-ttu-id="456a1-114">Dieses Handle muss mit dem Token für \_ doppelte Zugriffsrechte geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="456a1-114">This handle must be opened with the TOKEN\_DUPLICATE access right.</span></span>

</dd> <dt>

<span data-ttu-id="456a1-115">*Vererbe Token* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="456a1-115">*InheritingToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="456a1-116">Handle für das Token, das dupliziert wird und das geerbte Ursprungs Attribut empfängt.</span><span class="sxs-lookup"><span data-stu-id="456a1-116">Handle to the token which is duplicated and receives the inherited origin attribute.</span></span> <span data-ttu-id="456a1-117">Dieses Handle muss mit dem Token für \_ doppelte Zugriffsrechte geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="456a1-117">This handle must be opened with the TOKEN\_DUPLICATE access right.</span></span> 

</dd> <dt>

<span data-ttu-id="456a1-118">*Resulttoken*</span><span class="sxs-lookup"><span data-stu-id="456a1-118">*ResultToken*</span></span> 
</dt> <dd>

<span data-ttu-id="456a1-119">Bei Erfolg empfängt das duplizierte Token.</span><span class="sxs-lookup"><span data-stu-id="456a1-119">On success, receives the duplicated token.</span></span> <span data-ttu-id="456a1-120">Der Aufrufer kann ihn annehmen, um Vorgänge mit dem geerbten Ursprungs Attribut auszuführen.</span><span class="sxs-lookup"><span data-stu-id="456a1-120">The caller can impersonate it to perform operations with the inherited origin attribute.</span></span> <span data-ttu-id="456a1-121">Der Aufrufer übernimmt den Besitz dieses Handles und muss ihn schließen.</span><span class="sxs-lookup"><span data-stu-id="456a1-121">The caller takes ownership of this handle and must close it.</span></span> 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="456a1-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="456a1-122">Return value</span></span>

<span data-ttu-id="456a1-123">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="456a1-123">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="456a1-124">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="456a1-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="456a1-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="456a1-125">Requirements</span></span>



| <span data-ttu-id="456a1-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="456a1-126">Requirement</span></span> | <span data-ttu-id="456a1-127">Wert</span><span class="sxs-lookup"><span data-stu-id="456a1-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="456a1-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="456a1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="456a1-129">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="456a1-129">Windows 10 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="456a1-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="456a1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="456a1-131">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="456a1-131">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="456a1-132">DLL</span><span class="sxs-lookup"><span data-stu-id="456a1-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="456a1-133"><dt>Srpapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="456a1-133"><dt>Srpapi.dll</dt></span></span> </dl> |



 

