---
title: Show-Methode
description: Show-Methode
ms.assetid: 58adbb55-f4cb-4356-abc4-b85fa3af744d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a05a1adaa46c85f34e02128960330c68d9a86db1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106340486"
---
# <a name="show-method"></a><span data-ttu-id="af45e-103">Show-Methode</span><span class="sxs-lookup"><span data-stu-id="af45e-103">Show Method</span></span>

<span data-ttu-id="af45e-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="af45e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="af45e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="af45e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="af45e-106">Macht das angegebene Zeichen sichtbar und gibt dessen zugeordnete **Animation wieder** .</span><span class="sxs-lookup"><span data-stu-id="af45e-106">Makes the specified character visible and plays its associated **Showing** animation.</span></span>

</dd> <dt>

<span data-ttu-id="af45e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="af45e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="af45e-108">\*Agent ***. Zeichen ("*** Merkmal-ID \* \* *").* \*  \[ *Schnell* anzeigen\]</span><span class="sxs-lookup"><span data-stu-id="af45e-108">*agent ***.Characters ("*** CharacterID\*\*\*").Show*\* \[*Fast*\]</span></span>



| <span data-ttu-id="af45e-109">Teil</span><span class="sxs-lookup"><span data-stu-id="af45e-109">Part</span></span>   | <span data-ttu-id="af45e-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="af45e-110">Description</span></span>                                                                                                                                                                                                                              |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af45e-111">*Fast*</span><span class="sxs-lookup"><span data-stu-id="af45e-111">*Fast*</span></span> | <span data-ttu-id="af45e-112">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="af45e-112">Optional.</span></span> <span data-ttu-id="af45e-113">Ein boolescher Ausdruck, der angibt, ob der Server die **Anzeige** Animation wieder gibt.</span><span class="sxs-lookup"><span data-stu-id="af45e-113">A Boolean expression specifying whether the server plays the **Showing** animation.</span></span> <span data-ttu-id="af45e-114">**True** Überspringt die **Anzeige** Status Animation.</span><span class="sxs-lookup"><span data-stu-id="af45e-114">**True** Skips the **Showing** state animation.</span></span> <br/> <span data-ttu-id="af45e-115">**False** (Standard) lässt die **Anzeige** Status Animation nicht überspringen.</span><span class="sxs-lookup"><span data-stu-id="af45e-115">**False** (Default) Does not skip the **Showing** state animation.</span></span> <br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="af45e-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="af45e-116">Remarks</span></span>

<span data-ttu-id="af45e-117">Wenn Sie einen Objekt Verweis deklarieren und diesen auf diese Methode festlegen, wird ein [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="af45e-117">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="af45e-118">Wenn außerdem die zugeordnete **Anzeige** Animation nicht geladen wurde und Sie den **fast** -Parameter nicht als **true** angegeben haben, legt der Server die [**Status**](status-property.md) -Eigenschaft des **Anforderungs** Objekts auf "failed" (Fehler) mit einer entsprechenden Fehlernummer fest.</span><span class="sxs-lookup"><span data-stu-id="af45e-118">In addition, if the associated **Showing** animation has not been loaded and you have not specified the **Fast** parameter as **True**, the server sets the **Request** object's [**Status**](status-property.md) property to "failed" with an appropriate error number.</span></span> <span data-ttu-id="af45e-119">Wenn Sie also das HTTP-Protokoll verwenden, um auf **Daten der Zeichen** Animation zuzugreifen, verwenden Sie die [**Get**](get-method.md) -Methode, um die Show State-Animation vor dem Aufrufen der **Show** -Methode zu laden.</span><span class="sxs-lookup"><span data-stu-id="af45e-119">Therefore, if you are using the HTTP protocol to access character animation data, use the [**Get**](get-method.md) method to load the **Showing** state animation before calling the **Show** method.</span></span>

<span data-ttu-id="af45e-120">Legen Sie den **fast** -Parameter nicht auf " **true** " fest, ohne zuvor eine Animation vorher zu spielen Andernfalls wird der Zeichen Rahmen möglicherweise ohne Bild angezeigt.</span><span class="sxs-lookup"><span data-stu-id="af45e-120">Avoid setting the **Fast** parameter to **True** without first playing an animation beforehand; otherwise, the character frame may display with no image.</span></span> <span data-ttu-id="af45e-121">Beachten Sie insbesondere Folgendes: Wenn Sie " [**muveto**](moveto-method.md) " anrufen, wenn das Zeichen nicht sichtbar ist, wird keine Animation wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="af45e-121">In particular, note that if you call [**MoveTo**](moveto-method.md) when the character is not visible, it does not play any animation.</span></span> <span data-ttu-id="af45e-122">Wenn Sie also die **Show** -Methode aufrufen, bei der **fast** auf **true** festgelegt ist, wird kein Bild angezeigt.</span><span class="sxs-lookup"><span data-stu-id="af45e-122">Therefore, if you call the **Show** method with **Fast** set to **True**, no image will display.</span></span> <span data-ttu-id="af45e-123">Wenn Sie " [**Ausblenden**](hide-method.md) **" und "mit** **fast** festgelegtem" auf " **true**" aufzurufen, wird das Bild nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="af45e-123">Similarly, if you call [**Hide**](hide-method.md) then **Show** with **Fast** set to **True**, there will be no visible image.</span></span>

## <a name="see-also"></a><span data-ttu-id="af45e-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="af45e-124">See Also</span></span>

[<span data-ttu-id="af45e-125">**Hide-Methode**</span><span class="sxs-lookup"><span data-stu-id="af45e-125">**Hide method**</span></span>](hide-method.md)


 

