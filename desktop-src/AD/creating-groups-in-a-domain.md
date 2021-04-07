---
title: Erstellen von Gruppen in einer Domäne
description: Ein Gruppen Objekt wird in Active Directory Domain Services im Domänen Container erstellt, in dem die neue Gruppe enthalten sein wird.
ms.assetid: 40792878-4219-4242-8cf7-b092b28f2ff4
ms.tgt_platform: multiple
keywords:
- Gruppen anzeigen, Erstellen von Gruppen in einer Domäne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 100700b08fb82b750ee68dfed6bcb26060929e87
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038780"
---
# <a name="creating-groups-in-a-domain"></a>Erstellen von Gruppen in einer Domäne

Ein Gruppen Objekt wird in Active Directory Domain Services im Domänen Container erstellt, in dem die neue Gruppe enthalten sein wird. Gruppen können im Stammverzeichnis der Domäne, innerhalb einer Organisationseinheit oder innerhalb eines Containers erstellt werden. Verwenden Sie die [**IADsContainer:: Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) -Methode oder die [**IDirectoryObject::**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) -Methode, um ein Gruppen Objekt zu erstellen.

Die folgenden Attribute sind erforderlich, um das Gruppen Objekt zu einer gültigen Gruppe zu machen, die vom Active Directory Server und dem Windows-Sicherheitssystem erkannt wird:

<dl> <dt>

<span id="cn"></span><span id="CN"></span>**2.300**
</dt> <dd>

Gibt den Namen des Gruppen Objekts im Verzeichnis an. Dabei handelt es sich um den relativen Distinguished Name des Objekts innerhalb des Containers, in dem die Gruppe erstellt wird.

</dd> <dt>

<span id="groupType"></span><span id="grouptype"></span><span id="GROUPTYPE"></span>**GroupType**
</dt> <dd>

Enthält eine ganze Zahl, die den Gruppentyp und den Bereich angibt. Die Enumeration der [**ADS- \_ \_ Gruppentyp \_**](/windows/win32/api/iads/ne-iads-ads_group_type_enum) Enumeration definiert die möglichen Werte für das **GroupType** -Attribut.

In der folgenden Liste sind allgemeine Gruppen Typen und Werte für dieses Attribut definiert.

<dl> <dt>

<span id="Domain_Local_Distribution"></span><span id="domain_local_distribution"></span><span id="DOMAIN_LOCAL_DISTRIBUTION"></span>Lokale Domänen Verteilung
</dt> <dd>

**AD \_ - \_ Gruppentyp \_ Domäne \_ lokale \_ Gruppe**

</dd> <dt>

<span id="Domain_Local_Security"></span><span id="domain_local_security"></span><span id="DOMAIN_LOCAL_SECURITY"></span>Lokale Sicherheit der Domäne
</dt> <dd>

**Anzeigen \_ \_Gruppentyp \_ Domäne \_ lokale \_ Gruppen** \| **anzeigen \_ Gruppen \_ \_ Sicherheit \_ aktiviert**

</dd> <dt>

<span id="Global_Distribution"></span><span id="global_distribution"></span><span id="GLOBAL_DISTRIBUTION"></span>Globale Verteilung
</dt> <dd>

**\_ \_ \_ globale Gruppe "ADS Group Type" \_**

</dd> <dt>

<span id="Global_Security"></span><span id="global_security"></span><span id="GLOBAL_SECURITY"></span>Globale Sicherheit
</dt> <dd>

**Anzeigen \_ Gruppentyp der \_ \_ globalen \_ Gruppe** \| **ADS- \_ \_ Gruppentyp \_ Sicherheit \_ aktiviert**

</dd> <dt>

<span id="Universal_Distribution"></span><span id="universal_distribution"></span><span id="UNIVERSAL_DISTRIBUTION"></span>Universelle Verteilung
</dt> <dd>

**\_ \_ \_ universelle Gruppe ADS-Gruppentyp \_**

</dd> <dt>

<span id="Universal_Security"></span><span id="universal_security"></span><span id="UNIVERSAL_SECURITY"></span>Universelle Sicherheit
</dt> <dd>

**Anzeigen \_ \_Gruppentyp \_ \_** -Gruppentyp-Gruppentyp \| **\_ \_ \_ Sicherheit \_ aktiviert**

</dd> <dt>


</dt> <dd>

</dd> </dl>

Wenn die Gruppe für das Festlegen der Zugriffs Steuerung für Verzeichnisobjekte vorgesehen ist, sollte die Gruppe eine globale Sicherheits-oder universelle Sicherheitsgruppe sein.

Beachten Sie, dass universelle Sicherheitsgruppen nur auf Windows 2000-Domänen erstellt werden können, die im einheitlichen Modus ausgeführt werden. Weitere Informationen zum Erkennen von gemischtem und einheitlichem Modus finden Sie unter [Ermitteln des Betriebsmodus einer Domäne](detecting-the-operation-mode-of-a-domain.md).

</dd> <dt>

<span id="sAMAccountName"></span><span id="samaccountname"></span><span id="SAMACCOUNTNAME"></span>**sAMAccountName**
</dt> <dd>

Enthält eine Zeichenfolge, die den Namen für die Unterstützung von Clients und Servern aus einer früheren Version enthält. Der **sAMAccountName** sollte weniger als 20 Zeichen lang sein, damit Clients einer früheren Version von Windows unterstützt werden.

Der **sAMAccountName** muss für alle Sicherheits Prinzipal Objekte innerhalb der Domäne eindeutig sein. Eine Abfrage sollte für die Domäne ausgeführt werden, um zu überprüfen, ob **sAMAccountName** innerhalb der Domäne eindeutig ist.

</dd> </dl>

Die Mitglieder der Gruppe können zur Erstellungszeit mithilfe der [**IDirectoryObject:: deedsobject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) -Methode hinzugefügt werden. Optional können Mitglieder der Gruppe nach der Erstellung mithilfe der [**IADsGroup:: Add**](/windows/desktop/api/iads/nf-iads-iadsgroup-add) -Methode hinzugefügt werden. Weitere Informationen zum Hinzufügen von Mitgliedern zu einer Gruppe finden Sie unter [Hinzufügen von Mitgliedern zu Gruppen in einer Domäne](adding-members-to-groups-in-a-domain.md).

 

 