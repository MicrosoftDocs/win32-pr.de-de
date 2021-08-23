---
description: Listet die von CryptoAPI bereitgestellten Schnittstellen auf.
ms.assetid: f94f0264-78b8-4a28-9d3a-dda55db29897
title: Kryptografieschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5937dce6da8ffa3396c885d00c895b845de9889c2688c6daef4eba5db0beb90b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876100"
---
# <a name="cryptography-interfaces"></a>Kryptografieschnittstellen

Kryptografieschnittstellen werden gemäß der Verwendung wie folgt kategorisiert:

-   [Exportschnittstellen der Server-Engine](#server-engine-export-interfaces)
-   [Importschnittstellen der Server-Engine](#server-engine-import-interfaces)
-   [Codierungsschnittstellen](#encoding-interfaces)
-   [Schnittstellen für die Zertifikatregistrierung](#certificate-enrollment-interfaces)
-   [CAPICOM-Interoperabilitätsschnittstellen](#capicom-interoperability-interfaces)

## <a name="server-engine-export-interfaces"></a>Exportschnittstellen der Server-Engine

Im folgenden Referenzthema werden die Schnittstellen beschrieben, die von der Server-Engine exportiert und von externen Objekten aufgerufen werden.



| Schnittstelle                                                                | BESCHREIBUNG                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertAdmin**](/windows/desktop/api/Certadm/nn-certadm-icertadmin)                                         | Wird von Verwaltungsprogrammen zum Verwalten von Anforderungen, Zertifikaten und Sperrungen verwendet.                                                                                                                                                              |
| [**ICertAdmin2**](/windows/desktop/api/Certadm/nn-certadm-icertadmin2)                                       | Wird von Verwaltungsprogrammen zum Verwalten von Anforderungen, Zertifikaten und Sperrungen verwendet. Ersetzt [**ICertAdmin.**](/windows/desktop/api/Certadm/nn-certadm-icertadmin)                                                                                                                 |
| [**ICertConfig**](/windows/desktop/api/Certcli/nn-certcli-icertconfig)                                       | Wird von Clients verwendet, um Informationen zu den verfügbaren Servern abzurufen.                                                                                                                                                                                 |
| [**ICertConfig2**](/windows/desktop/api/Certcli/nn-certcli-icertconfig2)                                     | Wird von Clients verwendet, um Informationen zu den verfügbaren Servern abzurufen. Ersetzt [**ICertConfig.**](/windows/desktop/api/Certcli/nn-certcli-icertconfig)                                                                                                                                  |
| [**ICertGetConfig**](/windows/desktop/api/Certcli/nn-certcli-icertgetconfig)                                 | Stellt Funktionen zum Abrufen der (während der Clienteinrichtung angegebenen) öffentlichen Konfigurationsdaten für einen [*Zertifikatdienstserver*](../secgloss/c-gly.md) bereit.                |
| [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest)                                     | Wird verwendet, um eine Anforderung an den Server zu senden und die Ergebnisse der Anforderung abzurufen.                                                                                                                                                                        |
| [**ICertRequest2**](/windows/desktop/api/Certcli/nn-certcli-icertrequest2)                                   | Wird verwendet, um eine Anforderung an den Server zu senden und die Ergebnisse der Anforderung abzurufen. Ersetzt [**ICertRequest.**](/windows/desktop/api/Certcli/nn-certcli-icertrequest)                                                                                                                       |
| [**ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit)                               | Wird von [Exitmodulen](exit-modules.md) verwendet, um Zertifikat- und Anforderungseigenschaften abzurufen.                                                                                                                                                             |
| [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy)                           | Wird vom [Richtlinienmodul](policy-modules.md) zum Abrufen und Festlegen von Zertifikat- und Anforderungseigenschaften verwendet.                                                                                                                                              |
| [**ICertView**](/windows/desktop/api/Certview/nn-certview-icertview)                                           | Wird von Clients zum [Anzeigen der Zertifikatdienste-Datenbank](viewing-the-certificate-services-database.md)verwendet.                                                                                                                                 |
| [**ICertView2**](/windows/desktop/api/Certview/nn-certview-icertview2)                                         | Wird von Clients zum Anzeigen der Zertifikatdienste-Datenbank verwendet. Ersetzt [**ICertView.**](/windows/desktop/api/Certview/nn-certview-icertview)                                                                                                                                       |
| [**IEnumCERTVIEWATTRIBUTE**](/windows/desktop/api/Certview/nn-certview-ienumcertviewattribute)                 | Wird von Clients verwendet, um auf die Zertifikatattribute für eine Zeile in der Ansicht Zertifikatdienste zuzugreifen.                                                                                                                                                |
| [**IEnumCERTVIEWCOLUMN**](/windows/desktop/api/Certview/nn-certview-ienumcertviewcolumn)                       | Wird von Clients verwendet, um auf die Datenspalten einer Zeile in der Ansicht Zertifikatdienste zuzugreifen.                                                                                                                                                           |
| [**IEnumCERTVIEWEXTENSION**](/windows/desktop/api/Certview/nn-certview-ienumcertviewextension)                 | Wird von Clients verwendet, um auf die Zertifikaterweiterungsdaten für eine Zeile in der Ansicht Zertifikatdienste zuzugreifen.                                                                                                                                            |
| [**IEnumCERTVIEWROW**](/windows/desktop/api/Certview/nn-certview-ienumcertviewrow)                             | Wird von Clients verwendet, um die Zeilen der Ansicht Zertifikatdienste aufzuzählen.                                                                                                                                                                         |
| [**IOCSPAdmin**](/windows/desktop/api/certadm/nn-certadm-iocspadmin)                                         | Wird von Verwaltungsprogrammen zum Konfigurieren von OCSP-Antwortservern (Online Certificate Status Protocol) verwendet.                                                                                                                                       |
| [**IOCSPCAConfiguration**](/windows/desktop/api/Certadm/nn-certadm-iocspcaconfiguration)                     | Stellt Funktionen zum Konfigurieren eines OCSP-Antwortdiensts für die Verarbeitung von Statusanforderungen für eine bestimmte [*Zertifizierungsstelle*](../secgloss/c-gly.md) bereit.<br/> |
| [**IOCSPCAConfigurationCollection**](/windows/desktop/api/Certadm/nn-certadm-iocspcaconfigurationcollection) | Stellt Funktionen zum Verwalten der Konfigurationen der Zertifizierungsstelle bereit, für die ein OCSP-Antwortdienst Anforderungen verarbeiten kann.                                                                                                                                 |
| [**IOCSPProperty**](/windows/desktop/api/Certadm/nn-certadm-iocspproperty)                                   | Stellt Funktionen zum Konfigurieren eines OCSP-Antwortserverattributs bereit.                                                                                                                                                                         |
| [**IOCSPPropertyCollection**](/windows/desktop/api/Certadm/nn-certadm-iocsppropertycollection)               | Wird von Verwaltungsprogrammen zum Verwalten von OCSP-Antwortserverattributen verwendet.                                                                                                                                                                     |



 

## <a name="server-engine-import-interfaces"></a>Importschnittstellen der Server-Engine

In den folgenden Referenzthemen werden die Schnittstellen beschrieben, die von der Server-Engine importiert werden.



| Schnittstelle                                      | BESCHREIBUNG                                                                                                                            |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit)                 | Von Exitmodulen exportiert. Wird von der Server-Engine verwendet, um fertige Zertifikate und Sperrinformationen bereitzustellen.                       |
| [**ICertExit2**](/windows/desktop/api/Certexit/nn-certexit-icertexit2)               | Fügt [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit)die [**GetManageModule-Methode**](/windows/desktop/api/Certexit/nf-certexit-icertexit2-getmanagemodule) hinzu.                               |
| [**ICertManageModule**](/windows/desktop/api/Certmod/nn-certmod-icertmanagemodule) | Wird von Richtlinien- oder Exitmodulen exportiert. Wird zum Anzeigen von Modulinformationen oder zum Anzeigen einer Benutzeroberfläche für die Konfiguration des Moduls verwendet. |
| [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy)             | Wird vom Richtlinienmodul exportiert. Wird von der Server-Engine verwendet, um Anforderungen zu überprüfen und Eigenschaften für Zertifikate abzurufen.                        |
| [**ICertPolicy2**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy2)           | Fügt die [**GetManageModule-Methode**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy2-getmanagemodule) zu [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy)hinzu.                         |



 

## <a name="encoding-interfaces"></a>Codierungsschnittstellen

In den folgenden Referenzthemen werden die Schnittstellen beschrieben, die von [Erweiterungshandlern](writing-custom-extension-handlers.md) exportiert und vom Richtlinienmodul importiert werden können.



| Schnittstelle                                                | BESCHREIBUNG                                                                                                                                                                                                                                   |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertEncodeAltName**](/windows/desktop/api/Certenc/nn-certenc-icertencodealtname)         | Wird vom [Richtlinienmodul](policy-modules.md) zum Behandeln alternativer Namenserweiterungen verwendet.                                                                                                                                                          |
| [**ICertEncodeBitString**](/windows/desktop/api/Certenc/nn-certenc-icertencodebitstring)     | Wird vom Richtlinienmodul zum Verarbeiten von Bitzeichenfolgen verwendet, die in Zertifikaterweiterungen verwendet werden.                                                                                                                                                               |
| [**ICertEncodeCRLDistInfo**](/windows/desktop/api/Certenc/nn-certenc-icertencodecrldistinfo) | Wird vom Richtlinienmodul zum Verarbeiten von Verteilungsinformationsarrays für [*Zertifikatsperrlisten*](../secgloss/c-gly.md) (Certificate Revocation List, CRL) verwendet, die in Zertifikaterweiterungen verwendet werden. |
| [**ICertEncodeDateArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodedatearray)     | Wird vom Richtlinienmodul  verwendet, um Datumsarrays zu verarbeiten, die in Zertifikaterweiterungen verwendet werden.                                                                                                                                                           |
| [**ICertEncodeLongArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodelongarray)     | Wird vom Richtlinienmodul zum Verarbeiten von **Long-Arrays** verwendet, die in Zertifikaterweiterungen verwendet werden.                                                                                                                                                           |
| [**ICertEncodeStringArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodestringarray) | Wird vom Richtlinienmodul zum Behandeln von **STRING-Arrays** verwendet, die in Zertifikaterweiterungen verwendet werden.                                                                                                                                                         |



 

## <a name="certificate-enrollment-interfaces"></a>Schnittstellen für die Zertifikatregistrierung

In diesem Abschnitt werden die Objekte, Methoden und Eigenschaften des Zertifikatregistrierungssteuerelements sowie das Objekt, die Methoden und eigenschaften beschrieben, die im Smartcard-Registrierungssteuerelement verfügbar sind. Dazu gehören die folgenden Schnittstellen.



| Schnittstelle                                                                                  | BESCHREIBUNG                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICEnroll**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll)                                                               | Eine von mehreren Schnittstellen, die die Zertifikatregistrierungssteuerung darstellen. Dies ist in erster Linie dann von Interesse, wenn Sie Automation nicht verwenden.                                                                        |
| [**ICEnroll2**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll2)                                                             | Eine von mehreren Schnittstellen, die die Zertifikatregistrierungssteuerung darstellen. Dies ist in erster Linie dann von Interesse, wenn Sie Automation nicht verwenden.                                                                        |
| [**ICEnroll3**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll3)                                                             | Eine von mehreren Schnittstellen, die die Zertifikatregistrierungssteuerung darstellen. Dies ist in erster Linie dann von Interesse, wenn Sie Automation nicht verwenden.                                                                        |
| [**ICertificateEnrollmentPolicyServerSetup**](/windows/desktop/api/Casetup/nn-casetup-icertificateenrollmentpolicyserversetup) | Stellt den CEP-Webdienst (Certificate Enrollment Policy) in Active Directory-Zertifikatdienste (ADCS) dar. Mit dem Dienst können Benutzer und Computer Informationen zur Zertifikatregistrierungsrichtlinie abrufen. |
| [**ICertificateEnrollmentServerSetup**](/windows/desktop/api/Casetup/nn-casetup-icertificateenrollmentserversetup)             | Stellt die Zertifikatregistrierungs-Webdienst (CES) in ADCS dar. Der Dienst ermöglicht Es Benutzern und Computern, sich für Zertifikate zu registrieren und diese zu erneuern.                                                               |
| [**ICEnroll4**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll4)                                                             | Eine von mehreren Schnittstellen, die die Zertifikatregistrierungssteuerung darstellen. Dies ist in erster Linie dann von Interesse, wenn Sie Automation nicht verwenden.                                                                        |
| [**IEnroll**](/windows/desktop/api/Xenroll/nn-xenroll-ienroll)                                                                 | Eine von mehreren Schnittstellen, die die Zertifikatregistrierungssteuerung darstellen. Die Schnittstelle ist in erster Linie von Interesse, wenn Sie automation nicht verwenden.                                                             |
| [**IEnroll2**](/windows/desktop/api/Xenroll/nn-xenroll-ienroll2)                                                               | Eine von mehreren Schnittstellen, die die Zertifikatregistrierungssteuerung darstellen. Die Schnittstelle ist in erster Linie von Interesse, wenn Sie automation nicht verwenden.                                                             |
| [**IEnroll4**](/windows/desktop/api/Xenroll/nn-xenroll-ienroll4)                                                               | Eine von mehreren Schnittstellen, die die Zertifikatregistrierungssteuerung darstellen. Die Schnittstelle ist in erster Linie von Interesse, wenn Sie automation nicht verwenden.                                                             |
| [**ISCrdEnr**](iscrdenr.md)                                                               | Stellt das Smartcard-Registrierungssteuerelement dar. Dies ist in erster Linie dann von Interesse, wenn Sie Automation nicht verwenden.                                                                                                       |



 

## <a name="capicom-interoperability-interfaces"></a>CAPICOM-Interoperabilitätsschnittstellen

In den folgenden Referenzthemen werden die Schnittstellen beschrieben, mit denen Ableitungen von CryptoAPI mit CAPICOM 2.0 zusammenarbeiten können.



| Schnittstelle                              | BESCHREIBUNG                                                                                                                                                                              |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertContext**](icertcontext.md)   | Bietet Zugriff auf den Kontext eines CAPICOM X.509v3 [**Certificate-Objekts.**](certificate.md) Dieser Kontext ermöglicht die Verwendung des CAPICOM-Zertifikats in anderen Ableitungen von CryptoAPI. |
| [**ICertStore**](icertstore.md)       | Ermöglicht den Zugriff auf den [](store.md) Kontext eines CAPICOM-Store-Objekts. Dieser Kontext ermöglicht die Verwendung des CAPICOM-Zertifikatspeichers in anderen Ableitungen von CryptoAPI.               |
| [**IChainContext**](ichaincontext.md) | Ermöglicht den Zugriff auf den Kontext eines CAPICOM [**Chain-Objekts.**](chain.md) Dieser Kontext ermöglicht die Verwendung der CAPICOM-Zertifikatvertrauenskette in anderen Ableitungen von CryptoAPI.         |



 

 

 
