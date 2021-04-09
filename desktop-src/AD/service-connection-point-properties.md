---
title: Eigenschaften des Dienst Verbindungs Punkts
description: Die Attribute der serviceConnectionPoint-Klasse sind für die meisten Dienste ausreichend.
ms.assetid: 08888d2c-b46e-4b86-87e4-0c061ea147a0
ms.tgt_platform: multiple
keywords:
- Eigenschaften des Dienst Verbindungs Punkts
- Dienst Verbindungspunkte, Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 511bbba8acf50a185f1bdd8b55d9b7f8ce684817
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104101423"
---
# <a name="service-connection-point-properties"></a>Eigenschaften des Dienst Verbindungs Punkts

Die Attribute der **serviceConnectionPoint** -Klasse sind für die meisten Dienste ausreichend. Active Directory Domain Services nicht definieren, wie die Attribute verwendet werden, sodass die Clients Ihres Dienstanbieter in der Lage sein müssen, die Daten in Ihren Service-SCPs zu interpretieren und zu verwenden. Dienste, die zusätzliche Daten über sich selbst veröffentlichen müssen, können das Active Directory Schema erweitern, indem Sie eine Unterklasse der **serviceConnectionPoint** -Klasse erstellen und der Unterklasse einen eindeutigen Namen geben. Weitere Informationen zu Schema Erweiterungen finden Sie unter [Erweitern des Schemas](extending-the-schema.md).

Die wichtigsten Attribute eines SCP sind " **Keywords**", " **servicednsname**", " **serviceDNSNameType**", " **serviceClassName**" und " **serviceBindingInformation**". Client Anwendungen durchsuchen das Verzeichnis nach **Schlüsselwörtern** , um nach dem SCP zu suchen. Wenn Ihr Dienst Verbindungspunkt gefunden wird, können Clients andere Attribute zum Abrufen von Dienst Daten lesen.



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
<td><strong>Keywords</strong><br/></td>
<td>Das <strong>Keywords</strong> -Attribut kann mehrere Zeichen folgen Werte enthalten, die den Dienst identifizieren. Dieses Attribut ist im globalen Katalog enthalten. Dies bedeutet, dass Clients in einer beliebigen Domäne einer Unternehmens Gesamtstruktur den globalen Katalog nach Schlüsselwörtern durchsuchen können, die Ihrem Dienst zugeordnet sind. Dieses Attribut wird ebenfalls indiziert, wodurch die Abfrageleistung verbessert wird. Das Installationsprogramm, das den SCP erstellt, legt die Werte des Attributs " <strong>Keywords</strong> " fest. Diese Werte werden in der Regel vom aktiven Dienst nicht geändert.<br/> Die genauen Schlüsselwörter, die Sie in ihren SCP einbeziehen sollten, hängen davon ab, wie Clients nach Ihrem Dienst suchen. Die besten Schlüsselwörter für die Verwendung sind GUID-Zeichen folgen, da GUIDs garantiert in einer Gesamtstruktur eindeutig sind. Verwenden Sie das von der <a href="/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring"><strong>UUIDToString</strong></a> -Funktion in der RPC-Bibliothek zurückgegebene GUID-Zeichen folgen Format. Sie können auch lesbare Namen einschließen, wenn Sie von Clients verwendet werden können, um nach dem Dienst zu suchen. Die Schlüsselwörter in einem SCP sollten GUID-Zeichen folgen und/oder Namen enthalten, die die folgenden Daten zu Ihrem Dienst identifizieren:
<ul>
<li>Ihr Unternehmen oder Ihre Organisation: z. b. fabrikam.</li>
<li>Das Produkt oder der Dienst: z. b. SQL Server. Dadurch können Client Anwendungen SCPs für Dienste dieses Typs suchen.</li>
<li>Die spezifische Version des Produkts oder Dienstanbieter, z. b. 7,5.</li>
<li>Fügen Sie für SCPs, die einen bestimmten Satz von Daten oder Funktionen für einen Diensttyp veröffentlichen, eine GUID-Zeichenfolge oder einen Namen ein, der die jeweilige Instanz identifiziert. Ein Datenbankdienst könnte z. b. einen Dienst Verbindungspunkt für eine bestimmte Datenbank veröffentlichen. In diesem Fall würde der SCP eine Produkt-GUID enthalten, um den Dienst zu identifizieren, und eine weitere GUID, um die Datenbank zu identifizieren.</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><strong>servicednsname</strong> und <strong>serviceDNSNameType</strong><br/></td>
<td>Client Anwendungen verwenden das <strong>servicednsname</strong> -Attribut und das <strong>serviceDNSNameType</strong> -Attribut, um den Host Computer des Diensts zu bestimmen. Der Wert <strong>serviceDNSNameType</strong> gibt den Typ des DNS-Namens an, der von <strong>servicednsname</strong> angegeben wird. Dies ist normalerweise &quot; ein, &quot; Wenn <strong>servicednsname</strong> einen Hostnamen oder &quot; SRV enthält, &quot; Wenn <strong>servicednsname</strong> einen SRV-Daten Satz Namen enthält.<br/> Der Wert <strong>servicednsname</strong> ist in der Regel der DNS-Name des Host Computers des Diensts. Das Dienst Installationsprogramm kann die <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa"><strong>GetComputerNameEx</strong></a> -Funktion aufrufen, um den DNS-Namen des lokalen Computers abzurufen.<br/> Für Dienste mit DNS-SRV-Einträgen kann <strong>servicednsname</strong> der Name des SRV-Datensatzes sein. Eine Client Anwendung verwendet die DNS-APIs, um alle SRV-Einträge abzurufen, die diesem Namen entsprechen. Der Client ruft dann den DNS-Hostnamen aus einem der SRV-Datensätze ab. Dieses Verfahren ist für replizierte Dienste nützlich, da SRV-Einträge auch Daten enthalten, die es dem Client ermöglichen, das beste Replikat auszuwählen.<br/></td>
</tr>
<tr class="odd">
<td><strong>serviceBindingInformation</strong><br/></td>
<td>Eine mehrwertige Eigenschaft, die Zeichen folgen Werte enthält, die Daten speichern, die für die Bindung an einen Dienst erforderlich sind. Diese Eigenschaft wird indiziert und in den globalen Katalog repliziert.<br/> Der Inhalt von <strong>serviceBindingInformation</strong> ist spezifisch für den Dienst, der den SCP veröffentlicht hat. die Bindungs Daten müssen von Clients interpretiert werden. Im häufigsten Fall besteht die Bindungs Daten aus einer Portnummer auf dem Dienst Host Computer.<br/></td>
</tr>
<tr class="even">
<td><strong>serviceClassName</strong><br/></td>
<td>Eine Einzelwert Eigenschaft, die die Dienstklasse identifiziert, die vom SCP dargestellt wird. Dies ist eine beschreibende Zeichenfolge für den Dienst, der den SCP veröffentlicht hat. Beispiel: SqlServer. Bei Diensten, die die gegenseitige Authentifizierung unterstützen, können Clients diese Eigenschaft zusammen mit dem DNS-Namen des Host Computers des Diensts verwenden, um einen Dienst Prinzipal Namen zu bilden. Weitere Informationen finden Sie unter <a href="mutual-authentication-using-kerberos.md">gegenseitige Authentifizierung mithilfe von Kerberos</a>.<br/></td>
</tr>
</tbody>
</table>



 

 

