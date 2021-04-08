---
description: Ruft den Wert einer angegebenen Anbieter Eigenschaft ab.
ms.assetid: 69235520-acaa-4ec4-9fd6-4b3297e14376
title: Sslgetproviderproperty-Funktion (sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGetProviderProperty
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: ced0f32d45531a1220f7aae9fe0e660648e5d1bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867667"
---
# <a name="sslgetproviderproperty-function"></a><span data-ttu-id="bd8d2-103">Sslgetproviderproperty-Funktion</span><span class="sxs-lookup"><span data-stu-id="bd8d2-103">SslGetProviderProperty function</span></span>

<span data-ttu-id="bd8d2-104">Die **sslgetproviderproperty** -Funktion Ruft den Wert einer angegebenen Anbieter Eigenschaft ab.</span><span class="sxs-lookup"><span data-stu-id="bd8d2-104">The **SslGetProviderProperty** function retrieves the value of a specified provider property.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd8d2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd8d2-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslGetProviderProperty(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _In_    LPCWSTR            pszProperty,
  _Out_   PBYTE              ppbOutput,
  _Out_   DWORD              *pcbOutput,
  _Inout_ PVOID              *ppEnumState,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="bd8d2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd8d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd8d2-107">*hsslprovider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bd8d2-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd8d2-108">Das Handle des SSL-Anbieters ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ), für den die Eigenschaft abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="bd8d2-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) provider for which to retrieve the property.</span></span>

</dd> <dt>

<span data-ttu-id="bd8d2-109">*pszproperty* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bd8d2-109">*pszProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd8d2-110">Ein Zeiger auf eine NULL-terminierte Unicode-Zeichenfolge, die den Namen der abzurufenden Eigenschaft enthält.</span><span class="sxs-lookup"><span data-stu-id="bd8d2-110">A pointer to a null-terminated Unicode string that contains the name of the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="bd8d2-111">*ppboutput* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bd8d2-111">*ppbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd8d2-112">Die Adresse eines Puffers, der den Eigenschafts Wert empfängt.</span><span class="sxs-lookup"><span data-stu-id="bd8d2-112">The address of a buffer that receives the property value.</span></span>

<span data-ttu-id="bd8d2-113">Der Aufrufer der Funktion muss diesen Puffer durch Aufrufen der [**sslfreebuffer**](sslfreebuffer.md) -Funktion freigeben.</span><span class="sxs-lookup"><span data-stu-id="bd8d2-113">The caller of the function must free this buffer by calling the [**SslFreeBuffer**](sslfreebuffer.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="bd8d2-114">*pcboutput* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bd8d2-114">*pcbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd8d2-115">Die Größe des *pboutput* -Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="bd8d2-115">The size, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="bd8d2-116">" *ppumschlag State* \[ " in, out\]</span><span class="sxs-lookup"><span data-stu-id="bd8d2-116">*ppEnumState* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd8d2-117">Die Adresse eines **void** -Zeigers, der enumerationsstatusinformationen empfängt, die in nachfolgenden Aufrufen dieser Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bd8d2-117">The address of a **VOID** pointer that receives enumeration state information that is used in subsequent calls to this function.</span></span> <span data-ttu-id="bd8d2-118">Diese Informationen sind nur für den SSL-Anbieter von Bedeutung und für den Aufrufer nicht transparent.</span><span class="sxs-lookup"><span data-stu-id="bd8d2-118">This information only has meaning to the SSL provider and is opaque to the caller.</span></span> <span data-ttu-id="bd8d2-119">Der SSL-Anbieter verwendet diese Informationen, um zu bestimmen, welches Element als nächstes in der-Enumeration verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bd8d2-119">The SSL provider uses this information to determine which item is next in the enumeration.</span></span> <span data-ttu-id="bd8d2-120">Wenn die Variable, auf die dieser Parameter verweist, **null** enthält, wird die Enumeration von Anfang an gestartet.</span><span class="sxs-lookup"><span data-stu-id="bd8d2-120">If the variable pointed to by this parameter contains **NULL**, the enumeration is started from the beginning.</span></span>

<span data-ttu-id="bd8d2-121">Der Aufrufer der Funktion muss diesen Arbeitsspeicher freigeben, indem er die [**sslfreebuffer**](sslfreebuffer.md) -Funktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="bd8d2-121">The caller of the function must free this memory by calling the [**SslFreeBuffer**](sslfreebuffer.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="bd8d2-122">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bd8d2-122">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd8d2-123">Dieser Parameter ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="bd8d2-123">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd8d2-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bd8d2-124">Return value</span></span>

<span data-ttu-id="bd8d2-125">Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="bd8d2-125">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="bd8d2-126">Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bd8d2-126">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="bd8d2-127">Mögliche Rückgabecodes sind u. a. die folgenden:</span><span class="sxs-lookup"><span data-stu-id="bd8d2-127">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="bd8d2-128">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="bd8d2-128">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="bd8d2-129">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bd8d2-129">Description</span></span>                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bd8d2-130"><dt>**Ernte \_ Kein Arbeits \_ Speicher**</dt> <dt>0x8009000el</dt></span><span class="sxs-lookup"><span data-stu-id="bd8d2-130"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="bd8d2-131">Es ist nicht genügend Arbeitsspeicher verfügbar, um erforderliche Puffer zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="bd8d2-131">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="bd8d2-132"><dt>**Ernte \_ Ungültiges \_ handle**</dt> <dt>0x80090026l</dt></span><span class="sxs-lookup"><span data-stu-id="bd8d2-132"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="bd8d2-133">Das *hsslprovider* -Handle ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="bd8d2-133">The *hSslProvider* handle is not valid.</span></span><br/>                       |
| <dl> <span data-ttu-id="bd8d2-134"><dt>**Ernte \_ Ungültiger \_ Parameter**</dt> <dt>0x80090027l</dt></span><span class="sxs-lookup"><span data-stu-id="bd8d2-134"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="bd8d2-135">Einer der angegebenen Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="bd8d2-135">One of the supplied parameters is not valid.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="bd8d2-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bd8d2-136">Requirements</span></span>



| <span data-ttu-id="bd8d2-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bd8d2-137">Requirement</span></span> | <span data-ttu-id="bd8d2-138">Wert</span><span class="sxs-lookup"><span data-stu-id="bd8d2-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd8d2-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bd8d2-139">Minimum supported client</span></span><br/> | <span data-ttu-id="bd8d2-140">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bd8d2-140">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="bd8d2-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bd8d2-141">Minimum supported server</span></span><br/> | <span data-ttu-id="bd8d2-142">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bd8d2-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="bd8d2-143">Header</span><span class="sxs-lookup"><span data-stu-id="bd8d2-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd8d2-144"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd8d2-144"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="bd8d2-145">DLL</span><span class="sxs-lookup"><span data-stu-id="bd8d2-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd8d2-146"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd8d2-146"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

