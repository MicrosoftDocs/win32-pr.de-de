---
description: Löscht den Container für den privaten Schlüssel, auf den vom PrivateKey-Objekt verwiesen wird.
ms.assetid: 80bbe46b-1ec5-4d47-82b0-5a3177f86389
title: PrivateKey. Delete-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.Delete
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: dc5778e631abba9eb8cf122ddb99a4692c988f4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370585"
---
# <a name="privatekeydelete-method"></a><span data-ttu-id="a0d0b-103">PrivateKey. Delete-Methode</span><span class="sxs-lookup"><span data-stu-id="a0d0b-103">PrivateKey.Delete method</span></span>

<span data-ttu-id="a0d0b-104">\[Die **Delete** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="a0d0b-104">\[The **Delete** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a0d0b-105">Verwenden Sie stattdessen die [**X509Certificate2. PrivateKey-Eigenschaft**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="a0d0b-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="a0d0b-106">Die **Delete** -Methode löscht den Container für den privaten Schlüssel, auf den vom [**PrivateKey**](privatekey.md) -Objekt verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="a0d0b-106">The **Delete** method deletes the private key container referenced by the [**PrivateKey**](privatekey.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0d0b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0d0b-107">Syntax</span></span>


```VB
PrivateKey.Delete()
```



## <a name="parameters"></a><span data-ttu-id="a0d0b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0d0b-108">Parameters</span></span>

<span data-ttu-id="a0d0b-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="a0d0b-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a0d0b-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a0d0b-110">Return value</span></span>

<span data-ttu-id="a0d0b-111">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a0d0b-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0d0b-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a0d0b-112">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a0d0b-113">Diese Methode löscht den Container für den privaten Schlüssel, auf den vom [**PrivateKey**](privatekey.md) -Objekt und allen privaten Schlüsseln im Container verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="a0d0b-113">This method deletes the private key container referenced by the [**PrivateKey**](privatekey.md) object as well as all private keys in the container.</span></span> <span data-ttu-id="a0d0b-114">Alle Elemente, die mit den öffentlichen Schlüsseln verschlüsselt werden, die den gelöschten privaten Schlüsseln entsprechen, können nicht mehr entschlüsselt werden.</span><span class="sxs-lookup"><span data-stu-id="a0d0b-114">Anything encrypted using the public keys corresponding to the deleted private keys will no longer be able to be decrypted.</span></span>

 

<span data-ttu-id="a0d0b-115">Diese Methode löst CAPICOM \_ E \_ nicht \_ zulässig aus, wenn eine Skripterstellung aus einer webbasierten Anwendung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="a0d0b-115">This method raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0d0b-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a0d0b-116">Requirements</span></span>



| <span data-ttu-id="a0d0b-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a0d0b-117">Requirement</span></span> | <span data-ttu-id="a0d0b-118">Wert</span><span class="sxs-lookup"><span data-stu-id="a0d0b-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0d0b-119">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="a0d0b-119">Redistributable</span></span><br/> | <span data-ttu-id="a0d0b-120">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="a0d0b-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a0d0b-121">DLL</span><span class="sxs-lookup"><span data-stu-id="a0d0b-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="a0d0b-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0d0b-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
