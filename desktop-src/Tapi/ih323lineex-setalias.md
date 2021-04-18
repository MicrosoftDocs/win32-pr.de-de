---
description: Die Methode "ltalias" konfiguriert einen standardmäßigen H. 323-Alias für die Adresse. Dieser Alias wird im H. 323-Setup Austausch verwendet, damit die andere Partei den Namen dieser Partei kennt.
ms.assetid: 09608214-7346-4ee8-bbfd-0877d3ad0766
title: IH323LineEx::/talias-Methode (H323priv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7341d177297cf95f46d07e503244f06b2c4dea71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358000"
---
# <a name="ih323lineexsetalias-method"></a><span data-ttu-id="8a801-104">IH323LineEx::/talias-Methode</span><span class="sxs-lookup"><span data-stu-id="8a801-104">IH323LineEx::SetAlias method</span></span>

<span data-ttu-id="8a801-105">\[Der **Server ist für** die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8a801-105">\[**SetAlias** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8a801-106">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="8a801-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8a801-107">Die Methode " **ltalias** " konfiguriert einen standardmäßigen H. 323-Alias für die Adresse.</span><span class="sxs-lookup"><span data-stu-id="8a801-107">The **SetAlias** method configures a default H.323 alias for the address.</span></span> <span data-ttu-id="8a801-108">Dieser Alias wird im H. 323-Setup Austausch verwendet, damit die andere Partei den Namen dieser Partei kennt.</span><span class="sxs-lookup"><span data-stu-id="8a801-108">This alias will be used in the H.323 call setup exchange so that the other party knows the name of this party.</span></span>

<span data-ttu-id="8a801-109">Wenn Sie diese Methode ein zweites Mal aufrufen, wird der vorherige Alias überschrieben.</span><span class="sxs-lookup"><span data-stu-id="8a801-109">Calling this method a second time will overwrite the previous alias.</span></span>

<span data-ttu-id="8a801-110">Der für diese Schnittstelle festgelegte Alias wird nur verwendet, wenn es keine andere Möglichkeit gibt, dass der TSP einen richtigen Alias findet.</span><span class="sxs-lookup"><span data-stu-id="8a801-110">The alias set on this interface will be used only when there is no other way for the TSP to find a proper alias.</span></span> <span data-ttu-id="8a801-111">Wenn die Gatekeeper-Unterstützung in der Zukunft dem TSP hinzugefügt wird, überschreibt der Alias, der für den Gatekeeper registriert ist oder von Gatekeeper zugewiesen wurde, das, was durch diese Methode festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="8a801-111">In the future, when gatekeeper support is added into the TSP, the alias registered to the gatekeeper or assigned by the gatekeeper will override whatever is set through this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a801-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a801-112">Syntax</span></span>


```C++
HRESULT SetAlias(
  [in] WCHAR *strAlias,
  [in] DWORD dwLength
);
```



## <a name="parameters"></a><span data-ttu-id="8a801-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a801-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a801-114">"-"  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8a801-114">*strAlias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a801-115">Der zu verwendende Alias in Unicode.</span><span class="sxs-lookup"><span data-stu-id="8a801-115">The alias to be used, in Unicode.</span></span> <span data-ttu-id="8a801-116">**Null** -Beendigung ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8a801-116">**Null** termination is not required.</span></span>

</dd> <dt>

<span data-ttu-id="8a801-117">*dwLength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8a801-117">*dwLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a801-118">Die Länge des Alias Namens in Anzahl von Zeichen, einschließlich des **null** -Terminator.</span><span class="sxs-lookup"><span data-stu-id="8a801-118">The length of the alias name in number of characters, including the **null** terminator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a801-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8a801-119">Return value</span></span>

<span data-ttu-id="8a801-120">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="8a801-120">This method can return one of these values.</span></span>



| <span data-ttu-id="8a801-121">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="8a801-121">Return code</span></span>                                                                               | <span data-ttu-id="8a801-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8a801-122">Description</span></span>                                                                                                                      |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8a801-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8a801-123"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="8a801-124">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="8a801-124">Method succeeded.</span></span><br/>                                                                                                     |
| <dl> <span data-ttu-id="8a801-125"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="8a801-125"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="8a801-126">Die Anzahl von Zeichen, die in *dwLength* angegeben wird, überschreitet die tatsächliche Anzahl von Zeichen *im Parameter "* -Parameter".</span><span class="sxs-lookup"><span data-stu-id="8a801-126">The number of characters indicated in *dwLength* exceeds the actual number of characters in the *strAlias* parameter.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8a801-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8a801-127">Requirements</span></span>



| <span data-ttu-id="8a801-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8a801-128">Requirement</span></span> | <span data-ttu-id="8a801-129">Wert</span><span class="sxs-lookup"><span data-stu-id="8a801-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8a801-130">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="8a801-130">TAPI version</span></span><br/> | <span data-ttu-id="8a801-131">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="8a801-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="8a801-132">Header</span><span class="sxs-lookup"><span data-stu-id="8a801-132">Header</span></span><br/>       | <dl> <span data-ttu-id="8a801-133"><dt>H323priv. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a801-133"><dt>H323priv.h</dt></span></span> </dl> |
| <span data-ttu-id="8a801-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8a801-134">Library</span></span><br/>      | <dl> <span data-ttu-id="8a801-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8a801-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="8a801-136">DLL</span><span class="sxs-lookup"><span data-stu-id="8a801-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="8a801-137"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a801-137"><dt>Tapi3.dll</dt></span></span> </dl>  |



 

 




