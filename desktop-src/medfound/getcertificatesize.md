---
description: Ruft die Größe eines Zertifikats für einen Anzeigetreiber ab.
ms.assetid: fd52e939-127a-4493-8406-31f7767921cd
title: Getcertifialisiesize-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCertificateSize
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: bcd1f49ce65978c6a89c89cee1fda38e41434065
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342458"
---
# <a name="getcertificatesize-function"></a><span data-ttu-id="50a66-103">Getcertifialisiesize-Funktion</span><span class="sxs-lookup"><span data-stu-id="50a66-103">GetCertificateSize function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="50a66-104">Diese Funktion wird vom [Output Protection Manager](output-protection-manager.md) (OPM) verwendet, um auf die Funktionalität des Anzeige Treibers zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="50a66-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="50a66-105">Anwendungen sollten diese Funktion nicht aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="50a66-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="50a66-106">Ruft die Größe eines Zertifikats für einen Anzeigetreiber ab.</span><span class="sxs-lookup"><span data-stu-id="50a66-106">Gets the size of a certificate for a display driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="50a66-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="50a66-107">Syntax</span></span>


```C++
NTSTATUS WINAPI GetCertificateSize(
  _In_  PUNICODE_STRING          pstrDeviceName,
  _In_  DXGKMDT_CERTIFICATE_TYPE ctPVPCertificateType,
  _Out_ ULONG                    *pulCertificateLength
);
```



## <a name="parameters"></a><span data-ttu-id="50a66-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="50a66-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50a66-109">*pstrindevicename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="50a66-109">*pstrDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50a66-110">Ein Zeiger auf eine [**Unicode- \_ Zeichen**](/windows/win32/api/subauth/ns-subauth-unicode_string) folgen Struktur, die den Namen des Anzeige Geräts enthält, wie von der [**getmonitorinfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) -Funktion zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="50a66-110">A pointer to a [**UNICODE\_STRING**](/windows/win32/api/subauth/ns-subauth-unicode_string) structure that contains the name of the display device, as returned by the [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

</dd> <dt>

<span data-ttu-id="50a66-111">*ctpvpcertifialisietype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="50a66-111">*ctPVPCertificateType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50a66-112">Der Zertifikattyp, der als Member der **dxgkmdt- \_ \_ Zertifikattyp** -Enumeration angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="50a66-112">The type of certificate, specified as a member of the **DXGKMDT\_CERTIFICATE\_TYPE** enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="50a66-113">*pulcertifialisielength* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="50a66-113">*pulCertificateLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="50a66-114">Empfängt die Größe des Zertifikats in Bytes.</span><span class="sxs-lookup"><span data-stu-id="50a66-114">Receives the size of the certificate, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50a66-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="50a66-115">Return value</span></span>

<span data-ttu-id="50a66-116">Wenn die Methode erfolgreich ausgeführt wird, wird der **Status \_ erfolgreich** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="50a66-116">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="50a66-117">Andernfalls wird ein **NTSTATUS** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="50a66-117">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="50a66-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="50a66-118">Remarks</span></span>

<span data-ttu-id="50a66-119">Anwendungen sollten anstelle dieser Funktion die [**IOPMVideoOutput:: startinitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="50a66-119">Applications should call the [**IOPMVideoOutput::StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) method instead of this function.</span></span>

<span data-ttu-id="50a66-120">Diese Funktion verfügt über keine zugeordnete Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="50a66-120">This function has no associated import library.</span></span> <span data-ttu-id="50a66-121">Um diese Funktion aufzurufen, müssen Sie die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Gdi32.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="50a66-121">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="50a66-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="50a66-122">Requirements</span></span>



| <span data-ttu-id="50a66-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="50a66-123">Requirement</span></span> | <span data-ttu-id="50a66-124">Wert</span><span class="sxs-lookup"><span data-stu-id="50a66-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="50a66-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="50a66-125">Minimum supported client</span></span><br/> | <span data-ttu-id="50a66-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="50a66-126">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="50a66-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="50a66-127">Minimum supported server</span></span><br/> | <span data-ttu-id="50a66-128">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="50a66-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="50a66-129">DLL</span><span class="sxs-lookup"><span data-stu-id="50a66-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50a66-130"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50a66-130"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50a66-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50a66-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50a66-132">OPM-Funktionen</span><span class="sxs-lookup"><span data-stu-id="50a66-132">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="50a66-133">Output Protection Manager</span><span class="sxs-lookup"><span data-stu-id="50a66-133">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
