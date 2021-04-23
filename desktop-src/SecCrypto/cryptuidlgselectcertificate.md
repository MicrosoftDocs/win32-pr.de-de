---
description: Zeigt ein Dialogfeld an, in dem ein Benutzer ein Zertifikat auswählen kann.
ms.assetid: 242c19a7-179b-4fc0-a050-a1b598566a6b
title: CryptUIDlgSelectCertificate-Funktion
ms.topic: reference
ms.date: 05/29/2020
ms.openlocfilehash: 8f015796671990491407d91cbd51761816c5434b
ms.sourcegitcommit: 435ea8f5bf06808ffa7dce39afb0ee6de842ba2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2021
ms.locfileid: "107925691"
---
# <a name="cryptuidlgselectcertificate-function"></a><span data-ttu-id="d9e31-103">CryptUIDlgSelectCertificate-Funktion</span><span class="sxs-lookup"><span data-stu-id="d9e31-103">CryptUIDlgSelectCertificate function</span></span>

<span data-ttu-id="d9e31-104">Die **CryptUIDlgSelectCertificate-Funktion** zeigt ein Dialogfeld an, in dem ein Benutzer ein Zertifikat auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="d9e31-104">The **CryptUIDlgSelectCertificate** function displays a dialog box that allows a user to select a certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9e31-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9e31-105">Syntax</span></span>


```C++
PCCERT_CONTEXT WINAPI CryptUIDlgSelectCertificate(
  _In_  PCCRYPTUI_SELECTCERTIFICATE_STRUCT pcsc
);
```



## <a name="parameters"></a><span data-ttu-id="d9e31-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9e31-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9e31-107">*pcsc* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="d9e31-107">*pcsc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9e31-108">Ein Zeiger auf eine [**CRYPTUI \_ SELECTCERTIFICATE-STRUKTUR, \_**](cryptui-selectcertificate-struct.md) die Informationen über das anzuzeigende Dialogfeld enthält.</span><span class="sxs-lookup"><span data-stu-id="d9e31-108">A pointer to a [**CRYPTUI\_SELECTCERTIFICATE\_STRUCT**](cryptui-selectcertificate-struct.md) structure that contains information about the dialog box to display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9e31-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d9e31-109">Return value</span></span>

<span data-ttu-id="d9e31-110">Ein Zeiger auf eine [**CERT \_ CONTEXT-Struktur,**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) die das vom Benutzer ausgewählte Zertifikat darstellt.</span><span class="sxs-lookup"><span data-stu-id="d9e31-110">A pointer to a [**CERT\_CONTEXT**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) structure that represents the certificate selected by the user.</span></span> <span data-ttu-id="d9e31-111">Wenn Sie mit der Verwendung dieses Zertifikats fertig sind, müssen Sie diesen Zeiger an die [**CertFreeCertificateContext-Funktion**](/windows/win32/api/wincrypt/nf-wincrypt-certfreecertificatecontext) übergeben, um den Verweiszähler des Zertifikatkontexts zu dekrementieren.</span><span class="sxs-lookup"><span data-stu-id="d9e31-111">When you have finished using this certificate, you must pass this pointer to the [**CertFreeCertificateContext**](/windows/win32/api/wincrypt/nf-wincrypt-certfreecertificatecontext) function to decrement the reference count of the certificate context.</span></span>

<span data-ttu-id="d9e31-112">Wenn der **dwFlags-Member** der *pcsc-Struktur* das **CRYPTUI \_ SELECTCERT \_ MULTISELECT-Flag** nicht enthält, bedeutet ein Rückgabewert von **NULL,** dass der Benutzer das Dialogfeld geschlossen hat, ohne ein Zertifikat auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="d9e31-112">If the **dwFlags** member of the *pcsc* structure does not contain the **CRYPTUI\_SELECTCERT\_MULTISELECT** flag, a return value of **NULL** means that the user closed the dialog box without selecting a certificate.</span></span>

<span data-ttu-id="d9e31-113">Wenn der **dwFlags-Member** der *pcsc-Struktur* das **CRYPTUI \_ SELECTCERT \_ MULTISELECT-Flag** enthält, gibt diese Funktion immer **NULL** zurück.</span><span class="sxs-lookup"><span data-stu-id="d9e31-113">If the **dwFlags** member of the *pcsc* structure does contain the **CRYPTUI\_SELECTCERT\_MULTISELECT** flag, this function always returns **NULL**.</span></span> <span data-ttu-id="d9e31-114">Die ausgewählten Zertifikate werden im Zertifikatspeicher enthalten sein, der durch das **hSelectedCertStore-Element** von *pcsc* dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="d9e31-114">The selected certificates will be contained in the certificate store that is represented by the **hSelectedCertStore** member of *pcsc*.</span></span> <span data-ttu-id="d9e31-115">Wenn die Anzahl der Zertifikate im Speicher vor und nach dem Aufruf von **CryptUIDlgSelectCertificate** gleich ist, hat der Benutzer das Dialogfeld geschlossen, ohne Zertifikate auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="d9e31-115">If the number of certificates in the store is the same before and after calling **CryptUIDlgSelectCertificate**, the user closed the dialog box without selecting any certificates.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9e31-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d9e31-116">Remarks</span></span>

<span data-ttu-id="d9e31-117">Wenn der **dwFlags-Member** der [**CRYPTUI \_ SELECTCERTIFICATE-Struktur \_**](cryptui-selectcertificate-struct.md) auf **CRYPTUI \_ SELECTCERT \_ LEGACY** festgelegt ist, wird das Legacydialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d9e31-117">If the **dwFlags** member of the [**CRYPTUI\_SELECTCERTIFICATE\_STRUCT**](cryptui-selectcertificate-struct.md) structure is set to **CRYPTUI\_SELECTCERT\_LEGACY**, the legacy dialog is displayed.</span></span> <span data-ttu-id="d9e31-118">Andernfalls wird das aktuelle Dialogfeld für die Zertifikatauswahl angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d9e31-118">Otherwise, the current certificate selection dialog is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9e31-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d9e31-119">Requirements</span></span>



| <span data-ttu-id="d9e31-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d9e31-120">Requirement</span></span> | <span data-ttu-id="d9e31-121">Wert</span><span class="sxs-lookup"><span data-stu-id="d9e31-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9e31-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d9e31-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d9e31-123">Nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d9e31-123">Windows�XP \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="d9e31-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d9e31-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d9e31-125">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d9e31-125">Windows Server�2003 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="d9e31-126">Ende des Supports</span><span class="sxs-lookup"><span data-stu-id="d9e31-126">End of support</span></span><br/> | <span data-ttu-id="d9e31-127">Nur Windows \[ 7-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d9e31-127">Windows�7 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="d9e31-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d9e31-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="d9e31-129"><dt>Cryptui.lib</dt></span><span class="sxs-lookup"><span data-stu-id="d9e31-129"><dt>Cryptui.lib</dt></span></span> </dl>            |
| <span data-ttu-id="d9e31-130">DLL</span><span class="sxs-lookup"><span data-stu-id="d9e31-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9e31-131"><dt>Cryptui.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9e31-131"><dt>Cryptui.dll</dt></span></span> </dl>            |
| <span data-ttu-id="d9e31-132">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="d9e31-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d9e31-133">**CryptUIDlgSelectCertificateW** (Unicode) und **CryptUIDlgSelectCertificateA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d9e31-133">**CryptUIDlgSelectCertificateW** (Unicode) and **CryptUIDlgSelectCertificateA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d9e31-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9e31-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9e31-135">**CRYPTUI \_ \_ SELECTCERTIFICATE-STRUKTUR**</span><span class="sxs-lookup"><span data-stu-id="d9e31-135">**CRYPTUI\_SELECTCERTIFICATE\_STRUCT**</span></span>](cryptui-selectcertificate-struct.md)
</dt> </dl>






