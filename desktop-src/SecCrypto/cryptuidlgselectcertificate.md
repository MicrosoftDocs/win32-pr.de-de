---
description: Zeigt ein Dialogfeld an, in dem Benutzer ein Zertifikat auswählen können.
ms.assetid: 242c19a7-179b-4fc0-a050-a1b598566a6b
title: CryptUIDlgSelectCertificate-Funktion
ms.topic: reference
ms.date: 05/29/2020
ms.openlocfilehash: 65d9993cd1e035473e731056d33b7a391ef47b5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218187"
---
# <a name="cryptuidlgselectcertificate-function"></a><span data-ttu-id="bc306-103">CryptUIDlgSelectCertificate-Funktion</span><span class="sxs-lookup"><span data-stu-id="bc306-103">CryptUIDlgSelectCertificate function</span></span>

<span data-ttu-id="bc306-104">Die Funktion **cryptuidlgselectcertificate** zeigt ein Dialogfeld an, in dem Benutzer ein Zertifikat auswählen können.</span><span class="sxs-lookup"><span data-stu-id="bc306-104">The **CryptUIDlgSelectCertificate** function displays a dialog box that allows a user to select a certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc306-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc306-105">Syntax</span></span>


```C++
);
```



## <a name="parameters"></a><span data-ttu-id="bc306-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc306-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc306-107">*pcsc* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bc306-107">*pcsc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc306-108">Ein Zeiger auf eine [**cryptui \_ selectcertificate \_**](cryptui-selectcertificate-struct.md) -Struktur Struktur, die Informationen über das anzuzeigende Dialogfeld enthält.</span><span class="sxs-lookup"><span data-stu-id="bc306-108">A pointer to a [**CRYPTUI\_SELECTCERTIFICATE\_STRUCT**](cryptui-selectcertificate-struct.md) structure that contains information about the dialog box to display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc306-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bc306-109">Return value</span></span>

<span data-ttu-id="bc306-110">Ein Zeiger auf eine [**CERT- \_ Kontext**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) Struktur, die das vom Benutzer ausgewählte Zertifikat darstellt.</span><span class="sxs-lookup"><span data-stu-id="bc306-110">A pointer to a [**CERT\_CONTEXT**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) structure that represents the certificate selected by the user.</span></span> <span data-ttu-id="bc306-111">Nachdem Sie dieses Zertifikat verwendet haben, müssen Sie diesen Zeiger an die [**certfreecertifiskiecontext**](/windows/win32/api/wincrypt/nf-wincrypt-certfreecertificatecontext) -Funktion übergeben, um den Verweis Zähler des Zertifikat Kontexts zu verringern.</span><span class="sxs-lookup"><span data-stu-id="bc306-111">When you have finished using this certificate, you must pass this pointer to the [**CertFreeCertificateContext**](/windows/win32/api/wincrypt/nf-wincrypt-certfreecertificatecontext) function to decrement the reference count of the certificate context.</span></span>

<span data-ttu-id="bc306-112">Wenn der **dwFlags** -Member der *pcsc* -Struktur das **cryptui selectcert-Flag für die \_ \_ Mehrfachauswahl** nicht enthält, bedeutet der Rückgabewert **null** , dass der Benutzer das Dialogfeld geschlossen hat, ohne ein Zertifikat auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="bc306-112">If the **dwFlags** member of the *pcsc* structure does not contain the **CRYPTUI\_SELECTCERT\_MULTISELECT** flag, a return value of **NULL** means that the user closed the dialog box without selecting a certificate.</span></span>

<span data-ttu-id="bc306-113">Wenn der **dwFlags** -Member der *pcsc* -Struktur das **cryptui selectcert-Flag für die \_ \_ Mehrfachauswahl** enthält, gibt diese Funktion immer **null** zurück.</span><span class="sxs-lookup"><span data-stu-id="bc306-113">If the **dwFlags** member of the *pcsc* structure does contain the **CRYPTUI\_SELECTCERT\_MULTISELECT** flag, this function always returns **NULL**.</span></span> <span data-ttu-id="bc306-114">Die ausgewählten Zertifikate sind im Zertifikat Speicher enthalten, der durch das **hselectedcertstore** -Mitglied von *pcsc* repräsentiert wird.</span><span class="sxs-lookup"><span data-stu-id="bc306-114">The selected certificates will be contained in the certificate store that is represented by the **hSelectedCertStore** member of *pcsc*.</span></span> <span data-ttu-id="bc306-115">Wenn die Anzahl der Zertifikate im Speicher vor und nach dem Aufruf von **cryptuidlgselectcertificate** identisch ist, hat der Benutzer das Dialogfeld geschlossen, ohne Zertifikate auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="bc306-115">If the number of certificates in the store is the same before and after calling **CryptUIDlgSelectCertificate**, the user closed the dialog box without selecting any certificates.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc306-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bc306-116">Remarks</span></span>

<span data-ttu-id="bc306-117">Wenn der **dwFlags** -Member der " [**cryptui \_ selectcertificate \_ struct**](cryptui-selectcertificate-struct.md) "-Struktur auf " **cryptui \_ selectcert \_ Legacy**" festgelegt ist, wird das Dialogfeld "Legacy" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bc306-117">If the **dwFlags** member of the [**CRYPTUI\_SELECTCERTIFICATE\_STRUCT**](cryptui-selectcertificate-struct.md) structure is set to **CRYPTUI\_SELECTCERT\_LEGACY**, the legacy dialog is displayed.</span></span> <span data-ttu-id="bc306-118">Andernfalls wird das aktuelle Zertifikat Auswahl Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bc306-118">Otherwise, the current certificate selection dialog is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc306-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc306-119">Requirements</span></span>



| <span data-ttu-id="bc306-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc306-120">Requirement</span></span> | <span data-ttu-id="bc306-121">Wert</span><span class="sxs-lookup"><span data-stu-id="bc306-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc306-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bc306-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bc306-123">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc306-123">Windows�XP \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="bc306-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bc306-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bc306-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc306-125">Windows Server�2003 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="bc306-126">Ende des Supports</span><span class="sxs-lookup"><span data-stu-id="bc306-126">End of support</span></span><br/> | <span data-ttu-id="bc306-127">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc306-127">Windows�7 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="bc306-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bc306-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="bc306-129"><dt>Cryptui. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc306-129"><dt>Cryptui.lib</dt></span></span> </dl>            |
| <span data-ttu-id="bc306-130">DLL</span><span class="sxs-lookup"><span data-stu-id="bc306-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc306-131"><dt>Cryptui.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc306-131"><dt>Cryptui.dll</dt></span></span> </dl>            |
| <span data-ttu-id="bc306-132">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="bc306-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="bc306-133">**Cryptuidlgselectcertifi| EW** (Unicode) und **cryptuidlgselectcertifi-EA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="bc306-133">**CryptUIDlgSelectCertificateW** (Unicode) and **CryptUIDlgSelectCertificateA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bc306-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc306-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc306-135">**cryptui \_ selectcertificate- \_ Struktur**</span><span class="sxs-lookup"><span data-stu-id="bc306-135">**CRYPTUI\_SELECTCERTIFICATE\_STRUCT**</span></span>](cryptui-selectcertificate-struct.md)
</dt> </dl>

<span data-ttu-id="bc306-136">�</span><span class="sxs-lookup"><span data-stu-id="bc306-136">�</span></span>

<span data-ttu-id="bc306-137">�</span><span class="sxs-lookup"><span data-stu-id="bc306-137">�</span></span>




