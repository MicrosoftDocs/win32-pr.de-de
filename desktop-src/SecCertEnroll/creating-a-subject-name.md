---
description: Mit der IX500DistinguishedName-Schnittstelle können Sie einen Antragsteller Namen aus einer Distinguished Name-Zeichenfolge erstellen.
ms.assetid: 78fbf15a-678f-4d87-a309-e70374e3ecee
title: Erstellen eines Antragsteller namens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fe512be48c9a727857c4fac4abc6e04a705b7f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525097"
---
# <a name="creating-a-subject-name"></a>Erstellen eines Antragsteller namens

Mit der [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) -Schnittstelle können Sie einen Antragsteller Namen aus einer Distinguished Name-Zeichenfolge erstellen. Die Zeichenfolge besteht aus verketteten relativen Distinguished Names (rDNS). Die folgenden RDN-Schlüssel werden von der Zertifikatregistrierungs-API unterstützt.

| Schlüssel                               | OID                                             | BESCHREIBUNG                                                                                        |
|-----------------------------------|-------------------------------------------------|----------------------------------------------------------------------------------------------------|
| C<br/>                      | XCN- \_ OID- \_ Länder \_ Name<br/>              | Enthält einen aus zwei Buchstaben bestehenden Code für ISO 3166-Länder oder-Regionen.<br/>                                  |
| CN<br/>                     | allgemeiner Name der XCN- \_ OID \_ \_<br/>               | Enthält einen allgemeinen Namen.<br/>                                                                 |
| E<br/> E-Mail<br/>     | XCN \_ OID \_ RSA \_ EmailAddr<br/>             | Enthält eine e-Mail-Adresse.<br/>                                                              |
| SL<br/>                     | XCN \_ OID- \_ Domänen \_ Komponente<br/>          | Enthält einen Teil eines Domain Name System-namens (DNS).<br/>                                   |
| G<br/> GivenName<br/> | Vorname der XCN- \_ OID \_ \_<br/>                | Enthält den Teil des Namens einer Person, bei dem es sich nicht um einen Nachnamen handelt.<br/>                             |
| I<br/>                      | XCN- \_ OID- \_ Initialen<br/>                   | Enthält die Initialen einer Person.<br/>                                                           |
| L<br/>                      | XCN- \_ OID- \_ lokalitäts \_ Name<br/>             | Enthält den Ortsnamen, der eine Stadt, ein Land oder eine andere geografische Region identifiziert.<br/> |
| O<br/>                      | Name der XCN- \_ OID- \_ Organisation \_<br/>         | Enthält den Namen einer Organisation.<br/>                                                   |
| OU<br/>                     | Name der \_ \_ Organisations \_ Einheit \_ für XCN OID<br/> | Enthält den Namen einer Einheiten Teildivision innerhalb einer Organisation.<br/>                         |
| E<br/> ST<br/>        | XCN- \_ OID- \_ Status \_ oder \_ Provinz \_ Name<br/>  | Enthält den vollständigen Namen eines Bundesstaats oder Provinz-.<br/>                                          |
| STREET<br/>                 | XCN- \_ OID- \_ Straße \_<br/>            | Enthält die physische Adresse.<br/>                                                          |
| SN<br/>                     | XCN \_ OID \_ - \_ Name<br/>                  | Enthält den Familiennamen einer Person.<br/>                                                   |
| T<br/> TITLE-<br/>     | XCN- \_ OID- \_ Titel<br/>                      | Enthält den Titel einer Person in der Organisation.<br/>                                     |



 

Wenn Sie ein [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) -Objekt initialisieren, können Sie das Format des Distinguished Name-Objekts identifizieren, indem Sie einen Wert aus dem [**X500NameFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-x500nameflags) -Enumerationstyp angeben. Nehmen Sie beispielsweise an, dass der Distinguished Name des Antragstellers aus folgendem RDNs besteht:<dl> CN = Administrator  
CN = Benutzer  
DC = jdomcsc  
DC = nttest  
DC = Microsoft  
DC = com  
</dl>

Wenn Sie diese RDNs in der folgenden durch Trennzeichen getrennten Distinguished Name-Zeichenfolge verketten, können Sie beim Initialisieren eines [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) -Objekts den Wert für den **XCN \_ CERT \_ Name \_ Str-Komma- \_ \_ Flag** angeben.

``` syntax
CN=Administrator,CN=Users,DC=jdomcsc,DC=nttest,DC=microsoft,DC=com
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Codieren eines Antragsteller namens](encoding-a-subject-name.md)
</dt> <dt>

[Antragstellernamen](subject-names.md)
</dt> </dl>

 

 




