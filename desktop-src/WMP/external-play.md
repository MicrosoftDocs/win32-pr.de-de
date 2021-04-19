---
title: Extern. Play-Methode
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt. Die Play-Methode weist Windows Media Player an, einen Satz von Medien Elementen wiederzugeben.
ms.assetid: 3e1f45db-9e7f-4a1b-aaa2-513a19c46f70
keywords:
- Wiedergabemethode Windows Media Player
- Wiedergabemethode, Windows Media Player, externe Klasse
- Externe Klasse, Windows Media Player, Wiedergabemethode
topic_type:
- apiref
api_name:
- External.play
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94cfa40d96bbc67c7d41eb1a1a0188be68ec154e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355886"
---
# <a name="externalplay-method"></a><span data-ttu-id="9aeed-108">Extern. Play-Methode</span><span class="sxs-lookup"><span data-stu-id="9aeed-108">External.play method</span></span>

> [!Note]  
> <span data-ttu-id="9aeed-109">In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher</span><span class="sxs-lookup"><span data-stu-id="9aeed-109">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="9aeed-110">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9aeed-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="9aeed-111">Die **Play** -Methode weist Windows Media Player an, einen Satz von Medien Elementen wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="9aeed-111">The **play** method instructs Windows Media Player to play a set of media items.</span></span>

## <a name="syntax"></a><span data-ttu-id="9aeed-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="9aeed-112">Syntax</span></span>


```JScript
External.play(
  LibraryLocationType,
  LibraryLocationIDs
)
```



## <a name="parameters"></a><span data-ttu-id="9aeed-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="9aeed-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9aeed-114">*Librarylocationtype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9aeed-114">*LibraryLocationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aeed-115">Eine [Bibliotheks Speicherort Konstante](library-location-constants.md) , die den Typ der zu Wiedergabe enden Medienelemente angibt.</span><span class="sxs-lookup"><span data-stu-id="9aeed-115">A [library location constant](library-location-constants.md) that specifies the type of the media items to be played.</span></span> <span data-ttu-id="9aeed-116">Cpalbumid gibt beispielsweise an, dass ein oder mehrere Alben wiedergegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9aeed-116">For example, CPAlbumID specifies that one or more albums are to be played.</span></span>

</dd> <dt>

<span data-ttu-id="9aeed-117">*Librarylocationids* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9aeed-117">*LibraryLocationIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aeed-118">Eine **Zeichenfolge** mit den Bezeichnerzeichen, die durch Semikolons getrennt sind, der zu Wiedergabe enden Medienelemente.</span><span class="sxs-lookup"><span data-stu-id="9aeed-118">**String** containing the identifiers, delimited by semicolons, of the media items to be played.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9aeed-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9aeed-119">Return value</span></span>

<span data-ttu-id="9aeed-120">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9aeed-120">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9aeed-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9aeed-121">Requirements</span></span>



| <span data-ttu-id="9aeed-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9aeed-122">Requirement</span></span> | <span data-ttu-id="9aeed-123">Wert</span><span class="sxs-lookup"><span data-stu-id="9aeed-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9aeed-124">Version</span><span class="sxs-lookup"><span data-stu-id="9aeed-124">Version</span></span><br/> | <span data-ttu-id="9aeed-125">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="9aeed-125">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="9aeed-126">DLL</span><span class="sxs-lookup"><span data-stu-id="9aeed-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="9aeed-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9aeed-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9aeed-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9aeed-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9aeed-129">**Externes Objekt für den Typ 1-Online Speicher**</span><span class="sxs-lookup"><span data-stu-id="9aeed-129">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





