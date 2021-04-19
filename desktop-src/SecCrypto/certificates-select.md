---
description: Zeigt ein Dialogfeld für die Auswahl von Zertifikaten an und gibt eine Sammlung der ausgewählten Zertifikate zurück.
ms.assetid: dbf49a4b-6da1-4819-afcd-46db89a00fce
title: 'ICertificates2:: Select-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Select
- ICertificates2.Select
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: cfd5b1cb5e269c14e05de25262fda711549bf02d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362141"
---
# <a name="icertificates2select-method"></a><span data-ttu-id="434eb-103">ICertificates2:: Select-Methode</span><span class="sxs-lookup"><span data-stu-id="434eb-103">ICertificates2::Select method</span></span>

<span data-ttu-id="434eb-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="434eb-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="434eb-105">Verwenden Sie stattdessen die [**X509Certificate2Collection-Klasse**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="434eb-105">Instead, use the [**X509Certificate2Collection Class**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="434eb-106">Die **Select** -Methode zeigt ein Dialogfeld für die Auswahl von Zertifikaten an und gibt eine Sammlung der ausgewählten Zertifikate zurück.</span><span class="sxs-lookup"><span data-stu-id="434eb-106">The **Select** method displays a dialog box for selecting certificates and returns a collection of those certificates selected.</span></span> <span data-ttu-id="434eb-107">Diese Methode wurde in CAPICOM 2,0 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="434eb-107">This method was introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="434eb-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="434eb-108">Syntax</span></span>


```VB
Certificates.Select( _
  [ ByVal Title ], _
  [ ByVal DisplayString ], _
  [ ByVal bMultiSelect ] _
)
```



## <a name="parameters"></a><span data-ttu-id="434eb-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="434eb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="434eb-110">*Titel* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="434eb-110">*Title* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="434eb-111">Eine Zeichenfolge, die den Titel für das Dialogfeld enthält.</span><span class="sxs-lookup"><span data-stu-id="434eb-111">String that contains the title for the dialog box.</span></span> <span data-ttu-id="434eb-112">Der Standardwert ist eine leere Zeichenfolge ("").</span><span class="sxs-lookup"><span data-stu-id="434eb-112">The default value is an empty string ("").</span></span>

</dd> <dt>

<span data-ttu-id="434eb-113">*Display String* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="434eb-113">*DisplayString* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="434eb-114">Eine Zeichenfolge, die den im Dialogfeld angezeigten Eingabe Aufforderungs Text enthält.</span><span class="sxs-lookup"><span data-stu-id="434eb-114">String that contains the prompt text displayed with the dialog box.</span></span> <span data-ttu-id="434eb-115">Der Standardwert ist eine leere Zeichenfolge ("").</span><span class="sxs-lookup"><span data-stu-id="434eb-115">The default value is an empty string ("").</span></span>

</dd> <dt>

<span data-ttu-id="434eb-116">*bmultiselect* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="434eb-116">*bMultiSelect* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="434eb-117">Boolescher Wert, der angibt, ob der Benutzer mehr als ein Zertifikat auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="434eb-117">Boolean value that indicates whether the user can select more than one certificate.</span></span> <span data-ttu-id="434eb-118">True gibt an, dass mehrere Zertifikate mithilfe der STRG-oder der Umschalttaste ausgewählt werden können.</span><span class="sxs-lookup"><span data-stu-id="434eb-118">True indicates multiple certificates can be selected by using the CTRL or SHIFT key.</span></span> <span data-ttu-id="434eb-119">Der Standardwert ist „FALSE“.</span><span class="sxs-lookup"><span data-stu-id="434eb-119">The default value is false.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="434eb-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="434eb-120">Return value</span></span>

<span data-ttu-id="434eb-121">Ein [**Zertifikat**](certificates.md) Objekt, das die im Dialogfeld ausgewählten Zertifikate enthält.</span><span class="sxs-lookup"><span data-stu-id="434eb-121">A [**Certificates**](certificates.md) object that contains the certificates selected from the dialog box.</span></span>

<span data-ttu-id="434eb-122">**CAPICOM 2,1:** Das [**Zertifikat**](certificates.md) Objekt, das zurückgegeben wird, enthält Verweise auf die Zertifikate in der Sammlung, von der aus die Auswahl getroffen wurde.</span><span class="sxs-lookup"><span data-stu-id="434eb-122">**CAPICOM 2.1:** The [**Certificates**](certificates.md) object that is returned contains references to the certificates in the collection from which the selection was made.</span></span> <span data-ttu-id="434eb-123">Alle Änderungen, die an den Zertifikaten im zurückgegebenen **Zertifikat** Objekt vorgenommen werden, werden in dieser Sammlung widergespiegelt.</span><span class="sxs-lookup"><span data-stu-id="434eb-123">Any changes made to the certificates in the returned **Certificates** object are reflected in that collection.</span></span>

<span data-ttu-id="434eb-124">**CAPICOM 2,0, CAPICOM 2.0.0.1, CAPICOM 2.0.0.2 und CAPICOM 2.0.0.3:** Das [**Zertifikat**](certificates.md) Objekt, das zurückgegeben wird, enthält Kopien der Zertifikate in der Sammlung, aus der die Auswahl stammt.</span><span class="sxs-lookup"><span data-stu-id="434eb-124">**CAPICOM 2.0, CAPICOM 2.0.0.1, CAPICOM 2.0.0.2, and CAPICOM 2.0.0.3:** The [**Certificates**](certificates.md) object that is returned contains copies of the certificates in the collection from which the selection was made.</span></span> <span data-ttu-id="434eb-125">Alle Änderungen, die an den Zertifikaten im zurückgegebenen **Zertifikat** Objekt vorgenommen werden, werden in dieser Sammlung nicht widergespiegelt.</span><span class="sxs-lookup"><span data-stu-id="434eb-125">Any changes made to the certificates in the returned **Certificates** object are not reflected in that collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="434eb-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="434eb-126">Requirements</span></span>



| <span data-ttu-id="434eb-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="434eb-127">Requirement</span></span> | <span data-ttu-id="434eb-128">Wert</span><span class="sxs-lookup"><span data-stu-id="434eb-128">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="434eb-129">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="434eb-129">End of client support</span></span><br/> | <span data-ttu-id="434eb-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="434eb-130">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="434eb-131">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="434eb-131">End of server support</span></span><br/> | <span data-ttu-id="434eb-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="434eb-132">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="434eb-133">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="434eb-133">Redistributable</span></span><br/>       | <span data-ttu-id="434eb-134">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="434eb-134">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="434eb-135">DLL</span><span class="sxs-lookup"><span data-stu-id="434eb-135">DLL</span></span><br/>                   | <dl> <span data-ttu-id="434eb-136"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="434eb-136"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
