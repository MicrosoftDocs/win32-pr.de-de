---
description: Ruft ein Handle für das Dialogfeld ab, das Fehlermeldungen anzeigt und eine oder mehrere Schaltflächen zum Fortfahren, Abbrechen oder Abbrechen der Anwendung bereitstellt.
ms.assetid: 54deac2e-a395-45dc-b9f9-ecf8140fd9d7
title: 'Iwiaapperrorhandler:: GetWindow-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaAppErrorHandler.GetWindow
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 89a3b2bf87d99c767ab3bea46a27c8a53fab7825
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349428"
---
# <a name="iwiaapperrorhandlergetwindow-method"></a><span data-ttu-id="acae3-103">Iwiaapperrorhandler:: GetWindow-Methode</span><span class="sxs-lookup"><span data-stu-id="acae3-103">IWiaAppErrorHandler::GetWindow method</span></span>

<span data-ttu-id="acae3-104">Ruft ein Handle für das Dialogfeld ab, das Fehlermeldungen anzeigt und eine oder mehrere Schaltflächen zum Fortfahren, Abbrechen oder Abbrechen der Anwendung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="acae3-104">Gets a handle to the dialog box that displays error messages and provides one or more buttons to continue, cancel, or abort the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="acae3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="acae3-105">Syntax</span></span>


```C++
HRESULT GetWindow(
  [out] HWND *phwnd
);
```



## <a name="parameters"></a><span data-ttu-id="acae3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="acae3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acae3-107">*phwnd* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="acae3-107">*phwnd* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="acae3-108">Geben Sie Folgendes ein: \**HWND \** _</span><span class="sxs-lookup"><span data-stu-id="acae3-108">Type: \**HWND\** _</span></span>

<span data-ttu-id="acae3-109">HWND, das vom Anwendungsfehler Handler, dem Treiber Fehlerhandler und dem Standardfehler Handler für Geräte Meldungs Dialogfelder (Fehler und Information) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="acae3-109">HWND used by the application error handler, the driver error handler, and the default error handler for device message dialog boxes (both error and informational).</span></span> <span data-ttu-id="acae3-110">Der Ausgabewert ist möglicherweise _ \* NULL \* \*.</span><span class="sxs-lookup"><span data-stu-id="acae3-110">The output value may be _\*NULL\*\*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acae3-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="acae3-111">Return value</span></span>

<span data-ttu-id="acae3-112">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="acae3-112">Type: **HRESULT**</span></span>

<span data-ttu-id="acae3-113">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="acae3-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="acae3-114">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="acae3-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="acae3-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="acae3-115">Remarks</span></span>

<span data-ttu-id="acae3-116">*phwnd* zeigt auf das Fenster, das vom Windows-Abbild Erfassungs Proxy (WIA) 2,0 an [**Report Status**](-wia-iwiaerrorhandler-reportstatus.md) weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="acae3-116">*phwnd* points to the window passed into [**ReportStatus**](-wia-iwiaerrorhandler-reportstatus.md) by the Windows Image Acquisition (WIA) 2.0 Proxy.</span></span> <span data-ttu-id="acae3-117">Dieses Fenster muss für die Dauer der Datenübertragung gültig bleiben.</span><span class="sxs-lookup"><span data-stu-id="acae3-117">This window must remain valid for the duration of the data transfer.</span></span>

## <a name="requirements"></a><span data-ttu-id="acae3-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="acae3-118">Requirements</span></span>



| <span data-ttu-id="acae3-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="acae3-119">Requirement</span></span> | <span data-ttu-id="acae3-120">Wert</span><span class="sxs-lookup"><span data-stu-id="acae3-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="acae3-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="acae3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="acae3-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="acae3-122">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="acae3-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="acae3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="acae3-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="acae3-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="acae3-125">Header</span><span class="sxs-lookup"><span data-stu-id="acae3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="acae3-126"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="acae3-126"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="acae3-127">IDL</span><span class="sxs-lookup"><span data-stu-id="acae3-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="acae3-128"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="acae3-128"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="acae3-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="acae3-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="acae3-130"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="acae3-130"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 




