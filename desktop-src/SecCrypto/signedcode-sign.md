---
description: Erstellt eine digitale Authenticode-Signatur und signiert die ausführbare Datei, die in der signedcode. FileName-Eigenschaft angegeben ist.
ms.assetid: db17be29-35ec-4468-b5cc-5ba64c4cf3fb
title: Signedcode. Sign-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Sign
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 36e5c813b997ae452d44764ed88f51b273c75528
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362050"
---
# <a name="signedcodesign-method"></a><span data-ttu-id="315bb-103">Signedcode. Sign-Methode</span><span class="sxs-lookup"><span data-stu-id="315bb-103">SignedCode.Sign method</span></span>

<span data-ttu-id="315bb-104">\[Die **Sign** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="315bb-104">\[The **Sign** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="315bb-105">Verwenden Sie stattdessen den Platform invoations Dienst (PInvoke) zum Aufrufen der Win32-API [**signersignetx**](signersignex.md)-, [**signertimestampex**](signertimestampex.md)-und [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) -Funktionen, um Inhalte mit einer digitalen Authenticode-Signatur zu signieren.</span><span class="sxs-lookup"><span data-stu-id="315bb-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="315bb-106">Weitere Informationen zu PInvoke finden Sie unter [Tutorial zum Platt Form Aufruf](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="315bb-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="315bb-107">Die [.net-und CryptoAPI über p/aufrufen: Teil 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) und [.net und CryptoAPI über p/aufrufen: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) Unterabschnitte der [Erweiterung von .net-Kryptografie mit CAPICOM und p/aufrufen](/previous-versions/ms867087(v=msdn.10)) können ebenfalls hilfreich sein.\]</span><span class="sxs-lookup"><span data-stu-id="315bb-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="315bb-108">Die **Sign** -Methode erstellt eine digitale Authenticode-Signatur und signiert die ausführbare Datei, die in der [**signedcode. filename**](signedcode-filename.md) -Eigenschaft angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="315bb-108">The **Sign** method creates an Authenticode digital signature and signs the executable file specified in the [**SignedCode.FileName**](signedcode-filename.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="315bb-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="315bb-109">Syntax</span></span>


```VB
SignedCode.Sign( _
  [ ByVal Signer ] _
)
```



## <a name="parameters"></a><span data-ttu-id="315bb-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="315bb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="315bb-111">*Signatur Geber* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="315bb-111">*Signer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="315bb-112">Ein [**Signatur**](signer.md) Geber Objekt, das Zugriff auf den privaten Schlüssel des Zertifikats hat, das zum Signieren des Codes verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="315bb-112">A [**Signer**](signer.md) object that has access to the private key of the certificate used to sign the code.</span></span> <span data-ttu-id="315bb-113">Der Standardwert ist **null**.</span><span class="sxs-lookup"><span data-stu-id="315bb-113">The default value is **Null**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="315bb-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="315bb-114">Return value</span></span>

<span data-ttu-id="315bb-115">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="315bb-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="315bb-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="315bb-116">Remarks</span></span>

<span data-ttu-id="315bb-117">Bevor die **Sign** -Methode aufgerufen wird, muss die Datei, die den Code enthält, in der [**filename**](signedcode-filename.md) -Eigenschaft angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="315bb-117">Before the **Sign** method is called, the file that contains the code must be specified in the [**FileName**](signedcode-filename.md) property.</span></span>

<span data-ttu-id="315bb-118">Wenn die ausführbare Datei bereits signiert ist, überschreibt diese Methode die vorhandene Signatur.</span><span class="sxs-lookup"><span data-stu-id="315bb-118">If the executable file is already signed, this method overwrites the existing signature.</span></span>

<span data-ttu-id="315bb-119">Die folgenden Ergebnisse gelten für den Parameterwert des *Signatur* Gebers:</span><span class="sxs-lookup"><span data-stu-id="315bb-119">The following results apply to the *Signer* parameter value:</span></span>

-   <span data-ttu-id="315bb-120">Wenn der *Signatur* Geber Parameter nicht **null** ist, verwendet diese Methode den privaten Schlüssel, auf den das zugehörige Zertifikat zeigt, um die Signatur zu verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="315bb-120">If the *Signer* parameter is not **NULL**, this method uses the private key pointed to by the associated certificate to encrypt the signature.</span></span> <span data-ttu-id="315bb-121">Wenn der private Schlüssel, auf den vom Zertifikat verwiesen wird, nicht verfügbar ist, schlägt die Methode fehl.</span><span class="sxs-lookup"><span data-stu-id="315bb-121">If the private key pointed to by the certificate is not available, the method fails.</span></span>
-   <span data-ttu-id="315bb-122">Wenn der *Signatur* Geber Parameter **null** ist und im aktuellen \_ Benutzer mein Speicher, der Zugriff auf einen privaten Schlüssel mit Code Signatur Funktion hat, genau ein Zertifikat vorhanden ist, wird dieses Zertifikat zum Erstellen der Signatur verwendet.</span><span class="sxs-lookup"><span data-stu-id="315bb-122">If the *Signer* parameter is **NULL** and there is exactly one certificate in the CURRENT\_USER MY store that has access to a private key with code signing capability, that certificate is used to create the signature.</span></span>
-   <span data-ttu-id="315bb-123">Wenn der *Signatur* Geber Parameter den Wert **null** hat, ist der Wert [**Settings. enablepromptforcertifigateeui**](settings-enablepromptforcertificateui.md) Property true, und es gibt mehrere Zertifikate im aktuellen \_ Benutzer My Store mit einem verfügbaren privaten Schlüssel mit Code Signatur Funktion. Daraufhin wird ein Dialogfeld angezeigt, in dem der Benutzer auswählen kann, welches Zertifikat verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="315bb-123">If the *Signer* parameter is **NULL**, the [**Settings.EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) property value is true, and there is more than one certificate in the CURRENT\_USER MY store with an available private key with code signing capability, a dialog box appears that allows the user to select which certificate is used.</span></span>
-   <span data-ttu-id="315bb-124">Wenn der *Signatur* Geber Parameter den Wert **null** hat und die Eigenschaft [**Settings. enablepromptforcertifigateeui**](settings-enablepromptforcertificateui.md) den Wert false hat, schlägt die Methode fehl.</span><span class="sxs-lookup"><span data-stu-id="315bb-124">If the *Signer* parameter is **NULL** and the [**Settings.EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) property is false, the method fails.</span></span>
-   <span data-ttu-id="315bb-125">Wenn der *Signatur* Geber Parameter **null** ist und im aktuellen \_ Benutzer mein Speicher mit einem verfügbaren privaten Schlüssel mit Code Signatur Funktion keine Zertifikate vorhanden sind, schlägt die Methode fehl.</span><span class="sxs-lookup"><span data-stu-id="315bb-125">If the *Signer* parameter is **NULL** and there are no certificates in the CURRENT\_USER MY store with an available private key with code signing capability, the method fails.</span></span>

<span data-ttu-id="315bb-126">Diese Methode verwendet den SHA-1-Hash Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="315bb-126">This method uses the SHA-1 hashing algorithm.</span></span>

## <a name="requirements"></a><span data-ttu-id="315bb-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="315bb-127">Requirements</span></span>



| <span data-ttu-id="315bb-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="315bb-128">Requirement</span></span> | <span data-ttu-id="315bb-129">Wert</span><span class="sxs-lookup"><span data-stu-id="315bb-129">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="315bb-130">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="315bb-130">Redistributable</span></span><br/> | <span data-ttu-id="315bb-131">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="315bb-131">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="315bb-132">DLL</span><span class="sxs-lookup"><span data-stu-id="315bb-132">DLL</span></span><br/>             | <dl> <span data-ttu-id="315bb-133"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="315bb-133"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
