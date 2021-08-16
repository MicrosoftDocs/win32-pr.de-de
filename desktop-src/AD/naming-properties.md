---
title: Benutzerbenennungsattribute
description: Benutzerbenennungsattribute identifizieren Benutzerobjekte, z. B. Anmeldenamen und IDs, die zu Sicherheitszwecken verwendet werden.
ms.assetid: 2192743c-cedd-4b03-a402-3992d64a4801
ms.tgt_platform: multiple
keywords:
- Benutzerbenennungsattribute AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8548178bba8012231a803d476699e8ebb386b6fa9a29015f3721e7b32d94158
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185930"
---
# <a name="user-naming-attributes"></a>Benutzerbenennungsattribute

Benutzerbenennungsattribute identifizieren Benutzerobjekte, z. B. Anmeldenamen und IDs, die zu Sicherheitszwecken verwendet werden. Die **Attribute cn,** **name** und **distinguishedName** sind Beispiele für Benutzerbenennungsattribute. Ein Benutzerobjekt ist ein Sicherheitsprinzipalobjekt und enthält daher auch die folgenden Benutzernamensattribute:

-   [userPrincipalName:](#userprincipalname) Der Anmeldename für den Benutzer
-   [objectGUID](#objectguid) – der eindeutige Bezeichner eines Benutzers
-   [sAMAccountName:](#samaccountname) Ein Anmeldename, der frühere Versionen von Windows
-   [objectSid](#objectsid) – Sicherheits-ID (SID) des Benutzers
-   [sIDHistory:](#sidhistory) die vorherigen SIDs für das Benutzerobjekt

> [!Note]  
> Sie können diese Attribute mithilfe des MMC-Snap-Ins Active Directory-Benutzer und -Computer anzeigen und verwalten, das im Remoteserver-Verwaltungstools [(RSAT) verfügbar ist.](https://www.microsoft.com/download/details.aspx?id=45520)

 

## <a name="userprincipalname"></a>userPrincipalName

Das **userPrincipalName-Attribut** ist der Anmeldename für den Benutzer. Das Attribut besteht aus einem Benutzerprinzipalnamen (USER Principal Name, UPN), der der gängigste Anmeldename für Windows ist. Benutzer verwenden in der Regel ihren UPN, um sich bei einer Domäne zu anmelden. Dieses Attribut ist eine indizierte Zeichenfolge, die einwertige Werte hat.

Ein UPN ist ein Anmeldename im Internetformat für einen Benutzer, der auf dem Internetstandard RFC 822 basiert. Der UPN ist kürzer als ein Distinguished Name und leichter zu merken. Gemäß der Konvention sollte er dem E-Mail-Namen des Benutzers entsprechen. Der Punkt des UPN besteht in der Konsolidierung der E-Mail- und Anmeldenamespaces, damit sich der Benutzer nur einen einzelnen Namen merken muss.

### <a name="upn-format"></a>UPN-Format

Ein UPN besteht aus einem UPN-Präfix (dem Benutzerkontonamen) und einem UPN-Suffix (einem DNS-Domänennamen). Das Präfix wird mithilfe des @-Symbols mit dem Suffix verknüpft. Beispiel: "someone@ example.com". Ein UPN muss für alle Sicherheitsprinzipalobjekte innerhalb einer Verzeichnisgesamtstruktur eindeutig sein. Dies bedeutet, dass das Präfix eines UPN wiederverwendet werden kann, nur nicht mit dem gleichen Suffix.

Für ein UPN-Suffix gelten die folgenden Einschränkungen:

-   Es muss sich um den DNS-Namen einer Domäne, aber nicht um den Namen der Domäne, die den Benutzer enthält, befinden.
-   Dies muss der Name einer Domäne in der aktuellen Domänengestruktur oder ein alternativer Name sein, der im **upnSuffixes-Attribut** des Containers Partitionen im Konfigurationscontainer aufgeführt ist.

### <a name="upn-management"></a>UPN-Verwaltung

Ein UPN kann zugewiesen werden, ist aber nicht erforderlich, wenn ein Benutzerkonto erstellt wird. Wenn ein UPN erstellt wird, ist er nicht von Änderungen an anderen Attributen des Benutzerobjekts betroffen, z. B. dem Benutzer, der umbenannt oder verschoben wird. Dadurch kann der Benutzer denselben Anmeldenamen behalten, wenn ein Verzeichnis neu strukturiert wird. Ein Administrator kann jedoch einen UPN ändern. Wenn Sie ein neues Benutzerobjekt erstellen, sollten Sie die lokale Domäne und den globalen Katalog auf den vorgeschlagenen Namen überprüfen, um sicherzustellen, dass er noch nicht vorhanden ist.

Wenn ein Benutzer einen UPN für die Anmeldung bei einer Domäne verwendet, wird der UPN durch Durchsuchen der lokalen Domäne und dann des globalen Katalogs überprüft. Wenn der UPN nicht im globalen Katalog gefunden wird, schlägt der Anmeldeversuch fehl.

## <a name="objectguid"></a>objectGUID

Das **objectGUID-Attribut** ist der eindeutige Bezeichner eines Benutzers. Das -Attribut ist ein einwertige 128-Bit-GUID (Globally Unique Identifier) und wird als [**ADS \_ OCTET \_ STRING-Struktur**](/windows/win32/api/iads/ns-iads-ads_octet_string) gespeichert. Die GUID wird vom Active Directory-Server erstellt, wenn ein Benutzerobjekt erstellt wird.

Da sich der Distinguished Name eines Objekts ändert, wenn das Objekt umbenannt oder verschoben wird, ist der Distinguished Name kein zuverlässiger Bezeichner eines Objekts. In Active Directory Domain Services ändert sich das **objectGUID-Attribut** eines Objekts nie, auch wenn das Objekt umbenannt oder verschoben wird. Sie können die Zeichenfolgenform von **objectGUID** mithilfe der **GUID-Eigenschaftsmethode** in [IADs Property Methods abrufen.](/windows/desktop/ADSI/iads-property-methods)

## <a name="samaccountname"></a>sAMAccountName

Das **sAMAccountName-Attribut** ist ein Anmeldename, der zur Unterstützung von Clients und Servern aus früheren Versionen von Windows verwendet wird, z. B. Windows NT 4.0, Windows 95, Windows 98 und LAN Manager. Der Anmeldename muss mindestens 20 Zeichen lang sein und für alle Sicherheitsprinzipalobjekte innerhalb der Domäne eindeutig sein.

## <a name="objectsid"></a>objectSid

Das **objectSid-Attribut** ist die Sicherheits-ID (SID) des Benutzers. Die SID wird vom System verwendet, um einen Benutzer und seine Gruppenmitgliedschaften bei Interaktionen mit Windows identifizieren. Das Attribut ist einwertigen Wert. Die SID ist ein eindeutiger Binärwert, mit dem der Benutzer als Sicherheitsprinzipal identifiziert wird.

Die SID wird vom System festgelegt, wenn der Benutzer erstellt wird. Jeder Benutzer verfügt über eine eindeutige SID, die von einer Windows-Domäne ausgegeben und im **objectSid-Attribut** des Benutzerobjekts im Verzeichnis gespeichert wird. Jedes Mal, wenn sich ein Benutzer anmeldet, ruft das System die SID des Benutzers aus dem Verzeichnis ab und platziert sie im Zugriffstoken des Benutzers. Die SID des Benutzers wird auch verwendet, um die SIDs für die Gruppen abzurufen, deren Mitglied der Benutzer ist, und legt sie im Zugriffstoken des Benutzers ab. Wenn eine SID als eindeutiger Bezeichner für einen Benutzer oder eine Gruppe verwendet wurde, kann sie nicht erneut verwendet werden, um einen anderen Benutzer oder eine Gruppe zu identifizieren.

## <a name="sidhistory"></a>Sidhistory

Das **sIDHistory-Attribut** enthält die vorherigen SIDs für das Benutzerobjekt. Dies ist ein mehrwertige Attribut. Ein Benutzerobjekt verfügt über vorherige SIDs, wenn der Benutzer in eine andere Domäne verschoben wurde. Wenn ein Benutzerobjekt in eine neue Domäne verschoben wird, wird eine neue SID erstellt und dem **attribut objectSid** zugewiesen, und die vorherige SID wird dem **sIDHistory-Attribut** hinzugefügt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Benutzerobjektattribute](user-object-attributes.md)
</dt> </dl>

 

 