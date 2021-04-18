---
description: Eine statische erstellerfunktion, die einen xamluipresenter für eine Renderoberfläche in einer Desktop-App erstellen kann.
ms.assetid: 3160E4C2-39D3-8FF5-ED37-78E645D1AC2E
title: Funktion "kreatexamluipresenter"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateXamlUIPresenter
api_type:
- DllExport
api_location:
- Windows.UI.Xaml.dll
ms.openlocfilehash: f9561a179ec4501406e26cb2bbc38ea69b64b979
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365438"
---
# <a name="createxamluipresenter-function"></a><span data-ttu-id="d1e3c-103">Funktion "kreatexamluipresenter"</span><span class="sxs-lookup"><span data-stu-id="d1e3c-103">CreateXamlUIPresenter function</span></span>

<span data-ttu-id="d1e3c-104">Eine statische erstellerfunktion, die einen [**xamluipresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041) für eine Renderoberfläche in einer Desktop-App erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="d1e3c-104">A static creator function that can create a [**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041) for a render surface in a desktop app.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1e3c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1e3c-105">Syntax</span></span>


```C++
 static HRESULT WINAPI CreateXamlUIPresenter(
  _In_  IViewObjectPresentNotifySite                 *pPresentSite,
  _Out_ Windows::UI::Xaml::Hosting::IXamlUIPresenter **ppPresenter
);
```



## <a name="parameters"></a><span data-ttu-id="d1e3c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1e3c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1e3c-107">*ppresentsite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d1e3c-107">*pPresentSite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1e3c-108">Eine vorhandene Hostingschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d1e3c-108">An existing hosting interface.</span></span> <span data-ttu-id="d1e3c-109">Weitere Informationen finden Sie unter **iviewobjectpresentnotifysite** in der Internet Explorer-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="d1e3c-109">See **IViewObjectPresentNotifySite** in Internet Explorer documentation.</span></span>

</dd> <dt>

<span data-ttu-id="d1e3c-110">*pppresenter* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d1e3c-110">*ppPresenter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1e3c-111">Die **\[ exclusiveto \]** -Schnittstelle für eine [**xamluipresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041)-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d1e3c-111">The **\[exclusiveto\]** interface for a [**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1e3c-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d1e3c-112">Return value</span></span>

<span data-ttu-id="d1e3c-113">Ein **HRESULT**-Standard, S ist für Erfolg **\_ OK** .</span><span class="sxs-lookup"><span data-stu-id="d1e3c-113">A standard **HResult**, **S\_OK** for success.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1e3c-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d1e3c-114">Remarks</span></span>

<span data-ttu-id="d1e3c-115">Zum Aufrufen dieser Methode ist eine **DllImport** -Windows.UI.Xaml.dll erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d1e3c-115">Calling this method requires a **DllImport** from Windows.UI.Xaml.dll.</span></span>

<span data-ttu-id="d1e3c-116">Diese Methode kann nicht aus einer Windows Store-App aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d1e3c-116">You cannot call this method from a Windows Store app.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1e3c-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d1e3c-117">Requirements</span></span>



| <span data-ttu-id="d1e3c-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d1e3c-118">Requirement</span></span> | <span data-ttu-id="d1e3c-119">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e3c-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1e3c-120">Header</span><span class="sxs-lookup"><span data-stu-id="d1e3c-120">Header</span></span><br/> | <dl> <span data-ttu-id="d1e3c-121"><dt>Windows. UI. XAML-CoreTypes. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d1e3c-121"><dt>Windows.ui.xaml-coretypes.idl</dt></span></span> </dl> |
| <span data-ttu-id="d1e3c-122">DLL</span><span class="sxs-lookup"><span data-stu-id="d1e3c-122">DLL</span></span><br/>    | <dl> <span data-ttu-id="d1e3c-123"><dt>Windows.UI.Xaml.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1e3c-123"><dt>Windows.UI.Xaml.dll</dt></span></span> </dl>           |



## <a name="see-also"></a><span data-ttu-id="d1e3c-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1e3c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1e3c-125">**Xamluipresenter**</span><span class="sxs-lookup"><span data-stu-id="d1e3c-125">**XamlUIPresenter**</span></span>](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041)
</dt> </dl>

 

 
