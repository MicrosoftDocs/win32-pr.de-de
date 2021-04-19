---
title: Extern. Download-Methode
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt. Die Download-Methode initiiert den Download eines Satzes von Medien Elementen.
ms.assetid: 10bae41c-0658-4712-8a7e-375a1ec6dc25
keywords:
- Windows-Media Player für die Download Methode
- Download Methode, Windows Media Player, externe Klasse
- Externe Klasse, Windows Media Player, Download Methode
topic_type:
- apiref
api_name:
- External.download
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35ef0c6e6c32e8959e402080796f29a3860fe728
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352831"
---
# <a name="externaldownload-method"></a><span data-ttu-id="ed4f1-108">Extern. Download-Methode</span><span class="sxs-lookup"><span data-stu-id="ed4f1-108">External.download method</span></span>

> [!Note]  
> <span data-ttu-id="ed4f1-109">In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher</span><span class="sxs-lookup"><span data-stu-id="ed4f1-109">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="ed4f1-110">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ed4f1-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="ed4f1-111">Die **Download** -Methode initiiert den Download eines Satzes von Medien Elementen.</span><span class="sxs-lookup"><span data-stu-id="ed4f1-111">The **download** method initiates the download of a set of media items.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed4f1-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed4f1-112">Syntax</span></span>


```JScript
External.download(
  Type,
  IDs
)
```



## <a name="parameters"></a><span data-ttu-id="ed4f1-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed4f1-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed4f1-114">*Typ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed4f1-114">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed4f1-115">Eine [Bibliotheks Speicherort Konstante](library-location-constants.md) , die den Typ des herunter zuladenden Elements angibt.</span><span class="sxs-lookup"><span data-stu-id="ed4f1-115">A [library location constant](library-location-constants.md) that specifies the type of item to be downloaded.</span></span> <span data-ttu-id="ed4f1-116">Beispielsweise gibt cptrackid an, dass mindestens ein Titel heruntergeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ed4f1-116">For example, CPTrackID specifies that one or more tracks are to be downloaded.</span></span>

</dd> <dt>

<span data-ttu-id="ed4f1-117">*IDs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed4f1-117">*IDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed4f1-118">**Zeichenfolge** , die die durch Semikolons getrennten IDs der zu ladenden Medienelemente enthält.</span><span class="sxs-lookup"><span data-stu-id="ed4f1-118">**String** containing the IDs, delimited by semicolons, of the media items to be downloaded.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed4f1-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ed4f1-119">Return value</span></span>

<span data-ttu-id="ed4f1-120">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ed4f1-120">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed4f1-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed4f1-121">Requirements</span></span>



| <span data-ttu-id="ed4f1-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ed4f1-122">Requirement</span></span> | <span data-ttu-id="ed4f1-123">Wert</span><span class="sxs-lookup"><span data-stu-id="ed4f1-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ed4f1-124">Version</span><span class="sxs-lookup"><span data-stu-id="ed4f1-124">Version</span></span><br/> | <span data-ttu-id="ed4f1-125">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="ed4f1-125">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="ed4f1-126">DLL</span><span class="sxs-lookup"><span data-stu-id="ed4f1-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="ed4f1-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed4f1-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed4f1-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed4f1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed4f1-129">**Herunterladen von Medieninhalten**</span><span class="sxs-lookup"><span data-stu-id="ed4f1-129">**Downloading Media Content**</span></span>](downloading-media-content.md)
</dt> <dt>

[<span data-ttu-id="ed4f1-130">**Externes Objekt für den Typ 1-Online Speicher**</span><span class="sxs-lookup"><span data-stu-id="ed4f1-130">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="ed4f1-131">**Extern. kaufen**</span><span class="sxs-lookup"><span data-stu-id="ed4f1-131">**External.buy**</span></span>](external-buy.md)
</dt> <dt>

[<span data-ttu-id="ed4f1-132">**Iwmpcontentpartner::D ownload**</span><span class="sxs-lookup"><span data-stu-id="ed4f1-132">**IWMPContentPartner::Download**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-download)
</dt> </dl>

 

 





