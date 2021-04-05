---
description: Erstellt eine CMC-Zertifikat Anforderung und registriert einen Computer in einer Zertifikatshierarchie.
ms.assetid: ef09ef04-8925-4d66-97ad-70b4d7cf78b9
title: Registrier customcmc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2910e6a6ca784aaeb9ca97dc8de106932bd64c9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752736"
---
# <a name="enrollcustomcmc"></a>Registrier customcmc

Das Beispiel "registricustomcmc" erstellt eine CMC-Zertifikat Anforderung und registriert einen Computer in einer Zertifikatshierarchie.

## <a name="location"></a>Standort

Wenn Sie das Microsoft Windows Software Development Kit (SDK) installieren, wird das Beispiel standardmäßig im Ordner *% Program Files%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Registrierung \\ VC \\ registrierungscustomcmc installiert.

## <a name="discussion"></a>Diskussion

Das Beispiel "registricustomcmc":

1.  Verarbeitet die folgenden Befehlszeilenargumente:
    -   Ein benutzerdefiniertes Name-Wert-Paar, das der Zertifikat Anforderung hinzugefügt werden soll.
    -   Ein alternativer Antragsteller Name.
    -   Ein Objekt Bezeichner (OID) für die Erweiterung der erweiterten Schlüssel Verwendung (EKU).
2.  Erstellt ein [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) Request-Objekt und initialisiert es mithilfe des Computer Kontexts.
3.  Verwendet die PKCS \# 10-Anforderung, um ein [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) -Objekt zu initialisieren.
4.  Erstellt ein [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage) -Objekt, indem die in der Befehlszeile angegebene OID verwendet und der Erweiterungs Auflistung für die CMC-Anforderung hinzugefügt wird.
5.  Erstellt das [**ialternativename**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename) -Objekt unter Verwendung des in der Befehlszeile angegebenen Namens, fügt es der [**ialternativenames**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativenames) -Auflistung hinzu, verwendet die Auflistung, um eine [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames) -Erweiterung zu initialisieren, und fügt diese der Erweiterungs Auflistung für die CMC-Anforderung hinzu.
6.  Erstellt ein [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) -Objekt mit dem in der Befehlszeile angegebenen Namen und Wert und fügt es der [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) -Auflistung in der CMC-Anforderung hinzu.
7.  Erstellt ein [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) -Objekt, initialisiert es mit dem Objekt "CMC Request" und ruft eine Zeichenfolge ab, die eine Base64-codierte Anforderung enthält.
8.  Erstellt ein [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) -Objekt und verwendet es, um eine Zeichenfolge abzurufen, die die Zertifizierungsstellen Konfiguration enthält.
9.  Erstellt ein CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) -Objekt und verwendet es sowie die Zeichen folgen, die die Zertifizierungsstellen Konfiguration enthalten, und die Zertifikat Anforderung zum übermitteln der Anforderung an die Zertifizierungsstelle.
10. Überprüft den Übermittlungs Status und installiert, wenn erfolgreich, das Zertifikat im Zertifikat Speicher.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[CMC-Anforderung](cmc-request.md)
</dt> <dt>

[PKCS \# 10-Anforderung](pkcs--10-request.md)
</dt> <dt>

[Verwenden der enthaltenen Beispiele](using-the-included-samples.md)
</dt> </dl>

 

 
