---
title: Idschreitelocalfontfileloader-Schnittstelle
description: Eine integrierte Implementierung der idschreitefontfileloader-Schnittstelle, die mit lokalen Schriftart Dateien arbeitet und lokale Schriftart Dateiinformationen aus dem Schriftart Datei-Verweis Schlüssel verfügbar macht.
ms.assetid: acb777c8-24c6-452e-8f58-8fb2ad8c0b6c
keywords:
- Idwrite telocalfontfileloader-Schnittstelle direkt schreiben
- Direkter Schreibvorgang der idschreitelocalfontfileloader-Schnittstelle, beschrieben
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c65f537dc2a4a96161a11d85ae0a4e1869a331e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371185"
---
# <a name="idwritelocalfontfileloader-interface"></a><span data-ttu-id="350e8-105">Idschreitelocalfontfileloader-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="350e8-105">IDWriteLocalFontFileLoader interface</span></span>

<span data-ttu-id="350e8-106">Eine integrierte Implementierung der [**idschreitefontfileloader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) -Schnittstelle, die mit lokalen Schriftart Dateien arbeitet und lokale Schriftart Dateiinformationen aus dem Schriftart Datei-Verweis Schlüssel verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="350e8-106">A built-in implementation of the [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) interface, that operates on local font files and exposes local font file information from the font file reference key.</span></span> <span data-ttu-id="350e8-107">Verweise auf Schriftart Dateien, [**die mithilfe von**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) "" erstellt wurden, verwenden dieses Schriftart Datei Lade Tool.</span><span class="sxs-lookup"><span data-stu-id="350e8-107">Font file references created using [**CreateFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) use this font file loader.</span></span>

## <a name="members"></a><span data-ttu-id="350e8-108">Member</span><span class="sxs-lookup"><span data-stu-id="350e8-108">Members</span></span>

<span data-ttu-id="350e8-109">Die **idwrite telocalfontfileloader** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="350e8-109">The **IDWriteLocalFontFileLoader** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="350e8-110">**Idwrite telocalfontfileloader** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="350e8-110">**IDWriteLocalFontFileLoader** also has these types of members:</span></span>

-   [<span data-ttu-id="350e8-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="350e8-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="350e8-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="350e8-112">Methods</span></span>

<span data-ttu-id="350e8-113">Die **idwrite telocalfontfileloader** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="350e8-113">The **IDWriteLocalFontFileLoader** interface has these methods.</span></span>



| <span data-ttu-id="350e8-114">Methode</span><span class="sxs-lookup"><span data-stu-id="350e8-114">Method</span></span>                                                                                  | <span data-ttu-id="350e8-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="350e8-115">Description</span></span>                                                                               |
|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="350e8-116">**Getfilepathfromkey**</span><span class="sxs-lookup"><span data-stu-id="350e8-116">**GetFilePathFromKey**</span></span>](idwritelocalfontfileloader-getfilepathfromkey.md)             | <span data-ttu-id="350e8-117">Ruft den absoluten Schriftart Datei Pfad aus dem Verweis Schlüssel der Schriftart Datei ab.</span><span class="sxs-lookup"><span data-stu-id="350e8-117">Obtains the absolute font file path from the font file reference key.</span></span><br/>          |
| [<span data-ttu-id="350e8-118">**Getfilepathlängen fromkey**</span><span class="sxs-lookup"><span data-stu-id="350e8-118">**GetFilePathLengthFromKey**</span></span>](idwritelocalfontfileloader-getfilepathlengthfromkey.md) | <span data-ttu-id="350e8-119">Ruft die Länge des absoluten Dateipfads aus dem Verweis Schlüssel der Schriftart Datei ab.</span><span class="sxs-lookup"><span data-stu-id="350e8-119">Obtains the length of the absolute file path from the font file reference key.</span></span><br/> |
| [<span data-ttu-id="350e8-120">**Getlastschreitetimefromkey**</span><span class="sxs-lookup"><span data-stu-id="350e8-120">**GetLastWriteTimeFromKey**</span></span>](idwritelocalfontfileloader-getlastwritetimefromkey.md)   | <span data-ttu-id="350e8-121">Ruft den Zeitpunkt des letzten Schreibzugriffs auf die Datei aus dem Verweis Schlüssel der Schriftart Datei ab.</span><span class="sxs-lookup"><span data-stu-id="350e8-121">Obtains the last write time of the file from the font file reference key.</span></span><br/>      |



 

## <a name="requirements"></a><span data-ttu-id="350e8-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="350e8-122">Requirements</span></span>



| <span data-ttu-id="350e8-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="350e8-123">Requirement</span></span> | <span data-ttu-id="350e8-124">Wert</span><span class="sxs-lookup"><span data-stu-id="350e8-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="350e8-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="350e8-125">Library</span></span><br/> | <dl> <span data-ttu-id="350e8-126"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="350e8-126"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="350e8-127">DLL</span><span class="sxs-lookup"><span data-stu-id="350e8-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="350e8-128"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="350e8-128"><dt>Dwrite.dll</dt></span></span> </dl> |



 

