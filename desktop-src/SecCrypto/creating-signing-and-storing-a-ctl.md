---
description: Erstellen Sie eine signierte Zertifikats Vertrauens Liste (CTL), und speichern Sie Sie in einem Zertifikat Speicher.
ms.assetid: 82d75d60-2343-413c-ba53-ccee02d1ad41
title: Erstellen, Signieren und Speichern einer CTL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2da66ce5acb882d36451118700178519455a4ded
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356729"
---
# <a name="creating-signing-and-storing-a-ctl"></a><span data-ttu-id="11d93-103">Erstellen, Signieren und Speichern einer CTL</span><span class="sxs-lookup"><span data-stu-id="11d93-103">Creating, Signing, and Storing a CTL</span></span>

<span data-ttu-id="11d93-104">In den folgenden Verfahren wird eine signierte [*Zertifikats Vertrauens Liste (Certificate Trust List*](../secgloss/c-gly.md) , CTL) erstellt und in einem [*Zertifikat Speicher*](../secgloss/c-gly.md)gespeichert.</span><span class="sxs-lookup"><span data-stu-id="11d93-104">The following procedures create a signed [*certificate trust list*](../secgloss/c-gly.md) (CTL) and save it to a [*certificate store*](../secgloss/c-gly.md).</span></span>

<span data-ttu-id="11d93-105">**So erstellen und Signieren Sie eine CTL**</span><span class="sxs-lookup"><span data-stu-id="11d93-105">**To create and sign a CTL**</span></span>

1.  <span data-ttu-id="11d93-106">Erstellen Sie ein Array von Elementen, die in der [*CTL*](../secgloss/c-gly.md)gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="11d93-106">Create an array of items to be stored in the [*CTL*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="11d93-107">Im Fall vertrauenswürdiger Zertifikate müssen dies die SHA1-oder MD5-Hashwerte der vertrauenswürdigen Zertifikate sein.</span><span class="sxs-lookup"><span data-stu-id="11d93-107">In the case of trusted certificates, this must be the SHA1 or MD5 hashes of the trusted certificates.</span></span>
2.  <span data-ttu-id="11d93-108">Initialisieren Sie eine [**CTL- \_ Informations**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_info) Struktur, die das Array der soeben erstellten Elemente einschließt.</span><span class="sxs-lookup"><span data-stu-id="11d93-108">Initialize a [**CTL\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_info) structure that includes the array of items just created.</span></span>
3.  <span data-ttu-id="11d93-109">Initialisieren Sie eine [**CMSG- \_ signierte \_ \_ Informations**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info) Struktur mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="11d93-109">Initialize a [**CMSG\_SIGNED\_ENCODE\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info) structure.</span></span>
4.  <span data-ttu-id="11d93-110">Nennen Sie [**cryptmsgencodeandsignctl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgencodeandsignctl).</span><span class="sxs-lookup"><span data-stu-id="11d93-110">Call [**CryptMsgEncodeAndSignCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgencodeandsignctl).</span></span> <span data-ttu-id="11d93-111">Dieser Funktions aufrub gibt einen Zeiger auf eine signierte, codierte CTL (im PKCS \# 7-Format) zurück, die die Liste der in Schritt 1 erstellten Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="11d93-111">This function call returns a pointer to a signed, encoded CTL (in PKCS \#7 format) that contains the list of items created in step 1.</span></span>

<span data-ttu-id="11d93-112">**So fügen Sie einem Zertifikat Speicher eine CTL hinzu**</span><span class="sxs-lookup"><span data-stu-id="11d93-112">**To add a CTL to a certificate store**</span></span>

1.  <span data-ttu-id="11d93-113">Einen Zeiger auf eine signierte und codierte CTL erhalten.</span><span class="sxs-lookup"><span data-stu-id="11d93-113">Get a pointer to a signed and encoded CTL.</span></span>
2.  <span data-ttu-id="11d93-114">Öffnen Sie den Ziel Zertifikat Speicher mit einem [**certopesstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)-Rückruf.</span><span class="sxs-lookup"><span data-stu-id="11d93-114">Open the target certificate store with a call to [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore).</span></span>
3.  <span data-ttu-id="11d93-115">Nennen Sie [**certaddencodedctldestore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedctltostore).</span><span class="sxs-lookup"><span data-stu-id="11d93-115">Call [**CertAddEncodedCTLToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedctltostore).</span></span>

 

 
