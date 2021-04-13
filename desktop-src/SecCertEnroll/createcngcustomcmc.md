---
description: Erstellt ein Objekt vom Objekt "CMC Request" aus einer inneren geschachtelten PKCS \# 10-Anforderung.
ms.assetid: 8a0dc078-22ca-4bff-9cc0-46823912d3da
title: "\"kreatecngcustomcmc\""
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 669a52901981ea910ee3d1704ba892fb96664470
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342729"
---
# <a name="createcngcustomcmc"></a>"kreatecngcustomcmc"

Das Beispiel "samatecngcustomcmc" erstellt ein Objekt vom Objekt "CMC Request" aus einer inneren geschachtelten PKCS \# 10-Anforderung. Die innere Anforderung wird mit einem asymmetrischen [*privaten Schlüssel*](/windows/desktop/SecGloss/p-gly)erstellt. Der private Schlüssel wird mit dem Kryptografieanbieter Cryptography API: Next Generation (CNG) und dem in der Befehlszeile angegebenen Algorithmus erstellt. Außerdem werden benutzerdefinierte Optionen wie Export Richtlinie und Schlüsselschutz Ebene für den privaten Schlüssel festgelegt.

## <a name="location"></a>Standort

Wenn Sie das Microsoft Windows Software Development Kit (SDK) installieren, wird das Beispiel standardmäßig im Ordner *% Program Files%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Registrierung \\ VC | \\ atecngcustomcmc installiert.

## <a name="discussion"></a>Diskussion

Das Beispiel "samatecngcustomcmc":

1.  Verarbeitet die folgenden Befehlszeilenargumente:
    -   Der Name eines CNG- [*Kryptografiedienstanbieters*](/windows/desktop/SecGloss/c-gly) (CSP).
    -   Der Name des Algorithmus, der verwendet wird, um einen asymmetrischen privaten Schlüssel zu generieren.
    -   Der Name des Algorithmus, der zum [*Hash*](/windows/desktop/SecGloss/h-gly) der [*Zertifikat Anforderung*](/windows/desktop/SecGloss/c-gly)verwendet wird.
    -   Eine Ausgabedatei, in der die Zertifikat Anforderung gespeichert werden soll.
    -   Eine optionale Zeichenfolge (Alternative Signatur), die, falls vorhanden, angibt, dass ein diskreter anstelle eines kombinierten Signatur Algorithmus verwendet werden soll. Weitere Informationen finden Sie unter der Eigenschaft " [**Alternative**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm) Eigenschaft".
2.  Erstellt ein [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) -Objekt und legt die folgenden Eigenschaften fest:
    -   [**Legacycsp**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_legacycsp)
    -   [**ProviderName**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_providername)
    -   [**Algorithmus**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_algorithm)
    -   [**Keyprotection**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyprotection)
    -   [**ExportPolicy**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_exportpolicy)
3.  Erstellt einen asymmetrischen privaten Schlüssel.
4.  Erstellt ein [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) -Objekt und initialisiert es mit dem privaten Schlüssel.
5.  Erstellt ein [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) -Objekt und initialisiert es mit dem \# in Schritt 4 erstellten PKCS 10-Anforderungs Objekt.
6.  Legt das Flag für den alternativen Signatur Algorithmus auf **Variant \_ true** oder **Variant \_ false** fest, je nachdem, ob eine Alternative Signatur Zeichenfolge in der Befehlszeile angegeben ist. Weitere Informationen finden Sie unter " [**Alternative**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm)zu".
7.  Erstellt eine [*Hash Algorithmus*](/windows/desktop/SecGloss/h-gly) - [*Objekt Kennung*](/windows/desktop/SecGloss/o-gly) (OID) aus dem Algorithmusnamen, der in der Befehlszeile angegeben ist, und legt die OID für das Objekt "CMC Request" fest.
8.  Signiert die Zertifikat Anforderung und codiert Sie mithilfe von [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (der).
9.  Ruft eine Zeichenfolge ab, die die codierte CMC-Zertifikat Anforderung enthält, und speichert Sie in einer Datei. Die encodedefilew-Funktion ist in der Datei "registricommon. cpp" definiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[CMC-Anforderung](cmc-request.md)
</dt> <dt>

[PKCS \# 10-Anforderung](pkcs--10-request.md)
</dt> <dt>

[Verwenden der enthaltenen Beispiele](using-the-included-samples.md)
</dt> <dt>

[**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)
</dt> </dl>

 

 
