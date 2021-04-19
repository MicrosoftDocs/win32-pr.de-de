---
description: Die IX509SCEPEnrollment-Schnittstelle macht die folgenden Eigenschaften verfügbar.
ms.assetid: 53BE8DE9-87AC-41D1-B1B5-2FEC72F5FCEA
title: IX509SCEPEnrollment-Eigenschaften
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fd9b4cbf9df87f898e61ce0220243044b24607d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360672"
---
# <a name="ix509scepenrollment-properties"></a><span data-ttu-id="f5dd7-103">IX509SCEPEnrollment-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f5dd7-103">IX509SCEPEnrollment Properties</span></span>

<span data-ttu-id="f5dd7-104">Die [**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment) -Schnittstelle macht die folgenden Eigenschaften verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f5dd7-104">The [**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment) interface exposes the following properties.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f5dd7-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="f5dd7-105">In this section</span></span>



| <span data-ttu-id="f5dd7-106">Thema</span><span class="sxs-lookup"><span data-stu-id="f5dd7-106">Topic</span></span>                                                                                              | <span data-ttu-id="f5dd7-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f5dd7-107">Description</span></span>                                                                                                                                            |
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f5dd7-108">**Zertifikat Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="f5dd7-108">**Certificate property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_certificate)<br/>                         | <span data-ttu-id="f5dd7-109">Ruft das Zertifikat für die Anforderung ab.</span><span class="sxs-lookup"><span data-stu-id="f5dd7-109">Gets the certificate for the request.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="f5dd7-110">**Certificatefriendlyname (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="f5dd7-110">**CertificateFriendlyName property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_certificatefriendlyname)<br/> | <span data-ttu-id="f5dd7-111">Ruft den anzeigen Amen für das Zertifikat ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="f5dd7-111">Gets or sets the friendly name for the certificate.</span></span><br/>                                                                                         |
| [<span data-ttu-id="f5dd7-112">**Failinfo-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="f5dd7-112">**FailInfo property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_failinfo)<br/>                               | <span data-ttu-id="f5dd7-113">Ruft Informationen ab, wenn die [**ProcessResponse Message**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-processresponsemessage) -Methode eine fehlerhafte Umgebung erkennt.</span><span class="sxs-lookup"><span data-stu-id="f5dd7-113">Gets information when the [**ProcessResponseMessage**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-processresponsemessage) method detects a failed environment.</span></span><br/> |
| [<span data-ttu-id="f5dd7-114">**Oldcertificate (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="f5dd7-114">**OldCertificate property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_oldcertificate)<br/>                   | <span data-ttu-id="f5dd7-115">Ruft ein altes Zertifikat ab, das von einer Anforderung ersetzt werden soll, oder legt dieses fest.</span><span class="sxs-lookup"><span data-stu-id="f5dd7-115">Gets or sets an old certificate that a request is intended to replace.</span></span><br/>                                                                      |
| [<span data-ttu-id="f5dd7-116">**Anforderungs Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="f5dd7-116">**Request property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_request)<br/>                                 | <span data-ttu-id="f5dd7-117">Ruft die innere PKCS10-Anforderung ab.</span><span class="sxs-lookup"><span data-stu-id="f5dd7-117">Gets the inner PKCS10 request.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="f5dd7-118">**Serverfunktionalitäten (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="f5dd7-118">**ServerCapabilities property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-put_servercapabilities)<br/>           | <span data-ttu-id="f5dd7-119">Legt die bevorzugten Hash-und Verschlüsselungsalgorithmen für die Anforderung fest.</span><span class="sxs-lookup"><span data-stu-id="f5dd7-119">Sets the preferred hash and encryption algorithms for the request.</span></span><br/>                                                                          |
| [<span data-ttu-id="f5dd7-120">**SignerCertificate (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="f5dd7-120">**SignerCertificate property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_signercertificate)<br/>             | <span data-ttu-id="f5dd7-121">Ruft das Signatur Geber Zertifikat für die Anforderung ab oder legt es fest.</span><span class="sxs-lookup"><span data-stu-id="f5dd7-121">Gets or sets the signer certificate for the request.</span></span><br/>                                                                                        |
| [<span data-ttu-id="f5dd7-122">**Silent (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="f5dd7-122">**Silent property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-put_silent)<br/>                                   | <span data-ttu-id="f5dd7-123">Ruft ab oder legt fest, ob die Benutzeroberfläche während der Anforderung zugelassen wird.</span><span class="sxs-lookup"><span data-stu-id="f5dd7-123">Gets or sets whether to allow UI during the request.</span></span><br/>                                                                                        |
| [<span data-ttu-id="f5dd7-124">**Status (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="f5dd7-124">**Status property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_status)<br/>                                   | <span data-ttu-id="f5dd7-125">Ruft den Status der Anforderung ab.</span><span class="sxs-lookup"><span data-stu-id="f5dd7-125">Gets the status of the request.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="f5dd7-126">**Transaktionid (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="f5dd7-126">**TransactionId property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_transactionid)<br/>                     | <span data-ttu-id="f5dd7-127">Ruft die Transaktions-ID für die Anforderung ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="f5dd7-127">Gets or sets the transaction id for the request.</span></span><br/>                                                                                            |



 

 

 




