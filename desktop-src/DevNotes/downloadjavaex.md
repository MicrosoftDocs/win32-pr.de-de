---
description: Lädt die CAB-Datei Signatur herunter, überprüft die den Paketen zugeordneten Berechtigungen und führt Sie basierend auf der Authentifizierung aus.
ms.assetid: b86a8f39-73a1-4e17-ac83-9ed095de4922
title: Downloadjavaex-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownloadJavaEX
api_type:
- DllExport
api_location:
- Javacypt.dll
ms.openlocfilehash: 31371e91599d604db591ee3e921b42bc809aae21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370137"
---
# <a name="downloadjavaex-function"></a><span data-ttu-id="516b5-103">Downloadjavaex-Funktion</span><span class="sxs-lookup"><span data-stu-id="516b5-103">DownloadJavaEX function</span></span>

<span data-ttu-id="516b5-104">Lädt die CAB-Datei Signatur herunter, überprüft die den Paketen zugeordneten Berechtigungen und führt Sie basierend auf der Authentifizierung aus.</span><span class="sxs-lookup"><span data-stu-id="516b5-104">Downloads the .cab file signature, verifies the permissions associated with the packages, and executes them based on authentication.</span></span>

## <a name="syntax"></a><span data-ttu-id="516b5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="516b5-105">Syntax</span></span>


```C++
HRESULT WINAPI DownloadJavaEX(
  _In_ PALLOCATOR               Reserved,
  _In_ PCRYPT_PROVIDER_DATA     pProviderData,
  _In_ PJAVA_POLICY_PROVIDER    pJava,
  _In_ CRYPT_PROVIDER_FUNCTIONS *pFunctions,
  _In_ BOOL                     fCertificate,
  _In_ PJAVA_TRUST              pTrust
);
```



## <a name="parameters"></a><span data-ttu-id="516b5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="516b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="516b5-107">*Reserviert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="516b5-107">*Reserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="516b5-108">Dieser Parameter ist reserviert.</span><span class="sxs-lookup"><span data-stu-id="516b5-108">This parameter is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="516b5-109">*pproviderdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="516b5-109">*pProviderData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="516b5-110">Eine [**\_ \_ Daten**](/windows/win32/api/wintrust/ns-wintrust-crypt_provider_data) Struktur des Crypt-Anbieters, die Zertifikat Daten wie z. b. Datei-und Zonen Berechtigungen enthält.</span><span class="sxs-lookup"><span data-stu-id="516b5-110">A [**CRYPT\_PROVIDER\_DATA**](/windows/win32/api/wintrust/ns-wintrust-crypt_provider_data) structure that contains certificate data such as file and zone permissions.</span></span>

</dd> <dt>

<span data-ttu-id="516b5-111">*pjava* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="516b5-111">*pJava* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="516b5-112">Eine [**Java- \_ Richtlinien \_ Anbieter**](/previous-versions//bb432350(v=vs.85)) Struktur, die Daten enthält, die sich auf den Richtlinien Anbieter beziehen.</span><span class="sxs-lookup"><span data-stu-id="516b5-112">A [**JAVA\_POLICY\_PROVIDER**](/previous-versions//bb432350(v=vs.85)) structure that contains data related to the policy provider.</span></span>

</dd> <dt>

<span data-ttu-id="516b5-113">*pFunctions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="516b5-113">*pFunctions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="516b5-114">Eine [**crypt- \_ Anbieter \_ Funktions**](/windows/win32/api/wintrust/ns-wintrust-crypt_provider_functions) Struktur, die eine Liste von Methoden zum Überprüfen von Zertifikat Objekten, Signaturen und abschließenden Richtlinien enthält.</span><span class="sxs-lookup"><span data-stu-id="516b5-114">A [**CRYPT\_PROVIDER\_FUNCTIONS**](/windows/win32/api/wintrust/ns-wintrust-crypt_provider_functions) structure that contains a list of methods to verify certificate objects, signatures, and final policies.</span></span>

</dd> <dt>

<span data-ttu-id="516b5-115">*Zertifikat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="516b5-115">*fCertificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="516b5-116">Wenn ein Zertifikat vorhanden ist, ist dieser Parameter **true**.</span><span class="sxs-lookup"><span data-stu-id="516b5-116">If a certificate is present, this parameter is **TRUE**.</span></span> <span data-ttu-id="516b5-117">Andernfalls ist Sie **false**.</span><span class="sxs-lookup"><span data-stu-id="516b5-117">Otherwise, it is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="516b5-118">*ptrust* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="516b5-118">*pTrust* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="516b5-119">Eine [**Java- \_ Vertrauensstellungs**](/windows/desktop/api/Capi/ns-capi-java_trust) Struktur, die Vertrauensstellungs Informationen enthält, wie z. b. codierte Berechtigung, Codierungs Signatur und authentixes</span><span class="sxs-lookup"><span data-stu-id="516b5-119">A [**JAVA\_TRUST**](/windows/desktop/api/Capi/ns-capi-java_trust) structure that contains trust information such as encoded permission, encoder signature, and authentic return policy code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="516b5-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="516b5-120">Return value</span></span>

<span data-ttu-id="516b5-121">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="516b5-121">If the function succeeds, the return value is **S\_OK**.</span></span> <span data-ttu-id="516b5-122">Andernfalls ist der Rückgabewert ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="516b5-122">Otherwise, the return value is an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="516b5-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="516b5-123">Remarks</span></span>

<span data-ttu-id="516b5-124">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="516b5-124">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="516b5-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="516b5-125">Requirements</span></span>



| <span data-ttu-id="516b5-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="516b5-126">Requirement</span></span> | <span data-ttu-id="516b5-127">Wert</span><span class="sxs-lookup"><span data-stu-id="516b5-127">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="516b5-128">DLL</span><span class="sxs-lookup"><span data-stu-id="516b5-128">DLL</span></span><br/> | <dl> <span data-ttu-id="516b5-129"><dt>Javacypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="516b5-129"><dt>Javacypt.dll</dt></span></span> </dl> |



 

 
