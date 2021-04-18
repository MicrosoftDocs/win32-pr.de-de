---
title: Idwrite telocalfontfileloader getfilepathlängen fromkey-Methode
description: Ruft die Länge des absoluten Dateipfads aus dem Verweis Schlüssel der Schriftart Datei ab.
ms.assetid: bdd84d75-5a7a-448a-a52c-0f5997ab07b9
keywords:
- Getfilepathlängen fromkey-Methode direkt schreiben
- Getfilepathlängen fromkey-Methode Direct Write, idwrite telocalfontfileloader-Schnittstelle
- Idwrite telocalfontfileloader-Schnittstelle Direct Write, getfilepathlängen fromkey-Methode
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader.GetFilePathLengthFromKey
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 091c3cd5f1e13c40d364a3db005793f1dd0bf5f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365523"
---
# <a name="idwritelocalfontfileloadergetfilepathlengthfromkey-method"></a><span data-ttu-id="03d5a-106">Idwrite telocalfontfileloader:: getfilepathlängen fromkey-Methode</span><span class="sxs-lookup"><span data-stu-id="03d5a-106">IDWriteLocalFontFileLoader::GetFilePathLengthFromKey method</span></span>

<span data-ttu-id="03d5a-107">Ruft die Länge des absoluten Dateipfads aus dem Verweis Schlüssel der Schriftart Datei ab.</span><span class="sxs-lookup"><span data-stu-id="03d5a-107">Obtains the length of the absolute file path from the font file reference key.</span></span>

## <a name="syntax"></a><span data-ttu-id="03d5a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="03d5a-108">Syntax</span></span>


```C++
HRESULT GetFilePathLengthFromKey(
  [in]  const void   *fontFileReferenceKey,
              UINT32 fontFileReferenceKeySize,
  [out]       UINT32 *filePathLength
);
```



## <a name="parameters"></a><span data-ttu-id="03d5a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="03d5a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03d5a-110">*fontfilereferencekey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="03d5a-110">*fontFileReferenceKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03d5a-111">Typ: Konstante **void \***</span><span class="sxs-lookup"><span data-stu-id="03d5a-111">Type: **const void\***</span></span>

<span data-ttu-id="03d5a-112">Verweis Schlüssel der Schriftart Datei, der die lokale Schriftart Datei innerhalb des Gültigkeits Bereichs des verwendeten Schriftart Lade Moduls eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="03d5a-112">Font file reference key that uniquely identifies the local font file within the scope of the font loader being used.</span></span>

</dd> <dt>

<span data-ttu-id="03d5a-113">*fontfilereferencekeysize*</span><span class="sxs-lookup"><span data-stu-id="03d5a-113">*fontFileReferenceKeySize*</span></span> 
</dt> <dd>

<span data-ttu-id="03d5a-114">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="03d5a-114">Type: **UINT32**</span></span>

<span data-ttu-id="03d5a-115">Größe des Verweis Schlüssels der Schriftart Datei in Bytes.</span><span class="sxs-lookup"><span data-stu-id="03d5a-115">Size of font file reference key in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="03d5a-116">*filepathlength* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="03d5a-116">*filePathLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="03d5a-117">Typ: **UInt32 \***</span><span class="sxs-lookup"><span data-stu-id="03d5a-117">Type: **UINT32\***</span></span>

<span data-ttu-id="03d5a-118">Länge der Dateipfad-Zeichenfolge ohne das beendete **null** Zeichen.</span><span class="sxs-lookup"><span data-stu-id="03d5a-118">Length of the file path string, not including the terminated **NULL** character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03d5a-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="03d5a-119">Return value</span></span>

<span data-ttu-id="03d5a-120">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="03d5a-120">Type: **HRESULT**</span></span>

<span data-ttu-id="03d5a-121">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="03d5a-121">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="03d5a-122">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="03d5a-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="03d5a-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="03d5a-123">Requirements</span></span>



| <span data-ttu-id="03d5a-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="03d5a-124">Requirement</span></span> | <span data-ttu-id="03d5a-125">Wert</span><span class="sxs-lookup"><span data-stu-id="03d5a-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="03d5a-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="03d5a-126">Library</span></span><br/> | <dl> <span data-ttu-id="03d5a-127"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="03d5a-127"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="03d5a-128">DLL</span><span class="sxs-lookup"><span data-stu-id="03d5a-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="03d5a-129"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03d5a-129"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03d5a-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03d5a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03d5a-131">**Idschreitelocalfontfileloader**</span><span class="sxs-lookup"><span data-stu-id="03d5a-131">**IDWriteLocalFontFileLoader**</span></span>](idwritelocalfontfileloader.md)
</dt> </dl>

 

 





