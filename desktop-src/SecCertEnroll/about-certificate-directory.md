---
description: Eine Windows Public Key-Infrastruktur (PKI) speichert Zertifikate auf dem Server, der die Zertifizierungsstelle hostet, und auf dem lokalen Computer oder Gerät.
ms.assetid: b6aaafeb-30d1-453e-a70c-dcaa01fea1cf
title: Zertifikatsverzeichnis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b77a7c63e234460394005aac416d41ff7845470139ba2cb8b700132bea0118c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904829"
---
# <a name="certificate-directory"></a>Zertifikatsverzeichnis

Eine Windows Public Key-Infrastruktur (PKI) speichert Zertifikate auf dem Server, der die Zertifizierungsstelle hostet, und auf dem lokalen Computer oder Gerät. Der ZS-Speicher wird in der Regel als Zertifikatdatenbank bezeichnet, und der lokale Speicher wird als Zertifikatspeicher bezeichnet.

## <a name="certificate-database"></a>Zertifikatdatenbank

Wenn Sie Zertifikatdienste auf einem Windows Server hinzufügen und eine Zertifizierungsstelle konfigurieren, wird eine Zertifikatdatenbank erstellt. Standardmäßig ist die Datenbank im Ordner *%SystemRoot%* \\ System32 \\ Certlog enthalten, und der Name basiert auf dem Namen der Zertifizierungsstelle mit einer EDB-Erweiterung. Die Datenbank kann Folgendes enthalten:

-   Ausgestellte Zertifikate
-   Gesperrte Zertifikate
-   Archivierte private Schlüssel
-   Zertifikatanforderungen

Sie können die Zertifikatregistrierungs-API nicht verwenden, um die Datenbank zu bearbeiten. Der Registrierungsprozess erstellt automatisch die erforderlichen Einträge.

## <a name="certificate-stores"></a>Zertifikatspeicher

Microsoft Certificate Services kopiert ausgestellte Zertifikate und ausstehende oder abgelehnte Anforderungen auf lokale Computer und Geräte. Der Speicherort wird als Zertifikatspeicher bezeichnet und besteht aus den folgenden logischen Speichern.

| Logischer Speicher                                         | BESCHREIBUNG                                                                                                            |
|-------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Persönlich<br/>                                   | Enthält Zertifikate, die einem privaten Schlüssel zugeordnet sind, der vom Benutzer oder Computer gesteuert wird.<br/>                     |
| Trusted Root Certification Authorities<br/>     | Enthält Zertifikate von implizit vertrauenswürdigen Zertifizierungsstellen (CAs).<br/>                              |
| Organisationsvertrauen<br/>                           | Enthält Zertifikatvertrauenslisten, die in der Regel verwendet werden, um selbstsigniert Zertifikaten von anderen Organisationen zu vertrauen.<br/> |
| Zwischenzertifizierungsstellen<br/>     | Enthält Zertifikate, die für in der ZS-Hierarchie untergeordnete Zertifizierungsstellen ausgestellt wurden.<br/>                             |
| Active Directory-Benutzerobjekt<br/>               | Enthält das Benutzerobjektzertifikat oder die in Active Directory veröffentlichten Zertifikate.<br/>                         |
| Vertrauenswürdige Herausgeber<br/>                         | Enthält Zertifikate von vertrauenswürdigen Zertifizierungsstellen.<br/>                                                                     |
| Nicht vertrauenswürdige Zertifikate<br/>                     | Enthält Zertifikate, die explizit als nicht vertrauenswürdig identifiziert wurden.<br/>                                    |
| Stammzertifizierungsstellen von Drittanbietern<br/> | Enthält vertrauenswürdige Stammzertifikate von Zertifizierungsstellen außerhalb der internen Zertifikathierarchie.<br/>                     |
| Vertrauenswürdige Personen<br/>                             | Enthält Zertifikate, die für Benutzer oder Entitäten ausgestellt werden, die explizit als vertrauenswürdig eingestuft wurden.<br/>                        |
| Andere Personen<br/>                               | Enthält Zertifikate, die für Benutzer oder Entitäten ausgestellt werden, denen implizit vertraut wurde.<br/>                        |
| Zertifikatregistrierungsanforderungen<br/>            | Enthält ausstehende oder abgelehnte Zertifikatanforderungen.<br/>                                                          |



 

Sie können die Zertifikatregistrierungs-API nicht verwenden, um Speichereigenschaften anzugeben oder abzurufen oder Zertifikate in bestimmte Speicher zu kopieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[PKI-Elemente](about-pki-components.md)
</dt> </dl>

 

 




