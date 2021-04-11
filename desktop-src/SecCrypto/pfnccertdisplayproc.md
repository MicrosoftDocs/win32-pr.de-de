---
description: Eine benutzerdefinierte Rückruffunktion, die es dem Aufrufer der Funktion cryptuidlgselectcertificate ermöglicht, die Anzeige von Zertifikaten zu verarbeiten, die der Benutzer zum anzeigen auswählt.
ms.assetid: fdb9e9e0-02f1-42e0-9a11-204d916a1a88
title: Pfnccertdisplayproc-Rückruffunktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PFNCCERTDISPLAYPROC
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 7371e983b339ff8bfa9edb1b7fb795ab64596a98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042319"
---
# <a name="pfnccertdisplayproc-callback-function"></a><span data-ttu-id="a2742-103">Pfnccertdisplayproc-Rückruffunktion</span><span class="sxs-lookup"><span data-stu-id="a2742-103">PFNCCERTDISPLAYPROC callback function</span></span>

<span data-ttu-id="a2742-104">Die **pfnccertdisplayproc** -Funktion ist eine benutzerdefinierte Rückruffunktion, die es dem Aufrufer der Funktion [**cryptuidlgselectcertificate**](cryptuidlgselectcertificate.md) ermöglicht, die Anzeige von Zertifikaten zu verarbeiten, die der Benutzer zum anzeigen auswählt.</span><span class="sxs-lookup"><span data-stu-id="a2742-104">The **PFNCCERTDISPLAYPROC** function is a user-defined callback function that allows the caller of the [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) function to handle the display of certificates that the user selects to view.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2742-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2742-105">Syntax</span></span>


```C++
BOOL WINAPI * PFNCCERTDISPLAYPROC(
  _In_ PCCERT_CONTEXT pCertContext,
  _In_ HWND           hWndSelCertDlg,
  _In_ void           *pvCallbackData
);
```



## <a name="parameters"></a><span data-ttu-id="a2742-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2742-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2742-107">*pcertcontext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a2742-107">*pCertContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2742-108">Ein Zeiger auf eine [**CERT- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) Struktur, die das anzuzeigende Zertifikat darstellt.</span><span class="sxs-lookup"><span data-stu-id="a2742-108">A pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) structure that represents the certificate to display.</span></span>

</dd> <dt>

<span data-ttu-id="a2742-109">*hwndselcertdlg* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a2742-109">*hWndSelCertDlg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2742-110">Ein Handle für das Dialogfeld, in dem das Zertifikat zum Anzeigen ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="a2742-110">A handle to the dialog box from which the certificate was selected for viewing.</span></span>

</dd> <dt>

<span data-ttu-id="a2742-111">*pvcallbackdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a2742-111">*pvCallbackData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2742-112">Zusätzliche Daten, die von der Rückruffunktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a2742-112">Additional data used by the callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2742-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a2742-113">Return value</span></span>

<span data-ttu-id="a2742-114">Diese Funktion gibt **true** zurück, um anzugeben, dass Sie die Anzeige des Zertifikats behandelt und dass das Dialogfeld das Zertifikat nicht anzeigen soll.</span><span class="sxs-lookup"><span data-stu-id="a2742-114">This function returns **TRUE** to indicate that it handles display of the certificate and that the dialog box should not display the certificate.</span></span> <span data-ttu-id="a2742-115">Wenn diese Funktion **false** zurückgibt, wird das Zertifikat im Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a2742-115">If this function returns **FALSE**, the dialog box displays the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2742-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a2742-116">Requirements</span></span>



| <span data-ttu-id="a2742-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a2742-117">Requirement</span></span> | <span data-ttu-id="a2742-118">Wert</span><span class="sxs-lookup"><span data-stu-id="a2742-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a2742-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a2742-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a2742-120">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a2742-120">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="a2742-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a2742-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a2742-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a2742-122">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 




