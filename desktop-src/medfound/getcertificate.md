---
description: Ruft ein Zertifikat für einen Anzeigetreiber ab.
ms.assetid: eceaf151-1dae-4ff0-9139-7f1789f6c682
title: GetCertificate-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCertificate
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 30cb17345177b552e51120afd00758a3f6886584
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344979"
---
# <a name="getcertificate-function"></a><span data-ttu-id="d9bd5-103">GetCertificate-Funktion</span><span class="sxs-lookup"><span data-stu-id="d9bd5-103">GetCertificate function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d9bd5-104">Diese Funktion wird vom [Output Protection Manager](output-protection-manager.md) (OPM) verwendet, um auf die Funktionalität des Anzeige Treibers zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="d9bd5-105">Anwendungen sollten diese Funktion nicht aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="d9bd5-106">Ruft ein Zertifikat für einen Anzeigetreiber ab.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-106">Gets a certificate for a display driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9bd5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9bd5-107">Syntax</span></span>


```C++
NTSTATUS WINAPI GetCertificate(
  _In_  PUNICODE_STRING          pstrDeviceName,
  _In_  DXGKMDT_CERTIFICATE_TYPE ctPVPCertificateType,
  _Out_ BYTE                     *pbCertificate,
  _Out_ ULONG                    ulCertificateLength
);
```



## <a name="parameters"></a><span data-ttu-id="d9bd5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9bd5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9bd5-109">*pstrindevicename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9bd5-109">*pstrDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9bd5-110">Ein Zeiger auf eine [**Unicode- \_ Zeichen**](/windows/win32/api/subauth/ns-subauth-unicode_string) folgen Struktur, die den Namen des Anzeige Geräts enthält, wie von der [**getmonitorinfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) -Funktion zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-110">A pointer to a [**UNICODE\_STRING**](/windows/win32/api/subauth/ns-subauth-unicode_string) structure that contains the name of the display device, as returned by the [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

</dd> <dt>

<span data-ttu-id="d9bd5-111">*ctpvpcertifialisietype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9bd5-111">*ctPVPCertificateType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9bd5-112">Der Zertifikattyp, der als Member der **dxgkmdt- \_ \_ Zertifikattyp** -Enumeration angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-112">The type of certificate, specified as a member of the **DXGKMDT\_CERTIFICATE\_TYPE** enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="d9bd5-113">*pbcertificate* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d9bd5-113">*pbCertificate* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d9bd5-114">Ein Zeiger auf einen Puffer, der das Zertifikat empfängt.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-114">A pointer to a buffer that receives the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="d9bd5-115">*ulcertifialisielength* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d9bd5-115">*ulCertificateLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d9bd5-116">Die Größe des *pbcertificate* -Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-116">The size of the *pbCertificate* buffer, in bytes.</span></span> <span data-ttu-id="d9bd5-117">Um die Größe des Zertifikats abzurufen, nennen Sie [**getcertifikatesize**](getcertificatesize.md).</span><span class="sxs-lookup"><span data-stu-id="d9bd5-117">To get the size of the certificate, call [**GetCertificateSize**](getcertificatesize.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9bd5-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d9bd5-118">Return value</span></span>

<span data-ttu-id="d9bd5-119">Wenn die Methode erfolgreich ausgeführt wird, wird der **Status \_ erfolgreich** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-119">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="d9bd5-120">Andernfalls wird ein **NTSTATUS** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-120">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9bd5-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d9bd5-121">Remarks</span></span>

<span data-ttu-id="d9bd5-122">Anwendungen sollten anstelle dieser Funktion die [**IOPMVideoOutput:: startinitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-122">Applications should call the [**IOPMVideoOutput::StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) method instead of this function.</span></span>

<span data-ttu-id="d9bd5-123">Diese Funktion verfügt über keine zugeordnete Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-123">This function has no associated import library.</span></span> <span data-ttu-id="d9bd5-124">Um diese Funktion aufzurufen, müssen Sie die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Gdi32.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-124">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9bd5-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d9bd5-125">Requirements</span></span>



| <span data-ttu-id="d9bd5-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d9bd5-126">Requirement</span></span> | <span data-ttu-id="d9bd5-127">Wert</span><span class="sxs-lookup"><span data-stu-id="d9bd5-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d9bd5-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d9bd5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d9bd5-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d9bd5-129">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d9bd5-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d9bd5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d9bd5-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d9bd5-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d9bd5-132">DLL</span><span class="sxs-lookup"><span data-stu-id="d9bd5-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9bd5-133"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9bd5-133"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9bd5-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9bd5-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9bd5-135">OPM-Funktionen</span><span class="sxs-lookup"><span data-stu-id="d9bd5-135">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="d9bd5-136">Output Protection Manager</span><span class="sxs-lookup"><span data-stu-id="d9bd5-136">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
