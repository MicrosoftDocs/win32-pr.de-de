---
description: Ruft den Wert einer bestimmten Microsoft .NET Passport-Anmeldeoption ab.
ms.assetid: a38ffed3-a45b-4bac-8101-3e09f34f3891
title: 'IPassportManager3:: get_option-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPassportManager3.get_Option
api_type:
- COM
api_location: ''
ms.openlocfilehash: 289daf9ffbaad872115d0abfd7a618a4f7e44c10
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104392930"
---
# <a name="ipassportmanager3get_option-method"></a><span data-ttu-id="2aec4-103">IPassportManager3:: get- \_ options Methode</span><span class="sxs-lookup"><span data-stu-id="2aec4-103">IPassportManager3::get\_Option method</span></span>

<span data-ttu-id="2aec4-104">Ruft den Wert einer bestimmten Microsoft .NET Passport-Anmeldeoption ab.</span><span class="sxs-lookup"><span data-stu-id="2aec4-104">Retrieves the value of a specific Microsoft .NET Passport sign-in option.</span></span>

> [!Note]  
> <span data-ttu-id="2aec4-105">Die Methode **get \_ Option** gehört zur [**IPassportManager3**](/previous-versions/ms817681(v=msdn.10)) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="2aec4-105">The **get\_Option** method belongs to the [**IPassportManager3**](/previous-versions/ms817681(v=msdn.10)) interface.</span></span> <span data-ttu-id="2aec4-106">In diesem Thema wird die erste Dokumentation ergänzt.</span><span class="sxs-lookup"><span data-stu-id="2aec4-106">This topic supplements the initial documentation.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="2aec4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2aec4-107">Syntax</span></span>


```C++
HRESULT get_Option(
  [in]  BSTR    name,
  [out] VARIANT *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="2aec4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2aec4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2aec4-109">*Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2aec4-109">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2aec4-110">Die abzurufende Anmeldeoption.</span><span class="sxs-lookup"><span data-stu-id="2aec4-110">The sign-in option to be retrieved.</span></span> <span data-ttu-id="2aec4-111">Derzeit ist die einzige unterstützte Option "iMode".</span><span class="sxs-lookup"><span data-stu-id="2aec4-111">Currently, the only supported option is "iMode".</span></span>

</dd> <dt>

<span data-ttu-id="2aec4-112">*PVal* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2aec4-112">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2aec4-113">Ein Zeiger auf einen **Variant** (VT \_ bool), der den Wert der Option empfängt.</span><span class="sxs-lookup"><span data-stu-id="2aec4-113">A pointer to a **VARIANT** (VT\_BOOL) that receives the value of the option.</span></span> <span data-ttu-id="2aec4-114">Dieser Wert kann "true" oder "false" sein.</span><span class="sxs-lookup"><span data-stu-id="2aec4-114">This value can be True or False.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2aec4-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2aec4-115">Return value</span></span>

<span data-ttu-id="2aec4-116">Gibt S \_ OK zurück, wenn die Methode erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="2aec4-116">Returns S\_OK when the method succeeds.</span></span>

## <a name="remarks"></a><span data-ttu-id="2aec4-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2aec4-117">Remarks</span></span>

<span data-ttu-id="2aec4-118">Diese Methode wird mit älteren Versionen des Passport SDK ausgeliefert.</span><span class="sxs-lookup"><span data-stu-id="2aec4-118">This method ships with older versions of the Passport SDK.</span></span>

 

 
