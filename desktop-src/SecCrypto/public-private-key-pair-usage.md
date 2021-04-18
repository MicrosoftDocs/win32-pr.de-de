---
description: Alle normalen RSA/SChannel-und Diffie-Hellman/SChannel-Vorgänge verwenden das \_ Schlüsselpaar für den Schlüsselaustausch aus öffentlichem und privatem Schlüssel.
ms.assetid: e12afdbb-7ba8-444e-a43f-e262b481a353
title: Verwendung des öffentlichen/privaten Schlüssel Paars
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38dba78c487c433875ed23ce3f2f3c87a86b07c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357928"
---
# <a name="publicprivate-key-pair-usage"></a><span data-ttu-id="6aa72-103">Verwendung des öffentlichen/privaten Schlüssel Paars</span><span class="sxs-lookup"><span data-stu-id="6aa72-103">Public/Private Key Pair Usage</span></span>

<span data-ttu-id="6aa72-104">Alle normalen [*RSA*](../secgloss/r-gly.md)-/SChannel [*-und Diffie-Hellman/SChannel-*](../secgloss/d-gly.md)Vorgänge verwenden das \_ Schlüsselpaar für den Schlüsselaustausch aus [*öffentlichem und privatem*](../secgloss/p-gly.md)Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="6aa72-104">All normal [*RSA*](../secgloss/r-gly.md)/Schannel and [*Diffie-Hellman*](../secgloss/d-gly.md)/Schannel operations use the AT\_KEYEXCHANGE [*public/private key pair*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="6aa72-105">Zum Bereitstellen der Server [*Authentifizierung*](../secgloss/a-gly.md)muss die Serverseite von SChannel-Vorgängen Zugriff auf das [*X. 509*](../secgloss/x-gly.md) -Zertifikat haben, das seinen öffentlichen Schlüssel und Zugriff auf den entsprechenden [*privaten Schlüssel*](../secgloss/p-gly.md)enthält.</span><span class="sxs-lookup"><span data-stu-id="6aa72-105">To provide server [*authentication*](../secgloss/a-gly.md), the server-side of Schannel operations must have access to its [*X.509*](../secgloss/x-gly.md) certificate containing its public key and access to the matching [*private key*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="6aa72-106">Die Client seitige Ausführung von [*SChannel*](../secgloss/s-gly.md) benötigt das Zertifikat mit seinem öffentlichen Schlüssel und Zugriff auf den privaten Schlüssel, wenn die Client Authentifizierung implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="6aa72-106">The client-side of [*Schannel*](../secgloss/s-gly.md) needs its certificate with its public key and access to its private key if client authentication is implemented.</span></span>

<span data-ttu-id="6aa72-107">Da SChannel-Protokoll-Engines nie das \_ Schlüsselpaar für öffentliche/private Schlüssel in der Signatur verwenden, muss das Schlüsselpaar nicht von einem neuen CSP unterstützt werden, der nur RSA/SChannel oder Diffie-Hellman/SChannel unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6aa72-107">Since Schannel protocol engines never use the AT\_SIGNATURE public/private key pair, that key pair need not be supported by a new CSP supporting only RSA/Schannel or Diffie-Hellman/Schannel.</span></span>

<span data-ttu-id="6aa72-108">Wenn eine Protokoll-Engine eine SSL 3,0-Export Verschlüsselungs Sammlung mit einem- \_ Schlüsselaustausch-Schlüsselpaar verwendet, das größer als 512 Bits ist, muss der Server ein zusätzliches RSA-Schlüsselpaar verwenden.</span><span class="sxs-lookup"><span data-stu-id="6aa72-108">If a protocol engine uses an SSL 3.0 export cipher suite with an AT\_KEYEXCHANGE key pair larger than 512 bits, the server must use an additional RSA key pair.</span></span> <span data-ttu-id="6aa72-109">Dieses zusätzliche Schlüsselpaar ist immer genau 512 Bits und kann kurzlebig sein.</span><span class="sxs-lookup"><span data-stu-id="6aa72-109">This additional key pair is always exactly 512 bits and it can be ephemeral.</span></span> <span data-ttu-id="6aa72-110">Das Paar wird als in \_ keyexchange-Element in einem Schlüssel Container gespeichert, der im Besitz der Protokoll-Engine ist.</span><span class="sxs-lookup"><span data-stu-id="6aa72-110">The pair is stored as an AT\_KEYEXCHANGE element in a key container owned by the protocol engine.</span></span> <span data-ttu-id="6aa72-111">Ein Handle für diesen Schlüssel Container wird in der Regel beim Start der Protokoll-Engine abgerufen.</span><span class="sxs-lookup"><span data-stu-id="6aa72-111">A handle to this key container is typically acquired at protocol engine startup.</span></span>

<span data-ttu-id="6aa72-112">Diffie-Hellman unterstützt nur [*calg \_ dh \_ ephem*](../secgloss/c-gly.md) und verwendet normale RSA-oder DSS-öffentliche Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="6aa72-112">Diffie-Hellman supports only [*CALG\_DH\_EPHEM*](../secgloss/c-gly.md) and uses normal RSA or DSS public keys.</span></span>

 

 
