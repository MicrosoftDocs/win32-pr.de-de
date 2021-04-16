---
description: Die folgenden Funktionen sind unter den CryptoAPI-Funktionen, die erweitert werden können.
ms.assetid: eb4c1352-1432-4f45-a309-fa17b694a35e
title: Erstellen der neuen Funktionalität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d660c14e99247c7d17f57100858b104d1cbcc9ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525736"
---
# <a name="creating-the-new-functionality"></a><span data-ttu-id="7d0aa-103">Erstellen der neuen Funktionalität</span><span class="sxs-lookup"><span data-stu-id="7d0aa-103">Creating the New Functionality</span></span>

<span data-ttu-id="7d0aa-104">Die folgenden Funktionen sind unter den CryptoAPI-Funktionen, die erweitert werden können.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-104">The following functions are among the CryptoAPI functions that can be extended.</span></span>



| <span data-ttu-id="7d0aa-105">CryptoAPI-Funktion</span><span class="sxs-lookup"><span data-stu-id="7d0aa-105">CryptoAPI function</span></span>                                   | <span data-ttu-id="7d0aa-106">OID-Funktionsname definieren</span><span class="sxs-lookup"><span data-stu-id="7d0aa-106">OID function name define</span></span>                         | <span data-ttu-id="7d0aa-107">Name der OID-Funktionsname</span><span class="sxs-lookup"><span data-stu-id="7d0aa-107">OID function name string</span></span>  |
|------------------------------------------------------|--------------------------------------------------|---------------------------|
| [<span data-ttu-id="7d0aa-108">**Bei cryptencodeobject**</span><span class="sxs-lookup"><span data-stu-id="7d0aa-108">**CryptEncodeObject**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject)       | <span data-ttu-id="7d0aa-109">Crypt \_ OID-codiercodierungsobjekt \_ \_ \_ Func</span><span class="sxs-lookup"><span data-stu-id="7d0aa-109">CRYPT\_OID\_ENCODE\_ OBJECT\_FUNC</span></span><br/>     | <span data-ttu-id="7d0aa-110">"Cryptdllencodebug Object"</span><span class="sxs-lookup"><span data-stu-id="7d0aa-110">"CryptDllEncodeObject"</span></span>    |
| [<span data-ttu-id="7d0aa-111">**Cryptdecodeobject**</span><span class="sxs-lookup"><span data-stu-id="7d0aa-111">**CryptDecodeObject**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject)       | <span data-ttu-id="7d0aa-112">Crypt- \_ OID- \_ Decodieren von Objekten ( \_ \_ Func)</span><span class="sxs-lookup"><span data-stu-id="7d0aa-112">CRYPT\_OID\_DECODE\_ OBJECT\_FUNC</span></span><br/>     | <span data-ttu-id="7d0aa-113">"Cryptdlldecodeobject"</span><span class="sxs-lookup"><span data-stu-id="7d0aa-113">"CryptDllDecodeObject"</span></span>    |
| [<span data-ttu-id="7d0aa-114">**CertOpenStore übergebene**</span><span class="sxs-lookup"><span data-stu-id="7d0aa-114">**CertOpenStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)               | <span data-ttu-id="7d0aa-115">Crypt \_ OID \_ Open \_ Store \_ Prov \_ Func</span><span class="sxs-lookup"><span data-stu-id="7d0aa-115">CRYPT\_OID\_OPEN\_ STORE\_PROV\_FUNC</span></span><br/>  | <span data-ttu-id="7d0aa-116">"Certdllopenstoreprov"</span><span class="sxs-lookup"><span data-stu-id="7d0aa-116">"CertDllOpenStoreProv"</span></span>    |
| [<span data-ttu-id="7d0aa-117">**Certverifyctlusage**</span><span class="sxs-lookup"><span data-stu-id="7d0aa-117">**CertVerifyCTLUsage**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyctlusage)     | <span data-ttu-id="7d0aa-118">Crypt \_ OID \_ Verify \_ CTL \_ Usage \_ Func</span><span class="sxs-lookup"><span data-stu-id="7d0aa-118">CRYPT\_OID\_VERIFY\_ CTL\_USAGE\_FUNC</span></span><br/> | <span data-ttu-id="7d0aa-119">"Certdllverifyctlusage"</span><span class="sxs-lookup"><span data-stu-id="7d0aa-119">"CertDllVerifyCTLUsage"</span></span>   |
| [<span data-ttu-id="7d0aa-120">**Certverifywiderruf**</span><span class="sxs-lookup"><span data-stu-id="7d0aa-120">**CertVerifyRevocation**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyrevocation) | <span data-ttu-id="7d0aa-121">Sperr \_ Funktion der Crypt OID- \_ Überprüfung \_ \_</span><span class="sxs-lookup"><span data-stu-id="7d0aa-121">CRYPT\_OID\_VERIFY\_ REVOCATION\_FUNC</span></span><br/> | <span data-ttu-id="7d0aa-122">"Certdllverifywiderruf"</span><span class="sxs-lookup"><span data-stu-id="7d0aa-122">"CertDllVerifyRevocation"</span></span> |



 

<span data-ttu-id="7d0aa-123">Bei normaler Verwendung mit einer vorhandenen OID und einem Codierungstyp wird der Code in der CryptoAPI-Funktion selbst verwendet.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-123">In normal use with an existing OID and encoding type, the code in the CryptoAPI function, itself, is used.</span></span> <span data-ttu-id="7d0aa-124">Wenn eine dieser Funktionen mit einer OID und einem Codierungstyp aufgerufen wird, den Code in der CryptoAPI-Funktion nicht verarbeiten konnte, muss eine neue Funktion, die die neue Funktionalität enthält, in einer DLL erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-124">If one of these functions is called with an OID and encoding type that code in the CryptoAPI function was not designed to handle, a new function, containing the new functionality, must be created in a DLL.</span></span> <span data-ttu-id="7d0aa-125">Diese DLL muss in der Registrierung registriert oder im Arbeitsspeicher installiert sein.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-125">That DLL must be registered in the registry or installed in memory.</span></span>

<span data-ttu-id="7d0aa-126">Wenn eine der aufgelisteten Funktionen mit der neu bezeichneten OID und dem Codierungstyp aufgerufen wird, wird der Code in der neuen dll anstelle des Codes verwendet, der als Teil der CryptoAPI-Funktion bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-126">When one of the listed functions is called with the newly designated OID and encoding type, the code in the new DLL is used rather than the code provided as part of the CryptoAPI function.</span></span>

<span data-ttu-id="7d0aa-127">Der Name der neu entwickelten Funktion kann der Name sein, der unter "OID Function Name String" in der vorherigen Tabelle aufgeführt ist, oder es kann ein anderer Name angegeben werden, wenn der neue Funktionscode registriert wird.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-127">The name of the newly developed function can be the name listed under "OID function name string" in the previous table or a different name can be given when the new function code is registered.</span></span>

<span data-ttu-id="7d0aa-128">Die neue Funktion muss einen geeigneten Prototyp verwenden.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-128">The new function must use an appropriate prototype.</span></span> <span data-ttu-id="7d0aa-129">In allen Fällen mit Ausnahme von [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)ist dieser Prototyp identisch mit der CryptoAPI-Funktion, die die neue Funktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-129">In all cases except for [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore), this prototype is the same as the CryptoAPI function that calls the new function.</span></span> <span data-ttu-id="7d0aa-130">Im Fall von **certopeinstore** lautet der Prototyp wie folgt.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-130">In the case of **CertOpenStore** the prototype is as follows.</span></span>


```C++
#include <windows.h>

BOOL WINAPI CertDllOpenStoreProv(
  IN LPCSTR lpszStoreProvider,
  IN DWORD dwEncodingType,
  IN HCRYPTPROV hCryptProv,
  IN DWORD dwFlags,
  IN const void *pvPara,
  IN HCERTSTORE hCertStore,
  IN OUT PCERT_STORE_PROV_INFO pStoreProvInfo
);
```



> [!Note]  
> <span data-ttu-id="7d0aa-131">Wenn die Prototypen nicht identisch sind, wird der System Stapel beschädigt.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-131">If the prototypes do not match, the system stack will be corrupted.</span></span>

 

<span data-ttu-id="7d0aa-132">Zusätzlich zur Bereitstellung des Codes für die neue Funktion in einer DLL erfordert die Erweiterung der Funktionalität von " [**cryptencodeobject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) " oder " [**cryptdecodeobject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) " eine Typdefinition für die neue C-Datenstruktur, die in eine Header Datei eingefügt werden muss, wenn das Programm des Benutzers kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-132">In addition to providing the code for the new function in a DLL, extending the functionality of [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) or [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) requires a type definition for the new C data structure to be placed in a header file included when the user's program is compiled.</span></span>

 

 




