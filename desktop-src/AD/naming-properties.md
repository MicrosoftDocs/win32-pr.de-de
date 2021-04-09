---
title: Attribute für Benutzer Benennung
description: Benutzer Benennungs Attribute identifizieren Benutzer Objekte, wie z. b. Anmelde Namen und IDs, die aus Sicherheitsgründen verwendet werden.
ms.assetid: 2192743c-cedd-4b03-a402-3992d64a4801
ms.tgt_platform: multiple
keywords:
- Benutzer Benennungs Attribute ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a504070cf2e78cf5647072ff740d137b4a6e6056
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103948555"
---
# <a name="user-naming-attributes"></a>Attribute für Benutzer Benennung

Benutzer Benennungs Attribute identifizieren Benutzer Objekte, wie z. b. Anmelde Namen und IDs, die aus Sicherheitsgründen verwendet werden. Die Attribute " **CN**", " **Name**" und "Unterscheidung **Name** " sind Beispiele für Benutzer Benennungs Attribute. Ein Benutzerobjekt ist ein Sicherheits Prinzipal Objekt und enthält daher auch die folgenden Attribute für die Benutzer Benennung:

-   [userPrincipalName](#userprincipalname) – der Anmelde Name für den Benutzer.
-   [objectGUID](#objectguid) – der eindeutige Bezeichner eines Benutzers
-   [sAMAccountName](#samaccountname) – ein Anmelde Name, der die vorherige Version von Windows unterstützt.
-   [objectSID](#objectsid) – Sicherheits-ID (SID) des Benutzers
-   [SIDHistory](#sidhistory) – die vorherigen SIDs für das User-Objekt

> [!Note]  
> Sie können diese Attribute mit dem MMC-Snap-in "Active Directory-Benutzer und-Computer" anzeigen und verwalten, das im [Remoteserver-Verwaltungstools (RSAT)](https://www.microsoft.com/download/details.aspx?id=45520)verfügbar ist.

 

## <a name="userprincipalname"></a>userPrincipalName

Das **userPrincipalName** -Attribut ist der Anmelde Name für den Benutzer. Das-Attribut besteht aus einem Benutzer Prinzipal Namen (User Principal Name, UPN), der der häufigste Anmelde Name für Windows-Benutzer ist. Benutzer verwenden in der Regel ihren UPN, um sich bei einer Domäne anzumelden. Dieses Attribut ist eine indizierte Zeichenfolge, die einwertig ist.

Ein UPN ist ein Anmelde Name im Internet Format für einen Benutzer, der auf dem Internet Standard RFC 822 basiert. Der UPN ist kürzer als ein definierter Name und leichter zu merken. Gemäß der Konvention sollte er dem E-Mail-Namen des Benutzers entsprechen. Der Punkt des UPN besteht darin, die e-Mail-und LOGON-Namespaces zu konsolidieren, sodass sich der Benutzer nur einen einzelnen Namen merken muss.

### <a name="upn-format"></a>UPN-Format

Ein UPN besteht aus einem UPN-Präfix (dem Benutzerkontonamen) und einem UPN-Suffix (einem DNS-Domänennamen). Das Präfix wird mithilfe des @-Symbols mit dem Suffix verknüpft. Beispiel: "someone@ example.com". Ein UPN muss für alle Sicherheitsprinzipalobjekte innerhalb einer Verzeichnisgesamtstruktur eindeutig sein. Dies bedeutet, dass das Präfix eines UPN wieder verwendet werden kann, jedoch nicht mit demselben Suffix.

Ein UPN-Suffix weist die folgenden Einschränkungen auf:

-   Dabei muss es sich um den DNS-Namen einer Domäne handeln, aber es muss sich nicht um den Namen der Domäne handeln, die den Benutzer enthält.
-   Dabei muss es sich um den Namen einer Domäne in der aktuellen Domänen Gesamtstruktur oder um einen alternativen Namen handeln, der im **upnSuffixes** -Attribut des Partitions Containers im Konfigurations Container aufgeführt ist.

### <a name="upn-management"></a>UPN-Verwaltung

Ein UPN kann zugewiesen werden, ist jedoch nicht erforderlich, wenn ein Benutzerkonto erstellt wird. Wenn ein UPN erstellt wird, wirkt sich dies nicht auf Änderungen an anderen Attributen des Benutzer Objekts aus, z. b. den Benutzer, der umbenannt oder verschoben wurde. Dadurch kann der Benutzer denselben Anmelde Namen beibehalten, wenn ein Verzeichnis umstrukturiert wird. Ein Administrator kann jedoch einen UPN ändern. Wenn Sie ein neues Benutzerobjekt erstellen, sollten Sie die lokale Domäne und den globalen Katalog auf den vorgeschlagenen Namen überprüfen, um sicherzustellen, dass Sie nicht bereits vorhanden ist.

Wenn ein Benutzer einen UPN verwendet, um sich bei einer Domäne anzumelden, wird der UPN überprüft, indem die lokale Domäne und dann der globale Katalog durchsucht werden. Wenn der UPN nicht im globalen Katalog gefunden wird, tritt beim Anmeldeversuch ein Fehler auf.

## <a name="objectguid"></a>objectGUID

Das **objectGUID** -Attribut ist der eindeutige Bezeichner eines Benutzers. Das-Attribut ist eine GUID (Global Unique Identifier) mit einem einzelnen 128 Wert und wird als [**AD- \_ Oktett- \_ Zeichen**](/windows/win32/api/iads/ns-iads-ads_octet_string) folgen Struktur gespeichert Die GUID wird vom Active Directory Server erstellt, wenn ein Benutzerobjekt erstellt wird.

Da sich der Distinguished Name eines Objekts ändert, wenn das Objekt umbenannt oder verschoben wird, ist der Distinguished Name kein zuverlässiger Bezeichner eines Objekts. In Active Directory Domain Services ändert sich das **objectGUID** -Attribut eines Objekts nie, auch wenn das Objekt umbenannt oder verschoben wird. Sie können die Zeichen folgen Form von **objectGUID** mithilfe der **GUID** -Eigenschaften Methode in [IADs-Eigenschaften Methoden](/windows/desktop/ADSI/iads-property-methods)abrufen.

## <a name="samaccountname"></a>sAMAccountName

Das **sAMAccountName** -Attribut ist ein Anmelde Name, der verwendet wird, um Clients und Server aus früheren Versionen von Windows zu unterstützen, z. b. Windows NT 4,0, Windows 95, Windows 98 und LAN Manager. Der Anmelde Name darf maximal 20 Zeichen lang sein und muss für alle Sicherheits Prinzipal Objekte innerhalb der Domäne eindeutig sein.

## <a name="objectsid"></a>objectSid

Das **objectSID** -Attribut ist die Sicherheits-ID (SID) des Benutzers. Die SID wird vom System verwendet, um einen Benutzer und deren Gruppenmitgliedschaften während der Interaktion mit der Windows-Sicherheit zu identifizieren. Das Attribut ist einwertig. Die SID ist ein eindeutiger Binärwert, der verwendet wird, um den Benutzer als Sicherheits Prinzipal zu identifizieren.

Die SID wird vom System festgelegt, wenn der Benutzer erstellt wird. Jeder Benutzer verfügt über eine eindeutige SID, die von einer Windows-Domäne ausgegeben und im **objectSID** -Attribut des Benutzer Objekts im Verzeichnis gespeichert wird. Jedes Mal, wenn sich ein Benutzer anmeldet, ruft das System die SID des Benutzers aus dem Verzeichnis ab und platziert Sie im Zugriffs Token des Benutzers. Die SID des Benutzers dient auch zum Abrufen der SIDs für die Gruppen, denen der Benutzer angehört, und platziert Sie im Zugriffs Token des Benutzers. Wenn eine SID als eindeutiger Bezeichner für einen Benutzer oder eine Gruppe verwendet wurde, kann Sie nicht erneut verwendet werden, um einen anderen Benutzer oder eine andere Gruppe zu identifizieren.

## <a name="sidhistory"></a>SIDHistory

Das **SIDHistory** -Attribut enthält die vorherigen SIDs für das User-Objekt. Dabei handelt es sich um ein mehr wertiges Attribut. Ein Benutzerobjekt hat vorherige SIDs, wenn der Benutzer in eine andere Domäne verschoben wurde. Wenn ein Benutzerobjekt in eine neue Domäne verschoben wird, wird eine neue SID erstellt und das **objectSID** -Attribut zugewiesen, und die vorherige sid wird dem **SIDHistory** -Attribut hinzugefügt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Benutzerobjekt Attribute](user-object-attributes.md)
</dt> </dl>

 

 