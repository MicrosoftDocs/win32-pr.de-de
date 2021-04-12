---
description: Eine Windows-Public Key-Infrastruktur (PKI) speichert Zertifikate auf dem Server, auf dem die Zertifizierungsstelle (Certification Authority, ca) und auf dem lokalen Computer oder Gerät gehostet werden.
ms.assetid: b6aaafeb-30d1-453e-a70c-dcaa01fea1cf
title: Zertifikatsverzeichnis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee525e4d910de1c75516c6aaa27ca41a6cfa17c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218666"
---
# <a name="certificate-directory"></a>Zertifikatsverzeichnis

Eine Windows-Public Key-Infrastruktur (PKI) speichert Zertifikate auf dem Server, auf dem die Zertifizierungsstelle (Certification Authority, ca) und auf dem lokalen Computer oder Gerät gehostet werden. Der ca-Speicher wird in der Regel als Zertifikat Datenbank bezeichnet, und der lokale Speicher wird als Zertifikat Speicher bezeichnet.

## <a name="certificate-database"></a>Zertifikat Datenbank

Wenn Sie Zertifikat Dienste auf einem Windows-Server hinzufügen und eine Zertifizierungsstelle konfigurieren, wird eine Zertifikat Datenbank erstellt. Standardmäßig ist die Datenbank im Ordner *% systemroot%* \\ system32 \\ certlog enthalten, und der Name basiert auf dem Namen der Zertifizierungsstelle mit der Erweiterung EDB. Die Datenbank kann Folgendes enthalten:

-   Ausgestellte Zertifikate
-   Gesperrte Zertifikate
-   Archivierte private Schlüssel
-   Zertifikat Anforderungen

Die Zertifikat Registrierungs-API kann nicht zum Bearbeiten der Datenbank verwendet werden. Beim Registrierungsprozess werden automatisch die erforderlichen Einträge erstellt.

## <a name="certificate-stores"></a>Zertifikatspeicher

Die Microsoft-Zertifikat Dienste kopieren ausgestellte Zertifikate und ausstehende oder abgelehnte Anforderungen auf lokale Computer und Geräte. Der Speicherort wird als Zertifikat Speicher bezeichnet und besteht aus den folgenden logischen Speichern.

| Logischer Speicher                                         | BESCHREIBUNG                                                                                                            |
|-------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Persönlich<br/>                                   | Enthält Zertifikate, die einem privaten Schlüssel zugeordnet sind, der vom Benutzer oder Computer gesteuert wird.<br/>                     |
| Trusted Root Certification Authorities<br/>     | Enthält Zertifikate von implizit vertrauenswürdigen Zertifizierungsstellen (CAS).<br/>                              |
| Organisationsvertrauen<br/>                           | Enthält Zertifikat Vertrauens Listen, die normalerweise verwendet werden, um selbst signierte Zertifikate von anderen Organisationen zu vertrauen.<br/> |
| Zwischenzertifizierungsstellen<br/>     | Enthält Zertifikate, die für in der ZS-Hierarchie untergeordnete Zertifizierungsstellen ausgestellt wurden.<br/>                             |
| Active Directory-Benutzerobjekt<br/>               | Enthält das Benutzerobjekt Zertifikat oder die Zertifikate, die in Active Directory veröffentlicht wurden.<br/>                         |
| Vertrauenswürdige Herausgeber<br/>                         | Enthält Zertifikate von vertrauenswürdigen Zertifizierungsstellen.<br/>                                                                     |
| Nicht vertrauenswürdige Zertifikate<br/>                     | Enthält Zertifikate, die explizit als nicht vertrauenswürdig identifiziert wurden.<br/>                                    |
| Stammzertifizierungsstellen von Drittanbietern<br/> | Enthält vertrauenswürdige Stamm Zertifikate von CAS außerhalb der internen Zertifikat Hierarchie.<br/>                     |
| Vertrauenswürdige Personen<br/>                             | Enthält Zertifikate, die für Benutzer oder Entitäten ausgestellt werden, die explizit vertrauenswürdig sind.<br/>                        |
| Andere Personen<br/>                               | Enthält Zertifikate, die für Benutzer oder Entitäten ausgestellt wurden, die implizit vertrauenswürdig sind.<br/>                        |
| Zertifikatregistrierungsanforderungen<br/>            | Enthält ausstehende oder abgelehnte Zertifikat Anforderungen.<br/>                                                          |



 

Die Zertifikatregistrierungs-API kann nicht zum angeben oder Abrufen von Speicher Eigenschaften oder zum Kopieren von Zertifikaten in bestimmte Speicher verwendet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[PKI-Elemente](about-pki-components.md)
</dt> </dl>

 

 




