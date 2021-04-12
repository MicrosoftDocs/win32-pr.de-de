---
description: Die iwiatransfercallback-Schnittstelle empfängt Rückrufe während einer Datenübertragung.
ms.assetid: 8fcaccf5-4d7b-4984-97ec-ec8c838a8360
title: Iwiatransfercallback-Schnittstelle (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransferCallback
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 918482ebcb24f2638a006ab1bbc452ea28ff61e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129409"
---
# <a name="iwiatransfercallback-interface"></a><span data-ttu-id="14f1b-103">Iwiatransfercallback-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="14f1b-103">IWiaTransferCallback interface</span></span>

<span data-ttu-id="14f1b-104">Die **iwiatransfercallback** -Schnittstelle empfängt Rückrufe während einer Datenübertragung.</span><span class="sxs-lookup"><span data-stu-id="14f1b-104">The **IWiaTransferCallback** interface receives callbacks during a data transfer.</span></span>

## <a name="members"></a><span data-ttu-id="14f1b-105">Member</span><span class="sxs-lookup"><span data-stu-id="14f1b-105">Members</span></span>

<span data-ttu-id="14f1b-106">Die **iwiatransfercallback** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="14f1b-106">The **IWiaTransferCallback** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="14f1b-107">**Iwiatransfercallback** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="14f1b-107">**IWiaTransferCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="14f1b-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="14f1b-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="14f1b-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="14f1b-109">Methods</span></span>

<span data-ttu-id="14f1b-110">Die **iwiatransfercallback** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="14f1b-110">The **IWiaTransferCallback** interface has these methods.</span></span>



| <span data-ttu-id="14f1b-111">Methode</span><span class="sxs-lookup"><span data-stu-id="14f1b-111">Method</span></span>                                                                 | <span data-ttu-id="14f1b-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="14f1b-112">Description</span></span>                                                              |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [<span data-ttu-id="14f1b-113">**Getnextstream**</span><span class="sxs-lookup"><span data-stu-id="14f1b-113">**GetNextStream**</span></span>](-wia-iwiatransfercallback-getnextstream.md)       | <span data-ttu-id="14f1b-114">Ruft einen neuen Stream für das angegebene Element ab.</span><span class="sxs-lookup"><span data-stu-id="14f1b-114">Gets a new stream for the specified item.</span></span> <br/>                    |
| [<span data-ttu-id="14f1b-115">**Transfercallback**</span><span class="sxs-lookup"><span data-stu-id="14f1b-115">**TransferCallback**</span></span>](-wia-iwiatransfercallback-transfercallback.md) | <span data-ttu-id="14f1b-116">Gibt den Fortschritt und andere Benachrichtigungen während einer Übertragung an.</span><span class="sxs-lookup"><span data-stu-id="14f1b-116">Provides progress and other notifications during a transfer.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="14f1b-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="14f1b-117">Remarks</span></span>

<span data-ttu-id="14f1b-118">Bild Verarbeitungs Filter-Entwickler sollten diese Schnittstelle und die [**iwiaimagefilter**](-wia-iwiaimagefilter.md) -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="14f1b-118">Image processing filter developers should implement this interface and the [**IWiaImageFilter**](-wia-iwiaimagefilter.md) interface.</span></span>

<span data-ttu-id="14f1b-119">Die **iwiatransfercallback** -Schnittstelle erbt wie alle Component Object Model-Schnittstellen (com) die [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstellen Methoden.</span><span class="sxs-lookup"><span data-stu-id="14f1b-119">The **IWiaTransferCallback** interface, like all Component Object Model (COM) interfaces, inherits the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface methods.</span></span>



| <span data-ttu-id="14f1b-120">IUnknown-Methoden</span><span class="sxs-lookup"><span data-stu-id="14f1b-120">IUnknown Methods</span></span>                                        | <span data-ttu-id="14f1b-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="14f1b-121">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="14f1b-122">[IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="14f1b-122">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="14f1b-123">Gibt Zeiger auf unterstützte Schnittstellen zurück.</span><span class="sxs-lookup"><span data-stu-id="14f1b-123">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="14f1b-124">IUnknown:: adressf</span><span class="sxs-lookup"><span data-stu-id="14f1b-124">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="14f1b-125">Inkrementiert Verweiszähler.</span><span class="sxs-lookup"><span data-stu-id="14f1b-125">Increments reference count.</span></span>               |
| [<span data-ttu-id="14f1b-126">IUnknown:: Release</span><span class="sxs-lookup"><span data-stu-id="14f1b-126">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="14f1b-127">Dekrementiert Verweiszähler.</span><span class="sxs-lookup"><span data-stu-id="14f1b-127">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="14f1b-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="14f1b-128">Requirements</span></span>



| <span data-ttu-id="14f1b-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="14f1b-129">Requirement</span></span> | <span data-ttu-id="14f1b-130">Wert</span><span class="sxs-lookup"><span data-stu-id="14f1b-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="14f1b-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="14f1b-131">Minimum supported client</span></span><br/> | <span data-ttu-id="14f1b-132">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="14f1b-132">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="14f1b-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="14f1b-133">Minimum supported server</span></span><br/> | <span data-ttu-id="14f1b-134">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="14f1b-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="14f1b-135">Header</span><span class="sxs-lookup"><span data-stu-id="14f1b-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="14f1b-136"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="14f1b-136"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="14f1b-137">IDL</span><span class="sxs-lookup"><span data-stu-id="14f1b-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="14f1b-138"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="14f1b-138"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="14f1b-139">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="14f1b-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="14f1b-140"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="14f1b-140"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
