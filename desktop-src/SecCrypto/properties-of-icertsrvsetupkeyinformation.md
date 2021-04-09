---
description: Die folgenden Eigenschaften werden von der icertrvsetupkeyinformation-Schnittstelle definiert.
ms.assetid: d805a011-8728-4687-8e4a-ad331617abe7
title: Eigenschaften von icertrvsetupkeyinformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d2a41647c06015c011d4d7a36cddfd81466b3b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865455"
---
# <a name="properties-of-icertsrvsetupkeyinformation"></a><span data-ttu-id="9a0c0-103">Eigenschaften von icertrvsetupkeyinformation</span><span class="sxs-lookup"><span data-stu-id="9a0c0-103">Properties of ICertSrvSetupKeyInformation</span></span>

<span data-ttu-id="9a0c0-104">Die folgenden Eigenschaften werden von der [**icertrvsetupkeyinformation**](/windows/desktop/api/Casetup/nn-casetup-icertsrvsetupkeyinformation) -Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="9a0c0-104">The following properties are defined by the [**ICertSrvSetupKeyInformation**](/windows/desktop/api/Casetup/nn-casetup-icertsrvsetupkeyinformation) interface.</span></span>



| <span data-ttu-id="9a0c0-105">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9a0c0-105">Property</span></span>                                                                           | <span data-ttu-id="9a0c0-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9a0c0-106">Description</span></span>                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9a0c0-107">**Container Name**</span><span class="sxs-lookup"><span data-stu-id="9a0c0-107">**ContainerName**</span></span>](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_containername)                 | <span data-ttu-id="9a0c0-108">Ruft den Namen des [*Kryptografiedienstanbieters (kryptografischen Service Provider*](../secgloss/c-gly.md) , CSP) zum generieren, speichern oder zugreifen auf den Schlüssel ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="9a0c0-108">Gets or sets the name used by the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) to generate, store, or access the key.</span></span>                                                                       |
| [<span data-ttu-id="9a0c0-109">**Vorhanden**</span><span class="sxs-lookup"><span data-stu-id="9a0c0-109">**Existing**</span></span>](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_existing)                           | <span data-ttu-id="9a0c0-110">Dient zum Abrufen oder Festlegen eines Werts, der angibt, ob der private Schlüssel bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="9a0c0-110">Gets or sets a value that indicates whether the private key already exists.</span></span>                                                                                                                                                                                                                       |
| [<span data-ttu-id="9a0c0-111">**Existingcacertificate**</span><span class="sxs-lookup"><span data-stu-id="9a0c0-111">**ExistingCACertificate**</span></span>](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_existingcacertificate) | <span data-ttu-id="9a0c0-112">Ruft den binären Wert ab, der mit [*Distinguished Encoding Rules*](../secgloss/d-gly.md) (der) codiert wurde, oder legt diesen fest, der der binäre Wert des Zertifizierungsstellen Zertifikats ist, das einem vorhandenen Schlüssel entspricht.</span><span class="sxs-lookup"><span data-stu-id="9a0c0-112">Gets or sets the binary value that has been encoded by using [*Distinguished Encoding Rules*](../secgloss/d-gly.md) (DER) and that is the binary value of the CA certificate that corresponds to an existing key.</span></span> |
| [<span data-ttu-id="9a0c0-113">**HashAlgorithm**</span><span class="sxs-lookup"><span data-stu-id="9a0c0-113">**HashAlgorithm**</span></span>](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_hashalgorithm)                 | <span data-ttu-id="9a0c0-114">Ruft den Namen des Hash Algorithmus ab, mit dem das Zertifizierungsstellen Zertifikat für den Schlüssel signiert oder überprüft wird, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="9a0c0-114">Gets or sets the name of the hash algorithm used to sign or verify the CA certificate for the key.</span></span>                                                                                                                                                                                                |
| [<span data-ttu-id="9a0c0-115">**Länge**</span><span class="sxs-lookup"><span data-stu-id="9a0c0-115">**Length**</span></span>](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_length)                               | <span data-ttu-id="9a0c0-116">Ruft die Stärke des Schlüssels zu einem der vom CSP unterstützten Werte ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="9a0c0-116">Gets or sets the strength of the key to one of the values supported by the CSP.</span></span>                                                                                                                                                                                                                   |
| [<span data-ttu-id="9a0c0-117">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="9a0c0-117">**ProviderName**</span></span>](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_providername)                   | <span data-ttu-id="9a0c0-118">Ruft den Namen des CSP ab, der zum Generieren oder Speichern des privaten Schlüssels verwendet wird, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="9a0c0-118">Gets or sets the name of the CSP that is used to generate or store the private key.</span></span>                                                                                                                                                                                                               |



 

 

 
