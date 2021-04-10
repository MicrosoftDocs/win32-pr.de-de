---
title: IReferenceClock-Methode ohne Empfehlung
description: Mit der unempfehlung-Methode wird eine Benachrichtigungs Anforderung abgebrochen.
ms.assetid: 9817a054-0c6c-402f-afb1-54748ff46a4b
keywords:
- Unempfehlung-Methode Windows Media-Format
- Unempfehlung-Methode Windows Media-Format, IReferenceClock-Schnittstelle
- IReferenceClock-Schnittstelle Windows Media-Format, unempfehlung-Methode
topic_type:
- apiref
api_name:
- IReferenceClock.Unadvise
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ba093eefcedb48f2fb46a55ad8a90f9715c6e3c9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104101007"
---
# <a name="ireferenceclockunadvise-method"></a><span data-ttu-id="310e8-106">IReferenceClock:: unempfehlung-Methode</span><span class="sxs-lookup"><span data-stu-id="310e8-106">IReferenceClock::Unadvise method</span></span>

<span data-ttu-id="310e8-107">Mit der **unempfehlung** -Methode wird eine Benachrichtigungs Anforderung abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="310e8-107">The **Unadvise** method cancels a notification request.</span></span>

## <a name="syntax"></a><span data-ttu-id="310e8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="310e8-108">Syntax</span></span>


```C++
HRESULT Unadvise(
   DWORD dwAdviseCookie
);
```



## <a name="parameters"></a><span data-ttu-id="310e8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="310e8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="310e8-110">*dwadviabcookie*</span><span class="sxs-lookup"><span data-stu-id="310e8-110">*dwAdviseCookie*</span></span> 
</dt> <dd>

<span data-ttu-id="310e8-111">Der Bezeichner der zu entfernenden Anforderung.</span><span class="sxs-lookup"><span data-stu-id="310e8-111">Identifier of the request to remove.</span></span> <span data-ttu-id="310e8-112">Verwenden Sie den Wert, der von adviendtime im pdwadviscookie-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="310e8-112">Use the value returned by AdviseTime in the pdwAdviseCookie parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="310e8-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="310e8-113">Return value</span></span>

<span data-ttu-id="310e8-114">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="310e8-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="310e8-115">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="310e8-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="310e8-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="310e8-116">Return code</span></span>                                                                             | <span data-ttu-id="310e8-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="310e8-117">Description</span></span>                                         |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="310e8-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="310e8-118"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="310e8-119">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="310e8-119">The method succeeded.</span></span><br/>                    |
| <dl> <span data-ttu-id="310e8-120"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="310e8-120"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="310e8-121">Der-Bezeichner ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="310e8-121">The identifier passed in does not exist.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="310e8-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="310e8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="310e8-123">**IReferenceClock-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="310e8-123">**IReferenceClock Interface**</span></span>](ireferenceclock.md)
</dt> </dl>

 

 





