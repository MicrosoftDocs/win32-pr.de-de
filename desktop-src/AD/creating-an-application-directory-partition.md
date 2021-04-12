---
title: Erstellen einer Anwendungsverzeichnis Partition
description: Eine Anwendungsverzeichnis Partition wird durch ein domainDNS-Objekt mit dem instanceType-Attribut Wert ' DS \_ instanceType ' \_ ist eine NC- \_ \_ Kopfzeile, kombiniert mit dem DS \_ instanceType \_ NC \_ ist \_ beschreibbar.
ms.assetid: 5e90f316-9d67-484d-98b8-0632dd3c2c43
ms.tgt_platform: multiple
keywords:
- Erstellen einer Anwendungsverzeichnis-Partitions Anzeige
- Anwendungsverzeichnis Partitionen AD, erstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a17471696825179b6e49230b5168abbaf88b8e2
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472621"
---
# <a name="creating-an-application-directory-partition"></a>Erstellen einer Anwendungsverzeichnis Partition

Eine Anwendungsverzeichnis Partition wird durch ein [**domainDns**](/windows/desktop/ADSchema/c-domaindns) -Objekt mit dem [**instanceType**](/windows/desktop/ADSchema/a-instancetype) -Attribut Wert ' **DS \_ instanceType ' \_ ist eine NC- \_ \_ Kopfzeile** , kombiniert mit dem **DS \_ instanceType \_ NC \_ ist \_ beschreibbar**. Dieses **domainDns** -Objekt stellt den Stamm der Anwendungsverzeichnis Partition (NC-Head) dar und ähnelt einer regulären Domänen Partition, z. b. "DC = DynamicData, DC = fabrikam, DC = com", die dem DNS-Namen "DynamicData.fabrikam.com" entspricht. Eine Anwendungsverzeichnis Partition kann daher überall dort instanziiert werden, wo eine Domänen Partition instanziiert werden kann. Einer Anwendungsverzeichnis Partition ist kein NetBIOS-Name zugeordnet.

Es ist möglich, Anwendungsverzeichnis Partitionen zu schachteln, d. h., eine Anwendungsverzeichnis Partition kann über untergeordnete Anwendungsverzeichnis Partitionen verfügen. Suchvorgänge mit einem Teilstruktur Bereich, der auf einer Anwendungsverzeichnis Partition basiert, generieren Fortsetzungs Verweise auf die untergeordneten Anwendungsverzeichnis Partitionen.

Ein Anwendungsverzeichnis-Partitions Replikat kann nur auf einem Domänen Controller erstellt werden, der unter Windows Server 2003 und höher ausgeführt wird, und nur, wenn die Domain-Naming FSMO-Rolle von einem Domänen Controller mit Windows Server 2003 und höher belegt wird. In einer gemischten Gesamtstruktur mit Windows Server 2003-Domänen Controllern und untergeordneten Domänen Controllern (Windows 2000-Domänen Controller oder primäre Windows NT 4,0-Domänen Controller) tritt beim Versuch, ein Anwendungsverzeichnis-Partitions Replikat auf einem untergeordneten Domänen Controller zu erstellen, ein Fehler auf.

Eine Anwendungsverzeichnis Partition verfügt auch über ein entsprechendes [**CrossRef**](/windows/desktop/ADSchema/c-crossref) -Objekt im Partitions Container der Konfigurations Partition. Vor dem Erstellen des [**domainDns**](/windows/desktop/ADSchema/c-domaindns) -Objekts kann das **CrossRef** -Objekt manuell erstellt werden. Das vorab erstellte **CrossRef** -Objekt muss über die in der folgenden Tabelle angezeigten Attributwerte verfügen, oder die Partitions Erstellung schlägt fehl. Wenn das **CrossRef** -Objekt nicht vorhanden ist, wird es vom Active Directory Server beim Erstellen der Anwendungsverzeichnis Partition erstellt.

| Attribut                          | BESCHREIBUNG                                                                                                                               |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot) | Enthält den DNS-Pfad des Domänen Controllers, auf dem die Anwendungsverzeichnis Partition erstellt wird.                               |
| [**Aktiviert**](/windows/desktop/ADSchema/a-enabled) | Enthält **false**.                                                                                                                       |
| [**NCName**](/windows/desktop/ADSchema/a-ncname)   | Enthält den Distinguished Name der Partition. Im obigen Beispiel würde dieses Attribut "DC = DynamicData, DC = MyDomain, DC = com" enthalten. |



 

**Führen Sie die folgenden Schritte aus, um eine neue Anwendungsverzeichnis Partition mit dem ersten Replikat zu erstellen.**

1.  Binden Sie an den Namespace für die neue Partition, und geben Sie dabei den Domänen Controller an, der die Anwendungsverzeichnis Partition im ADsPath hostet. Um z. b. eine Partition mit dem ADsPath "DC = DynamicData, DC = MyDomain, DC = com" zu erstellen, lautet der ADsPath der Bindung "LDAP:// <domain controller> "/DC = MyDomain, DC = com ", wobei" &lt; Domänen Controller &gt; "der DNS-Name des Domänen Controllers ist, der die Partition hostet.

    Der Bindungs Vorgang muss die Optionen "schnell" und "Delegierung" angeben. Die Option fast ermöglicht die erfolgreiche Bindung, auch wenn der Namespace nicht vorhanden ist. Die Delegierungs Option ist erforderlich, damit der Domänen Controller den Inhaber der Domain-Naming FSMO-Rolle mit denselben Anmelde Informationen kontaktieren kann.

    Die System Version des Domänen Controllers muss das Betriebssystem Windows Server 2003 und höher aufweisen.

2.  Erstellen Sie ein [**domainDns**](/windows/desktop/ADSchema/c-domaindns) -Objekt mit einem entsprechenden Namen für die Partition, z. b. "DC = DynamicData", um den namens Kontext Kopf für die neue Partition darzustellen. Das **domainDns** -Objekt muss ein [**instanceType**](/windows/desktop/ADSchema/a-instancetype) -Attribut mit dem Wert 5 aufweisen (der **DS- \_ instanceType \_ ist \_ NC \_ Head** \| **DS \_ instanceType \_ NC \_ ist \_ beschreibbar**). Das **instanceType** -Attribut kann nur zum Zeitpunkt der Erstellung festgelegt werden, da es sich um ein System eigenes Attribut handelt.

Wenn das [**domainDns**](/windows/desktop/ADSchema/c-domaindns) -Objekt erstellt wird, führt der Active Directory Server die folgenden Schritte aus:

1.  Sucht im Partitions Container nach einem [**CrossRef**](/windows/desktop/ADSchema/c-crossref) -Objekt, das über einen [**NCName**](/windows/desktop/ADSchema/a-ncname) -Attribut Wert verfügt, der mit dem Distinguished Name der Partition übereinstimmt, und ändert, wenn eine Übereinstimmung gefunden wird, das **CrossRef** -Objekt so, dass es die Anwendungsverzeichnis Partition darstellt. Wenn ein entsprechendes **CrossRef** -Objekt nicht gefunden wird, erstellt der Active Directory Server ein neues **CrossRef** -Objekt, das die Anwendungsverzeichnis Partition darstellt.

    In der folgenden Tabelle sind wichtige Attribute des [**CrossRef**](/windows/desktop/ADSchema/c-crossref) -Objekts aufgeführt.

    | Attribut                                                              | BESCHREIBUNG                                                                                                                                        |
    |------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
    | [**NCName**](/windows/desktop/ADSchema/a-ncname)                                       | Enthält den Distinguished Name der Partition.                                                                                                  |
    | [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot)                                     | Enthält den DNS-Namen der Partition.                                                                                                            |
    | [**MSDS-NC-Replikat-Standorte**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) | Diesem Attribut wird der Distinguished Name des [**NTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) -Objekts des Domänen Controllers für das erste Replikat hinzugefügt. |

    

     

2.  Initiieren Sie eine Synchronisierung der Konfigurations Partition, und warten Sie auf den Abschluss. Dadurch kann die Client Anwendung Konfigurationsparameter für die neu erstellte Anwendungsverzeichnis Partition ändern, während Sie an denselben Domänen Controller gebunden ist, der zum Erstellen der Anwendungsverzeichnis Partition verwendet wird.
3.  Erstellen Sie das [**domainDns**](/windows/desktop/ADSchema/c-domaindns) -Objekt mit dem **DS \_ instanceType \_ is \_ NC \_ Head** , und der **DS \_ instanceType \_ NC \_ ist \_ beschreibbare** Flags, die für die [**instanceType**](/windows/desktop/ADSchema/a-instancetype) -Eigenschaft festgelegt sind. Die **instanceType** -Eigenschaft kann auch andere private Flags enthalten.
4.  Füllen Sie das Attribut [**ms-DS-has-Master-NCS**](/windows/desktop/ADSchema/a-msds-hasmasterncs) des [**NTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) -Objekts für den Zieldomänen Controller mit dem Distinguished Name der neu erstellten Anwendungsverzeichnis Partition auf.

Wenn die Anwendungsverzeichnis Partition erstellt wird oder wenn ein neues Replikat der Anwendungsverzeichnis Partition hinzugefügt und vollständig synchronisiert wird, registriert der Active Directory Server das Replikat ordnungsgemäß bei Netlogon und DNS. Weitere Informationen und eine Liste der registrierten SRV-Einträge finden Sie untersuchen [eines Anwendungsverzeichnis-Partitions Host Servers](locating-an-application-directory-partition-host-server.md).

Weitere Informationen zum Erstellen einer Anwendungsverzeichnis Partition finden Sie unter [Beispiel Code zum Erstellen einer Anwendungsverzeichnis Partition](example-code-for-creating-an-application-directory-partition.md).

## <a name="locating-the-partitions-container"></a>Suchen des Partitions Containers

Der Distinguished Name des Partitions Containers kann auf zwei Arten gefunden werden. Der erste Vorgang ist komplizierter, aber es wird immer ein genaues Ergebnis bereitgestellt:

1.  Binden an RootDSE und Abrufen des **configurationNamingContext** -Attributs.
2.  Verwenden Sie das **configurationNamingContext** -Attribut, um eine Bindung an den Konfigurations Container herzustellen.
3.  Suchen Sie im Konfigurations Container nach einem Objekt, das den Typ [**CrossRef Container**](/windows/desktop/ADSchema/c-crossrefcontainer) hat.
4.  Rufen Sie den Wert des Attributs " **unterbrechname** " des [**crossrefcontainer**](/windows/desktop/ADSchema/c-crossrefcontainer) -Objekts ab. Dabei handelt es sich um den Distinguished Name des Partitions Containers.

Weitere Informationen und ein Codebeispiel, in dem diese Methode zum Suchen des Partitions Containers gezeigt wird, finden Sie in der **getpartitionsdnsearch** -Funktion im [Beispielcode zum Suchen des Partitions Containers](example-code-for-locating-the-partitions-container.md).

Die zweite Methode ist einfacher zu implementieren, aber Sie basiert auf dem Partitions Container, der einen bestimmten relativen Distinguished Name aufweist. Es ist derzeit nicht möglich, den Namen des Partitions Containers zu ändern. wenn diese Funktion jedoch in Zukunft hinzugefügt wird, funktioniert das nachfolgende Verfahren nicht ordnungsgemäß, wenn der Partitions Container umbenannt wurde.

1.  Binden an RootDSE und Abrufen des **configurationNamingContext** -Attributs.
2.  Kombinieren Sie die Zeichenfolge "CN = Partitions", gefolgt vom **configurationNamingContext** -Attribut, um den Distinguished Name des Partitions Containers zu bilden. Der Distinguished Name hat das Format "CN = Partitions <configuration DN> ".

Weitere Informationen und ein Codebeispiel, in dem diese Methode für die Suche nach dem Partitions Container veranschaulicht wird, finden Sie in der **getpartitionsdnmanual** -Funktion im [Beispielcode zum Suchen des Partitions Containers](example-code-for-locating-the-partitions-container.md).

 

 