---
title: Eigenschaften des Dienstverbindungspunkts
description: Die Attribute der serviceConnectionPoint-Klasse sind für die meisten Dienste ausreichend.
ms.assetid: 08888d2c-b46e-4b86-87e4-0c061ea147a0
ms.tgt_platform: multiple
keywords:
- Eigenschaften des Dienstverbindungspunkts
- Dienstverbindungspunkte AD , Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1343833d1a61e4df6dfc44238f9f094b00844f0b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473486"
---
# <a name="service-connection-point-properties"></a>Eigenschaften des Dienstverbindungspunkts

Die Attribute der **serviceConnectionPoint-Klasse** sind für die meisten Dienste ausreichend. Active Directory Domain Services nicht definieren, wie die Attribute verwendet werden. Daher müssen die Clients Ihres Diensts in der Lage sein, die Daten in Ihren Dienst-SCPs zu interpretieren und zu verwenden. Dienste, die zusätzliche Daten über sich selbst veröffentlichen müssen, können das Active Directory-Schema erweitern, indem sie eine Unterklasse der **serviceConnectionPoint-Klasse** erstellen und der Unterklasse einen eindeutigen Namen geben. Weitere Informationen zu Schemaerweiterungen finden Sie unter [Erweitern des Schemas.](extending-the-schema.md)

Die wichtigsten Attribute eines SCP sind die **Schlüsselwörter**, **serviceDNSName**, **serviceDNSNameType**, **serviceClassName** und **serviceBindingInformation**. Clientanwendungen durchsuchen das Verzeichnis nach **Schlüsselwörterwerten,** um Ihren SCP zu suchen. Wenn Ihr SCP gefunden wird, können Clients andere Attribute lesen, um Dienstdaten abzurufen.




| Attribut | BESCHREIBUNG | 
|-----------|-------------|
| <strong>Schlüsselwörter</strong><br /> | Das <strong></strong> Schlüsselwortattribut kann mehrere Zeichenfolgenwerte enthalten, die Ihren Dienst identifizieren. Dieses Attribut ist im globalen Katalog enthalten. Dies bedeutet, dass Clients in einer beliebigen Domäne einer Unternehmensstruktur den globalen Katalog nach Schlüsselwörtern durchsuchen können, die Ihrem Dienst zugeordnet sind. Dieses Attribut wird ebenfalls indiziert, wodurch die Abfrageleistung verbessert wird. Das Installationsprogramm, das den SCP erstellt, legt die Werte des <strong>Schlüsselwortattributs</strong> fest. In der Regel werden diese Werte vom aktiven Dienst nicht geändert.<br /> Die genauen Schlüsselwörter, die Sie in Ihren SCP einschließen sollten, hängen davon ab, wie Clients nach Ihrem Dienst suchen. Die am besten zu verwendenden Schlüsselwörter sind GUID-Zeichenfolgen, da GUIDs in einer Gesamtstruktur garantiert eindeutig sind. Verwenden Sie das GUID-Zeichenfolgenformat, das von der <a href="/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring"><strong>UuidToString-Funktion</strong></a> in der RPC-Bibliothek zurückgegeben wird. Sie können auch für Menschen lesbare Namen einschließen, wenn Clients diese für die Suche nach Ihrem Dienst verwenden können. Die Schlüsselwörter in einem SCP sollten GUID-Zeichenfolgen und/oder Namen enthalten, die die folgenden Daten zu Ihrem Dienst identifizieren:<ul><li>Ihr Unternehmen oder Ihre Organisation: z. B. Fabrikam.</li><li>Das Produkt oder der Dienst, z. B. SQL Server. Dadurch können Clientanwendungen SCPs für Dienste dieses Typs finden.</li><li>Die spezifische Version des Produkts oder Diensts, z. B. 7.5.</li><li>Schließen Sie für SCPs, die einen bestimmten Satz von Daten oder Funktionen für einen Diensttyp veröffentlichen, eine GUID-Zeichenfolge oder einen Namen ein, der die jeweilige Instanz identifiziert. Beispielsweise kann ein Datenbankdienst einen SCP für eine bestimmte Datenbank veröffentlichen. In diesem Fall würde der SCP eine Produkt-GUID zum Identifizieren des Diensts und eine andere GUID zum Identifizieren der Datenbank enthalten.</li></ul><br /> | 
| <strong>serviceDNSName</strong> und <strong>serviceDNSNameType</strong><br /> | Clientanwendungen verwenden die Attribute <strong>serviceDNSName</strong> und <strong>serviceDNSNameType,</strong> um den Hostcomputer des Diensts zu bestimmen. Der <strong>Wert serviceDNSNameType</strong> gibt den Typ des DNS-Namens an, der von <strong>serviceDNSName</strong> in der Regel "A" angegeben wird, wenn <strong>serviceDNSName</strong> einen Hostnamen enthält, oder "SRV", wenn <strong>serviceDNSName</strong> einen SRV-Eintragsnamen enthält.<br /> Der <strong>Wert serviceDNSName</strong> ist in der Regel der DNS-Name des Hostcomputers des Diensts. Ihr Dienstinstallationsprogramm kann die <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa"><strong>GetComputerNameEx-Funktion</strong></a> aufrufen, um den DNS-Namen des lokalen Computers abzurufen.<br /> Für Dienste mit DNS-SRV-Einträgen kann <strong>serviceDNSName</strong> der Name des SRV-Eintrags sein. Eine Clientanwendung verwendet die DNS-APIs, um alle SRV-Einträge abzurufen, die diesem Namen entsprechen. Der Client ruft dann den DNS-Hostnamen aus einem der SRV-Einträge ab. Diese Technik ist für replizierte Dienste nützlich, da SRV-Einträge auch Daten enthalten, mit denen der Client das beste Replikat auswählen kann.<br /> | 
| <strong>serviceBindingInformation</strong><br /> | Eine Mehrwerteigenschaft, die Zeichenfolgenwerte enthält, die Daten speichern, die zum Binden an einen Dienst erforderlich sind. Diese Eigenschaft wird indiziert und im globalen Katalog repliziert.<br /> Der Inhalt von <strong>serviceBindingInformation</strong> ist spezifisch für den Dienst, der den SCP veröffentlicht hat. -Clients müssen die Bindungsdaten interpretieren. Im häufigsten Fall bestehen die Bindungsdaten aus einer Portnummer auf dem Diensthostcomputer.<br /> | 
| <strong>serviceClassName</strong><br /> | Eine Eigenschaft mit einem Wert, die die Vom SCP dargestellte Dienstklasse identifiziert. Dies ist eine beschreibende Zeichenfolge, die für den Dienst spezifisch ist, der den SCP veröffentlicht hat. Beispiel: SqlServer. Für Dienste, die gegenseitige Authentifizierung unterstützen, können Clients diese Eigenschaft zusammen mit dem DNS-Namen des Hostcomputers des Diensts verwenden, um einen Dienstprinzipalnamen zu bilden. Weitere Informationen finden Sie unter <a href="mutual-authentication-using-kerberos.md">Gegenseitige Authentifizierung mit Kerberos.</a><br /> | 




 

 

