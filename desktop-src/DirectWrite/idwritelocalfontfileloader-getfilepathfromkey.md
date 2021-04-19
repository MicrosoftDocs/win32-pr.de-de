---
title: Idwrite telocalfontfileloader getfilepathfromkey-Methode
description: Ruft den absoluten Schriftart Datei Pfad aus dem Verweis Schlüssel der Schriftart Datei ab.
ms.assetid: a61cfe80-100d-4813-b04f-a39f626893dd
keywords:
- Getfilepathfromkey-Methode direkt schreiben
- Getfilepathfromkey-Methode Direct Write, idwrite telocalfontfileloader-Schnittstelle
- Idwrite telocalfontfileloader-Schnittstelle Direct Write, getfilepathfromkey-Methode
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader.GetFilePathFromKey
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14fb3070ddc2f0d82554c86f005343faa3c087fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361966"
---
# <a name="idwritelocalfontfileloadergetfilepathfromkey-method"></a><span data-ttu-id="2b678-106">Idwrite telocalfontfileloader:: getfilepathfromkey-Methode</span><span class="sxs-lookup"><span data-stu-id="2b678-106">IDWriteLocalFontFileLoader::GetFilePathFromKey method</span></span>

<span data-ttu-id="2b678-107">Ruft den absoluten Schriftart Datei Pfad aus dem Verweis Schlüssel der Schriftart Datei ab.</span><span class="sxs-lookup"><span data-stu-id="2b678-107">Obtains the absolute font file path from the font file reference key.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b678-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b678-108">Syntax</span></span>


```C++
virtual HRESULT GetFilePathFromKey(
  [in]  const void   *fontFileReferenceKey,
              UINT32 fontFileReferenceKeySize,
  [out]       WCHAR  *filePath,
              UINT32 filePathSize
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="2b678-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b678-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b678-110">*fontfilereferencekey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2b678-110">*fontFileReferenceKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b678-111">Typ: Konstante **void \***</span><span class="sxs-lookup"><span data-stu-id="2b678-111">Type: **const void\***</span></span>

<span data-ttu-id="2b678-112">Der Verweis Schlüssel der Schriftart Datei, der die lokale Schriftart Datei innerhalb des Gültigkeits Bereichs des verwendeten Schriftart Lade Moduls eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="2b678-112">The font file reference key that uniquely identifies the local font file within the scope of the font loader being used.</span></span>

</dd> <dt>

<span data-ttu-id="2b678-113">*fontfilereferencekeysize*</span><span class="sxs-lookup"><span data-stu-id="2b678-113">*fontFileReferenceKeySize*</span></span> 
</dt> <dd>

<span data-ttu-id="2b678-114">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2b678-114">Type: **UINT32**</span></span>

<span data-ttu-id="2b678-115">Die Größe des Verweis Schlüssels der Schriftart Datei in Bytes.</span><span class="sxs-lookup"><span data-stu-id="2b678-115">The size of font file reference key in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="2b678-116">*FilePath* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2b678-116">*filePath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b678-117">Typ: **WCHAR \***</span><span class="sxs-lookup"><span data-stu-id="2b678-117">Type: **WCHAR\***</span></span>

<span data-ttu-id="2b678-118">Das Zeichen Array, das den lokalen Dateipfad empfängt.</span><span class="sxs-lookup"><span data-stu-id="2b678-118">The character array that receives the local file path.</span></span>

</dd> <dt>

<span data-ttu-id="2b678-119">*filepathsize*</span><span class="sxs-lookup"><span data-stu-id="2b678-119">*filePathSize*</span></span> 
</dt> <dd>

<span data-ttu-id="2b678-120">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2b678-120">Type: **UINT32**</span></span>

<span data-ttu-id="2b678-121">Die Länge des Dateipfad-Zeichen Arrays.</span><span class="sxs-lookup"><span data-stu-id="2b678-121">The length of the file path character array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b678-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2b678-122">Return value</span></span>

<span data-ttu-id="2b678-123">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2b678-123">Type: **HRESULT**</span></span>

<span data-ttu-id="2b678-124">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="2b678-124">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2b678-125">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2b678-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b678-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2b678-126">Requirements</span></span>



| <span data-ttu-id="2b678-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2b678-127">Requirement</span></span> | <span data-ttu-id="2b678-128">Wert</span><span class="sxs-lookup"><span data-stu-id="2b678-128">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2b678-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2b678-129">Library</span></span><br/> | <dl> <span data-ttu-id="2b678-130"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2b678-130"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="2b678-131">DLL</span><span class="sxs-lookup"><span data-stu-id="2b678-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="2b678-132"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b678-132"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b678-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b678-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b678-134">**Idschreitelocalfontfileloader**</span><span class="sxs-lookup"><span data-stu-id="2b678-134">**IDWriteLocalFontFileLoader**</span></span>](idwritelocalfontfileloader.md)
</dt> </dl>

 

 





