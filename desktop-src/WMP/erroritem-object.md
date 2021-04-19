---
title: ErrorItem-Objekt
description: Das ErrorItem-Objekt bietet eine Möglichkeit, auf Fehlerinformationen zuzugreifen.
ms.assetid: 14bc9c12-98c6-4b72-9ae5-d6afeb1303f9
keywords:
- ErrorItem-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- ErrorItem Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c273d00477363c66c49dfa1f77a66dab42c711cb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106338635"
---
# <a name="erroritem-object"></a><span data-ttu-id="7a146-104">ErrorItem-Objekt</span><span class="sxs-lookup"><span data-stu-id="7a146-104">ErrorItem Object</span></span>

<span data-ttu-id="7a146-105">Das **ErrorItem** -Objekt bietet eine Möglichkeit, auf Fehlerinformationen zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="7a146-105">The **ErrorItem** object provides a way to access error information.</span></span>

<span data-ttu-id="7a146-106">Das **ErrorItem** -Objekt unterstützt die folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7a146-106">The **ErrorItem** object supports the following properties.</span></span>



| <span data-ttu-id="7a146-107">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7a146-107">Property</span></span>                                           | <span data-ttu-id="7a146-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7a146-108">Description</span></span>                                                                                     |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7a146-109">condition</span><span class="sxs-lookup"><span data-stu-id="7a146-109">condition</span></span>](erroritem-condition.md)               | <span data-ttu-id="7a146-110">Ruft einen Wert ab, der die Bedingung für den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="7a146-110">Retrieves a value indicating the condition for the error.</span></span>                                       |
| [<span data-ttu-id="7a146-111">CustomURL</span><span class="sxs-lookup"><span data-stu-id="7a146-111">customUrl</span></span>](erroritem-customurl.md)               | <span data-ttu-id="7a146-112">Ruft die URL einer Website ab, auf der bestimmte Informationen zum Download Fehler beim Codec angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="7a146-112">Retrieves the URL of a website that displays specific information about codec download failure.</span></span> |
| [<span data-ttu-id="7a146-113">ErrorCode</span><span class="sxs-lookup"><span data-stu-id="7a146-113">errorCode</span></span>](erroritem-errorcode.md)               | <span data-ttu-id="7a146-114">Ruft den aktuellen Fehlercode ab.</span><span class="sxs-lookup"><span data-stu-id="7a146-114">Retrieves the current error code.</span></span>                                                               |
| [<span data-ttu-id="7a146-115">errorcontext</span><span class="sxs-lookup"><span data-stu-id="7a146-115">errorContext</span></span>](erroritem-errorcontext.md)         | <span data-ttu-id="7a146-116">Ruft einen Wert ab, der den Kontext des Fehlers angibt.</span><span class="sxs-lookup"><span data-stu-id="7a146-116">Retrieves a value indicating the context of the error.</span></span>                                          |
| [<span data-ttu-id="7a146-117">errorDescription</span><span class="sxs-lookup"><span data-stu-id="7a146-117">errorDescription</span></span>](erroritem-errordescription.md) | <span data-ttu-id="7a146-118">Ruft eine Beschreibung des Fehlers ab.</span><span class="sxs-lookup"><span data-stu-id="7a146-118">Retrieves a description of the error.</span></span>                                                           |
| <span data-ttu-id="7a146-119">**Lösung**</span><span class="sxs-lookup"><span data-stu-id="7a146-119">**remedy**</span></span>                                         | <span data-ttu-id="7a146-120">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="7a146-120">Reserved for future use.</span></span>                                                                        |



 

<span data-ttu-id="7a146-121">Der Zugriff auf das **ErrorItem** -Objekt erfolgt über die folgenden Methoden.</span><span class="sxs-lookup"><span data-stu-id="7a146-121">The **ErrorItem** object is accessed through the following methods.</span></span>



| <span data-ttu-id="7a146-122">Object</span><span class="sxs-lookup"><span data-stu-id="7a146-122">Object</span></span>                    | <span data-ttu-id="7a146-123">Methode</span><span class="sxs-lookup"><span data-stu-id="7a146-123">Method</span></span>                   |
|---------------------------|--------------------------|
| [<span data-ttu-id="7a146-124">Fehler</span><span class="sxs-lookup"><span data-stu-id="7a146-124">Error</span></span>](error-object.md) | [<span data-ttu-id="7a146-125">item</span><span class="sxs-lookup"><span data-stu-id="7a146-125">item</span></span>](error-item.md)   |
| [<span data-ttu-id="7a146-126">Medien</span><span class="sxs-lookup"><span data-stu-id="7a146-126">Media</span></span>](media-object.md) | [<span data-ttu-id="7a146-127">error</span><span class="sxs-lookup"><span data-stu-id="7a146-127">error</span></span>](media-error.md) |



 

<span data-ttu-id="7a146-128">Dient zur Veranschaulichung des *Players*. *Fehler*. *Item*(*Index*) wird in den Abschnitten der Verweis Syntax verwendet.</span><span class="sxs-lookup"><span data-stu-id="7a146-128">For purposes of illustration, *player*.*error*.*item*(*index*) is used in the reference syntax sections.</span></span>

## <a name="see-also"></a><span data-ttu-id="7a146-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a146-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a146-130">**Objektmodell Referenz für die Skripterstellung**</span><span class="sxs-lookup"><span data-stu-id="7a146-130">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




