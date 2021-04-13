---
description: Listet die von CryptoAPI bereitgestellten Schnittstellen auf.
ms.assetid: f94f0264-78b8-4a28-9d3a-dda55db29897
title: Kryptografieschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccf5284f5c2107e741fd91e2936ff3dea0853e71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343129"
---
# <a name="cryptography-interfaces"></a>Kryptografieschnittstellen

Kryptografieschnittstellen werden gemäß der Verwendung wie folgt kategorisiert:

-   [Server-Engine-Export Schnittstellen](#server-engine-export-interfaces)
-   [Server-Engine-Import Schnittstellen](#server-engine-import-interfaces)
-   [Codierungs Schnittstellen](#encoding-interfaces)
-   [Zertifikat Registrierungs Schnittstellen](#certificate-enrollment-interfaces)
-   [CAPICOM-Interoperabilitäts Schnittstellen](#capicom-interoperability-interfaces)

## <a name="server-engine-export-interfaces"></a>Server-Engine-Export Schnittstellen

Im folgenden Referenz Thema werden die Schnittstellen beschrieben, die von der Server-Engine exportiert und von externen Objekten aufgerufen werden.



| Schnittstelle                                                                | BESCHREIBUNG                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertAdmin**](/windows/desktop/api/Certadm/nn-certadm-icertadmin)                                         | Wird von Verwaltungsprogrammen zur Verwaltung von Anforderungen, Zertifikaten und Widerruf verwendet.                                                                                                                                                              |
| [**ICertAdmin2**](/windows/desktop/api/Certadm/nn-certadm-icertadmin2)                                       | Wird von Verwaltungsprogrammen zur Verwaltung von Anforderungen, Zertifikaten und Widerruf verwendet. Ersetzt [**ICertAdmin**](/windows/desktop/api/Certadm/nn-certadm-icertadmin).                                                                                                                 |
| [**ICertConfig**](/windows/desktop/api/Certcli/nn-certcli-icertconfig)                                       | Wird von Clients verwendet, um Informationen zu den verfügbaren Servern zu erhalten.                                                                                                                                                                                 |
| [**ICertConfig2**](/windows/desktop/api/Certcli/nn-certcli-icertconfig2)                                     | Wird von Clients verwendet, um Informationen zu den verfügbaren Servern zu erhalten. Ersetzt [**ICertConfig**](/windows/desktop/api/Certcli/nn-certcli-icertconfig).                                                                                                                                  |
| [**ICertGetConfig**](/windows/desktop/api/Certcli/nn-certcli-icertgetconfig)                                 | Stellt Funktionen bereit, mit denen die während der Client Installation angegebenen öffentlichen Konfigurationsdaten für einen [*Zertifikat Dienst*](../secgloss/c-gly.md) Server abgerufen werden.                |
| [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest)                                     | Wird verwendet, um eine Anforderung an den Server zu senden und die Ergebnisse der Anforderung zu erhalten.                                                                                                                                                                        |
| [**ICertRequest2**](/windows/desktop/api/Certcli/nn-certcli-icertrequest2)                                   | Wird verwendet, um eine Anforderung an den Server zu senden und die Ergebnisse der Anforderung zu erhalten. Ersetzt [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest).                                                                                                                       |
| [**Icertserverexit**](/windows/desktop/api/Certif/nn-certif-icertserverexit)                               | Wird von [Exit-Modulen](exit-modules.md) verwendet, um Zertifikat-und Anforderungs Eigenschaften zu erhalten.                                                                                                                                                             |
| [**Icertserverpolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy)                           | Wird vom- [Richtlinien Modul](policy-modules.md) verwendet, um Zertifikat-und Anforderungs Eigenschaften zu erhalten und festzulegen.                                                                                                                                              |
| [**Icertview**](/windows/desktop/api/Certview/nn-certview-icertview)                                           | Wird von Clients zum [Anzeigen der Zertifikat Dienst Datenbank](viewing-the-certificate-services-database.md)verwendet.                                                                                                                                 |
| [**ICertView2**](/windows/desktop/api/Certview/nn-certview-icertview2)                                         | Wird von Clients zum Anzeigen der Zertifikat Dienst Datenbank verwendet. Ersetzt [**icertview**](/windows/desktop/api/Certview/nn-certview-icertview).                                                                                                                                       |
| [**Ienumcertviewattribute**](/windows/desktop/api/Certview/nn-certview-ienumcertviewattribute)                 | Wird von Clients verwendet, um auf die Zertifikat Attribute für eine Zeile in der Zertifikat Dienst Ansicht zuzugreifen.                                                                                                                                                |
| [**Ienumcertviewcolumn**](/windows/desktop/api/Certview/nn-certview-ienumcertviewcolumn)                       | Wird von Clients verwendet, um auf die Datenspalten einer Zeile in der Zertifikat Dienst Ansicht zuzugreifen.                                                                                                                                                           |
| [**Ienumcertviewextension**](/windows/desktop/api/Certview/nn-certview-ienumcertviewextension)                 | Wird von Clients verwendet, um auf die Zertifikat Erweiterungs Daten für eine Zeile in der Zertifikat Dienst Ansicht zuzugreifen.                                                                                                                                            |
| [**Ienumcertviewrow**](/windows/desktop/api/Certview/nn-certview-ienumcertviewrow)                             | Wird von Clients verwendet, um die Zeilen der Zertifikat Dienst Ansicht aufzulisten.                                                                                                                                                                         |
| [**IOCSPAdmin**](/windows/desktop/api/certadm/nn-certadm-iocspadmin)                                         | Wird von Verwaltungsprogrammen verwendet, um OCSP-responderserver (Online Certificate Status-Protokoll) zu konfigurieren.                                                                                                                                       |
| [**Iocspcaconfiguration**](/windows/desktop/api/Certadm/nn-certadm-iocspcaconfiguration)                     | Stellt Funktionen bereit, mit denen ein OCSP-Beantworter-Dienst zum Verarbeiten von Status Anforderungen für eine bestimmte [*Zertifizierungs*](../secgloss/c-gly.md) Stelle konfiguriert werden können.<br/> |
| [**Iocspcaconfigurationcollection**](/windows/desktop/api/Certadm/nn-certadm-iocspcaconfigurationcollection) | Stellt Funktionen zum Verwalten der Zertifizierungsstellen Konfigurationen bereit, für die ein OCSP-Beantworter-Dienst Anforderungen verarbeiten kann.                                                                                                                                 |
| [**Iocspproperty**](/windows/desktop/api/Certadm/nn-certadm-iocspproperty)                                   | Stellt Funktionen zum Konfigurieren eines OCSP-Beantworter-Server Attributs bereit.                                                                                                                                                                         |
| [**Iocsppropertycollection**](/windows/desktop/api/Certadm/nn-certadm-iocsppropertycollection)               | Wird von Verwaltungsprogrammen zum Verwalten von OCSP-Beantworter-Server Attributen verwendet.                                                                                                                                                                     |



 

## <a name="server-engine-import-interfaces"></a>Server-Engine-Import Schnittstellen

In den folgenden Referenz Themen werden die Schnittstellen beschrieben, die von der Server-Engine importiert werden.



| Schnittstelle                                      | BESCHREIBUNG                                                                                                                            |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Icertexit**](/windows/desktop/api/Certexit/nn-certexit-icertexit)                 | Exportiert durch Exit-Module. Wird von der Server-Engine verwendet, um fertige Zertifikate und Sperrinformationen bereitzustellen.                       |
| [**ICertExit2**](/windows/desktop/api/Certexit/nn-certexit-icertexit2)               | Fügt [**icertexit**](/windows/desktop/api/Certexit/nn-certexit-icertexit)die [**getmanagemodule**](/windows/desktop/api/Certexit/nf-certexit-icertexit2-getmanagemodule) -Methode hinzu.                               |
| [**Icertmanagemodule**](/windows/desktop/api/Certmod/nn-certmod-icertmanagemodule) | Exportiert nach Richtlinien-oder Beendigungs Modulen. Wird verwendet, um Modul Informationen anzuzeigen oder um eine Benutzeroberfläche für die Konfiguration des Moduls anzuzeigen. |
| [**Icertpolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy)             | Wird vom-Richtlinien Modul exportiert. Wird von der Server-Engine verwendet, um Anforderungen zu überprüfen und Eigenschaften für Zertifikate zu erhalten.                        |
| [**ICertPolicy2**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy2)           | Fügt [**icertpolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy)die [**getmanagemodule**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy2-getmanagemodule) -Methode hinzu.                         |



 

## <a name="encoding-interfaces"></a>Codierungs Schnittstellen

In den folgenden Referenz Themen werden die Schnittstellen beschrieben, die von [Erweiterungs Handlern](writing-custom-extension-handlers.md) exportiert und durch das-Richtlinien Modul importiert werden können.



| Schnittstelle                                                | BESCHREIBUNG                                                                                                                                                                                                                                   |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Icertencodealtname**](/windows/desktop/api/Certenc/nn-certenc-icertencodealtname)         | Wird vom- [Richtlinien Modul](policy-modules.md) verwendet, um alternative namens Erweiterungen zu verarbeiten.                                                                                                                                                          |
| [**Icertencodebitstring**](/windows/desktop/api/Certenc/nn-certenc-icertencodebitstring)     | Wird vom-Richtlinien Modul verwendet, um in Zertifikat Erweiterungen verwendete Bitzeichenfolgen zu verarbeiten.                                                                                                                                                               |
| [**Icertencodecrldistinfo**](/windows/desktop/api/Certenc/nn-certenc-icertencodecrldistinfo) | Wird vom-Richtlinien Modul verwendet, um die in Zertifikat Erweiterungen verwendeten CRL-Verteilungs Informations Arrays [*zu verarbeiten.*](../secgloss/c-gly.md) |
| [**Icertencodedatearray**](/windows/desktop/api/Certenc/nn-certenc-icertencodedatearray)     | Wird vom-Richtlinien Modul verwendet, um **Datums** Arrays zu verarbeiten, die in Zertifikat Erweiterungen verwendet werden.                                                                                                                                                           |
| [**Icertencodelta ongarray**](/windows/desktop/api/Certenc/nn-certenc-icertencodelongarray)     | Wird vom-Richtlinien Modul verwendet, um **lange** Arrays zu verarbeiten, die in Zertifikat Erweiterungen verwendet werden.                                                                                                                                                           |
| [**Icertencodestringarray**](/windows/desktop/api/Certenc/nn-certenc-icertencodestringarray) | Wird vom Richtlinien Modul verwendet, um **Zeichen** folgen Arrays zu verarbeiten, die in Zertifikat Erweiterungen verwendet werden.                                                                                                                                                         |



 

## <a name="certificate-enrollment-interfaces"></a>Zertifikat Registrierungs Schnittstellen

In diesem Abschnitt werden die Objekte, Methoden und Eigenschaften der Zertifikat Registrierungs Steuerung sowie das Objekt, die Methoden und die Eigenschaften beschrieben, die in der Smartcard-Registrierungs Steuerung zur Verfügung stehen. Hierzu gehören die folgenden Schnittstellen.



| Schnittstelle                                                                                  | BESCHREIBUNG                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Icenroll**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll)                                                               | Eine von mehreren Schnittstellen, die das Zertifikat Registrierungs Steuerelement darstellen. Dies ist in erster Linie von Interesse, wenn Sie keine Automatisierung verwenden.                                                                        |
| [**ICEnroll2**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll2)                                                             | Eine von mehreren Schnittstellen, die das Zertifikat Registrierungs Steuerelement darstellen. Dies ist in erster Linie von Interesse, wenn Sie keine Automatisierung verwenden.                                                                        |
| [**ICEnroll3**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll3)                                                             | Eine von mehreren Schnittstellen, die das Zertifikat Registrierungs Steuerelement darstellen. Dies ist in erster Linie von Interesse, wenn Sie keine Automatisierung verwenden.                                                                        |
| [**Icertificateregistrimentpolicyserversetup**](/windows/desktop/api/Casetup/nn-casetup-icertificateenrollmentpolicyserversetup) | Stellt den CEP-Webdienst (Certificate Anmeldungs Richtlinie) in Active Directory Zertifikat Diensten (ADCs) dar. Der-Dienst ermöglicht Benutzern und Computern das Abrufen von Informationen zur Zertifikat Registrierungs Richtlinie. |
| [**Icertificateregistrimentserversetup**](/windows/desktop/api/Casetup/nn-casetup-icertificateenrollmentserversetup)             | Stellt die Zertifikatregistrierungs-Webdienst (CES) innerhalb von ADCs dar. Der-Dienst ermöglicht Benutzern und Computern das registrieren und erneuern von Zertifikaten.                                                               |
| [**ICEnroll4**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll4)                                                             | Eine von mehreren Schnittstellen, die das Zertifikat Registrierungs Steuerelement darstellen. Dies ist in erster Linie von Interesse, wenn Sie keine Automatisierung verwenden.                                                                        |
| [**Ienroll**](/windows/desktop/api/Xenroll/nn-xenroll-ienroll)                                                                 | Eine von mehreren Schnittstellen, die das Zertifikat Registrierungs Steuerelement darstellen. Die Schnittstelle ist in erster Linie von Interesse, wenn Sie keine Automatisierung verwenden.                                                             |
| [**IEnroll2**](/windows/desktop/api/Xenroll/nn-xenroll-ienroll2)                                                               | Eine von mehreren Schnittstellen, die das Zertifikat Registrierungs Steuerelement darstellen. Die Schnittstelle ist in erster Linie von Interesse, wenn Sie keine Automatisierung verwenden.                                                             |
| [**IEnroll4**](/windows/desktop/api/Xenroll/nn-xenroll-ienroll4)                                                               | Eine von mehreren Schnittstellen, die das Zertifikat Registrierungs Steuerelement darstellen. Die Schnittstelle ist in erster Linie von Interesse, wenn Sie keine Automatisierung verwenden.                                                             |
| [**Iscrdenr**](iscrdenr.md)                                                               | Stellt die Smartcard-Registrierungs Steuerung dar. Dies ist in erster Linie von Interesse, wenn Sie keine Automatisierung verwenden.                                                                                                       |



 

## <a name="capicom-interoperability-interfaces"></a>CAPICOM-Interoperabilitäts Schnittstellen

In den folgenden Referenz Themen werden die Schnittstellen beschrieben, mit denen die Ableitung von CryptoAPI mit CAPICOM 2,0 zusammenarbeiten kann.



| Schnittstelle                              | BESCHREIBUNG                                                                                                                                                                              |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Icertcontext**](icertcontext.md)   | Bietet Zugriff auf den Kontext eines CAPICOM X. 509v3- [**Zertifikat**](certificate.md) Objekts. In diesem Kontext kann das CAPICOM-Zertifikat in anderen Ableitungen von CryptoAPI verwendet werden. |
| [**Icertstore**](icertstore.md)       | Bietet Zugriff auf den Kontext eines CAPICOM- [**Speicher**](store.md) Objekts. In diesem Kontext kann der CAPICOM-Zertifikat Speicher in anderen Ableitungen von CryptoAPI verwendet werden.               |
| [**Ichaincontext**](ichaincontext.md) | Bietet Zugriff auf den Kontext eines CAPICOM- [**Ketten**](chain.md) Objekts. In diesem Kontext kann die CAPICOM-Zertifikats Vertrauenskette in anderen Ableitungen von CryptoAPI verwendet werden.         |



 

 

 
