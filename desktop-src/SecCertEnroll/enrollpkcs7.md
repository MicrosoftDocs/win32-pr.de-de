---
description: Erstellt eine PKCS \# 7-Anforderung von einem vorhandenen Zertifikat, indem die öffentlichen und privaten Schlüssel und die Zertifikat Vorlage geerbt werden.
ms.assetid: e7df1a2e-5674-4cc6-874b-45bcc7e25127
title: enrollPKCS7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34bc7f9d7b7d5ae9fa88db0dd70c177c3aa69da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750017"
---
# <a name="enrollpkcs7"></a>enrollPKCS7

Das enrollPKCS7-Beispiel erstellt eine PKCS \# 7-Anforderung von einem vorhandenen Zertifikat, indem die öffentlichen und privaten Schlüssel und die Zertifikat Vorlage geerbt werden. Das vorhandene Zertifikat wird verwendet, um die Anforderung zu signieren. In diesem Beispiel wird der Benutzer in einer Zertifikat Hierarchie registriert und die Zertifikats Antwort installiert. Im Beispiel wird ein vorhandenes Zertifikat verwendet, um ein neues Zertifikat zu registrieren und zu installieren. Weitere Informationen zum Erneuern eines vorhandenen Zertifikats finden Sie unter [enrollRenewalPKCS7](enrollrenewalpkcs7.md).

## <a name="location"></a>Standort

Wenn Sie das Microsoft Windows Software Development Kit (SDK) installieren, wird das Beispiel standardmäßig im Ordner *% Program Files%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Einschreibung \\ VC \\ enrollPKCS7 installiert.

## <a name="discussion"></a>Diskussion

Das enrollPKCS7-Beispiel:

1.  Verarbeitet die Befehlszeilenargumente. Die Befehlszeile muss den Namen der Zertifikat Vorlage enthalten, die für die Suche nach einem vorhandenen Zertifikat verwendet wird.
2.  Ruft ein vorhandenes Zertifikat mit dem Namen der Vorlage ab, die in der Befehlszeile angegeben ist, oder wenn ein Zertifikat nicht gefunden werden kann, versucht, eine neue zu registrieren, die mithilfe der Vorlage erstellt wurde. Die Funktionen "findcertbytemplate" und "registricertbytemplate" sind in der Datei "registricommon. cpp" definiert.
3.  Überprüft die Zertifikat Kette und konvertiert das Zertifikat in ein **BSTR**.
4.  Erstellt ein [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) -Objekt und initialisiert es mithilfe des vorhandenen Zertifikats. Das neue PKCS \# 7-Anforderungs Objekt erbt die privaten und öffentlichen Schlüssel und die Vorlage aus dem vorhandenen Zertifikat.
5.  Erstellt ein [**isignercertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) -Objekt, initialisiert es mit dem vorhandenen Zertifikat und fügt es dem PKCS 7- \# Anforderungs Objekt hinzu.
6.  Erstellt ein [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) -Objekt, initialisiert es mit dem PKCS \# 7-Anforderungs Objekt, versucht, es bei der Zertifizierungsstelle zu registrieren, und überwacht den Status des Registrierungsprozesses. Die Funktion "checkenrollstatus" wird in der Datei "registricommon. cpp" definiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[CMC-Anforderung](cmc-request.md)
</dt> <dt>

[Verwenden der enthaltenen Beispiele](using-the-included-samples.md)
</dt> </dl>

 

 



