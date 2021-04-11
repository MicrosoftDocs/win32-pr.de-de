---
title: ADSI-Strukturen
description: Active Directory Service Interfaces (ADSI) definieren und verwenden Sie die in der folgenden Tabelle aufgeführten Strukturen.
ms.assetid: 3ee0e469-9932-4135-8798-27d318011786
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, Referenz, Strukturen
- Strukturen ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f35ba74f0334e8b66329d8f526266c315056af9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100578"
---
# <a name="adsi-structures"></a>ADSI-Strukturen

Active Directory Service Interfaces (ADSI) definieren und verwenden Sie die in der folgenden Tabelle aufgeführten Strukturen.



| Struktur                                                                      | BESCHREIBUNG                                                                                                    |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**Werbeeinblendungen \_ \_**](/windows/desktop/api/Iads/ns-iads-ads_attr_def)<br/>                              | Beschreibt einen Satz von Attribut Definitionen eines **attributeSchema** -Objekts.<br/>                          |
| [**Anzeige \_ \_ Informationen**](/windows/desktop/api/Iads/ns-iads-ads_attr_info)<br/>                            | Enthält den Wert eines benannten Attributs und gibt Vorgänge zum Ändern des Attributs an.<br/>              |
| [**anzeigen ( \_ Backlink)**](/windows/win32/api/iads/ns-iads-ads_backlink)<br/>                               | Stellt eine ADSI-Darstellung des **backlinkattributs** dar.<br/>                                   |
| [**Liste der anzeigen \_ caseignore \_**](/windows/desktop/api/Iads/ns-iads-ads_caseignore_list)<br/>                | Stellt eine ADSI-Darstellung des Attributs " **Case ignore list** " dar.<br/>                            |
| [**ADS- \_ Klasse \_ DEF**](/windows/desktop/api/Iads/ns-iads-ads_class_def)<br/>                            | Beschreibt Schema Daten für ein-Objekt.<br/>                                                                |
| [**ADS \_ DN \_ mit \_ Binär**](/windows/win32/api/iads/ns-iads-ads_dn_with_binary)<br/>                 | Eine ADSI-definierte-Struktur, die einem Objekt- **GUID** einen Distinguished Name zuordnet.<br/>                     |
| [**ADS \_ DN \_ mit \_ Zeichenfolge**](/windows/win32/api/iads/ns-iads-ads_dn_with_string)<br/>                 | Eine ADSI-definierte-Struktur, die einen Distinguished Name eines Objekts einem nicht abweichenden Zeichen folgen Wert zuordnet.<br/> |
| [**Werbung \_ per e-Mail**](/windows/win32/api/iads/ns-iads-ads_email)<br/>                                     | Stellt eine ADSI-Darstellung des **e-Mail-** Attributs dar.<br/>                                       |
| [**\_Faxnummer des ADS**](/windows/win32/api/iads/ns-iads-ads_faxnumber)<br/>                             | Stellt eine ADSI-Darstellung des **Fax-Telefonnummern** Attributs dar.<br/>                  |
| [**Werbung \_ halten**](/windows/win32/api/iads/ns-iads-ads_hold)<br/>                                       | Stellt eine ADSI-Darstellung des **Hold** -Attributs dar.<br/>                                        |
| [**ADS- \_ netaddress**](/windows/win32/api/iads/ns-iads-ads_netaddress)<br/>                           | Stellt eine ADSI-Darstellung des **Net Address** -Attributs dar.<br/>                                 |
| [**AD \_ NT- \_ Sicherheits \_ Beschreibung**](/windows/win32/api/iads/ns-iads-ads_nt_security_descriptor)<br/> | Beschreibt eine Sicherheits Beschreibung.<br/>                                                                    |
| [**ADS- \_ Objekt \_ Informationen**](/windows/desktop/api/Iads/ns-iads-ads_object_info)<br/>                        | Beschreibt Verzeichnisdienst-Objektdaten.<br/>                                                            |
| [**Liste der ADS- \_ Oktett \_**](/windows/desktop/api/Iads/ns-iads-ads_octet_list)<br/>                          | Stellt eine ADSI-Darstellung des **Octett List** -Attributs dar.<br/>                                  |
| [**ADS- \_ Oktett- \_ Zeichenfolge**](/windows/win32/api/iads/ns-iads-ads_octet_string)<br/>                      | Stellt eine ADSI-Darstellung des **Oktett-Zeichen** folgen Attributs dar.<br/>                                |
| [**ADS- \_ Pfad**](/windows/win32/api/iads/ns-iads-ads_path)<br/>                                       | Stellt eine ADSI-Darstellung des **path** -Attributs dar.<br/>                                        |
| [**Werbung \_ PostalAddress**](/windows/win32/api/iads/ns-iads-ads_postaladdress)<br/>                     | Stellt eine ADSI-Darstellung des **Postal Address** -Attributs dar.<br/>                              |
| [**ADS \_ Prov- \_ spezifisch**](/windows/win32/api/iads/ns-iads-ads_prov_specific)<br/>                    | Beschreibt einen anbieterspezifischen Datentyp.<br/>                                                            |
| [**ADS \_ replicapointer**](/windows/win32/api/iads/ns-iads-ads_replicapointer)<br/>                   | Stellt eine ADSI-Darstellung des Replikat Zeiger Attributs dar.<br/>                                 |
| [**ADS- \_ Such \_ Spalte**](/windows/desktop/api/Iads/ns-iads-ads_search_column)<br/>                    | Stellt eine Spalte dar, die sich aus einer Verzeichnisabfrage ergibt.<br/>                                               |
| [**Anzeigen von \_ searchpref- \_ Informationen**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info)<br/>                | Beschreibt Abfrage Einstellungen.<br/>                                                                        |
| [**ADS \_ SortKey**](/windows/desktop/api/Iads/ns-iads-ads_sortkey)<br/>                                 | Beschreibt den Sortierschlüssel, der zum Sortieren einer Abfrage verwendet wird.<br/>                                                    |
| [**Werbe \_ Zeitstempel**](/windows/win32/api/iads/ns-iads-ads_timestamp)<br/>                             | Stellt eine ADSI-Darstellung des **timestamp** -Attributs dar.<br/>                                   |
| [**ADS \_ typedName**](/windows/win32/api/iads/ns-iads-ads_typedname)<br/>                             | Stellt eine ADSI-Darstellung des **typisierten Name** -Attributs dar.<br/>                                  |
| [**ADSVALUE**](/windows/desktop/api/Iads/ns-iads-adsvalue)<br/>                                        | Beschreibt den Wert eines ADSI-Datentyps.<br/>                                                           |
| [**ADS \_ VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv)<br/>                                         | Gibt an, dass die virtuelle Listenansicht beim Zurückgeben von Suchergebnissen vom Server verwendet werden soll.<br/>  |



 

 

 





