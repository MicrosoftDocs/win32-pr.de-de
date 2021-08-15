---
title: Gruppenobjekte
description: Eine Gruppe wird als Gruppenobjekt in Active Directory Domain Services dargestellt.
ms.assetid: 2dd5a293-047a-4639-9c95-7074578952be
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9811a365f321a0fb81b770e87a0987bac4c52d7bc681c44c90c35cbd3e7a1d7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188728"
---
# <a name="group-objects"></a>Gruppenobjekte

Eine Gruppe wird in Active Directory Domain Services als [**Gruppenobjekt**](/windows/desktop/ADSchema/c-group) dargestellt. In der folgenden Tabelle sind wichtige Attribute des **Gruppenobjekts** aufgeführt.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>attribute</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Cn</strong></td>
<td>Der <strong>cn</strong> (oder Common-Name) ist ein Attribut mit einem Wert, das den relativen Distinguished Name des Objekts ist. <strong>CN</strong> ist der Name der Gruppe in Active Directory Domain Services. Wie bei allen anderen Objekten muss der <strong>CN</strong> einer Gruppe unter den gleichgeordneten Objekten im Container, der die Gruppe enthält, eindeutig sein.<br/></td>
</tr>
<tr class="even">
<td><strong>Mitglied</strong></td>
<td>Das <strong></strong> Memberattribut ist ein Mehrwertattribut, das die Liste der Distinguished Names für die Benutzer-, Gruppen- und Kontaktobjekte enthält, die Mitglieder der Gruppe sind. Jedes Element in der Liste ist ein verknüpfter Verweis auf das Objekt, das den Member darstellt. Daher aktualisiert der Active Directory-Server automatisch die Distinguished Names in der Membereigenschaft, wenn ein Memberobjekt verschoben oder umbenannt wird.<br/></td>
</tr>
<tr class="odd">
<td><strong>groupType</strong></td>
<td>Das <strong>groupType-Attribut</strong> ist ein Einzelwertattribut, das eine ganze Zahl ist, die den Gruppentyp und den Bereich mithilfe der folgenden Bitflags angibt:
<ul>
<li><strong>ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP</strong></li>
<li><strong>ADS_GROUP_TYPE_GLOBAL_GROUP</strong></li>
<li><strong>ADS_GROUP_TYPE_UNIVERSAL_GROUP</strong></li>
<li><strong>ADS_GROUP_TYPE_SECURITY_ENABLED</strong></li>
</ul>
<br/> Die ersten drei Flags geben den Gruppenbereich an. Das <strong>flag ADS_GROUP_TYPE_SECURITY_ENABLED</strong> gibt den Gruppentyp an. Wenn dieses Flag festgelegt ist, ist die Gruppe eine Sicherheitsgruppe. Wenn dieses Flag nicht festgelegt ist, ist die Gruppe eine Verteilergruppe. Weitere Informationen finden Sie unter <a href="#group-types">Gruppentypen.</a><br/></td>
</tr>
<tr class="even">
<td><strong>memberOf</strong></td>
<td>Das <strong>memberOf-Attribut</strong> ist ein Attribut mit mehreren Werten, das die Liste der Distinguished Names für Gruppen enthält, die die Gruppe als Mitglied enthalten. Dieses Attribut listet die Gruppen auf, unter denen die Gruppe direkt geschachtelt ist. Es enthält nicht die rekursive Liste der geschachtelten Vorgänger. Wenn z. B. Gruppe D in Gruppe C geschachtelt und Gruppe B und Gruppe B in Gruppe A geschachtelt sind, würde das <strong>memberOf-Attribut</strong> von Gruppe D Gruppe C und Gruppe B auflisten, aber nicht Gruppe A.<br/></td>
</tr>
<tr class="odd">
<td><strong>objectGUID</strong></td>
<td>Das <strong>objectGUID-Attribut</strong> ist ein Einzelwertattribut, das der eindeutige Bezeichner für das Objekt ist. Dieses Attribut ist eine GUID (Globally Unique Identifier). Wenn ein Objekt im Verzeichnis erstellt wird, generiert der Active Directory-Server eine GUID und weist sie dem <strong>objectGUID-Attribut</strong> des Objekts zu. Die GUID ist unternehmensweit und überall anders eindeutig.<br/> <strong>ObjectGUID</strong> ist eine 128-Bit-GUID-Struktur, die als OctetString gespeichert ist.<br/></td>
</tr>
<tr class="even">
<td><strong>Objectsid</strong></td>
<td>Das <strong>objectSid-Attribut</strong> ist ein Ein-Wert-Attribut, das die Sicherheits-ID (SID) der Gruppe angibt. Die SID ist ein eindeutiger Wert, mit dem die Gruppe als Sicherheitsprinzipal identifiziert wird. Es handelt sich um einen binären Wert, den das System beim Erstellen der Gruppe festlegt.<br/> Jede Gruppe verfügt über eine eindeutige SID, die die Windows NT/Windows 2000 Server-Domäne ausgibt, die im <strong>objectSid-Attribut</strong> des Gruppenobjekts im Verzeichnis gespeichert ist. Jedes Mal, wenn sich ein Benutzer anmeldet, ruft das System die SID für die Gruppen ab, denen der Benutzer angehört, und platziert sie im Zugriffstoken des Benutzers. Das System verwendet die SIDs im Zugriffstoken des Benutzers, um den Benutzer und seine Gruppenmitgliedschaften in allen nachfolgenden Interaktionen mit Windows NT/Windows 2000-Sicherheit zu identifizieren.<br/> Wenn eine SID als eindeutiger Bezeichner für einen Benutzer oder eine Gruppe verwendet wurde, kann sie nie wieder verwendet werden, um einen anderen Benutzer oder eine andere Gruppe zu identifizieren.<br/></td>
</tr>
<tr class="odd">
<td><strong>Samaccountname</strong></td>
<td>Das <strong>sAMAccountName-Attribut</strong> ist ein Attribut mit einem Wert, bei dem es sich um den Anmeldenamen handelt, der zur Unterstützung von Clients und Servern einer früheren Version (Windows 95, Windows 98 und LAN-Manager) verwendet wird. Der <strong>sAMAccountName</strong> sollte weniger als 20 Zeichen lang sein, um Clients und Server aus einer früheren Version zu unterstützen.<br/> <strong>sAMAccountName</strong> muss für alle Sicherheitsprinzipalobjekte innerhalb einer Domäne eindeutig sein.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="group-types"></a>Gruppentypen

Es gibt zwei Arten von Gruppen, die von Active Directory Domain Services definiert werden: *Sicherheitsgruppen* und *Verteilergruppen.*

Eine Sicherheitsgruppe stellt eine logische Gruppierung von Objekten bereit, und die Gruppe selbst kann als Sicherheitsprinzipal in einer Access Control Liste (ACL) verwendet werden. Wenn einer Sicherheitsgruppe Zugriff auf ein Objekt gewährt wird, erhalten alle Mitglieder der Sicherheitsgruppe automatisch den gleichen Zugriff auf das Objekt. Sicherheitsgruppen mit universellem Gültigkeitsbereich können auch als E-Mail-Entität verwendet werden. Wenn Sie eine E-Mail an eine universelle Sicherheitsgruppe senden, wird die Nachricht an alle Mitglieder der Gruppe gesendet.

Eine Verteilergruppe stellt auch eine logische Gruppierung von Objekten bereit, kann jedoch keine Zugriffsberechtigungen bereitstellen. Verteilergruppen sind nicht sicherheitsfähig und können nicht als Sicherheitsprinzipal in einer ACL verwendet werden. Verteilergruppen werden nur zu Gruppierungszwecken verwendet. Beispielsweise können Verteilerlisten mit E-Mail-Anwendungen wie Exchange verwendet werden, um E-Mails an eine Sammlung von Benutzern zu senden.

Weitere Informationen zu Gruppentypen in Active Directory Domain Services finden Sie im Thema [Gruppentypen](/previous-versions/windows/it-pro/windows-server-2003/cc781446(v=ws.10)) auf [Microsoft TechNet.](https://technet.microsoft.com/default.aspx)

## <a name="group-scope"></a>Gruppenbereich

Es gibt drei Gruppenbereiche, die durch Active Directory Domain Services definiert werden: *Universal,* *Global* und *Domain Local.* Der Bereich der Gruppe definiert, welche Objekttypen zur Gruppe gehören können, welche Gruppentypen die Gruppe als Mitglied verwenden kann und auf welchen Bereich von Objekten Sicherheitsgruppen Zugriff erhalten kann. Wenn die Domänenfunktionsebene auf Windows gemischten Modus 2000 festgelegt ist, können keine Sicherheitsgruppen mit universellem Gültigkeitsbereich erstellt werden.

In der folgenden Tabelle sind die drei Gruppenbereiche und weitere Informationen zu den einzelnen Bereichen für eine Sicherheitsgruppe aufgeführt.

| Bereich                   | Mögliche Member                                                                                                                                                                                                                                      | Bereichskonvertierung                                                                                                                                                 | Kann Berechtigungen erteilen                                                       | Möglicher Member von                                                                                                                                                                                                  |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Universell<br/>    | Konten aus einer beliebigen Domäne in derselben Gesamtstruktur.<br/> Globale Gruppen aus einer beliebigen Domäne in derselben Gesamtstruktur.<br/> Andere universelle Gruppen aus einer beliebigen Domäne in derselben Gesamtstruktur.<br/>                                                            | Kann in den lokalen Domänenbereich konvertiert werden.<br/> Kann in einen globalen Bereich konvertiert werden, solange die Gruppe keine anderen universellen Gruppen enthält.<br/> | In einer Domäne in derselben Gesamtstruktur oder in vertrauenswürdigen Gesamtstrukturen.<br/>            | Andere universelle Gruppen in derselben Gesamtstruktur.<br/> Lokale Domänengruppen in derselben Gesamtstruktur oder vertrauenswürdigen Gesamtstrukturen.<br/> Lokale Gruppen auf Computern in derselben Gesamtstruktur oder vertrauenswürdigen Gesamtstrukturen.<br/>            |
| Global<br/>       | Konten aus derselben Domäne.<br/> Andere globale Gruppen aus derselben Domäne.<br/>                                                                                                                                                        | Kann in den universellen Gültigkeitsbereich konvertiert werden, solange die Gruppe kein Mitglied einer anderen globalen Gruppe ist.<br/>                                                   | In jeder Domäne in derselben Gesamtstruktur oder in vertrauenswürdigen Domänen oder Gesamtstrukturen.<br/> | Universelle Gruppen aus einer beliebigen Domäne in derselben Gesamtstruktur.<br/> Andere globale Gruppen aus derselben Domäne.<br/> Lokale Domänengruppen aus einer beliebigen Domäne in derselben Gesamtstruktur oder aus einer vertrauenden Domäne.<br/> |
| Domäne lokal<br/> | Konten aus einer beliebigen Domäne oder einer beliebigen vertrauenswürdigen Domäne.<br/> Globale Gruppen aus einer beliebigen Domäne oder einer beliebigen vertrauenswürdigen Domäne.<br/> Universelle Gruppen aus einer beliebigen Domäne in derselben Gesamtstruktur.<br/> Andere lokale Domänengruppen aus derselben Domäne.<br/> | Kann in den universellen Bereich konvertiert werden, solange die Gruppe keine anderen lokalen Domänengruppen enthält.<br/>                                              | Innerhalb derselben Domäne.<br/>                                          | Andere lokale Domänengruppen aus derselben Domäne.<br/> Lokale Gruppen auf Computern in derselben Domäne, ausgenommen integrierte Gruppen mit bekannten SIDs.<br/>                                             |



 

 

