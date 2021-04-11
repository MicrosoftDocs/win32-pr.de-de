---
description: Die iwiatransfer-Schnittstelle stellt Datenstrom basierte Übertragung von Daten bereit.
ms.assetid: 7bc6d3b8-9bf0-4b77-aa2b-b7c64c5730c0
title: Iwiatransfer-Schnittstelle (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 623cc21591289f4c1fff33cabe1d504b3682708c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214651"
---
# <a name="iwiatransfer-interface"></a><span data-ttu-id="64302-103">Iwiatransfer-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="64302-103">IWiaTransfer interface</span></span>

<span data-ttu-id="64302-104">Die **iwiatransfer** -Schnittstelle stellt Datenstrom basierte Übertragung von Daten bereit.</span><span class="sxs-lookup"><span data-stu-id="64302-104">The **IWiaTransfer** interface provides stream-based transfer of data.</span></span>

## <a name="members"></a><span data-ttu-id="64302-105">Member</span><span class="sxs-lookup"><span data-stu-id="64302-105">Members</span></span>

<span data-ttu-id="64302-106">Die **iwiatransfer** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="64302-106">The **IWiaTransfer** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="64302-107">**Iwiatransfer** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="64302-107">**IWiaTransfer** also has these types of members:</span></span>

-   [<span data-ttu-id="64302-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="64302-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="64302-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="64302-109">Methods</span></span>

<span data-ttu-id="64302-110">Die **iwiatransfer** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="64302-110">The **IWiaTransfer** interface has these methods.</span></span>



| <span data-ttu-id="64302-111">Methode</span><span class="sxs-lookup"><span data-stu-id="64302-111">Method</span></span>                                                                 | <span data-ttu-id="64302-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="64302-112">Description</span></span>                                                                                 |
|:-----------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="64302-113">**Abbrechen**</span><span class="sxs-lookup"><span data-stu-id="64302-113">**Cancel**</span></span>](-wia-iwiatransfer-cancel.md)                             | <span data-ttu-id="64302-114">Bricht den aktuellen Übertragungsvorgang ab.</span><span class="sxs-lookup"><span data-stu-id="64302-114">Cancels the current transfer operation.</span></span> <br/>                                         |
| [<span data-ttu-id="64302-115">**Herunterladen**</span><span class="sxs-lookup"><span data-stu-id="64302-115">**Download**</span></span>](-wia-iwiatransfer-download.md)                         | <span data-ttu-id="64302-116">Initiiert einen Daten Download für den Aufrufer.</span><span class="sxs-lookup"><span data-stu-id="64302-116">Initiates a data download to the caller.</span></span> <br/>                                        |
| [<span data-ttu-id="64302-117">**Enumwia- \_ Format \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="64302-117">**EnumWIA\_FORMAT\_INFO**</span></span>](-wia-iwiatransfer-enumwia-format-info.md) | <span data-ttu-id="64302-118">Erstellt einen Enumerator für die Übertragungs Formate, die das WIA 2,0-Gerät unterstützt.</span><span class="sxs-lookup"><span data-stu-id="64302-118">Creates an enumerator for the transfer formats that the WIA 2.0 device supports.</span></span><br/> |
| [<span data-ttu-id="64302-119">**Upload**</span><span class="sxs-lookup"><span data-stu-id="64302-119">**Upload**</span></span>](-wia-iwiatransfer-upload.md)                             | <span data-ttu-id="64302-120">Initiiert einen Daten Upload eines einzelnen Elements vom Aufrufer.</span><span class="sxs-lookup"><span data-stu-id="64302-120">Initiates a data upload of a single item from the caller.</span></span> <br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="64302-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="64302-121">Remarks</span></span>

<span data-ttu-id="64302-122">Die **iwiatransfer** -Schnittstelle erbt wie alle Component Object Model-Schnittstellen (com) die [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstellen Methoden.</span><span class="sxs-lookup"><span data-stu-id="64302-122">The **IWiaTransfer** interface, like all Component Object Model (COM) interfaces, inherits the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface methods.</span></span>



| <span data-ttu-id="64302-123">IUnknown-Methoden</span><span class="sxs-lookup"><span data-stu-id="64302-123">IUnknown Methods</span></span>                                        | <span data-ttu-id="64302-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="64302-124">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="64302-125">[IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="64302-125">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="64302-126">Gibt Zeiger auf unterstützte Schnittstellen zurück.</span><span class="sxs-lookup"><span data-stu-id="64302-126">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="64302-127">IUnknown:: adressf</span><span class="sxs-lookup"><span data-stu-id="64302-127">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="64302-128">Inkrementiert Verweiszähler.</span><span class="sxs-lookup"><span data-stu-id="64302-128">Increments reference count.</span></span>               |
| [<span data-ttu-id="64302-129">IUnknown:: Release</span><span class="sxs-lookup"><span data-stu-id="64302-129">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="64302-130">Dekrementiert Verweiszähler.</span><span class="sxs-lookup"><span data-stu-id="64302-130">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="64302-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="64302-131">Requirements</span></span>



| <span data-ttu-id="64302-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="64302-132">Requirement</span></span> | <span data-ttu-id="64302-133">Wert</span><span class="sxs-lookup"><span data-stu-id="64302-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="64302-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="64302-134">Minimum supported client</span></span><br/> | <span data-ttu-id="64302-135">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="64302-135">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="64302-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="64302-136">Minimum supported server</span></span><br/> | <span data-ttu-id="64302-137">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="64302-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="64302-138">Header</span><span class="sxs-lookup"><span data-stu-id="64302-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="64302-139"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="64302-139"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="64302-140">IDL</span><span class="sxs-lookup"><span data-stu-id="64302-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="64302-141"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="64302-141"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="64302-142">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="64302-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="64302-143"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="64302-143"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
