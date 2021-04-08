---
description: Die folgenden Schnittstellen können verwendet werden, um Zertifikat Signaturen sowie öffentliche und private Schlüssel zu verwalten.
ms.assetid: 628d6629-3ec3-447e-8b60-a2db5b23e780
title: Zertifikat Signatur und Schlüssel Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e35d2f3b1404397b1e6f2e436ef27fb740bbb594
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866671"
---
# <a name="certificate-signature-and-key-interfaces"></a><span data-ttu-id="4bd3a-103">Zertifikat Signatur und Schlüssel Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="4bd3a-103">Certificate Signature and Key Interfaces</span></span>

<span data-ttu-id="4bd3a-104">Die folgenden Schnittstellen können verwendet werden, um Zertifikat Signaturen sowie öffentliche und private Schlüssel zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="4bd3a-104">The following interfaces can be used to manage certificate signatures, and public and private keys.</span></span>



| <span data-ttu-id="4bd3a-105">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="4bd3a-105">Interface</span></span>                                                      | <span data-ttu-id="4bd3a-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4bd3a-106">Description</span></span>                                                                                       |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4bd3a-107">**Isignercertificate**</span><span class="sxs-lookup"><span data-stu-id="4bd3a-107">**ISignerCertificate**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate)               | <span data-ttu-id="4bd3a-108">Stellt ein Signaturzertifikat dar, mit dem Sie eine Zertifikat Anforderung signieren können.</span><span class="sxs-lookup"><span data-stu-id="4bd3a-108">Represents a signing certificate that enables you to sign a certificate request.</span></span>                  |
| [<span data-ttu-id="4bd3a-109">**Isignerzertifikate**</span><span class="sxs-lookup"><span data-stu-id="4bd3a-109">**ISignerCertificates**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates)             | <span data-ttu-id="4bd3a-110">Verwaltet eine Auflistung von [**isignercertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) -Objekten.</span><span class="sxs-lookup"><span data-stu-id="4bd3a-110">Manages a collection of [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) objects.</span></span>                 |
| [<span data-ttu-id="4bd3a-111">**IX509PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="4bd3a-111">**IX509PrivateKey**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)                     | <span data-ttu-id="4bd3a-112">Stellt einen asymmetrischen privaten Schlüssel dar, der für die Verschlüsselung, Signierung und Schlüssel Übereinstimmung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="4bd3a-112">Represents an asymmetric private key that can be used for encryption, signing, and key agreement.</span></span> |
| [<span data-ttu-id="4bd3a-113">**IX509PublicKey**</span><span class="sxs-lookup"><span data-stu-id="4bd3a-113">**IX509PublicKey**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509publickey)                       | <span data-ttu-id="4bd3a-114">Stellt einen öffentlichen Schlüssel in einem Paar aus öffentlichem und privatem Schlüssel dar.</span><span class="sxs-lookup"><span data-stu-id="4bd3a-114">Represents a public key in a public/private key pair.</span></span>                                             |
| [<span data-ttu-id="4bd3a-115">**IX509SignatureInformation**</span><span class="sxs-lookup"><span data-stu-id="4bd3a-115">**IX509SignatureInformation**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509signatureinformation) | <span data-ttu-id="4bd3a-116">Stellt Informationen dar, die zum Signieren einer Zertifikat Anforderung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4bd3a-116">Represents information used to sign a certificate request.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="4bd3a-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4bd3a-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4bd3a-118">CertEnroll-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="4bd3a-118">CertEnroll Interfaces</span></span>](certenroll-interfaces.md)
</dt> </dl>

 

 



