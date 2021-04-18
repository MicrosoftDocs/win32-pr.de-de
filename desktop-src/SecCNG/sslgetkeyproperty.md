---
description: Ruft den Wert einer benannten Eigenschaft für ein SSL-Anbieter Schlüsselobjekt (Secure Sockets Layer Protocol) ab.
ms.assetid: 01a7e82a-3888-4f96-85a2-e07811f1895e
title: Sslgetkeyproperty-Funktion (sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGetKeyProperty
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 42952b76bfb46eeeb31b9f76b1f677e7b3b8e3e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352259"
---
# <a name="sslgetkeyproperty-function"></a><span data-ttu-id="58e1d-103">Sslgetkeyproperty-Funktion</span><span class="sxs-lookup"><span data-stu-id="58e1d-103">SslGetKeyProperty function</span></span>

<span data-ttu-id="58e1d-104">Die **sslgetkeyproperty** -Funktion Ruft den Wert einer benannten Eigenschaft für ein SSL-Anbieter Schlüsselobjekt ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ) ab.</span><span class="sxs-lookup"><span data-stu-id="58e1d-104">The **SslGetKeyProperty** function retrieves the value of a named property for a [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) provider key object.</span></span>

## <a name="syntax"></a><span data-ttu-id="58e1d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="58e1d-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslGetKeyProperty(
  _In_  NCRYPT_KEY_HANDLE hKey,
  _In_  LPCWSTR           pszProperty,
  _Out_ PBYTE             ppbOutput,
  _Out_ DWORD             *pcbOutput,
  _In_  DWORD             dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="58e1d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="58e1d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58e1d-107">*HKEY* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58e1d-107">*hKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58e1d-108">Das Handle des SSL-Anbieters.</span><span class="sxs-lookup"><span data-stu-id="58e1d-108">The handle of the SSL provider.</span></span>

</dd> <dt>

<span data-ttu-id="58e1d-109">*pszproperty* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58e1d-109">*pszProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58e1d-110">Ein Zeiger auf eine NULL-terminierte Unicode-Zeichenfolge, die den Namen der abzurufenden Eigenschaft enthält.</span><span class="sxs-lookup"><span data-stu-id="58e1d-110">A pointer to a null-terminated Unicode string that contains the name of the property to retrieve.</span></span> <span data-ttu-id="58e1d-111">Hierbei kann es sich um einen der vordefinierten [**Schlüsselspeicher-Eigenschaften**](key-storage-property-identifiers.md) Bezeichner oder um einen benutzerdefinierten Eigenschaften Bezeichner handeln.</span><span class="sxs-lookup"><span data-stu-id="58e1d-111">This can be one of the predefined [**Key Storage Property Identifiers**](key-storage-property-identifiers.md) or a custom property identifier.</span></span>

</dd> <dt>

<span data-ttu-id="58e1d-112">*ppboutput* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="58e1d-112">*ppbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="58e1d-113">Ein Zeiger auf einen Puffer, der den Eigenschafts Wert empfängt.</span><span class="sxs-lookup"><span data-stu-id="58e1d-113">A pointer to a buffer that receives the property value.</span></span> <span data-ttu-id="58e1d-114">Der Aufrufer der Funktion muss diesen Puffer durch Aufrufen der [**sslfreebuffer**](sslfreebuffer.md) -Funktion freigeben.</span><span class="sxs-lookup"><span data-stu-id="58e1d-114">The caller of the function must free this buffer by calling the [**SslFreeBuffer**](sslfreebuffer.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="58e1d-115">*pcboutput* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="58e1d-115">*pcbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="58e1d-116">Die Größe des *pboutput* -Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="58e1d-116">The size, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="58e1d-117">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58e1d-117">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58e1d-118">Dieser Parameter ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="58e1d-118">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58e1d-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="58e1d-119">Return value</span></span>

<span data-ttu-id="58e1d-120">Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="58e1d-120">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="58e1d-121">Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="58e1d-121">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="58e1d-122">Mögliche Rückgabecodes sind u. a. die folgenden:</span><span class="sxs-lookup"><span data-stu-id="58e1d-122">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="58e1d-123">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="58e1d-123">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="58e1d-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="58e1d-124">Description</span></span>                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <dl> <span data-ttu-id="58e1d-125"><dt>**Ernte \_ Ungültiges \_ handle**</dt> <dt>0x80090026l</dt></span><span class="sxs-lookup"><span data-stu-id="58e1d-125"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="58e1d-126">Eines der bereitgestellten Handles ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="58e1d-126">One of the provided handles is not valid.</span></span><br/>    |
| <dl> <span data-ttu-id="58e1d-127"><dt>**Ernte \_ Ungültiger \_ Parameter**</dt> <dt>0x80090027l</dt></span><span class="sxs-lookup"><span data-stu-id="58e1d-127"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="58e1d-128">Einer der angegebenen Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="58e1d-128">One of the supplied parameters is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="58e1d-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="58e1d-129">Requirements</span></span>



| <span data-ttu-id="58e1d-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="58e1d-130">Requirement</span></span> | <span data-ttu-id="58e1d-131">Wert</span><span class="sxs-lookup"><span data-stu-id="58e1d-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="58e1d-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="58e1d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="58e1d-133">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="58e1d-133">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="58e1d-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="58e1d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="58e1d-135">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="58e1d-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="58e1d-136">Header</span><span class="sxs-lookup"><span data-stu-id="58e1d-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="58e1d-137"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="58e1d-137"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="58e1d-138">DLL</span><span class="sxs-lookup"><span data-stu-id="58e1d-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58e1d-139"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58e1d-139"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

