---
description: Erstellt ein CMC-Anforderungsobjekt aus einer inner geschachtelten PKCS \# 10-Anforderung.
ms.assetid: 8a0dc078-22ca-4bff-9cc0-46823912d3da
title: createCNGCustomCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0494fdf2af9e4e96983ed1aff462b38e749516eafe87f645a3bf8ae1b342292d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119798270"
---
# <a name="createcngcustomcmc"></a>createCNGCustomCMC

Im Beispiel createCNGCustomCMC wird ein CMC-Anforderungsobjekt aus einer inner geschachtelten PKCS \# 10-Anforderung erstellt. Die innere Anforderung wird mithilfe eines asymmetrischen [*privaten Schlüssels erstellt.*](/windows/desktop/SecGloss/p-gly) Der private Schlüssel wird mithilfe des Kryptografieanbieters Cryptography API: Next Generation (CNG) und des in der Befehlszeile angegebenen Algorithmus erstellt. Benutzerdefinierte Optionen wie Exportrichtlinie und Schlüsselschutzebene werden auch für den privaten Schlüssel festgelegt.

## <a name="location"></a>Standort

Wenn Sie das Microsoft Windows Software Development Kit (SDK) installieren, wird das Beispiel standardmäßig im Ordner *%ProgramFiles%* \\ Microsoft SDKs Windows \\ \\ v7.0 \\ Samples Security \\ \\ X509 Certificate Enrollment \\ VC \\ createCNGCustomCMC installiert.

## <a name="discussion"></a>Diskussion (Discussion)

Das createCNGCustomCMC-Beispiel:

1.  Verarbeitet die folgenden Befehlszeilenargumente:
    -   Der Name eines [](/windows/desktop/SecGloss/c-gly) CNG-Kryptografiedienstanbieters (CSP).
    -   Der Name des Algorithmus, der zum Generieren eines asymmetrischen privaten Schlüssels verwendet wird.
    -   Der Name des Algorithmus, der zum Hashen [*der Zertifikatanforderung*](/windows/desktop/SecGloss/h-gly) [*verwendet wird.*](/windows/desktop/SecGloss/c-gly)
    -   Eine Ausgabedatei, in der die Zertifikatanforderung gespeichert werden soll.
    -   Eine optionale Zeichenfolge (AlternateSignature), die, falls vorhanden, angibt, dass ein diskreter anstelle eines kombinierten Signaturalgorithmus verwendet wird. Weitere Informationen finden Sie unter [**der AlternateSignatureAlgorithm-Eigenschaft.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm)
2.  Erstellt ein [**IX509PrivateKey-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) und legt die folgenden Eigenschaften fest:
    -   [**LegacyCsp**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_legacycsp)
    -   [**ProviderName**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_providername)
    -   [**Algorithmus**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_algorithm)
    -   [**KeyProtection**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyprotection)
    -   [**ExportPolicy**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_exportpolicy)
3.  Erstellt einen asymmetrischen privaten Schlüssel.
4.  Erstellt ein [**IX509CertificateRequestPkcs10-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) und initialisiert es mit dem privaten Schlüssel.
5.  Erstellt ein [**IX509CertificateRequestCmc-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) und initialisiert es mithilfe des in Schritt 4 erstellten PKCS \# 10-Anforderungsobjekts.
6.  Legt das alternative Signaturalgorithmusflag abhängig davon, ob eine alternative Signaturzeichenfolge in der Befehlszeile angegeben ist, auf **VARIANT \_ TRUE** oder **VARIANT \_ FALSE** fest. Weitere Informationen finden Sie unter [**AlternateSignatureAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm).
7.  Erstellt einen [*Hashalgorithmus-Objektbezeichner (Hashing Algorithm*](/windows/desktop/SecGloss/h-gly) [*Object Identifier,*](/windows/desktop/SecGloss/o-gly) OID) aus dem in der Befehlszeile angegebenen Algorithmusnamen und legt die OID für das CMC-Anforderungsobjekt fest.
8.  Signiert die Zertifikatanforderung und codiert sie mit [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER).
9.  Ruft eine Zeichenfolge ab, die die codierte CMC-Zertifikatanforderung enthält, und speichert sie in einer Datei. Die EncodeToFileW-Funktion ist in EnrollCommon.cpp definiert.

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

 

 
