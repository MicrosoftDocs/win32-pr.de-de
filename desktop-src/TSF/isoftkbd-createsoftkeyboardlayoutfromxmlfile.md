---
title: ISOFT kbd-Methode für die Methode "deesoftkeyboardlayoutfromxmlfile" (Software-Domänen Controller. h)
description: Die Methode isoftkbd kreatesoftkeyboardlayoutfromxmlfile erstellt ein weiches Tastaturlayout aus der angegebenen XML-Datei.
ms.assetid: e665adab-1d75-4e41-87bf-c8ce0f7a0399
keywords:
- "\"Kreatesoftkeyboardlayoutfromxmlfile\"-Methode Text Dienst-Framework"
- "\"Kreatesoftkeyboardlayoutfromxmlfile\"-Methode Text Dienste-Framework, iSOFT kbd-Schnittstelle"
- ISOFT kbd Interface Text Services Framework, Methode "kreatesoftkeyboardlayoutfromxmlfile"
topic_type:
- apiref
api_name:
- ISoftKbd.CreateSoftKeyboardLayoutFromXMLFile
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9252db845c5e1cc732adc295e1989fee83d4ac6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346317"
---
# <a name="isoftkbdcreatesoftkeyboardlayoutfromxmlfile-method"></a><span data-ttu-id="30727-106">ISOFT kbd:: kreatesoftkeyboardlayoutfromxmlfile-Methode</span><span class="sxs-lookup"><span data-stu-id="30727-106">ISoftKbd::CreateSoftKeyboardLayoutFromXMLFile method</span></span>

<span data-ttu-id="30727-107">Die **isoftkbd:: deesoftkeyboardlayoutfromxmlfile** -Methode erstellt ein weiches Tastaturlayout aus der angegebenen XML-Datei.</span><span class="sxs-lookup"><span data-stu-id="30727-107">The **ISoftKbd::CreateSoftKeyboardLayoutFromXMLFile** method creates a soft keyboard layout from the specified XML file.</span></span>

## <a name="syntax"></a><span data-ttu-id="30727-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="30727-108">Syntax</span></span>


```C++
HRESULT CreateSoftKeyboardLayoutFromXMLFile(
  [in]  WCHAR *lpszKeyboardDesFile,
  [in]  INT   szFileStrLen,
  [out] DWORD *pdwLayoutCookie
);
```



## <a name="parameters"></a><span data-ttu-id="30727-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="30727-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30727-110">*lpszkeyboarddesfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30727-110">*lpszKeyboardDesFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30727-111">Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen der XML-Datei angibt.</span><span class="sxs-lookup"><span data-stu-id="30727-111">Pointer to a zero-terminated string indicating the name of the XML file.</span></span>

</dd> <dt>

<span data-ttu-id="30727-112">*szfilestrinlen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30727-112">*szFileStrLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30727-113">Eine 0-terminierte Zeichenfolge, die die Länge der XML-Datei angibt.</span><span class="sxs-lookup"><span data-stu-id="30727-113">Zero-terminated string indicating the length of the XML file.</span></span>

</dd> <dt>

<span data-ttu-id="30727-114">*pdwlayoutcookie* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="30727-114">*pdwLayoutCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="30727-115">Ein Zeiger auf den Puffer, in dem diese Methode ein weiches Tastaturlayout-Cookie abruft.</span><span class="sxs-lookup"><span data-stu-id="30727-115">Pointer to the buffer in which this method retrieves a soft keyboard layout cookie.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30727-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="30727-116">Return value</span></span>

<span data-ttu-id="30727-117">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="30727-117">This method can return one of these values.</span></span>



| <span data-ttu-id="30727-118">Wert</span><span class="sxs-lookup"><span data-stu-id="30727-118">Value</span></span>                                                                                        | <span data-ttu-id="30727-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="30727-119">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="30727-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="30727-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="30727-121">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="30727-121">The method was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="30727-122"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="30727-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="30727-123">Mindestens ein Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="30727-123">One or more parameters are invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="30727-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30727-124">Requirements</span></span>



| <span data-ttu-id="30727-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="30727-125">Requirement</span></span> | <span data-ttu-id="30727-126">Wert</span><span class="sxs-lookup"><span data-stu-id="30727-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="30727-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="30727-127">Minimum supported client</span></span><br/> | <span data-ttu-id="30727-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="30727-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="30727-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="30727-129">Minimum supported server</span></span><br/> | <span data-ttu-id="30727-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="30727-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="30727-131">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="30727-131">Redistributable</span></span><br/>          | <span data-ttu-id="30727-132">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="30727-132">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="30727-133">Header</span><span class="sxs-lookup"><span data-stu-id="30727-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="30727-134"><dt>Software-Domänen Controller. h</dt></span><span class="sxs-lookup"><span data-stu-id="30727-134"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="30727-135">IDL</span><span class="sxs-lookup"><span data-stu-id="30727-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="30727-136"><dt>Software. idl</dt></span><span class="sxs-lookup"><span data-stu-id="30727-136"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="30727-137">DLL</span><span class="sxs-lookup"><span data-stu-id="30727-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30727-138"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30727-138"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30727-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30727-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30727-140">**Iweichkbd**</span><span class="sxs-lookup"><span data-stu-id="30727-140">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="30727-141">**ISOFT kbd:: kreatesoftkeyboardlayoutfromresource**</span><span class="sxs-lookup"><span data-stu-id="30727-141">**ISoftKbd::CreateSoftKeyboardLayoutFromResource**</span></span>](isoftkbd-createsoftkeyboardlayoutfromresource.md)
</dt> </dl>

 

 





