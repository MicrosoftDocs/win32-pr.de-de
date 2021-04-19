---
description: Die IX509SCEPEnrollment-Schnittstelle stellt die folgenden Methoden zur Verfügung.
ms.assetid: B45B68D2-A14D-4D14-AF5F-1A1BB9921A0D
title: IX509SCEPEnrollment-Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a33c3bdee14b865211b53649075dec6d4617a4c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363584"
---
# <a name="ix509scepenrollment-methods"></a><span data-ttu-id="f1d2c-103">IX509SCEPEnrollment-Methoden</span><span class="sxs-lookup"><span data-stu-id="f1d2c-103">IX509SCEPEnrollment Methods</span></span>

<span data-ttu-id="f1d2c-104">Die [**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment) -Schnittstelle stellt die folgenden Methoden zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="f1d2c-104">The [**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f1d2c-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="f1d2c-105">In this section</span></span>



| <span data-ttu-id="f1d2c-106">Thema</span><span class="sxs-lookup"><span data-stu-id="f1d2c-106">Topic</span></span>                                                                                                              | <span data-ttu-id="f1d2c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f1d2c-107">Description</span></span>                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f1d2c-108">**Methode "samaterequestmessage"**</span><span class="sxs-lookup"><span data-stu-id="f1d2c-108">**CreateRequestMessage method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createrequestmessage)<br/>                         | <span data-ttu-id="f1d2c-109">Erstellen Sie eine PKCS10-Anforderungs Nachricht mit einem Challenge-Kennwort.</span><span class="sxs-lookup"><span data-stu-id="f1d2c-109">Create a PKCS10 request message with a challenge password.</span></span> <span data-ttu-id="f1d2c-110">Die Anforderungs Nachricht befindet sich in einem eingeschlossenen PKCS7, das mit dem SCEP-Server Verschlüsselungs Zertifikat verschlüsselt und vom Server-Signaturzertifikat signiert wurde.</span><span class="sxs-lookup"><span data-stu-id="f1d2c-110">The request message is in an enveloped PKCS7 encrypted with the SCEP server encryption certificate and signed by the server signing certificate.</span></span><br/> |
| [<span data-ttu-id="f1d2c-111">**Methode "| aterezevecertificess"**</span><span class="sxs-lookup"><span data-stu-id="f1d2c-111">**CreateRetrieveCertificateMessage method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createretrievecertificatemessage)<br/> | <span data-ttu-id="f1d2c-112">Rufen Sie ein zuvor ausgestelltes Zertifikat ab.</span><span class="sxs-lookup"><span data-stu-id="f1d2c-112">Retrieve a previously issued certificate.</span></span><br/>                                                                                                                                                                   |
| [<span data-ttu-id="f1d2c-113">**Methode "kreaterezeveperedingmessage"**</span><span class="sxs-lookup"><span data-stu-id="f1d2c-113">**CreateRetrievePendingMessage method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createretrievependingmessage)<br/>         | <span data-ttu-id="f1d2c-114">Erstellen Sie eine Nachricht für die Zertifikat Abruf Sperre (manuelle Registrierung).</span><span class="sxs-lookup"><span data-stu-id="f1d2c-114">Create a message for certificate polling (manual enrollment).</span></span><br/>                                                                                                                                               |
| [<span data-ttu-id="f1d2c-115">**DeleteRequest-Methode**</span><span class="sxs-lookup"><span data-stu-id="f1d2c-115">**DeleteRequest method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-deleterequest)<br/>                                       | <span data-ttu-id="f1d2c-116">Löschen Sie alle Zertifikate und Schlüssel, die für die Anforderung erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="f1d2c-116">Delete any certificates or keys created for the request.</span></span><br/>                                                                                                                                                    |
| [<span data-ttu-id="f1d2c-117">**Initialize-Methode**</span><span class="sxs-lookup"><span data-stu-id="f1d2c-117">**Initialize method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-initialize)<br/>                                             | <span data-ttu-id="f1d2c-118">Initialisieren Sie die-Instanz als Vorbereitung für eine neue Anforderung.</span><span class="sxs-lookup"><span data-stu-id="f1d2c-118">Initialize the instance in preparation for a new request.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="f1d2c-119">**Initializeforpending-Methode**</span><span class="sxs-lookup"><span data-stu-id="f1d2c-119">**InitializeForPending method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-initializeforpending)<br/>                         | <span data-ttu-id="f1d2c-120">Initialisieren Sie die-Instanz, um eine Nachricht zu generieren, um entweder ein ausgestelltes Zertifikat abzurufen, oder eine Antwort für eine vorherige Anforderung vom Aussteller zu installieren.</span><span class="sxs-lookup"><span data-stu-id="f1d2c-120">Initialize the instance to prepare to generate a message to either retrieve an issued certificate, or install a response for a previous request by the issuer.</span></span><br/>                                              |
| [<span data-ttu-id="f1d2c-121">**ProcessResponse Message-Methode**</span><span class="sxs-lookup"><span data-stu-id="f1d2c-121">**ProcessResponseMessage method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-processresponsemessage)<br/>                     | <span data-ttu-id="f1d2c-122">Verarbeiten einer Antwortnachricht und Zurückgeben der Disposition der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="f1d2c-122">Process a response message and return the disposition of the message.</span></span><br/>                                                                                                                                       |



 

 

 




