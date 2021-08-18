---
description: Schannel-Anmeldeinformationen werden intern als CERT \_ CONTEXT-Strukturen dargestellt.
ms.assetid: 3d2deb61-8e86-4461-8f2a-4880ca5b9d34
title: CryptoAPI 2.0 Private Schlüssel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 653ca6356849894ac5d15c07a0116bee7c2a2ba84df8c79de360d96f1e147fef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008688"
---
# <a name="cryptoapi-20-private-keys"></a>CryptoAPI 2.0 Private Schlüssel

Schannel-Anmeldeinformationen werden intern als [**CERT \_ CONTEXT-Strukturen**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) dargestellt. Schannel sucht den [*privaten Schlüssel,*](/windows/desktop/SecGloss/p-gly) der einem bestimmten Zertifikatkontext zugeordnet ist, mithilfe der Eigenschaft CERT KEY PROV INFO PROP ID des \_ \_ \_ \_ \_ Zertifikats. Mit dieser Eigenschaft greift Schannel auf den *privaten Schlüssel* zu, indem die [**CryptAcquireContext-Funktion**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta) aufgerufen wird. Weitere Informationen finden Sie unter [Öffentliche/private Schlüsselpaare.](/windows/desktop/SecCrypto/public-private-key-pairs)

Jede Schannel-Anmeldeinformation enthält einen Verweis auf einen oder mehrere private Schlüssel, die jeweils einem bestimmten Zertifikat zugeordnet sind. Die [*privaten Schlüssel*](/windows/desktop/SecGloss/p-gly) werden ganz unterschiedlich behandelt, je nachdem, ob die Anmeldeinformationen für einen Client oder einen Server gelten.

## <a name="client-private-keys"></a>Private Clientschlüssel

[*Private Clientschlüssel*](/windows/desktop/SecGloss/p-gly) werden vom verwendeten [*Kryptografiedienstanbieter (Cryptographic Service Provider,*](/windows/desktop/SecGloss/c-gly) CSP) verwaltet. Private Clientschlüssel werden in der Regel von CSPs vom Typ [PROV \_ RSA \_ FULL](/windows/desktop/SecCrypto/prov-rsa-full) oder PROV \_ RSA SIGNATURE \_ gespeichert.

Wenn die Clientanwendung den [**CryptAcquireContext-Aufruf**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta) manuell vor dem Aufruf von [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea)vornimmt, muss der Client das Handle des CSP mithilfe der CERT \_ KEY \_ PROV \_ HANDLE PROP \_ ID-Eigenschaft an den Zertifikatkontext \_ binden. Wenn Schannel diesen Eigenschaftensatz findet, verwendet er nicht die CERT \_ KEY \_ PROV \_ INFO PROP \_ \_ ID-Eigenschaft.

## <a name="server-private-keys"></a>Private Serverschlüssel

Private Serverschlüssel werden von einem der folgenden CSPs gespeichert:

-   PROV \_ RSA \_ SCHANNEL
-   PROV \_ DH \_ SCHANNEL
-   PROV \_ FORTEZZA CSP

Die Auswahl des CSP hängt vom ausgewählten [*Schlüsselaustauschalgorithmus*](/windows/desktop/SecGloss/k-gly)ab. Private Serverschlüssel müssen vom Typ AT \_ KEYEXCHANGE sein.

 

 
