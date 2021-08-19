---
title: Erstellen einer Anwendungsverzeichnispartition
description: Eine Anwendungsverzeichnispartition wird durch ein domainDNS-Objekt mit dem instanceType-Attributwert DS \_ INSTANCETYPE \_ IS NC HEAD in Kombination mit \_ \_ DS \_ INSTANCETYPE NC IS \_ \_ \_ WRITEABLE dargestellt.
ms.assetid: 5e90f316-9d67-484d-98b8-0632dd3c2c43
ms.tgt_platform: multiple
keywords:
- Erstellen einer Anwendungsverzeichnispartition AD
- Anwendungsverzeichnispartitionen AD , Erstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c340bac215be62867dcddcda97326c33fc70c458ee242965258cc1ee24cf25f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118020539"
---
# <a name="creating-an-application-directory-partition"></a>Erstellen einer Anwendungsverzeichnispartition

Eine Anwendungsverzeichnispartition wird durch ein [**domainDNS-Objekt**](/windows/desktop/ADSchema/c-domaindns) mit dem [**instanceType-Attributwert**](/windows/desktop/ADSchema/a-instancetype) **DS \_ INSTANCETYPE \_ IS NC \_ \_ HEAD** in Kombination mit **DS \_ INSTANCETYPE NC IS \_ \_ \_ WRITEABLE** dargestellt. Dieses **domainDNS-Objekt** stellt den Stamm der Anwendungsverzeichnispartition (NC-Kopf) dar und ist ähnlich wie eine reguläre Domänenpartition benannt, z.B. "DC=dynamicdata,DC=fabrikam,DC=com", was dem DNS-Namen "dynamicdata.fabrikam.com" entspricht. Eine Anwendungsverzeichnispartition kann daher überall instanziiert werden, wo eine Domänenpartition instanziiert werden kann. Einer Anwendungsverzeichnispartition ist kein NetBIOS-Name zugeordnet.

Es ist möglich, Anwendungsverzeichnispartitionen zu schachteln, d. h. eine Anwendungsverzeichnispartition kann untergeordnete Anwendungsverzeichnispartitionen aufweisen. Suchvorgänge mit Unterstrukturbereich, die auf einem Hauptteil der Anwendungsverzeichnispartition basieren, generieren Fortsetzungsverweise auf die untergeordneten Anwendungsverzeichnispartitionen.

Ein Anwendungsverzeichnispartitionsreplikat kann nur auf einem Domänencontroller erstellt werden, der auf Windows Server 2003 und höher ausgeführt wird, und nur, wenn die fsmo-Rolle Domain-Naming von einem Windows Server 2003- und höher-Domänencontroller gehalten wird. In einer gemischten Gesamtstruktur mit Windows Server 2003-Domänencontrollern und Domänencontrollern auf der unteren Ebene (Windows 2000-Domänencontrollern oder Windows primären NT 4.0-Domänencontrollern) schlägt der Versuch fehl, ein Anwendungsverzeichnispartitionsreplikat auf einem Domänencontroller auf der unteren Ebene zu erstellen.

Eine Anwendungsverzeichnispartition verfügt auch über ein entsprechendes [**crossRef-Objekt**](/windows/desktop/ADSchema/c-crossref) im Container Partitionen der Konfigurationspartition. **CrossRef** kann vor dem Erstellen des [**domainDNS-Objekts**](/windows/desktop/ADSchema/c-domaindns) manuell erstellt werden. Das vorab erstellte **crossRef-Objekt** muss über die in der folgenden Tabelle aufgeführten Attributwerte verfügen. Andernfalls tritt bei der Partitionserstellung ein Fehler auf. Wenn das **crossRef-Objekt** nicht vorhanden ist, erstellt der Active Directory-Server eines, wenn die Anwendungsverzeichnispartition erstellt wird.

| attribute                          | Beschreibung                                                                                                                               |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot) | Enthält den DNS-Pfad des Domänencontrollers, auf dem die Anwendungsverzeichnispartition erstellt wird.                               |
| [**Aktiviert**](/windows/desktop/ADSchema/a-enabled) | Enthält **FALSE.**                                                                                                                       |
| [**Ncname**](/windows/desktop/ADSchema/a-ncname)   | Enthält den Distinguished Name der Partition. Im obigen Beispiel würde dieses Attribut "DC=dynamicdata,DC=mydomain,DC=com" enthalten. |



 

**Führen Sie die folgenden Schritte aus, um eine neue Anwendungsverzeichnispartition mit dem ersten Replikat zu erstellen.**

1.  Binden Sie an den Namespace für die neue Partition, und geben Sie dabei den Domänencontroller an, der die Anwendungsverzeichnispartition im ADsPath hosten soll. Um beispielsweise eine Partition mit einem ADsPath von "DC=dynamicdata,DC=mydomain,DC=com" zu erstellen, lautet die Bindung ADsPath "LDAP:// <domain controller> /DC=mydomain,DC=com", wobei &lt; "Domänencontroller" &gt; der DNS-Name des Domänencontrollers ist, der die Partition hosten soll.

    Der Bindungsvorgang muss die Optionen für schnelles Und Delegierungsvorgangs angeben. Mit der Option "Schnell" kann die Bindung auch dann erfolgreich ausgeführt werden, wenn der Namespace nicht vorhanden ist. Die Delegierungsoption ist erforderlich, damit der Domänencontroller sich mit den gleichen Anmeldeinformationen an den Domain-Naming FSMO-Rolleninhaber wenden kann.

    Die Systemversion des Domänencontrollers muss Windows Server 2003-Betriebssystem und höher sein.

2.  Erstellen Sie ein [**domainDNS-Objekt**](/windows/desktop/ADSchema/c-domaindns) mit einem entsprechenden Namen für die Partition, z. B. "DC=dynamicdata", um den Namenkontextkopf für die neue Partition darzustellen. Das **domainDNS-Objekt** muss über ein [**instanceType-Attribut**](/windows/desktop/ADSchema/a-instancetype) mit dem Wert 5 verfügen (**DS \_ INSTANCETYPE \_ IS NC \_ \_ HEAD** \| **DS \_ INSTANCETYPE NC IS \_ \_ \_ WRITEABLE**). Das **instanceType-Attribut** kann nur zur Erstellungszeit festgelegt werden, da es sich um ein systemspezifisches Attribut handelt.

Wenn das [**DomainDNS-Objekt**](/windows/desktop/ADSchema/c-domaindns) erstellt wird, führt der Active Directory-Server die folgenden Schritte aus:

1.  Sucht im Container Partitions nach einem [**crossRef-Objekt,**](/windows/desktop/ADSchema/c-crossref) das über einen [**nCName-Attributwert**](/windows/desktop/ADSchema/a-ncname) verfügt, der dem Distinguished Name der Partition entspricht, und ändert, wenn eine Übereinstimmung gefunden wird, das **crossRef-Objekt,** um die Anwendungsverzeichnispartition darzustellen. Wenn kein übereinstimmendes **crossRef-Objekt** gefunden wird, erstellt der Active Directory-Server ein neues **crossRef-Objekt,** das die Anwendungsverzeichnispartition darstellt.

    In der folgenden Tabelle sind wichtige Attribute des [**crossRef-Objekts**](/windows/desktop/ADSchema/c-crossref) aufgeführt.

    | attribute                                                              | Beschreibung                                                                                                                                        |
    |------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
    | [**Ncname**](/windows/desktop/ADSchema/a-ncname)                                       | Enthält den Distinguished Name der Partition.                                                                                                  |
    | [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot)                                     | Enthält den DNS-Namen der Partition.                                                                                                            |
    | [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) | Der Distinguished Name des [**nTDSDSA-Objekts**](/windows/desktop/ADSchema/c-ntdsdsa) des Domänencontrollers für das erste Replikat wird diesem Attribut hinzugefügt. |

    

     

2.  Initiieren Sie eine Synchronisierung der Konfigurationspartition, und warten Sie auf den Abschluss. Dadurch kann die Clientanwendung Konfigurationsparameter für die neu erstellte Anwendungsverzeichnispartition ändern, während sie an den gleichen Domänencontroller gebunden ist, der zum Erstellen der Anwendungsverzeichnispartition verwendet wird.
3.  Erstellen Sie das [**domainDNS-Objekt**](/windows/desktop/ADSchema/c-domaindns) mit den **Flags DS \_ INSTANCETYPE \_ IS NC \_ \_ HEAD** und **DS \_ INSTANCETYPE NC IS \_ \_ \_ WRITEABLE,** die für die [**instanceType-Eigenschaft**](/windows/desktop/ADSchema/a-instancetype) festgelegt sind. Die **instanceType-Eigenschaft** kann auch andere private Flags enthalten.
4.  Füllen Sie das [**Attribut ms-DS-Has-Master-NCs**](/windows/desktop/ADSchema/a-msds-hasmasterncs) des [**nTDSDSA-Objekts**](/windows/desktop/ADSchema/c-ntdsdsa) für den Zieldomänencontroller mit dem Distinguished Name der neu erstellten Anwendungsverzeichnispartition auf.

Wenn die Anwendungsverzeichnispartition erstellt oder ein neues Replikat der Anwendungsverzeichnispartition hinzugefügt und vollständig synchronisiert wird, registriert der Active Directory-Server das Replikat ordnungsgemäß bei NetLogon und DNS. Weitere Informationen und eine Liste der registrierten SRV-Einträge finden Sie unter [Suchen eines Anwendungsverzeichnispartitionshostservers.](locating-an-application-directory-partition-host-server.md)

Weitere Informationen zum Erstellen einer Anwendungsverzeichnispartition finden Sie unter [Beispielcode zum Erstellen einer Anwendungsverzeichnispartition.](example-code-for-creating-an-application-directory-partition.md)

## <a name="locating-the-partitions-container"></a>Suchen des Partitionscontainers

Der Distinguished Name des Partitionscontainers kann auf zwei Arten gefunden werden. Die erste ist komplizierter auszuführen, liefert aber immer ein genaues Ergebnis:

1.  Binden Sie an RootDSE, und rufen Sie das **configurationNamingContext-Attribut** ab.
2.  Verwenden Sie das **configurationNamingContext-Attribut,** um eine Bindung an den Konfigurationscontainer vorzunehmen.
3.  Suchen Sie im Konfigurationscontainer nach einem Objekt vom Typ [**crossRefContainer.**](/windows/desktop/ADSchema/c-crossrefcontainer)
4.  Rufen Sie den **DistinguishedName-Attributwert** des [**crossRefContainer-Objekts**](/windows/desktop/ADSchema/c-crossrefcontainer) ab. Dies ist der Distinguished Name des Partitionscontainers.

Weitere Informationen und ein Codebeispiel, das diese Methode zum Suchen des Partitionscontainers zeigt, finden Sie in der **GetPartitionsDNSearch-Funktion** im [Beispielcode zum Suchen des Partitionscontainers.](example-code-for-locating-the-partitions-container.md)

Die zweite Methode ist einfacher zu implementieren, basiert jedoch darauf, dass der Partitions-Container über einen bestimmten relativen Distinguished Name verfügt. Es ist derzeit nicht möglich, den Namen des Partitionscontainers zu ändern. Wenn diese Funktion jedoch in Zukunft hinzugefügt wird, funktioniert das folgende Verfahren nicht ordnungsgemäß, wenn der Partitions-Container umbenannt wurde.

1.  Binden Sie an RootDSE, und rufen Sie das **configurationNamingContext-Attribut** ab.
2.  Kombinieren Sie die Zeichenfolge "CN=Partitions", gefolgt vom **configurationNamingContext-Attribut,** um den Distinguished Name des Partitions-Containers zu bilden. Der Distinguished Name hat die Form "CN=Partitions,". <configuration DN>

Weitere Informationen und ein Codebeispiel, das diese Methode zum Suchen des Partitionscontainers zeigt, finden Sie in der **GetPartitionsDNManual-Funktion** im [Beispielcode zum Suchen des Partitionscontainers.](example-code-for-locating-the-partitions-container.md)

 

 