---
title: Gruppenobjekte
description: Eine Gruppe wird als Gruppenobjekt in der Active Directory Domain Services.
ms.assetid: 2dd5a293-047a-4639-9c95-7074578952be
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15de5c1577e6c4b0ca738c0f17ea5453020987d9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469937"
---
# <a name="group-objects"></a>Gruppenobjekte

Eine Gruppe wird als [**Gruppenobjekt**](/windows/desktop/ADSchema/c-group) in der Active Directory Domain Services. In der folgenden Tabelle sind wichtige Attribute des **Gruppenobjekts** aufgeführt.




| Attribut | BESCHREIBUNG | 
|-----------|-------------|
| <strong>Cn</strong> | Der <strong>cn</strong> (oder Common-Name) ist ein Einzelwertattribut, das den relativen Distinguished Name des Objekts ist. Der <strong>cn</strong> ist der Name der Gruppe in Active Directory Domain Services. Wie bei allen anderen Objekten muss <strong>der cn</strong> einer Gruppe unter den gleichgeordneten Objekten im Container, der die Gruppe enthält, eindeutig sein.<br /> | 
| <strong>Member</strong> | Das <strong></strong> Memberattribut ist ein Mehrwertattribut, das die Liste der Distinguished Names für die Benutzer-, Gruppen- und Kontaktobjekte enthält, die Mitglieder der Gruppe sind. Jedes Element in der Liste ist ein verknüpfter Verweis auf das Objekt, das den Member darstellt. Daher aktualisiert der Active Directory-Server automatisch die Distinguished Names in der Membereigenschaft, wenn ein Memberobjekt verschoben oder umbenannt wird.<br /> | 
| <strong>groupType</strong> | Das <strong>groupType-Attribut</strong> ist ein Einzelwertattribut, das eine ganze Zahl ist, die den Gruppentyp und -bereich mithilfe der folgenden Bitflags angibt:<ul><li><strong>ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP</strong></li><li><strong>ADS_GROUP_TYPE_GLOBAL_GROUP</strong></li><li><strong>ADS_GROUP_TYPE_UNIVERSAL_GROUP</strong></li><li><strong>ADS_GROUP_TYPE_SECURITY_ENABLED</strong></li></ul><br /> Die ersten drei Flags geben den Gruppenbereich an. Das <strong>ADS_GROUP_TYPE_SECURITY_ENABLED-Flag</strong> gibt den Gruppentyp an. Wenn dieses Flag festgelegt ist, ist die Gruppe eine Sicherheitsgruppe. Wenn dieses Flag nicht festgelegt ist, ist die Gruppe eine Verteilergruppe. Weitere Informationen finden Sie unter <a href="#group-types">Gruppentypen.</a><br /> | 
| <strong>memberOf</strong> | Das <strong>memberOf-Attribut</strong> ist ein Attribut mit mehreren Wert, das die Liste der Distinguished Names für Gruppen enthält, die die Gruppe als Mitglied enthalten. Dieses Attribut listet die Gruppen auf, unter denen die Gruppe direkt geschachtelt ist. Es enthält nicht die rekursive Liste der geschachtelten Vorgänger. Wenn z. B. Gruppe D in Gruppe C geschachtelt und Gruppe B und Gruppe B in Gruppe A geschachtelt wären, würde das <strong>memberOf-Attribut</strong> von Gruppe D Gruppe C und Gruppe B auflisten, aber nicht Gruppe A.<br /> | 
| <strong>objectGUID</strong> | Das <strong>objectGUID-Attribut</strong> ist ein Einzelwertattribut, das der eindeutige Bezeichner für das Objekt ist. Dieses Attribut ist eine GUID (Globally Unique Identifier). Wenn ein Objekt im Verzeichnis erstellt wird, generiert der Active Directory-Server eine GUID und weist sie dem <strong>objectGUID-Attribut des Objekts</strong> zu. Die GUID ist unternehmensweit und überall anders eindeutig.<br /> <strong>ObjectGUID ist</strong> eine 128-Bit-GUID-Struktur, die als OctetString gespeichert ist.<br /> | 
| <strong>Objectsid</strong> | Das <strong>objectSid-Attribut</strong> ist ein Einzelwertattribut, das die Sicherheits-ID (SID) der Gruppe angibt. Die SID ist ein eindeutiger Wert, mit dem die Gruppe als Sicherheitsprinzipal identifiziert wird. Dies ist ein Binärwert, den das System beim Erstellen der Gruppe fest legt.<br /> Jede Gruppe verfügt über eine eindeutige SID, die von der Windows NT/Windows 2000-Serverdomäne ausgelagert wird, die im <strong>objectSid-Attribut</strong> des Gruppenobjekts im Verzeichnis gespeichert ist. Jedes Mal, wenn sich ein Benutzer anmeldet, ruft das System die SID für die Gruppen ab, deren Mitglied der Benutzer ist, und platziert sie im Zugriffstoken des Benutzers. Das System verwendet die SIDs im Zugriffstoken des Benutzers, um den Benutzer und seine Gruppenmitgliedschaften in allen nachfolgenden Interaktionen mit Windows NT/Windows 2000-Sicherheit zu identifizieren.<br /> Wenn eine SID als eindeutiger Bezeichner für einen Benutzer oder eine Gruppe verwendet wurde, kann sie niemals erneut verwendet werden, um einen anderen Benutzer oder eine Gruppe zu identifizieren.<br /> | 
| <strong>Samaccountname</strong> | Das <strong>sAMAccountName-Attribut</strong> ist ein Ein-Wert-Attribut, bei dem es sich um den Anmeldenamen handelt, der zur Unterstützung von Clients und Servern aus einer früheren Version (Windows 95, Windows 98 und LAN-Manager) verwendet wird. Der <strong>sAMAccountName sollte</strong> weniger als 20 Zeichen lang sein, um Clients und Server aus einer früheren Version zu unterstützen.<br /> Der <strong>sAMAccountName muss</strong> für alle Sicherheitsprinzipalobjekte innerhalb einer Domäne eindeutig sein.<br /> | 




 

## <a name="group-types"></a>Gruppentypen

Es gibt zwei Typen von Gruppen, die von Active Directory Domain Services definiert werden: *Sicherheitsgruppen* und *Verteilergruppen.*

Eine Sicherheitsgruppe bietet eine logische Gruppierung von Objekten, und die Gruppe selbst kann als Sicherheitsprinzipal in einer Access Control List (ACL) verwendet werden. Wenn einer Sicherheitsgruppe Zugriff auf ein Objekt erteilt wird, erhalten alle Mitglieder der Sicherheitsgruppe automatisch denselben Zugriff auf das Objekt. Sicherheitsgruppen mit universellem Gültigkeitsbereich können auch als E-Mail-Entität verwendet werden. Das Senden einer E-Mail-Nachricht an eine universelle Sicherheitsgruppe sendet die Nachricht an alle Mitglieder der Gruppe.

Eine Verteilergruppe bietet auch eine logische Gruppierung von Objekten, kann jedoch keine Zugriffsberechtigungen bereitstellen. Verteilergruppen sind nicht sicherheits aktiviert und können nicht als Sicherheitsprinzipal in einer ACL verwendet werden. Verteilergruppen werden nur zu Gruppierungszwecken verwendet. Verteilerlisten können beispielsweise mit E-Mail-Anwendungen wie Exchange verwendet werden, um E-Mails an eine Sammlung von Benutzern zu senden.

Weitere Informationen zu Gruppentypen in Active Directory Domain Services finden Sie im Thema [Gruppentypen](/previous-versions/windows/it-pro/windows-server-2003/cc781446(v=ws.10)) auf [Microsoft TechNet.](https://technet.microsoft.com/default.aspx)

## <a name="group-scope"></a>Gruppenbereich

Es gibt drei Gruppenbereich, die durch Active Directory Domain Services definiert werden: *Universal,* *Global* und *Domain Local.* Der Bereich der Gruppe definiert, welche Objekttypen zur Gruppe gehören können, welche Gruppentypen der Gruppe angehören können und auf welche Objekttypen Sicherheitsgruppen Zugriff erhalten können. Wenn die Domänenfunktionsebene auf den gemischten Windows 2000 festgelegt ist, können keine Sicherheitsgruppen mit universellem Gültigkeitsbereich erstellt werden.

In der folgenden Tabelle sind die drei Gruppenbereich und weitere Informationen zu jedem Bereich für eine Sicherheitsgruppe aufgeführt.

| Bereich                   | Mögliche Member                                                                                                                                                                                                                                      | Bereichskonvertierung                                                                                                                                                 | Kann Berechtigungen erteilen                                                       | Möglicher Member von                                                                                                                                                                                                  |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Universell<br/>    | Konten aus einer beliebigen Domäne in derselben Gesamtstruktur.<br/> Globale Gruppen aus einer beliebigen Domäne in derselben Gesamtstruktur.<br/> Andere universelle Gruppen aus einer beliebigen Domäne in derselben Gesamtstruktur.<br/>                                                            | Kann in den lokalen Domänenbereich konvertiert werden.<br/> Kann in einen globalen Bereich konvertiert werden, solange die Gruppe keine anderen universellen Gruppen enthält.<br/> | Für jede Domäne in derselben Gesamtstruktur oder vertrauenswürdigen Gesamtstrukturen.<br/>            | Andere universelle Gruppen in derselben Gesamtstruktur.<br/> Lokale Domänengruppen in derselben Gesamtstruktur oder vertrauenswürdigen Gesamtstrukturen.<br/> Lokale Gruppen auf Computern in derselben Gesamtstruktur oder vertrauenswürdigen Gesamtstrukturen.<br/>            |
| Global<br/>       | Konten aus derselben Domäne.<br/> Andere globale Gruppen aus derselben Domäne.<br/>                                                                                                                                                        | Kann in einen universellen Bereich konvertiert werden, solange die Gruppe kein Mitglied einer anderen globalen Gruppe ist.<br/>                                                   | Für jede Domäne in derselben Gesamtstruktur oder vertrauenswürdigen Domänen oder Gesamtstrukturen.<br/> | Universelle Gruppen aus einer beliebigen Domäne in derselben Gesamtstruktur.<br/> Andere globale Gruppen aus derselben Domäne.<br/> Lokale Domänengruppen aus einer beliebigen Domäne in derselben Gesamtstruktur oder einer vertrauenswürdigen Domäne.<br/> |
| Lokale Domäne<br/> | Konten aus einer beliebigen Domäne oder einer beliebigen vertrauenswürdigen Domäne.<br/> Globale Gruppen aus beliebigen Domänen oder vertrauenswürdigen Domänen.<br/> Universelle Gruppen aus einer beliebigen Domäne in derselben Gesamtstruktur.<br/> Andere lokale Domänengruppen aus derselben Domäne.<br/> | Kann in einen universellen Bereich konvertiert werden, solange die Gruppe keine anderen lokalen Domänengruppen enthält.<br/>                                              | Innerhalb derselben Domäne.<br/>                                          | Andere lokale Domänengruppen aus derselben Domäne.<br/> Lokale Gruppen auf Computern in derselben Domäne, ausgenommen integrierte Gruppen mit bekannten SIDs.<br/>                                             |



 

 

