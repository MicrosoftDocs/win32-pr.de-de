---
description: Erstellt ein PKCS \# 7-Anforderungs Objekt, um ein vorhandenes Zertifikat zu erneuern. Das Anforderungs Objekt verwendet ein neues Schlüsselpaar, behält jedoch den Kryptografieanbieter bei, der dem erneuert-Zertifikat zugeordnet ist.
ms.assetid: 12a3f1b4-b31e-470e-8ce6-87f497841240
title: enrollRenewalPKCS7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8795758a2744dcee07a100f87eb1db0a1af49eac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529390"
---
# <a name="enrollrenewalpkcs7"></a>enrollRenewalPKCS7

Das enrollRenewalPKCS7-Beispiel erstellt ein PKCS \# 7-Anforderungs Objekt, um ein vorhandenes Zertifikat zu erneuern. Das Anforderungs Objekt verwendet ein neues Schlüsselpaar, behält jedoch den Kryptografieanbieter bei, der dem erneuert-Zertifikat zugeordnet ist.

## <a name="location"></a>Standort

Wenn Sie das Microsoft Windows Software Development Kit (SDK) installieren, wird das Beispiel standardmäßig im Ordner *% Program Files%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Einschreibung \\ VC \\ enrollRenewalPKCS7 installiert.

## <a name="discussion"></a>Diskussion

Das enrollRenewalPKCS7-Beispiel:

1.  Verarbeitet die Befehlszeilenargumente. Die Befehlszeile muss den Namen der Vorlage enthalten, die zum Erstellen der Zertifikat Anforderung verwendet wird.
2.  Ruft ein vorhandenes Zertifikat mit dem Namen der Vorlage ab, die in der Befehlszeile angegeben ist, oder wenn ein Zertifikat nicht gefunden werden kann, versucht, ein Zertifikat mithilfe der Vorlage zu registrieren. Die Funktionen "findcertbytemplate" und "registricertbytemplate" sind in der Datei "registricommon. cpp" definiert.
3.  Überprüft die Zertifikat Kette und konvertiert das Zertifikat in ein **BSTR**.
4.  Erstellt ein [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) -Objekt und initialisiert es mithilfe des vorhandenen Zertifikats. Da der Parameter " *geerbt Options* " auf "geerbt default" festgelegt ist, wird ein neues Schlüsselpaar für die Anforderung erstellt, aber der Kryptografieanbieter im vorhandenen Zertifikat wird verwendet. Weitere Informationen finden Sie unter der [**initializefromcertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate) -Methode.
5.  Erstellt ein [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) -Objekt, initialisiert es mit dem PKCS \# 7-Anforderungs Objekt, versucht, es bei der Zertifizierungsstelle zu registrieren, und überwacht den Status des Registrierungsprozesses. Die Funktion "checkenrollstatus" wird in der Datei "registricommon. cpp" definiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[CMC-Anforderung](cmc-request.md)
</dt> <dt>

[PKCS \# 7-Erneuerungs Anforderung](pkcs--7--renewal-request.md)
</dt> <dt>

[Verwenden der enthaltenen Beispiele](using-the-included-samples.md)
</dt> </dl>

 

 



