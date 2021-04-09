---
description: Die iwiaerrorhandler-Schnittstelle stellt Methoden bereit, um Fehler zu behandeln, die auftreten können, wenn eine Anwendung Bilddaten anfordert, ob für die Vorschau oder die endgültige Bits.
ms.assetid: 33d8ccc5-6856-4a54-b1f0-d015933d63ab
title: Iwiaerrorhandler-Schnittstelle (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaErrorHandler
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 7b3ea9f5556f1f919336e4abb4085f9e0c32d81d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130012"
---
# <a name="iwiaerrorhandler-interface"></a><span data-ttu-id="214f7-103">Iwiaerrorhandler-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="214f7-103">IWiaErrorHandler interface</span></span>

<span data-ttu-id="214f7-104">Die **iwiaerrorhandler** -Schnittstelle stellt Methoden bereit, um Fehler zu behandeln, die auftreten können, wenn eine Anwendung Bilddaten anfordert, ob für die Vorschau oder die endgültige Bits.</span><span class="sxs-lookup"><span data-stu-id="214f7-104">The **IWiaErrorHandler** interface provides methods to handle errors that may occur when an application requests image data, whether for preview or final bits.</span></span>

## <a name="members"></a><span data-ttu-id="214f7-105">Member</span><span class="sxs-lookup"><span data-stu-id="214f7-105">Members</span></span>

<span data-ttu-id="214f7-106">Die **iwiaerrorhandler** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="214f7-106">The **IWiaErrorHandler** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="214f7-107">**Iwiaerrorhandler** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="214f7-107">**IWiaErrorHandler** also has these types of members:</span></span>

-   [<span data-ttu-id="214f7-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="214f7-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="214f7-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="214f7-109">Methods</span></span>

<span data-ttu-id="214f7-110">Die **iwiaerrorhandler** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="214f7-110">The **IWiaErrorHandler** interface has these methods.</span></span>



| <span data-ttu-id="214f7-111">Methode</span><span class="sxs-lookup"><span data-stu-id="214f7-111">Method</span></span>                                                                     | <span data-ttu-id="214f7-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="214f7-112">Description</span></span>                                                                                             |
|:---------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="214f7-113">**GetStatus Description**</span><span class="sxs-lookup"><span data-stu-id="214f7-113">**GetStatusDescription**</span></span>](-wia-iwiaerrorhandler-getstatusdescription.md) | <span data-ttu-id="214f7-114">Gibt eine Zeichenfolge zurück, die den Statuscode beschreibt.</span><span class="sxs-lookup"><span data-stu-id="214f7-114">Returns a string that describes the status code.</span></span><br/>                                             |
| [<span data-ttu-id="214f7-115">**Report Status**</span><span class="sxs-lookup"><span data-stu-id="214f7-115">**ReportStatus**</span></span>](-wia-iwiaerrorhandler-reportstatus.md)                 | <span data-ttu-id="214f7-116">Verarbeitet Status-und Fehlermeldungen während der Bild Datenübertragungen und zeigt Sie dem Benutzer an.</span><span class="sxs-lookup"><span data-stu-id="214f7-116">Handles status and error messages during image data transfers and displays them to the user.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="214f7-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="214f7-117">Remarks</span></span>

<span data-ttu-id="214f7-118">Das Anwendungs Rückruf Objekt kann **iwiaerrorhandler** implementieren.</span><span class="sxs-lookup"><span data-stu-id="214f7-118">The application callback object can implement **IWiaErrorHandler**.</span></span>

<span data-ttu-id="214f7-119">Diese Schnittstelle ist nicht für die Behandlung von Fehlern konzipiert, die außerhalb der Bild Datenübertragungen aufgetreten sind, z. b. Fehler beim Aufrufen oder Festlegen von Geräteeigenschaften oder nicht zurückgegebene Rückrufe an einen Treiber.</span><span class="sxs-lookup"><span data-stu-id="214f7-119">This interface is not designed to handle errors encountered outside of image data transfers, for example, errors in getting or setting device properties or unreturned callbacks into a driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="214f7-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="214f7-120">Requirements</span></span>



| <span data-ttu-id="214f7-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="214f7-121">Requirement</span></span> | <span data-ttu-id="214f7-122">Wert</span><span class="sxs-lookup"><span data-stu-id="214f7-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="214f7-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="214f7-123">Minimum supported client</span></span><br/> | <span data-ttu-id="214f7-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="214f7-124">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="214f7-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="214f7-125">Minimum supported server</span></span><br/> | <span data-ttu-id="214f7-126">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="214f7-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="214f7-127">Header</span><span class="sxs-lookup"><span data-stu-id="214f7-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="214f7-128"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="214f7-128"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="214f7-129">IDL</span><span class="sxs-lookup"><span data-stu-id="214f7-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="214f7-130"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="214f7-130"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="214f7-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="214f7-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="214f7-132"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="214f7-132"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
