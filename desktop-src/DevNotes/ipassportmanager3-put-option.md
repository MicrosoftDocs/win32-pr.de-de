---
description: Legt eine bestimmte Microsoft .NET Passport-Anmeldeoption fest.
ms.assetid: 5ec79faa-1c74-42a4-b964-ea15edacda79
title: IPassportManager3::p ut_Option-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPassportManager3.put_Option
api_type:
- COM
api_location: ''
ms.openlocfilehash: 52a1324c4b1a04a207b5bccac1a95bcd060be8ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958176"
---
# <a name="ipassportmanager3put_option-method"></a><span data-ttu-id="3c4c4-103">IPassportManager3::p UT- \_ options Methode</span><span class="sxs-lookup"><span data-stu-id="3c4c4-103">IPassportManager3::put\_Option method</span></span>

<span data-ttu-id="3c4c4-104">Legt eine bestimmte Microsoft .NET Passport-Anmeldeoption fest.</span><span class="sxs-lookup"><span data-stu-id="3c4c4-104">Sets a specific Microsoft .NET Passport sign-in option.</span></span>

> [!Note]  
> <span data-ttu-id="3c4c4-105">Die **Put- \_ options** Methode gehört zur [**IPassportManager3**](/previous-versions/ms817681(v=msdn.10)) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="3c4c4-105">The **put\_Option** method belongs to the [**IPassportManager3**](/previous-versions/ms817681(v=msdn.10)) interface.</span></span> <span data-ttu-id="3c4c4-106">In diesem Thema wird die erste Dokumentation ergänzt.</span><span class="sxs-lookup"><span data-stu-id="3c4c4-106">This topic supplements the initial documentation.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="3c4c4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c4c4-107">Syntax</span></span>


```C++
HRESULT put_Option(
   BSTR    name,
   VARIANT newVal
);
```



## <a name="parameters"></a><span data-ttu-id="3c4c4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3c4c4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c4c4-109">*name*</span><span class="sxs-lookup"><span data-stu-id="3c4c4-109">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="3c4c4-110">Die festzulegende Anmeldeoption.</span><span class="sxs-lookup"><span data-stu-id="3c4c4-110">The sign-in option to be set.</span></span> <span data-ttu-id="3c4c4-111">Derzeit ist die einzige unterstützte Option iMode.</span><span class="sxs-lookup"><span data-stu-id="3c4c4-111">Currently, the only supported option is iMode.</span></span>

</dd> <dt>

<span data-ttu-id="3c4c4-112">*NewVal*</span><span class="sxs-lookup"><span data-stu-id="3c4c4-112">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="3c4c4-113">Ein **Variant** (VT \_ bool), der den neuen Wert für die Option angibt.</span><span class="sxs-lookup"><span data-stu-id="3c4c4-113">A **VARIANT** (VT\_BOOL) that specifies the new value for the option.</span></span> <span data-ttu-id="3c4c4-114">Dieser Wert kann "true" oder "false" sein.</span><span class="sxs-lookup"><span data-stu-id="3c4c4-114">This value can be True or False.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c4c4-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3c4c4-115">Return value</span></span>

<span data-ttu-id="3c4c4-116">Gibt S \_ OK zurück, wenn die Methode erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="3c4c4-116">Returns S\_OK when the method succeeds.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c4c4-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3c4c4-117">Remarks</span></span>

<span data-ttu-id="3c4c4-118">Diese Methode wird mit älteren Versionen des Passport SDK ausgeliefert.</span><span class="sxs-lookup"><span data-stu-id="3c4c4-118">This method ships with older versions of the Passport SDK.</span></span>

 

 
