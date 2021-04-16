---
description: Überprüfen Sie die Signatur der CTL bei jeder Verwendung der CTL, damit ein interloper-CTL (Certificate Trust List, CTL) eine vorhandene CTL-Datei nicht ersetzen kann.
ms.assetid: 24ba6955-f6d1-4123-ab39-50385f6e03a0
title: Überprüfen einer CTL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac88362c96d5b419a7c16731e31456b569079d7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527614"
---
# <a name="verifying-a-ctl"></a><span data-ttu-id="75059-103">Überprüfen einer CTL</span><span class="sxs-lookup"><span data-stu-id="75059-103">Verifying a CTL</span></span>

<span data-ttu-id="75059-104">Überprüfen Sie die Signatur der CTL bei jeder Verwendung der CTL, damit ein interloper-CTL ( [*Certificate Trust List*](../secgloss/c-gly.md) , CTL) eine vorhandene CTL-Datei nicht ersetzen kann.</span><span class="sxs-lookup"><span data-stu-id="75059-104">To make it more difficult for an interloper to substitute a bogus [*certificate trust list*](../secgloss/c-gly.md) (CTL) for an existing one, verify the signature on the CTL each time the CTL is used.</span></span> <span data-ttu-id="75059-105">Verwenden Sie keine CTL, die keine vertrauenswürdige Signatur enthält.</span><span class="sxs-lookup"><span data-stu-id="75059-105">Do not use a CTL that does not contain a trusted signature.</span></span>

<span data-ttu-id="75059-106">**So überprüfen Sie eine CTL-Signatur**</span><span class="sxs-lookup"><span data-stu-id="75059-106">**To verify a CTL signature**</span></span>

1.  <span data-ttu-id="75059-107">Öffnen Sie den [*Zertifikat Speicher*](../secgloss/c-gly.md) , der die gewünschte CTL enthält.</span><span class="sxs-lookup"><span data-stu-id="75059-107">Open the [*certificate store*](../secgloss/c-gly.md) containing the desired CTL.</span></span>
2.  <span data-ttu-id="75059-108">Erhalten Sie ein Handle für einen [**CTL- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) für die CTL.</span><span class="sxs-lookup"><span data-stu-id="75059-108">Get a handle to a [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) for the CTL.</span></span> <span data-ttu-id="75059-109">Dies kann durch Aufrufen einer der Funktionen erfolgen, die ein Handle für den **CTL- \_ Kontext** zurückgeben, z. [**b. certfindctlinstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore).</span><span class="sxs-lookup"><span data-stu-id="75059-109">This can be done by calling any of the functions that return a handle to the **CTL\_CONTEXT**, such as [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore).</span></span>
3.  <span data-ttu-id="75059-110">Nennen Sie [**cryptmsggetandverifysigner**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetandverifysigner), und übergeben Sie dabei den in Schritt 2 des Parameters " *hcryptmsg* " abgerufenen [**CTL- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) , ein Handle für den Zertifikat Speicher, das das Zertifikat der vertrauenswürdigen Quelle für CTLs im *rghsignerstore* -Parameter enthält, und das Flag "CMSG \_ Trusted \_ Signer" \_ im *dwFlags* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="75059-110">Call [**CryptMsgGetAndVerifySigner**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetandverifysigner), passing the [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) retrieved in step 2 in the *hCryptMsg* parameter, a handle to the certificate store containing the certificate of the trusted source for CTLs in the *rghSignerStore* parameter, and the CMSG\_TRUSTED\_SIGNER\_FLAG in the *dwFlags* parameter.</span></span> <span data-ttu-id="75059-111">Wenn die Funktion " **true**" zurückgibt, wurde die Signatur überprüft, und ein Zeiger auf den [**pccert- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) des CTL-Signatur Gebers wird im Parameter " *ppsigner* " zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="75059-111">If the function returns **TRUE**, the signature was verified, and a pointer to the CTL signer's [**PCCERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) is returned in the *ppSigner* parameter.</span></span>

 

 
