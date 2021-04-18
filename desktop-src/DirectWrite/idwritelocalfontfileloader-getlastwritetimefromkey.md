---
title: Idwrite telocalfontfileloader getlastschreitetimefromkey-Methode
description: Ruft den Zeitpunkt des letzten Schreibzugriffs auf die Datei aus dem Verweis Schlüssel der Schriftart Datei ab.
ms.assetid: ce7f5321-8ad8-4412-a54c-7102790e99c0
keywords:
- Getlastwrite tetimefromkey-Methode direkt schreiben
- Getlastwrite tetimefromkey-Methode Direct Write, idwrite telocalfontfileloader-Schnittstelle
- Idwrite telocalfontfileloader-Schnittstelle Direct Write, getlastschreitetimefromkey-Methode
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader.GetLastWriteTimeFromKey
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea9817917a59761278a961a6fcafcdeaea5fda32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365678"
---
# <a name="idwritelocalfontfileloadergetlastwritetimefromkey-method"></a><span data-ttu-id="46954-106">Idwrite telocalfontfileloader:: getlastschreitetimefromkey-Methode</span><span class="sxs-lookup"><span data-stu-id="46954-106">IDWriteLocalFontFileLoader::GetLastWriteTimeFromKey method</span></span>

<span data-ttu-id="46954-107">Ruft den Zeitpunkt des letzten Schreibzugriffs auf die Datei aus dem Verweis Schlüssel der Schriftart Datei ab.</span><span class="sxs-lookup"><span data-stu-id="46954-107">Obtains the last write time of the file from the font file reference key.</span></span>

## <a name="syntax"></a><span data-ttu-id="46954-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="46954-108">Syntax</span></span>


```C++
virtual HRESULT GetLastWriteTimeFromKey(
  [in]  const void     *fontFileReferenceKey,
              UINT32   fontFileReferenceKeySize,
  [out]       FILETIME *lastWriteTime
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="46954-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="46954-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46954-110">*fontfilereferencekey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46954-110">*fontFileReferenceKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46954-111">Typ: Konstante **void \***</span><span class="sxs-lookup"><span data-stu-id="46954-111">Type: **const void\***</span></span>

<span data-ttu-id="46954-112">Der Verweis Schlüssel der Schriftart Datei, der die lokale Schriftart Datei innerhalb des Gültigkeits Bereichs des verwendeten Schriftart Lade Moduls eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="46954-112">The font file reference key that uniquely identifies the local font file within the scope of the font loader being used.</span></span>

</dd> <dt>

<span data-ttu-id="46954-113">*fontfilereferencekeysize*</span><span class="sxs-lookup"><span data-stu-id="46954-113">*fontFileReferenceKeySize*</span></span> 
</dt> <dd>

<span data-ttu-id="46954-114">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="46954-114">Type: **UINT32**</span></span>

<span data-ttu-id="46954-115">Die Größe des Verweis Schlüssels der Schriftart Datei in Bytes.</span><span class="sxs-lookup"><span data-stu-id="46954-115">The size of font file reference key in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="46954-116">*lastschreibzeit* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="46954-116">*lastWriteTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46954-117">Typ: **FILETIME \***</span><span class="sxs-lookup"><span data-stu-id="46954-117">Type: **FILETIME\***</span></span>

<span data-ttu-id="46954-118">Der Zeitpunkt der letzten Änderung der Schriftart Datei.</span><span class="sxs-lookup"><span data-stu-id="46954-118">The time of the last font file modification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46954-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="46954-119">Return value</span></span>

<span data-ttu-id="46954-120">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="46954-120">Type: **HRESULT**</span></span>

<span data-ttu-id="46954-121">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="46954-121">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="46954-122">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="46954-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="46954-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46954-123">Requirements</span></span>



| <span data-ttu-id="46954-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="46954-124">Requirement</span></span> | <span data-ttu-id="46954-125">Wert</span><span class="sxs-lookup"><span data-stu-id="46954-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="46954-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="46954-126">Library</span></span><br/> | <dl> <span data-ttu-id="46954-127"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="46954-127"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="46954-128">DLL</span><span class="sxs-lookup"><span data-stu-id="46954-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="46954-129"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46954-129"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46954-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46954-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46954-131">**Idschreitelocalfontfileloader**</span><span class="sxs-lookup"><span data-stu-id="46954-131">**IDWriteLocalFontFileLoader**</span></span>](idwritelocalfontfileloader.md)
</dt> </dl>

 

 





