---
description: Anmelde Informationen sind für den SChannel-Authentifizierungsprozess erforderlich. sowohl der Client als auch der Server müssen gültige Anmelde Informationen zum Einrichten eines Sicherheits Kontexts für den Nachrichtenaustausch erhalten. Ein Beispiel zur Veranschaulichung dieses Verfahrens finden Sie unter "erhalten von Anmelde Informationen".
ms.assetid: ee4a9908-7ba8-4701-84a4-c50b6b989e82
title: Abrufen von SChannel-Anmelde Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34e5a5b82b3ed76e905c967009da52d17bff0f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756438"
---
# <a name="obtaining-schannel-credentials"></a><span data-ttu-id="cf832-104">Abrufen von SChannel-Anmelde Informationen</span><span class="sxs-lookup"><span data-stu-id="cf832-104">Obtaining Schannel Credentials</span></span>

<span data-ttu-id="cf832-105">Anmelde Informationen sind für den SChannel-Authentifizierungsprozess erforderlich. sowohl der Client als auch der Server müssen gültige Anmelde Informationen zum Einrichten eines [*Sicherheits Kontexts*](../secgloss/s-gly.md) für den Nachrichtenaustausch erhalten.</span><span class="sxs-lookup"><span data-stu-id="cf832-105">Credentials are required by the Schannel authentication process; both client and server must obtain valid credentials to establish a [*security context*](../secgloss/s-gly.md) for message exchange.</span></span> <span data-ttu-id="cf832-106">Ein Beispiel zur Veranschaulichung dieses Verfahrens finden Sie unter " [erhalten von Anmelde](getting-a-certificate-for-schannel.md)Informationen".</span><span class="sxs-lookup"><span data-stu-id="cf832-106">For an example that demonstrates this procedure, see [Getting credentials](getting-a-certificate-for-schannel.md).</span></span>

<span data-ttu-id="cf832-107">Die Anwendung erhält Anmelde Informationen, indem Sie die [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) -Funktion aufruft, die ein Handle für die angeforderten Anmelde Informationen zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="cf832-107">Your application obtains credentials by calling the [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) function, which returns a handle to the requested credentials.</span></span> <span data-ttu-id="cf832-108">Da Anmelde Informationen zum Speichern von Konfigurationsinformationen verwendet werden, kann das gleiche Handle nicht sowohl für Client seitige als auch für serverseitige Vorgänge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cf832-108">Because credentials handles are used to store configuration information, the same handle cannot be used for both client-side and server-side operations.</span></span> <span data-ttu-id="cf832-109">Dies bedeutet, dass Anwendungen, die sowohl Client-als auch Serververbindungen unterstützen, mindestens zwei Handles für die Anmelde Informationen erhalten müssen.</span><span class="sxs-lookup"><span data-stu-id="cf832-109">This means that applications that support both client and server connections must obtain a minimum of two credentials handles.</span></span>

<span data-ttu-id="cf832-110">In Windows XP gibt eine [**SChannel- \_ Kred-**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) Struktur Folgendes an:</span><span class="sxs-lookup"><span data-stu-id="cf832-110">In Windows XP, an [**SCHANNEL\_CRED**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) structure specifies the following:</span></span>

-   <span data-ttu-id="cf832-111">Ein Sicherheitsprotokoll</span><span class="sxs-lookup"><span data-stu-id="cf832-111">A security protocol</span></span>
-   <span data-ttu-id="cf832-112">Die zulässigen Chiffren</span><span class="sxs-lookup"><span data-stu-id="cf832-112">The allowable ciphers</span></span>
-   <span data-ttu-id="cf832-113">Minimale und maximale Verschlüsselungsstärke</span><span class="sxs-lookup"><span data-stu-id="cf832-113">Minimum and maximum cipher strengths</span></span>
-   <span data-ttu-id="cf832-114">Ein für die Authentifizierung verwendetes [*X. 509*](../secgloss/x-gly.md) -Zertifikat – erforderlich für den-Server, sofern der Server keine Client Authentifizierung anfordert.</span><span class="sxs-lookup"><span data-stu-id="cf832-114">An [*X.509*](../secgloss/x-gly.md) certificate used for authentication — Required for server, optional for client unless server requests client authentication.</span></span>

<span data-ttu-id="cf832-115">Übergeben Sie die [**SChannel- \_ Kred-**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) Struktur (über den *pauthdata* -Parameter) an die [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="cf832-115">Pass the [**SCHANNEL\_CRED**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) structure (via the *pAuthData* parameter) to the [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) function.</span></span> <span data-ttu-id="cf832-116">Diese Funktion gibt den Anmelde Informations Handle zurück, der zum Einrichten eines [*Sicherheits Kontexts*](../secgloss/s-gly.md)erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="cf832-116">This function returns the credentials handle required to establish a [*security context*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="cf832-117">Ausführliche Informationen zum Festlegen der mit SChannel verwendeten Chiffren finden Sie unter [Angeben von SChannel-Chiffren und Verschlüsselungs stärken](specifying-schannel-ciphers-and-cipher-strengths.md).</span><span class="sxs-lookup"><span data-stu-id="cf832-117">For detailed information on setting the ciphers used with Schannel, see [Specifying Schannel Ciphers and Cipher Strengths](specifying-schannel-ciphers-and-cipher-strengths.md).</span></span>

<span data-ttu-id="cf832-118">Weitere Informationen zu Zertifikaten finden Sie unter [Zertifikat-und Zertifikat Speicherfunktionen](../seccrypto/cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="cf832-118">For information about certificates, see [Certificate and Certificate Store Functions](../seccrypto/cryptography-functions.md).</span></span>

<span data-ttu-id="cf832-119">Ein Beispiel für das Öffnen eines [*Zertifikat Speicher*](../secgloss/c-gly.md) und Suchen eines Zertifikats für die SChannel-Authentifizierung finden Sie unter [erhalten eines Zertifikats](getting-a-certificate-for-schannel.md).</span><span class="sxs-lookup"><span data-stu-id="cf832-119">For an example that demonstrates opening a [*certificate store*](../secgloss/c-gly.md) and locating a certificate to use for Schannel authentication, see [Getting a Certificate](getting-a-certificate-for-schannel.md).</span></span>

 

 
