---
description: Erstellt ein PKCS \# 7-Anforderungsobjekt, um ein vorhandenes Zertifikat zu erneuern. Das Anforderungsobjekt verwendet ein neues Schlüsselpaar, behält jedoch den Kryptografieanbieter bei, der dem zu erneuernden Zertifikat zugeordnet ist.
ms.assetid: 12a3f1b4-b31e-470e-8ce6-87f497841240
title: enrollRenewalPKCS7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3da14719cc2a9e6bdf4c16cad57d24b9ee4ec0c2ee955cc8b7c20643b2b6f9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119740430"
---
# <a name="enrollrenewalpkcs7"></a>enrollRenewalPKCS7

Im Beispiel enrollRenewalPKCS7 wird ein PKCS \# 7-Anforderungsobjekt erstellt, um ein vorhandenes Zertifikat zu erneuern. Das Anforderungsobjekt verwendet ein neues Schlüsselpaar, behält jedoch den Kryptografieanbieter bei, der dem zu erneuernden Zertifikat zugeordnet ist.

## <a name="location"></a>Standort

Wenn Sie das Microsoft Windows Software Development Kit (SDK) installieren, wird das Beispiel standardmäßig im Ordner *%ProgramFiles%* \\ Microsoft SDKs Windows \\ \\ v7.0 \\ Samples Security \\ \\ X509 Certificate Enrollment \\ VC \\ enrollRenewalPKCS7 installiert.

## <a name="discussion"></a>Diskussion (Discussion)

Das Beispiel enrollRenewalPKCS7:

1.  Verarbeitet die Befehlszeilenargumente. Die Befehlszeile sollte den Namen der Vorlage enthalten, die zum Erstellen der Zertifikatanforderung verwendet wird.
2.  Ruft ein vorhandenes Zertifikat ab, indem der Name der in der Befehlszeile angegebenen Vorlage verwendet wird, oder, wenn kein Zertifikat gefunden werden kann, versucht, ein Zertifikat mithilfe der Vorlage zu registrieren. Die Funktionen findCertByTemplate und enrollCertByTemplate werden in enrollCommon.cpp definiert.
3.  Überprüft die Zertifikatkette und konvertiert das Zertifikat in einen **BSTR.**
4.  Erstellt ein [**IX509CertificateRequestPkcs7-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) und initialisiert es mithilfe des vorhandenen Zertifikats. Da der *parameter inheritOptions* auf InheritDefault festgelegt ist, wird ein neues Schlüsselpaar für die Anforderung erstellt, aber der Kryptografieanbieter im vorhandenen Zertifikat wird verwendet. Weitere Informationen finden Sie in der [**InitializeFromCertificate-Methode.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate)
5.  Erstellt ein [**IX509Enrollment-Objekt,**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) initialisiert es mithilfe des PKCS \# 7-Anforderungsobjekts, versucht, es bei der Zertifizierungsstelle zu registrieren, und überwacht den Status des Registrierungsprozesses. Die checkEnrollStatus-Funktion ist in enrollCommon.cpp definiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[CMC-Anforderung](cmc-request.md)
</dt> <dt>

[PKCS \# 7-Verlängerungsanforderung](pkcs--7--renewal-request.md)
</dt> <dt>

[Verwenden der enthaltenen Beispiele](using-the-included-samples.md)
</dt> </dl>

 

 



