---
title: Gruppenobjekte
description: Eine Gruppe wird in Active Directory Domain Services als Gruppen Objekt dargestellt.
ms.assetid: 2dd5a293-047a-4639-9c95-7074578952be
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a935d2a44d3350d8c24ca3bdb388f0a4bd8f16ee
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103948567"
---
# <a name="group-objects"></a>Gruppenobjekte

Eine Gruppe wird in Active Directory Domain Services als [**Gruppen**](/windows/desktop/ADSchema/c-group) Objekt dargestellt. In der folgenden Tabelle sind wichtige Attribute des **Group** -Objekts aufgeführt.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>2.300</strong></td>
<td><strong>CN</strong> (oder Common-Name) ist ein Einzelwert Attribut, bei dem es sich um den relativen Distinguished Name des Objekts handelt. <strong>CN</strong> ist der Name der Gruppe in Active Directory Domain Services. Wie bei allen anderen Objekten muss der <strong>CN</strong> einer Gruppe unter den gleich geordneten Objekten im Container, der die Gruppe enthält, eindeutig sein.<br/></td>
</tr>
<tr class="even">
<td><strong>Kollege</strong></td>
<td>Das <strong>Member</strong> -Attribut ist ein Attribut mit mehreren Werten, das die Liste der definierten Namen für die Benutzer-, Gruppen-und Kontakt Objekte enthält, die Mitglieder der Gruppe sind. Jedes Element in der Liste ist ein verknüpfter Verweis auf das Objekt, das den Member darstellt. Daher aktualisiert der Active Directory Server die Distinguished Names in der Element Eigenschaft automatisch, wenn ein Element Objekt verschoben oder umbenannt wird.<br/></td>
</tr>
<tr class="odd">
<td><strong>groupType</strong></td>
<td>Das <strong>GroupType</strong> -Attribut ist ein Einzelwert Attribut, bei dem es sich um eine ganze Zahl handelt, die den Gruppentyp und den Bereich mithilfe der folgenden Bitflags angibt:
<ul>
<li><strong>ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP</strong></li>
<li><strong>ADS_GROUP_TYPE_GLOBAL_GROUP</strong></li>
<li><strong>ADS_GROUP_TYPE_UNIVERSAL_GROUP</strong></li>
<li><strong>ADS_GROUP_TYPE_SECURITY_ENABLED</strong></li>
</ul>
<br/> Die ersten drei Flags geben den Gruppenbereich an. Das <strong>ADS_GROUP_TYPE_SECURITY_ENABLED</strong> -Flag gibt den Gruppentyp an. Wenn dieses Flag festgelegt ist, handelt es sich bei der Gruppe um eine Sicherheitsgruppe. Wenn dieses Flag nicht festgelegt ist, handelt es sich bei der Gruppe um eine Verteiler Gruppe. Weitere Informationen finden Sie unter <a href="#group-types">Group Types</a>.<br/></td>
</tr>
<tr class="even">
<td><strong>memberOf</strong></td>
<td>Das Attribut " <strong>Member</strong> " ist ein Attribut mit mehreren Werten, das die Liste der Distinguished Names für Gruppen enthält, die die Gruppe als Member enthalten. Dieses Attribut listet die Gruppen auf, unter denen die Gruppe direkt in die Liste eingefügt wird. Sie enthält nicht die rekursive Liste der gruppierten Vorgänger. Wenn z. b. Gruppe d in Gruppe c und Gruppe b und Gruppe b in Gruppe A eingefügt wurden, <strong>würde das Attribut Attribut der Gruppe</strong> D die Gruppe c und Gruppe b auflisten, aber nicht gruppieren a.<br/></td>
</tr>
<tr class="odd">
<td><strong>objectGUID</strong></td>
<td>Das <strong>objectGUID</strong> -Attribut ist ein Einzelwert Attribut, bei dem es sich um den eindeutigen Bezeichner des Objekts handelt. Dieses Attribut ist ein global eindeutiger Bezeichner (GUID). Wenn ein Objekt im Verzeichnis erstellt wird, generiert der Active Directory Server eine GUID und weist Sie dem <strong>objectGUID</strong> -Attribut des Objekts zu. Die GUID ist im gesamten Unternehmen und an anderer Stelle eindeutig.<br/> Die <strong>objectGUID</strong> ist eine 128-Bit-GUID-Struktur, die als oktetstring gespeichert wird.<br/></td>
</tr>
<tr class="even">
<td><strong>objectSID</strong></td>
<td>Das <strong>objectSID</strong> -Attribut ist ein Einzelwert Attribut, das die Sicherheits-ID (SID) der Gruppe angibt. Die SID ist ein eindeutiger Wert, der zum Identifizieren der Gruppe als Sicherheits Prinzipal verwendet wird. Es handelt sich um einen binären Wert, den das System festlegt, wenn die Gruppe erstellt wird.<br/> Jede Gruppe verfügt über eine eindeutige SID, auf der sich die Windows NT/Windows 2000-Server Domäne befindet, die im <strong>objectSID</strong> -Attribut des Group-Objekts im Verzeichnis gespeichert wird. Jedes Mal, wenn sich ein Benutzer anmeldet, ruft das System die sid für die Gruppen ab, denen der Benutzer angehört, und legt Sie im Zugriffs Token des Benutzers ab. Das System verwendet die SIDs im Zugriffs Token des Benutzers, um den Benutzer und seine Gruppenmitgliedschaften in allen nachfolgenden Interaktionen mit der Sicherheit von Windows NT/Windows 2000 zu identifizieren.<br/> Wenn eine SID als eindeutiger Bezeichner für einen Benutzer oder eine Gruppe verwendet wurde, kann Sie nicht mehr verwendet werden, um einen anderen Benutzer oder eine andere Gruppe zu identifizieren.<br/></td>
</tr>
<tr class="odd">
<td><strong>sAMAccountName</strong></td>
<td>Das <strong>sAMAccountName</strong> -Attribut ist ein Einzelwert Attribut, bei dem es sich um den Anmelde Namen handelt, der zur Unterstützung von Clients und Servern aus einer früheren Version (Windows 95, Windows 98 und LAN-Manager) verwendet wird. Der <strong>sAMAccountName</strong> sollte weniger als 20 Zeichen lang sein, damit Clients und Server aus einer früheren Version unterstützt werden.<br/> Der <strong>sAMAccountName</strong> muss für alle Sicherheits Prinzipal Objekte innerhalb einer Domäne eindeutig sein.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="group-types"></a>Gruppen Typen

Es gibt zwei Typen von Gruppen, die durch Active Directory Domain Services, *Sicherheitsgruppen* und *Verteiler Gruppen* definiert werden.

Eine Sicherheitsgruppe bietet eine logische Gruppierung von Objekten, und die Gruppe selbst kann als Sicherheits Prinzipal in einer Access Control Liste (ACL) verwendet werden. Wenn eine Sicherheitsgruppe Zugriff auf ein Objekt erhält, erhalten alle Mitglieder der Sicherheitsgruppe automatisch denselben Zugriff auf das Objekt. Sicherheitsgruppen mit universellem Bereich können auch als e-Mail-Entität verwendet werden. Wenn eine e-Mail-Nachricht an eine universelle Sicherheitsgruppe gesendet wird, wird die Nachricht an alle Mitglieder der Gruppe gesendet.

Eine Verteiler Gruppe bietet auch eine logische Gruppierung von Objekten, kann aber keine Zugriffsberechtigungen bereitstellen. Verteiler Gruppen sind nicht für die Sicherheit aktiviert und können nicht als Sicherheits Prinzipal in einer ACL verwendet werden. Verteiler Gruppen werden nur zu Gruppierungs Zwecken verwendet. Verteilerlisten können z. b. mit e-Mail-Anwendungen wie Exchange verwendet werden, um eine e-Mail an eine Sammlung von Benutzern zu senden.

Weitere Informationen zu Gruppen Typen in Active Directory Domain Services finden Sie im Thema zu [Gruppen Typen](/previous-versions/windows/it-pro/windows-server-2003/cc781446(v=ws.10)) in [Microsoft TechNet](https://technet.microsoft.com/default.aspx).

## <a name="group-scope"></a>Gruppenbereich

Es gibt drei Gruppen Bereiche, die durch Active Directory Domain Services, *universell*, *Global* und in der *lokalen Domäne* definiert werden. Der Bereich der Gruppe definiert, welche Typen von Objekten zur Gruppe gehören können, welche Typen von Gruppen die Gruppe als Mitglied aufweisen kann und welcher Bereich von Objekten, auf die Sicherheitsgruppen zugreifen können, zugänglich ist. Wenn die Domänen Funktionsebene auf den gemischten Modus von Windows 2000 festgelegt ist, können keine Sicherheitsgruppen mit universellem Bereich erstellt werden.

In der folgenden Tabelle werden die drei Gruppen Bereiche und weitere Informationen zu den einzelnen Bereichen für eine Sicherheitsgruppe aufgelistet.

| Bereich                   | Mögliche Member                                                                                                                                                                                                                                      | Bereichs Konvertierung                                                                                                                                                 | Berechtigungen können erteilt werden.                                                       | Möglicher Member von                                                                                                                                                                                                  |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Universell<br/>    | Konten aus einer beliebigen Domäne in derselben Gesamtstruktur.<br/> Globale Gruppen aus beliebigen Domänen in derselben Gesamtstruktur.<br/> Andere universelle Gruppen aus beliebigen Domänen in derselben Gesamtstruktur.<br/>                                                            | Kann in einen lokalen Domänen Bereich konvertiert werden.<br/> Kann in den globalen Gültigkeitsbereich konvertiert werden, solange die Gruppe keine anderen universellen Gruppen enthält.<br/> | In einer beliebigen Domäne in derselben Gesamtstruktur oder vertrauenden Gesamtstrukturen.<br/>            | Andere universelle Gruppen in derselben Gesamtstruktur.<br/> Lokale Domänen Gruppen in derselben Gesamtstruktur oder vertrauenden Gesamtstrukturen.<br/> Lokale Gruppen auf Computern in derselben Gesamtstruktur oder vertrauenden Gesamtstrukturen.<br/>            |
| Global<br/>       | Konten aus derselben Domäne.<br/> Andere globale Gruppen aus derselben Domäne.<br/>                                                                                                                                                        | Kann in den universellen Gültigkeitsbereich konvertiert werden, solange die Gruppe nicht Mitglied einer anderen globalen Gruppe ist.<br/>                                                   | In einer beliebigen Domäne in derselben Gesamtstruktur oder in vertrauenswürdigen Domänen oder Gesamtstrukturen.<br/> | Universelle Gruppen aus beliebigen Domänen in derselben Gesamtstruktur.<br/> Andere globale Gruppen aus derselben Domäne.<br/> Lokale Domänen Gruppen aus einer beliebigen Domäne in derselben Gesamtstruktur oder einer vertrauenswürdigen Domäne.<br/> |
| Lokale Domäne<br/> | Konten aus einer beliebigen Domäne oder einer beliebigen vertrauenswürdigen Domäne.<br/> Globale Gruppen aus beliebigen Domänen oder einer beliebigen vertrauenswürdigen Domäne.<br/> Universelle Gruppen aus beliebigen Domänen in derselben Gesamtstruktur.<br/> Andere lokale Domänen Gruppen aus derselben Domäne.<br/> | Kann in den universellen Gültigkeitsbereich konvertiert werden, solange die Gruppe keine anderen lokalen Domänen Gruppen enthält.<br/>                                              | Innerhalb derselben Domäne.<br/>                                          | Andere lokale Domänen Gruppen aus derselben Domäne.<br/> Lokale Gruppen auf Computern in derselben Domäne, ausgenommen integrierte Gruppen mit bekannten SIDs.<br/>                                             |



 

 

