---
title: Closedcaption. getsamilangname-Methode
description: Die getsamilangname-Methode ruft den Namen einer Sprache ab, die von der aktuellen Sami-Datei unterstützt wird.
ms.assetid: 20cf8faf-3a8c-4d7b-9bd1-2366672f0e67
keywords:
- getsamilangname-Methode, Windows Media Player
- getsamilangname-Methode, Windows Media Player, closedcaption-Klasse
- Closedcaption-Klasse, Windows Media Player, getsamilangname-Methode
topic_type:
- apiref
api_name:
- ClosedCaption.getSAMILangName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccd4b481de808ac8814e596cfc038aec38c7f19b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359410"
---
# <a name="closedcaptiongetsamilangname-method"></a><span data-ttu-id="fac6a-106">Closedcaption. getsamilangname-Methode</span><span class="sxs-lookup"><span data-stu-id="fac6a-106">ClosedCaption.getSAMILangName method</span></span>

<span data-ttu-id="fac6a-107">Die **getsamilangname** -Methode ruft den Namen einer Sprache ab, die von der aktuellen Sami-Datei unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="fac6a-107">The **getSAMILangName** method retrieves the name of a language supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="fac6a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="fac6a-108">Syntax</span></span>


```JScript
strRetVal = ClosedCaption.getSAMILangName(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="fac6a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="fac6a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fac6a-110">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fac6a-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fac6a-111">**Number** (**Long**), der den Index des abzurufenden sprach namens angibt.</span><span class="sxs-lookup"><span data-stu-id="fac6a-111">**Number** (**long**) specifying the index of the language name to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fac6a-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fac6a-112">Return value</span></span>

<span data-ttu-id="fac6a-113">Diese Methode gibt eine **Zeichenfolge** zurück, die den Namen der Sprache enthält, wie in der Sami-Datei angegeben.</span><span class="sxs-lookup"><span data-stu-id="fac6a-113">This method returns a **String** containing the name of the language as specified in the SAMI file.</span></span>

## <a name="remarks"></a><span data-ttu-id="fac6a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fac6a-114">Remarks</span></span>

<span data-ttu-id="fac6a-115">Die Sprachen in einer Sami-Datei werden in der in der Datei gezeigten Reihenfolge indiziert, beginnend mit 0 (null).</span><span class="sxs-lookup"><span data-stu-id="fac6a-115">The languages in a SAMI file are indexed in the order shown in the file, starting with zero.</span></span>

<span data-ttu-id="fac6a-116">Diese Methode kann erst verwendet werden, wenn eine digitale Mediendatei (*Player*) geöffnet ist.**openstate** ist gleich 13).</span><span class="sxs-lookup"><span data-stu-id="fac6a-116">This method cannot be used until a digital media file is open (*Player*.**openState** is equal to 13).</span></span>

<span data-ttu-id="fac6a-117">**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fac6a-117">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="fac6a-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fac6a-118">Requirements</span></span>



| <span data-ttu-id="fac6a-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fac6a-119">Requirement</span></span> | <span data-ttu-id="fac6a-120">Wert</span><span class="sxs-lookup"><span data-stu-id="fac6a-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fac6a-121">Version</span><span class="sxs-lookup"><span data-stu-id="fac6a-121">Version</span></span><br/> | <span data-ttu-id="fac6a-122">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="fac6a-122">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="fac6a-123">DLL</span><span class="sxs-lookup"><span data-stu-id="fac6a-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="fac6a-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fac6a-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fac6a-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fac6a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fac6a-126">**Hinzufügen von Untertiteln zu digitalen Medien**</span><span class="sxs-lookup"><span data-stu-id="fac6a-126">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="fac6a-127">**Closedcaption-Objekt**</span><span class="sxs-lookup"><span data-stu-id="fac6a-127">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> <dt>

[<span data-ttu-id="fac6a-128">**Closedcaption. samilang**</span><span class="sxs-lookup"><span data-stu-id="fac6a-128">**ClosedCaption.SAMILang**</span></span>](closedcaption-samilang.md)
</dt> </dl>

 

 





