---
description: SChannel-Anmelde Informationen werden intern als CERT- \_ Kontext Strukturen dargestellt.
ms.assetid: 3d2deb61-8e86-4461-8f2a-4880ca5b9d34
title: Private Schlüssel CryptoAPI 2.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5180515b529e33ae385fa94688a7e8fb436bd32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358991"
---
# <a name="cryptoapi-20-private-keys"></a>Private Schlüssel CryptoAPI 2.0

SChannel-Anmelde Informationen werden intern als [**CERT- \_ Kontext**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) Strukturen dargestellt. SChannel identifiziert den [*privaten Schlüssel*](/windows/desktop/SecGloss/p-gly) , der einem bestimmten Zertifikat Kontext zugeordnet ist, mithilfe der Zertifikat \_ Schlüssel Proxy-Eigenschaft der Zertifikat- \_ \_ \_ \_ ID. Wenn Sie diese Eigenschaft verwenden, greift SChannel auf den *privaten Schlüssel* zu, indem er die [**CryptAcquireContext**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta) -Funktion aufruft. Weitere Informationen finden Sie unter [öffentliche/private Schlüsselpaare](/windows/desktop/SecCrypto/public-private-key-pairs).

Alle SChannel-Anmelde Informationen enthalten einen Verweis auf einen oder mehrere private Schlüssel, die jeweils einem bestimmten Zertifikat zugeordnet sind. Die [*privaten Schlüssel*](/windows/desktop/SecGloss/p-gly) werden ganz anders behandelt, je nachdem, ob die Anmelde Informationen für einen Client oder Server gelten.

## <a name="client-private-keys"></a>Private Client Schlüssel

[*Private Client Schlüssel*](/windows/desktop/SecGloss/p-gly) werden vom verwendeten [*Kryptografiedienstanbieter (kryptografischen Service Provider*](/windows/desktop/SecGloss/c-gly) , CSP) verwaltet. Private Client Schlüssel werden in der Regel von CSPs des Typs [Prov \_ RSA \_ Full](/windows/desktop/SecCrypto/prov-rsa-full) oder Prov \_ RSA \_ Signature gespeichert.

Wenn die Client Anwendung den [**CryptAcquireContext**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta) -Aufruf manuell ausführt, muss der Client vor dem Aufrufen von [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea)das Handle des CSP an den Zertifikat Kontext binden, indem er die Eigenschaften der prop-ID des CERT- \_ Schlüssel \_ Prov- \_ Handles verwendet \_ \_ . Wenn SChannel diese Eigenschaft festgelegt hat, wird die Eigenschaft "CERT \_ Key \_ Prov \_ Info \_ Prop \_ ID" nicht verwendet.

## <a name="server-private-keys"></a>Private Server Schlüssel

Private Server Schlüssel werden von einem der folgenden CSPs gespeichert:

-   Prov \_ RSA \_ SChannel
-   Prov \_ dh \_ SChannel
-   Prov \_ Fortezza CSP

Die Auswahl des CSP hängt vom ausgewählten Algorithmus für den [*Schlüsselaustausch*](/windows/desktop/SecGloss/k-gly)ab. Private Server Schlüssel müssen den Typ " \_ keyexchange" aufweisen.

 

 
