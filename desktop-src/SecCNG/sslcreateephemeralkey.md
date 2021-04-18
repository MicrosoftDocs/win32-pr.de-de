---
description: Erstellt einen kurzlebigen Schlüssel zur Verwendung während der Authentifizierung, die während des SSL-Handshakes (Secure Sockets Layer Protocol) auftritt.
ms.assetid: faad9b3b-e476-4e61-b978-bcb517ecaeb7
title: Sslkreatekurzlealkey-Funktion (sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslCreateEphemeralKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 452b0166da367bb6b1530f5669e55b7ca909e13e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347113"
---
# <a name="sslcreateephemeralkey-function"></a><span data-ttu-id="82547-103">Sslkreatekurzlealkey-Funktion</span><span class="sxs-lookup"><span data-stu-id="82547-103">SslCreateEphemeralKey function</span></span>

<span data-ttu-id="82547-104">Die **sslkreatekurzlealkey** -Funktion erstellt einen kurzlebigen Schlüssel zur Verwendung während der Authentifizierung, die während des [*Secure Sockets Layer Protokoll*](/windows/desktop/SecGloss/s-gly) -Handshake (SSL) auftritt.</span><span class="sxs-lookup"><span data-stu-id="82547-104">The **SslCreateEphemeralKey** function creates an ephemeral key for use during the authentication that occurs during the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) handshake.</span></span>

## <a name="syntax"></a><span data-ttu-id="82547-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="82547-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslCreateEphemeralKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_KEY_HANDLE  *phEphemeralKey,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  DWORD              dwKeyType,
  _In_  DWORD              dwKeyBitLen,
  _In_  PBYTE              pbParams,
  _In_  DWORD              cbParams,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="82547-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="82547-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82547-107">*hsslprovider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="82547-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82547-108">Das Handle der SSL-Protokoll Anbieter Instanz.</span><span class="sxs-lookup"><span data-stu-id="82547-108">The handle of the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="82547-109">*phphemeralkey* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="82547-109">*phEphemeralKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82547-110">Das Handle des kurzlebigen Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="82547-110">The handle of the ephemeral key.</span></span>

</dd> <dt>

<span data-ttu-id="82547-111">*dwprotocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="82547-111">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82547-112">Einer der [**CNG-SSL-Anbieter Protokoll-Bezeichnerwerte**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="82547-112">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="82547-113">*dwciphersuite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="82547-113">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82547-114">Einer der [**Cipher Suite-Bezeichnerwerte des CNG-SSL-Anbieters**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="82547-114">One of the [**CNG SSL Provider Cipher Suite Identifier**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="82547-115">*dwkeytype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="82547-115">*dwKeyType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82547-116">Einer der [**Schlüsseltyp-Bezeichnerwerte des CNG-SSL-Anbieters**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="82547-116">One of the [**CNG SSL Provider Key Type Identifier**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) values.</span></span> <span data-ttu-id="82547-117">Legen Sie diesen Parameter für Schlüsseltypen, die keine [*Kryptografie (Elliptic Curve Kryptografie*](/windows/desktop/SecGloss/e-gly) , ECC) sind, auf NULL fest.</span><span class="sxs-lookup"><span data-stu-id="82547-117">Set this parameter to zero for key types that are not [*elliptic curve cryptography*](/windows/desktop/SecGloss/e-gly) (ECC).</span></span>

</dd> <dt>

<span data-ttu-id="82547-118">*dwkeybitlen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="82547-118">*dwKeyBitLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82547-119">Die Länge des Schlüssels in Bits.</span><span class="sxs-lookup"><span data-stu-id="82547-119">The length, in bits, of the key.</span></span>

</dd> <dt>

<span data-ttu-id="82547-120">*pbparameams* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="82547-120">*pbParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82547-121">Ein Zeiger auf einen Puffer, der Parameter für den Schlüssel enthalten soll, der erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="82547-121">A pointer to a buffer to contain parameters for the key that is to be created.</span></span> <span data-ttu-id="82547-122">Wenn ein [*Diffie-Hellman (kurzlebiger) Key-Exchange-Algorithmus*](/windows/desktop/SecGloss/d-gly) (DHE) Verschlüsselungs Suite nicht verwendet wird, legen Sie den *pbparser* -Parameter auf **null** und den *cbparameams* -Parameter auf 0 (null) fest.</span><span class="sxs-lookup"><span data-stu-id="82547-122">If a [*Diffie-Hellman (ephemeral) key-exchange algorithm*](/windows/desktop/SecGloss/d-gly) (DHE) cipher suite is not used, set the *pbParams* parameter to **NULL** and the *cbParams* parameter to zero.</span></span>

</dd> <dt>

<span data-ttu-id="82547-123">*cbparametriams* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="82547-123">*cbParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82547-124">Die Länge der Daten im *pbparameams* -Puffer in Bytes.</span><span class="sxs-lookup"><span data-stu-id="82547-124">The length, in bytes, of the data in the *pbParams* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="82547-125">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="82547-125">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82547-126">Dieser Parameter ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="82547-126">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82547-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="82547-127">Return value</span></span>

<span data-ttu-id="82547-128">Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="82547-128">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="82547-129">Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="82547-129">If the function fails, it returns a nonzero error value.</span></span>



| <span data-ttu-id="82547-130">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="82547-130">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="82547-131">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="82547-131">Description</span></span>                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="82547-132"><dt>**Ernte \_ Kein Arbeits \_ Speicher**</dt> <dt>0x8009000el</dt></span><span class="sxs-lookup"><span data-stu-id="82547-132"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="82547-133">Es ist nicht genügend Arbeitsspeicher vorhanden, um den Puffer zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="82547-133">There is insufficient memory to allocate the buffer.</span></span><br/> |
| <dl> <span data-ttu-id="82547-134"><dt>**Ernte \_ Ungültiges \_ handle**</dt> <dt>0x80090026l</dt></span><span class="sxs-lookup"><span data-stu-id="82547-134"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="82547-135">Das *hsslprovider* -Handle ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="82547-135">The *hSslProvider* handle is not valid.</span></span><br/>              |
| <dl> <span data-ttu-id="82547-136"><dt>**Ernte \_ Ungültiger \_ Parameter**</dt> <dt>0x80090027l</dt></span><span class="sxs-lookup"><span data-stu-id="82547-136"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="82547-137">Einer der angegebenen Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="82547-137">One of the supplied parameters is not valid.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="82547-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="82547-138">Remarks</span></span>

<span data-ttu-id="82547-139">Wenn eine dit-Verschlüsselungs Sammlung verwendet wird, übergibt die interne SSL-Implementierung Server- *p* -und *g* -Parameter an die **sslkreatekurzlealkey** -Funktion in den Parametern *pbpara AMS* und *cbparameame.*</span><span class="sxs-lookup"><span data-stu-id="82547-139">When using a DHE cipher suite, the internal SSL implementation passes server *p* and *g* parameters to the **SslCreateEphemeralKey** function in the *pbParams* and *cbParams* parameters.</span></span>

<span data-ttu-id="82547-140">Das Format der Daten im *pbparameams* -Puffer ist mit dem Format identisch, das beim Festlegen der [**bcrypt \_ dh- \_ Parameter**](cng-property-identifiers.md) Eigenschaft verwendet wird, und beginnt mit einer [**bcrypt \_ dh- \_ Parameter \_ Header**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) Struktur.</span><span class="sxs-lookup"><span data-stu-id="82547-140">The format of the data in the *pbParams* buffer is the same as that used when setting the [**BCRYPT\_DH\_PARAMETERS**](cng-property-identifiers.md) property, and it starts with a [**BCRYPT\_DH\_PARAMETER\_HEADER**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="82547-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="82547-141">Requirements</span></span>



| <span data-ttu-id="82547-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="82547-142">Requirement</span></span> | <span data-ttu-id="82547-143">Wert</span><span class="sxs-lookup"><span data-stu-id="82547-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="82547-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="82547-144">Minimum supported client</span></span><br/> | <span data-ttu-id="82547-145">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="82547-145">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="82547-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="82547-146">Minimum supported server</span></span><br/> | <span data-ttu-id="82547-147">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="82547-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="82547-148">Header</span><span class="sxs-lookup"><span data-stu-id="82547-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="82547-149"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="82547-149"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="82547-150">DLL</span><span class="sxs-lookup"><span data-stu-id="82547-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82547-151"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82547-151"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

