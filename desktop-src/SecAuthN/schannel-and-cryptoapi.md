---
description: SChannel verwendet CryptoAPI für kryptografische Vorgänge, wie z. b. das Speichern von öffentlichen und privaten Schlüsseln.
ms.assetid: 5ad9a171-5f69-4035-aac5-ae8d27d0abfb
title: SChannel und CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0684cd690911444b77ba27d2876e578fd71c73a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393357"
---
# <a name="schannel-and-cryptoapi"></a><span data-ttu-id="c3cc8-103">SChannel und CryptoAPI</span><span class="sxs-lookup"><span data-stu-id="c3cc8-103">Schannel and CryptoAPI</span></span>

<span data-ttu-id="c3cc8-104">SChannel verwendet [CryptoAPI](../seccrypto/cryptography-essentials.md) für kryptografische Vorgänge, wie z. b. das Speichern von [*öffentlichen und privaten Schlüsseln*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="c3cc8-104">Schannel uses [CryptoAPI](../seccrypto/cryptography-essentials.md) for cryptographic operations such as storing [*public/private keys*](../secgloss/p-gly.md).</span></span>

<span data-ttu-id="c3cc8-105">Die folgenden Themen enthalten ausführliche Informationen zur Verwendung von CryptoAPI durch Schannel.</span><span class="sxs-lookup"><span data-stu-id="c3cc8-105">The following topics provide detailed information about how Schannel makes use of CryptoAPI.</span></span>



| <span data-ttu-id="c3cc8-106">Thema</span><span class="sxs-lookup"><span data-stu-id="c3cc8-106">Topic</span></span>                                                                   | <span data-ttu-id="c3cc8-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c3cc8-107">Description</span></span>                                                                                                          |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c3cc8-108">Zertifikatspeicher</span><span class="sxs-lookup"><span data-stu-id="c3cc8-108">Certificate Stores</span></span>](certificate-stores.md)<br/>                 | <span data-ttu-id="c3cc8-109">Client-und Server Zertifikate müssen in einem Zertifikat Speicher gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="c3cc8-109">Both client and server certificates must be stored in a certificate store.</span></span><br/>                                |
| [<span data-ttu-id="c3cc8-110">Private Schlüssel CryptoAPI 2.0</span><span class="sxs-lookup"><span data-stu-id="c3cc8-110">CryptoAPI 2.0 Private Keys</span></span>](cryptoapi-2-0-private-keys.md)<br/> | <span data-ttu-id="c3cc8-111">SChannel-Anmelde Informationen werden intern als [**CERT- \_ Kontext**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) Strukturen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="c3cc8-111">Schannel credentials are represented internally as [**CERT\_CONTEXT**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) structures.</span></span><br/> |



 

 

 
