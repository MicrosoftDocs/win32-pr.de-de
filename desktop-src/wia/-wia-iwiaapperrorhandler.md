---
description: Mithilfe der iwiaapperrorhandler-Schnittstelle können Anwendungen Fehler Fenster (während der Datenübertragungen) anzeigen, von denen der Benutzer auswählen kann, ob die Übertragung fortgesetzt, abgebrochen oder abgebrochen werden soll.
ms.assetid: ac2597e6-2857-4694-bea7-1ea65d63b365
title: Iwiaapperrorhandler-Schnittstelle (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaAppErrorHandler
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 6ccac7b689055bfaab926a8db46b4632606811d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106373056"
---
# <a name="iwiaapperrorhandler-interface"></a><span data-ttu-id="17a67-103">Iwiaapperrorhandler-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="17a67-103">IWiaAppErrorHandler interface</span></span>

<span data-ttu-id="17a67-104">Mithilfe der **iwiaapperrorhandler** -Schnittstelle können Anwendungen Fehler Fenster (während der Datenübertragungen) anzeigen, von denen der Benutzer auswählen kann, ob die Übertragung fortgesetzt, abgebrochen oder abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="17a67-104">The **IWiaAppErrorHandler** interface enables applications to display error windows (during data transfers) from which the user can choose whether to continue, cancel, or abort the transfer.</span></span>

## <a name="members"></a><span data-ttu-id="17a67-105">Member</span><span class="sxs-lookup"><span data-stu-id="17a67-105">Members</span></span>

<span data-ttu-id="17a67-106">Die **iwiaapperrorhandler** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="17a67-106">The **IWiaAppErrorHandler** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="17a67-107">**Iwiaapperrorhandler** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="17a67-107">**IWiaAppErrorHandler** also has these types of members:</span></span>

-   [<span data-ttu-id="17a67-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="17a67-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="17a67-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="17a67-109">Methods</span></span>

<span data-ttu-id="17a67-110">Die **iwiaapperrorhandler** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="17a67-110">The **IWiaAppErrorHandler** interface has these methods.</span></span>



| <span data-ttu-id="17a67-111">Methode</span><span class="sxs-lookup"><span data-stu-id="17a67-111">Method</span></span>                                                        | <span data-ttu-id="17a67-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="17a67-112">Description</span></span>                                                                                                                                             |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="17a67-113">**GetWindow**</span><span class="sxs-lookup"><span data-stu-id="17a67-113">**GetWindow**</span></span>](-wia-iwiaapperrorhandler-getwindow.md)       | <span data-ttu-id="17a67-114">Ruft ein Handle für das Dialogfeld ab, das Fehlermeldungen anzeigt und eine oder mehrere Schaltflächen zum Fortfahren, Abbrechen oder Abbrechen der Anwendung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="17a67-114">Gets a handle to the dialog box that displays error messages and provides one or more buttons to continue, cancel, or abort the application.</span></span><br/> |
| [<span data-ttu-id="17a67-115">**Report Status**</span><span class="sxs-lookup"><span data-stu-id="17a67-115">**ReportStatus**</span></span>](-wia-iwiaapperrorhandler-reportstatus.md) | <span data-ttu-id="17a67-116">Verarbeitet den Gerätestatus und Fehlermeldungen während der Bild Datenübertragungen und zeigt dem Benutzer die Nachrichten an.</span><span class="sxs-lookup"><span data-stu-id="17a67-116">Handles device status and error messages during image data transfers and displays the messages to the user.</span></span><br/>                                  |



 

## <a name="remarks"></a><span data-ttu-id="17a67-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="17a67-117">Remarks</span></span>

<span data-ttu-id="17a67-118">Die Fehlerbehandlung oder das Rückruf Objekt, das diese Schnittstelle implementiert, wird an [**iwiatransfer::D ownload**](-wia-iwiatransfer-download.md) und [**iwiatransfer:: Upload**](-wia-iwiatransfer-upload.md)übergeben.</span><span class="sxs-lookup"><span data-stu-id="17a67-118">The error handling, or callback, object that implements this interface is passed into [**IWiaTransfer::Download**](-wia-iwiatransfer-download.md) and [**IWiaTransfer::Upload**](-wia-iwiatransfer-upload.md).</span></span>

<span data-ttu-id="17a67-119">Diese Schnittstelle ist nicht für die Behandlung von Fehlern konzipiert, die außerhalb der Bild Datenübertragungen aufgetreten sind, z. b. Fehler beim Aufrufen oder Festlegen von Geräteeigenschaften oder nicht zurückgegebene Rückrufe an einen Treiber.</span><span class="sxs-lookup"><span data-stu-id="17a67-119">This interface is not designed to handle errors encountered outside of image data transfers, for example, errors in getting or setting device properties or unreturned callbacks into a driver.</span></span>

<span data-ttu-id="17a67-120">Ein Treiber Fehlerhandler sollte [**iwiaerrorhandler**](-wia-iwiaerrorhandler.md)anstelle von **iwiaapperrorhandler** implementieren.</span><span class="sxs-lookup"><span data-stu-id="17a67-120">A driver error handler should implement [**IWiaErrorHandler**](-wia-iwiaerrorhandler.md), instead of **IWiaAppErrorHandler**.</span></span>

<span data-ttu-id="17a67-121">Das Objekt, das diese Schnittstelle implementiert, sollte auch [**iwiatransfercallback**](-wia-iwiatransfercallback.md)implementieren.</span><span class="sxs-lookup"><span data-stu-id="17a67-121">The object that implements this interface should also implement [**IWiaTransferCallback**](-wia-iwiatransfercallback.md).</span></span>

<span data-ttu-id="17a67-122">Wenn Sie möchten, dass ein Treiber Fehlerhandler und der Standardfehler Handler Fehler Meldungs Fenster anzeigen, aber keinen kompletten Fehlerhandler für die Anwendung erstellen möchten, implementieren Sie diese Schnittstelle, und implementieren Sie außerdem die [**iwiaapperrorhandler:: Report Status**](-wia-iwiaapperrorhandler-reportstatus.md) -Methode, um einen \_ \_ nicht behandelten WIA-Status zurückzugeben \_ .</span><span class="sxs-lookup"><span data-stu-id="17a67-122">If you want a driver error handler and default error handler to display error message windows, but you do not want to create a complete error handler for the application, implement this interface and also implement the [**IWiaAppErrorHandler::ReportStatus**](-wia-iwiaapperrorhandler-reportstatus.md) method to return WIA\_STATUS\_NOT\_HANDLED.</span></span>

## <a name="requirements"></a><span data-ttu-id="17a67-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="17a67-123">Requirements</span></span>



| <span data-ttu-id="17a67-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="17a67-124">Requirement</span></span> | <span data-ttu-id="17a67-125">Wert</span><span class="sxs-lookup"><span data-stu-id="17a67-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="17a67-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="17a67-126">Minimum supported client</span></span><br/> | <span data-ttu-id="17a67-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="17a67-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="17a67-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="17a67-128">Minimum supported server</span></span><br/> | <span data-ttu-id="17a67-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="17a67-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="17a67-130">Header</span><span class="sxs-lookup"><span data-stu-id="17a67-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="17a67-131"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="17a67-131"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="17a67-132">IDL</span><span class="sxs-lookup"><span data-stu-id="17a67-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="17a67-133"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="17a67-133"><dt>Wia.idl</dt></span></span> </dl> |



 

 
