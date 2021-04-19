---
description: Die folgenden Datentypen werden von Kryptografiefunktionen, Schnittstellen und Objekten verwendet.
ms.assetid: 9d6a065d-c765-4d17-9f4c-38a984439278
title: Kryptografiedatentypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f84c6f21faa25e1ccc478c178a3f21458ff589ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348149"
---
# <a name="cryptography-data-types"></a><span data-ttu-id="22aa0-103">Kryptografiedatentypen</span><span class="sxs-lookup"><span data-stu-id="22aa0-103">Cryptography Data Types</span></span>

<span data-ttu-id="22aa0-104">Die folgenden Datentypen werden von Kryptografiefunktionen, Schnittstellen und Objekten verwendet.</span><span class="sxs-lookup"><span data-stu-id="22aa0-104">The following data types are used by cryptography functions, interfaces, and objects.</span></span>



| <span data-ttu-id="22aa0-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="22aa0-105">Data type</span></span>                                                                      | <span data-ttu-id="22aa0-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="22aa0-106">Description</span></span>                                                                                                                                                                                      |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="22aa0-107">**ALG- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="22aa0-107">**ALG\_ID**</span></span>](alg-id.md)                                                      | <span data-ttu-id="22aa0-108">Gibt Algorithmusbezeichner an.</span><span class="sxs-lookup"><span data-stu-id="22aa0-108">Specifies algorithm identifiers.</span></span>                                                                                                                                                                 |
| [<span data-ttu-id="22aa0-109">**hcert- \_ Server- \_ OCSP- \_ Antwort**</span><span class="sxs-lookup"><span data-stu-id="22aa0-109">**HCERT\_SERVER\_OCSP\_RESPONSE**</span></span>](hcert-server-ocsp-response.md)            | <span data-ttu-id="22aa0-110">Stellt ein Handle für eine OCSP-Antwort dar, die einer Serverzertifikat Kette zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="22aa0-110">Represents a handle to an OCSP response associated with a server certificate chain.</span></span>                                                                                                              |
| [<span data-ttu-id="22aa0-111">**Hcrypthash**</span><span class="sxs-lookup"><span data-stu-id="22aa0-111">**HCRYPTHASH**</span></span>](hcrypthash.md)                                               | <span data-ttu-id="22aa0-112">Gibt Handles für ein [*Hash Objekt*](../secgloss/h-gly.md)an.</span><span class="sxs-lookup"><span data-stu-id="22aa0-112">Specifies handles to a [*hash object*](../secgloss/h-gly.md).</span></span>                                                                                      |
| [<span data-ttu-id="22aa0-113">**Hcryptkey**</span><span class="sxs-lookup"><span data-stu-id="22aa0-113">**HCRYPTKEY**</span></span>](hcryptkey.md)                                                 | <span data-ttu-id="22aa0-114">Gibt Handles für kryptografische Schlüssel an.</span><span class="sxs-lookup"><span data-stu-id="22aa0-114">Specifies handles to cryptographic keys.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="22aa0-115">**Hcryptoidfuncaddr**</span><span class="sxs-lookup"><span data-stu-id="22aa0-115">**HCRYPTOIDFUNCADDR**</span></span>](hcryptoidfuncaddr.md)                                 | <span data-ttu-id="22aa0-116">Stellt ein Handle für eine Funktion dar, die mithilfe eines [*Objekt Bezeichners*](../secgloss/o-gly.md) (OID) installiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="22aa0-116">Represents a handle to a function that can be installed by using an [*object identifier*](../secgloss/o-gly.md) (OID).</span></span>                 |
| [<span data-ttu-id="22aa0-117">**Hcryptoidfuncset**</span><span class="sxs-lookup"><span data-stu-id="22aa0-117">**HCRYPTOIDFUNCSET**</span></span>](hcryptoidfuncset.md)                                   | <span data-ttu-id="22aa0-118">Stellt ein Handle für eine Reihe von Funktionen dar, die mithilfe einer OID installiert werden können.</span><span class="sxs-lookup"><span data-stu-id="22aa0-118">Represents a handle to a set of functions that can be installed by using an OID.</span></span>                                                                                                                 |
| [<span data-ttu-id="22aa0-119">**hcryptprov- \_ Legacy**</span><span class="sxs-lookup"><span data-stu-id="22aa0-119">**HCRYPTPROV\_LEGACY**</span></span>](hcryptprov-legacy.md)                                | <span data-ttu-id="22aa0-120">Wird zum Ersetzen des [**hcryptprov**](hcryptprov.md) -Datentyps verwendet, bei dem der **hcryptprov** -Datentyp nicht mehr verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="22aa0-120">Used to replace the [**HCRYPTPROV**](hcryptprov.md) data type where the **HCRYPTPROV** data type is no longer used.</span></span>                                                                             |
| [<span data-ttu-id="22aa0-121">**hcryptprov- \_ oder \_ NCrypt- \_ Schlüssel \_ handle**</span><span class="sxs-lookup"><span data-stu-id="22aa0-121">**HCRYPTPROV\_OR\_NCRYPT\_KEY\_HANDLE**</span></span>](hcryptprov-or-ncrypt-key-handle.md) | <span data-ttu-id="22aa0-122">Gibt ein Handle für einen [*Kryptografiedienstanbieter (kryptografischen Service Provider*](../secgloss/c-gly.md) , CSP) oder CNG-CSP an.</span><span class="sxs-lookup"><span data-stu-id="22aa0-122">Specifies a handle to a CryptoAPI [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) or CNG CSP.</span></span> |
| [<span data-ttu-id="22aa0-123">**Hcryptprov**</span><span class="sxs-lookup"><span data-stu-id="22aa0-123">**HCRYPTPROV**</span></span>](hcryptprov.md)                                               | <span data-ttu-id="22aa0-124">Gibt ein Handle für einen CryptoAPI-CSP an.</span><span class="sxs-lookup"><span data-stu-id="22aa0-124">Specifies a handle to a CryptoAPI CSP.</span></span>                                                                                                                                                           |
| [<span data-ttu-id="22aa0-125">**keysvcc- \_ handle**</span><span class="sxs-lookup"><span data-stu-id="22aa0-125">**KEYSVCC\_HANDLE**</span></span>](keysvcc-handle.md)                                      | <span data-ttu-id="22aa0-126">Gibt Handles für den Schlüsseldienst an.</span><span class="sxs-lookup"><span data-stu-id="22aa0-126">Specifies handles to the key service.</span></span>                                                                                                                                                            |



 

 

 
