---
description: Verschlüsselt ein einzelnes Secure Sockets Layer Protocol (SSL)-Paket.
ms.assetid: 1002158b-1a4f-4461-978f-b221ef6332e0
title: Sslencryptpacket-Funktion (sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslEncryptPacket
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: e839b37e839fd09d5df5f9902474b7ce7c4c74a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106354000"
---
# <a name="sslencryptpacket-function"></a><span data-ttu-id="dcec6-103">Sslencryptpacket-Funktion</span><span class="sxs-lookup"><span data-stu-id="dcec6-103">SslEncryptPacket function</span></span>

<span data-ttu-id="dcec6-104">Die **sslencryptpacket** -Funktion verschlüsselt ein einzelnes [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) (SSL)-Paket.</span><span class="sxs-lookup"><span data-stu-id="dcec6-104">The **SslEncryptPacket** function encrypts a single [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcec6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dcec6-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslEncryptPacket(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _Inout_ NCRYPT_KEY_HANDLE  hKey,
  _In_    PBYTE              *pbInput,
  _In_    DWORD              cbInput,
  _Out_   PBYTE              pbOutput,
  _In_    DWORD              cbOutput,
  _Out_   DWORD              *pcbResult,
  _In_    ULONGLONG          SequenceNumber,
  _In_    DWORD              dwContentType,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="dcec6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dcec6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcec6-107">*hsslprovider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dcec6-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcec6-108">Das Handle der SSL-Protokoll Anbieter Instanz.</span><span class="sxs-lookup"><span data-stu-id="dcec6-108">The handle of the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="dcec6-109">*HKEY* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="dcec6-109">*hKey* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dcec6-110">Das Handle für den Schlüssel, der zum Verschlüsseln des Pakets verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dcec6-110">The handle to the key that is used to encrypt the packet.</span></span>

</dd> <dt>

<span data-ttu-id="dcec6-111">*pbinput* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dcec6-111">*pbInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcec6-112">Ein Zeiger auf den Puffer, der das Paket enthält, das verschlüsselt werden soll.</span><span class="sxs-lookup"><span data-stu-id="dcec6-112">A pointer to the buffer that contains the packet to be encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="dcec6-113">*cbinput* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dcec6-113">*cbInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcec6-114">Die Länge des *pbinput* -Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="dcec6-114">The length, in bytes, of the *pbInput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="dcec6-115">*pboutput* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="dcec6-115">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dcec6-116">Ein Zeiger auf einen Puffer, um das verschlüsselte Paket zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="dcec6-116">A pointer to a buffer to receive the encrypted packet.</span></span>

</dd> <dt>

<span data-ttu-id="dcec6-117">*cboutput* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dcec6-117">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcec6-118">Die Länge (Bytes) des *pboutput* -Puffers.</span><span class="sxs-lookup"><span data-stu-id="dcec6-118">The length, bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="dcec6-119">*pcbresult* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="dcec6-119">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dcec6-120">Die Anzahl der in den *pboutput* -Puffer geschriebenen Bytes.</span><span class="sxs-lookup"><span data-stu-id="dcec6-120">The number of bytes written to the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="dcec6-121">*Sequencennummer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dcec6-121">*SequenceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcec6-122">Die Sequenznummer, die diesem Paket entspricht.</span><span class="sxs-lookup"><span data-stu-id="dcec6-122">The sequence number that corresponds to this packet.</span></span>

</dd> <dt>

<span data-ttu-id="dcec6-123">*dwcontenttype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dcec6-123">*dwContentType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcec6-124">Der Inhaltstyp, der diesem Paket entspricht, das das Protokoll der höheren Ebene angibt, das zum Verarbeiten des eingeschlossenen Pakets verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dcec6-124">The content type that corresponds to this packet, which specifies the higher level protocol used to process the enclosed packet.</span></span>



| <span data-ttu-id="dcec6-125">Wert</span><span class="sxs-lookup"><span data-stu-id="dcec6-125">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="dcec6-126">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="dcec6-126">Meaning</span></span>                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="CT_CHANGE_CIPHER_SPEC"></span><span id="ct_change_cipher_spec"></span><dl> <span data-ttu-id="dcec6-127"><dt>**CT \_ \_Chiffre \_ Spezifikation ändern**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="dcec6-127"><dt>**CT\_CHANGE\_CIPHER\_SPEC**</dt> <dt>20</dt></span></span> </dl> | <span data-ttu-id="dcec6-128">Gibt eine Änderung in der Verschlüsselungs Strategie an.</span><span class="sxs-lookup"><span data-stu-id="dcec6-128">Indicates a change in the ciphering strategy.</span></span><br/>                         |
| <span id="CT_ALERT"></span><span id="ct_alert"></span><dl> <span data-ttu-id="dcec6-129"><dt>**CT \_ Warnung**</dt> <dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="dcec6-129"><dt>**CT\_ALERT**</dt> <dt>21</dt></span></span> </dl>                                          | <span data-ttu-id="dcec6-130">Gibt an, dass das eingeschlossene Paket eine Warnung enthält.</span><span class="sxs-lookup"><span data-stu-id="dcec6-130">Indicates that the enclosed packet contains an alert.</span></span><br/>                 |
| <span id="CT_HANDSHAKE"></span><span id="ct_handshake"></span><dl> <span data-ttu-id="dcec6-131"><dt>**CT \_ HANDSHAKE**</dt> <dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="dcec6-131"><dt>**CT\_HANDSHAKE**</dt> <dt>22</dt></span></span> </dl>                              | <span data-ttu-id="dcec6-132">Gibt an, dass das eingeschlossene Paket Teil des Handshake-Protokolls ist.</span><span class="sxs-lookup"><span data-stu-id="dcec6-132">Indicates that the enclosed packet is part of the handshake protocol.</span></span><br/> |
| <span id="CT_APPLICATIONDATA"></span><span id="ct_applicationdata"></span><dl> <span data-ttu-id="dcec6-133"><dt>**CT \_ ApplicationData**</dt> <dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="dcec6-133"><dt>**CT\_APPLICATIONDATA**</dt> <dt>23</dt></span></span> </dl>            | <span data-ttu-id="dcec6-134">Gibt an, dass das Paket Anwendungsdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="dcec6-134">Indicates that the packet contains application data.</span></span><br/>                  |



 

</dd> <dt>

<span data-ttu-id="dcec6-135">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dcec6-135">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcec6-136">Dieser Parameter ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="dcec6-136">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcec6-137">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dcec6-137">Return value</span></span>

<span data-ttu-id="dcec6-138">Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="dcec6-138">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="dcec6-139">Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="dcec6-139">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="dcec6-140">Mögliche Rückgabecodes sind u. a. die folgenden:</span><span class="sxs-lookup"><span data-stu-id="dcec6-140">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="dcec6-141">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="dcec6-141">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="dcec6-142">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dcec6-142">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="dcec6-143"><dt>**Ernte \_ Ungültiges \_ handle**</dt> <dt>0x80090026l</dt></span><span class="sxs-lookup"><span data-stu-id="dcec6-143"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="dcec6-144">Eines der bereitgestellten Handles ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="dcec6-144">One of the provided handles is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="dcec6-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dcec6-145">Requirements</span></span>



| <span data-ttu-id="dcec6-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dcec6-146">Requirement</span></span> | <span data-ttu-id="dcec6-147">Wert</span><span class="sxs-lookup"><span data-stu-id="dcec6-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcec6-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dcec6-148">Minimum supported client</span></span><br/> | <span data-ttu-id="dcec6-149">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dcec6-149">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="dcec6-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dcec6-150">Minimum supported server</span></span><br/> | <span data-ttu-id="dcec6-151">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dcec6-151">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="dcec6-152">Header</span><span class="sxs-lookup"><span data-stu-id="dcec6-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="dcec6-153"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcec6-153"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="dcec6-154">DLL</span><span class="sxs-lookup"><span data-stu-id="dcec6-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dcec6-155"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dcec6-155"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

