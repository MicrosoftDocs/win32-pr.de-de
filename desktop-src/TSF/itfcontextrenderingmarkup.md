---
title: ITF contextrenderingmarkup-Schnittstelle
description: Die ITF contextrenderingmarkup-Schnittstelle wird von TSF Manager implementiert und von Anwendungen verwendet. Diese Schnittstelle kann mit iqueryinterface aus dem ITfContext-Objekt abgerufen werden. Diese Schnittstelle unterstützt die Anwendung beim Auflisten von Renderinginformationen.
ms.assetid: 733d2db2-f9e9-4b78-af13-adc03825bf2b
keywords:
- ITF contextrenderingmarkup Interface Text Services-Framework
- ITF contextrenderingmarkup Interface Text Services-Framework, beschrieben
topic_type:
- apiref
api_name:
- ITfContextRenderingMarkup
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1b71e977665a4b3a6e817ef782ee558064e0986a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858341"
---
# <a name="itfcontextrenderingmarkup-interface"></a><span data-ttu-id="3b564-107">ITF contextrenderingmarkup-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="3b564-107">ITfContextRenderingMarkup interface</span></span>

<span data-ttu-id="3b564-108">Die **ITF contextrenderingmarkup** -Schnittstelle wird von TSF Manager implementiert und von Anwendungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="3b564-108">The **ITfContextRenderingMarkup** interface is implemented by TSF manager and used by applications.</span></span> <span data-ttu-id="3b564-109">Diese Schnittstelle kann mit iqueryinterface aus dem [ITfContext](/windows/desktop/api/Msctf/nn-msctf-itfcontext) -Objekt abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="3b564-109">This interface can be retrieved using IQueryInterface from [ITfContext](/windows/desktop/api/Msctf/nn-msctf-itfcontext) object.</span></span> <span data-ttu-id="3b564-110">Diese Schnittstelle unterstützt die Anwendung beim Auflisten von Renderinginformationen.</span><span class="sxs-lookup"><span data-stu-id="3b564-110">This interface helps the application enumerate rendering information.</span></span>



| <span data-ttu-id="3b564-111">ITF contextrenderingmarkup-Methoden</span><span class="sxs-lookup"><span data-stu-id="3b564-111">ITfContextRenderingMarkup methods</span></span>                                                | <span data-ttu-id="3b564-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3b564-112">Description</span></span>                                                           |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="3b564-113">GetRenderingMarkup</span><span class="sxs-lookup"><span data-stu-id="3b564-113">GetRenderingMarkup</span></span>](itfcontextrenderingmarkup-getrenderingmarkup.md)           | <span data-ttu-id="3b564-114">Ruft einen Enumerator der rendermarkups für den angegebenen Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="3b564-114">Retrieves an enumerator of the rendering markups for the given range.</span></span> |
| [<span data-ttu-id="3b564-115">Findnextrenderingmarkup</span><span class="sxs-lookup"><span data-stu-id="3b564-115">FindNextRenderingMarkup</span></span>](itfcontextrenderingmarkup-findnextrenderingmarkup.md) | <span data-ttu-id="3b564-116">Diese Funktion ist nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="3b564-116">This function is not implemented.</span></span> <span data-ttu-id="3b564-117">Er gibt immer E \_ notimpl zurück.</span><span class="sxs-lookup"><span data-stu-id="3b564-117">It always returns E\_NOTIMPL.</span></span>       |



 

## <a name="members"></a><span data-ttu-id="3b564-118">Member</span><span class="sxs-lookup"><span data-stu-id="3b564-118">Members</span></span>

<span data-ttu-id="3b564-119">Die **itfcontextrenderingmarkup** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.</span><span class="sxs-lookup"><span data-stu-id="3b564-119">The **ITfContextRenderingMarkup** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b564-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3b564-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3b564-121">Diese Schnittstelle befindet sich derzeit nicht in den öffentlichen Header Dateien.</span><span class="sxs-lookup"><span data-stu-id="3b564-121">This interface is not currently in the public header files.</span></span> <span data-ttu-id="3b564-122">Um diese API verwenden zu können, müssen Sie den [Prototyp](prototypes.md)als Mittelpunkt kompilieren.</span><span class="sxs-lookup"><span data-stu-id="3b564-122">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 

 