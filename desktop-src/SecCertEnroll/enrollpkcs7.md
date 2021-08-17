---
description: Erstellt eine PKCS 7-Anforderung aus einem vorhandenen Zertifikat, indem die öffentlichen und privaten Schlüssel und \# die Zertifikatvorlage geerbt werden.
ms.assetid: e7df1a2e-5674-4cc6-874b-45bcc7e25127
title: enrollPKCS7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0635fdf4daacc9c7a04db98c7e34e9d3495c6f18ca3e145b166f19e3cd49610a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117779951"
---
# <a name="enrollpkcs7"></a>enrollPKCS7

Im Beispiel enrollPKCS7 wird eine PKCS 7-Anforderung aus einem vorhandenen Zertifikat erstellt, indem die öffentlichen und privaten Schlüssel und die \# Zertifikatvorlage geerbt werden. Das vorhandene Zertifikat wird zum Signieren der Anforderung verwendet. In diesem Beispiel wird der Benutzer in einer Zertifikathierarchie registriert und die Zertifikatantwort installiert. Im Beispiel wird ein vorhandenes Zertifikat zum Registrieren und Installieren eines neuen Zertifikats verwendet. Weitere Informationen zum Erneuern eines vorhandenen Zertifikats finden Sie unter [enrollRenewalPKCS7](enrollrenewalpkcs7.md).

## <a name="location"></a>Standort

Wenn Sie das Microsoft Windows Software Development Kit (SDK) installieren, wird das Beispiel standardmäßig im Ordner *%ProgramFiles%* \\ Microsoft SDKs Windows \\ \\ v7.0 \\ Samples Security \\ \\ X509 Certificate Enrollment \\ VC \\ enrollPKCS7 installiert.

## <a name="discussion"></a>Diskussion (Discussion)

Beispiel für enrollPKCS7:

1.  Verarbeitet die Befehlszeilenargumente. Die Befehlszeile sollte den Namen der Zertifikatvorlage enthalten, die zum Suchen eines vorhandenen Zertifikats verwendet wird.
2.  Ruft ein vorhandenes Zertifikat mithilfe des in der Befehlszeile angegebenen Namens der Vorlage ab oder versucht, ein neues, mithilfe der Vorlage erstelltes Zertifikat zu registrieren, wenn kein Zertifikat gefunden werden kann. Die Funktionen findCertByTemplate und enrollCertByTemplate sind in enrollCommon.cpp definiert.
3.  Überprüft die Zertifikatkette und konvertiert das Zertifikat in einen **BSTR.**
4.  Erstellt ein [**IX509CertificateRequestPkcs7-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) und initialisiert es mithilfe des vorhandenen Zertifikats. Das neue PKCS \# 7-Anforderungsobjekt erbt die privaten und öffentlichen Schlüssel und die Vorlage vom vorhandenen Zertifikat.
5.  Erstellt ein [**ISignerCertificate-Objekt,**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) initialisiert es mithilfe des vorhandenen Zertifikats und fügt es dem PKCS \# 7-Anforderungsobjekt hinzu.
6.  Erstellt ein [**IX509Enrollment-Objekt,**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) initialisiert es mithilfe des PKCS 7-Anforderungsobjekts, versucht, es bei der Zertifizierungsstelle zu registrieren, und überwacht den Status des \# Registrierungsprozesses. Die checkEnrollStatus-Funktion ist in enrollCommon.cpp definiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[CMC-Anforderung](cmc-request.md)
</dt> <dt>

[Verwenden der enthaltenen Beispiele](using-the-included-samples.md)
</dt> </dl>

 

 



