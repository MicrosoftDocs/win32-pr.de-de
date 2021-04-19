---
description: Lädt ein Signaturzertifikat aus einer angegebenen PFX-Datei.
ms.assetid: 98963354-c237-40d0-9235-8318728e2c8e
title: Signer. Load-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer.Load
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9a817a95ca825b67b54a41fc674db10bf81b5740
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372612"
---
# <a name="signerload-method"></a><span data-ttu-id="71dee-103">Signer. Load-Methode</span><span class="sxs-lookup"><span data-stu-id="71dee-103">Signer.Load method</span></span>

<span data-ttu-id="71dee-104">\[Die **Load** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="71dee-104">\[The **Load** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="71dee-105">Verwenden Sie stattdessen die [**CmsSigner-Klasse**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="71dee-105">Instead, use the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="71dee-106">Die **Load** -Methode lädt ein Signaturzertifikat aus einer angegebenen PFX-Datei.</span><span class="sxs-lookup"><span data-stu-id="71dee-106">The **Load** method loads a signing certificate from a specified .pfx file.</span></span>

## <a name="syntax"></a><span data-ttu-id="71dee-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="71dee-107">Syntax</span></span>


```VB
Signer.Load( _
  ByVal FileName, _
  [ ByVal Password ] _
)
```



## <a name="parameters"></a><span data-ttu-id="71dee-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="71dee-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71dee-109">*FileName*</span><span class="sxs-lookup"><span data-stu-id="71dee-109">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="71dee-110">Der Name der PFX-Datei, die das Signaturzertifikat enthält.</span><span class="sxs-lookup"><span data-stu-id="71dee-110">Name of the .pfx file that contains the signing certificate.</span></span>

</dd> <dt>

<span data-ttu-id="71dee-111">*Kennwort* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="71dee-111">*Password* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="71dee-112">Zeichenfolge, die das Klartext-Kennwort enthält, das zum Öffnen der Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="71dee-112">String containing the plaintext password used to open the file.</span></span> <span data-ttu-id="71dee-113">Bis zu 32 Unicode-Zeichen, einschließlich eines abschließenden NULL-Zeichens, können für das Kennwort verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="71dee-113">Up to 32 Unicode characters, including a terminating null character, can be used for the password.</span></span> <span data-ttu-id="71dee-114">Der Standardwert ist eine leere Zeichenfolge ("").</span><span class="sxs-lookup"><span data-stu-id="71dee-114">The default value is an empty string ("").</span></span> <span data-ttu-id="71dee-115">Informationen zum Schützen des Kennworts finden Sie unter Behandeln von Kenn [Wörtern](../secbp/handling-passwords.md).</span><span class="sxs-lookup"><span data-stu-id="71dee-115">For information about protecting the password, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71dee-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="71dee-116">Return value</span></span>

<span data-ttu-id="71dee-117">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="71dee-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="71dee-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="71dee-118">Remarks</span></span>

<span data-ttu-id="71dee-119">Diese Methode lädt das erste Zertifikat in der PFX-Datei, der ein privater Schlüssel zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="71dee-119">This method loads the first certificate in the .pfx file that has a private key associated with it.</span></span>

<span data-ttu-id="71dee-120">Diese Methode löst CAPICOM \_ E \_ nicht \_ zulässig aus, wenn eine Skripterstellung aus einer webbasierten Anwendung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="71dee-120">This method raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

## <a name="requirements"></a><span data-ttu-id="71dee-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="71dee-121">Requirements</span></span>



| <span data-ttu-id="71dee-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="71dee-122">Requirement</span></span> | <span data-ttu-id="71dee-123">Wert</span><span class="sxs-lookup"><span data-stu-id="71dee-123">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="71dee-124">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="71dee-124">Redistributable</span></span><br/> | <span data-ttu-id="71dee-125">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="71dee-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="71dee-126">DLL</span><span class="sxs-lookup"><span data-stu-id="71dee-126">DLL</span></span><br/>             | <dl> <span data-ttu-id="71dee-127"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71dee-127"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71dee-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71dee-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71dee-129">**Signatur Geber**</span><span class="sxs-lookup"><span data-stu-id="71dee-129">**Signer**</span></span>](signer.md)
</dt> </dl>

 

 
