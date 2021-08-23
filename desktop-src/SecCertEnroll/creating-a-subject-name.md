---
description: Sie können die IX500DistinguishedName-Schnittstelle verwenden, um einen Betreffnamen aus einer Distinguished Name-Zeichenfolge zu erstellen.
ms.assetid: 78fbf15a-678f-4d87-a309-e70374e3ecee
title: Erstellen eines Betreffnamens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00a7350268c4b7fe5f0d6bde0630bfa7556bc8dd6085e11261456299b725dd57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119670210"
---
# <a name="creating-a-subject-name"></a>Erstellen eines Betreffnamens

Sie können die [**IX500DistinguishedName-Schnittstelle**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) verwenden, um einen Betreffnamen aus einer Distinguished Name-Zeichenfolge zu erstellen. Die Zeichenfolge besteht aus verketteten relativen Distinguished Names (RDNs). Die folgenden RDN-Schlüssel werden von der Zertifikatregistrierungs-API unterstützt.

| Key                               | OID                                             | Beschreibung                                                                                        |
|-----------------------------------|-------------------------------------------------|----------------------------------------------------------------------------------------------------|
| C<br/>                      | NAME DES \_ XCN-OID-LANDS \_ \_<br/>              | Enthält einen aus zwei Buchstaben großen ISO 3166-Länder- oder -Region-Code.<br/>                                  |
| CN<br/>                     | ALLGEMEINE \_ XCN-OID-NAME \_ \_<br/>               | Enthält einen allgemeinen Namen.<br/>                                                                 |
| E<br/> E-Mail<br/>     | XCN \_ OID \_ RSA \_ emailAddr<br/>             | Enthält eine E-Mail-Adresse.<br/>                                                              |
| DC<br/>                     | \_XCN-OID-DOMÄNENKOMPONENTE \_ \_<br/>          | Enthält einen Teil eines DNS-namens (Domain Name System Dns).<br/>                                   |
| G<br/> GivenName<br/> | VORNAME DER \_ XCN-OID \_ \_<br/>                | Enthält den Teil des Namens einer Person, der kein Nachname ist.<br/>                             |
| I<br/>                      | \_XCN-OID-INITIALEN \_<br/>                   | Enthält die Initialen einer Person.<br/>                                                           |
| L<br/>                      | NAME DER \_ XCN-OID-LOKALITÄT \_ \_<br/>             | Enthält den Ortsnamen, der eine Stadt, ein Land oder eine andere geografische Region identifiziert.<br/> |
| O<br/>                      | NAME DER \_ XCN-OID-ORGANISATION \_ \_<br/>         | Enthält den Namen einer Organisation.<br/>                                                   |
| OU<br/>                     | NAME DER \_ XCN-OID-ORGANISATIONSEINHEIT \_ \_ \_<br/> | Enthält den Namen einer Einheitenunterteilung innerhalb einer Organisation.<br/>                         |
| E<br/> ST<br/>        | NAME DES \_ XCN-OID-BUNDESSTAATS \_ ODER DER \_ \_ \_ PROVINZ<br/>  | Enthält den vollständigen Namen eines Bundesstaats oder einer Provinz.<br/>                                          |
| STREET<br/>                 | \_XCN-OID-STRAßENADRESSE \_ \_<br/>            | Enthält die physische Adresse.<br/>                                                          |
| SN<br/>                     | \_ \_ XCN-OID-SUR-NAME \_<br/>                  | Enthält den Familiennamen einer Person.<br/>                                                   |
| T<br/> TITLE-<br/>     | \_XCN-OID-TITEL \_<br/>                      | Enthält den Titel einer Person in der Organisation.<br/>                                     |



 

Wenn Sie ein [**IX500DistinguishedName-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) initialisieren, können Sie das Format des Distinguished Name identifizieren, indem Sie einen Wert aus dem [**X500NameFlags-Enumerationstyp**](/windows/desktop/api/CertEnroll/ne-certenroll-x500nameflags) angeben. Angenommen, der Distinguished Name des Betreffs besteht aus den folgenden RDNs:<dl> CN=Administrator  
CN=Users  
DC=jdomcsc  
DC=nttest  
DC=microsoft  
DC=com  
</dl>

Wenn Sie diese RDNs mit der folgenden durch Trennzeichen getrennten Distinguished Name-Zeichenfolge verketten, können Sie beim Initialisieren eines [**IX500DistinguishedName-Objekts**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) den **XCN \_ CERT \_ NAME STR \_ \_ COMMA \_ FLAG-Wert** angeben.

``` syntax
CN=Administrator,CN=Users,DC=jdomcsc,DC=nttest,DC=microsoft,DC=com
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Codieren eines Betreffnamens](encoding-a-subject-name.md)
</dt> <dt>

[Antragstellernamen](subject-names.md)
</dt> </dl>

 

 




