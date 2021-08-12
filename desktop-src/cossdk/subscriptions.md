---
description: Abonnementdaten befinden sich im COM+-Katalog des Abonnements. Ein Abonnement kann entweder mithilfe des Component Services-Verwaltungstools oder programmgesteuert mithilfe der ICOMAdminCatalog::InstallComponent-Schnittstelle erstellt werden.
ms.assetid: 190e88f3-1d87-4c27-9451-0a633cbae829
title: Abonnements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48810ae90f3507ea7afb661b106c4d05f8cc5b9a4f1b09aafdfb26d9fdb03a75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546172"
---
# <a name="subscriptions"></a>Abonnements

Abonnementdaten befinden sich im COM+-Katalog des Abonnements. Ein Abonnement kann entweder mithilfe des Component Services-Verwaltungstools oder programmgesteuert mithilfe der [**ICOMAdminCatalog::InstallComponent-Schnittstelle**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installcomponent) erstellt werden.

Die [**SubscriptionsForComponent-Sammlung**](subscriptionsforcomponent.md) wird verwendet, um Informationen zu Abonnements hinzuzufügen, zu löschen oder zu ändern. Die **SubscriptionsForComponent-Auflistung** ist eine untergeordnete Sammlung für eine Komponente. Um ein Abonnement hinzuzufügen, abrufen Sie die **SubscriptionsForComponent-Sammlung** der Komponente, und verwenden Sie die [**Add-Methode,**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) um der Sammlung einen Eintrag hinzuzufügen. Verwenden Sie die Value-Eigenschaft, um die verschiedenen Eigenschaften des [**Abonnementobjekts**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_value) einzurichten. Um die Änderungen zu speichern, verwenden [**Sie SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) für das **SubscriptionsForComponent-Sammlungsobjekt.**

Sie können auch das Verwaltungstool Komponentendienste verwenden, um einige, aber nicht alle Abonnementeigenschaften zu ändern. Abonnements geben die folgenden Informationen an:

-   Identität und Speicherort des Abonnenten
-   Bereitstellungsmethode
-   Zu übermittelnde Ereignismethoden
-   Ereignisklassenobjekt und PublisherID-Eigenschaft einer Ereignisklassenkomponente, von der der Abonnent Ereignisse empfangen möchte

Abonnements sind unabhängig von Ereignisklassenobjekten vorhanden. Sie können ein Abonnement deaktivieren, indem Sie die Enabled-Eigenschaft auf False festlegen. Ein deaktiviertes Abonnement wird nicht von COM+-Ereignissen aufgerufen.

Die drei Abonnementtypen sind wie folgt:

<dl> <dt>

<span id="Persistent"></span><span id="persistent"></span><span id="PERSISTENT"></span>Persistente
</dt> <dd>

Persistente Abonnements befinden sich im COM+-Katalog und sind unabhängig von der Lebensdauer des Abonnenten. Persistente Abonnements überstehen einen Systemneustart. Im Allgemeinen wird ein persistentes Abonnement erstellt, wenn eine Anwendung auf dem Computer eines Abonnenten installiert und entfernt wird, wenn die Anwendung entfernt wird. Nachdem ein persistentes Abonnement erstellt wurde, aktiviert COM+-Ereignisse den Abonnenten jedes Mal, wenn ein Ereignis an ihn übermittelt werden soll.

Wenn ein Herausgeber ein [Ereignisklassenobjekt](the-com--event-class-object.md) instanziiert und aufruft, sucht das Objekt nach allen persistenten Abonnements im COM+-Katalog und erstellt eine neue Instanz jedes Objekts. Der Erstellungsprozess kann entweder direkt oder über einen Moniker für Komponenten in der Warteschlange erfolgen. Geben Sie das Abonnentenobjekt durch die [**SubscriberMoniker-Eigenschaft**](subscriptionsforcomponent.md) des Abonnements an. Abonnentenobjekte, die von einem persistenten Abonnement erstellt werden, werden immer nach jedem Ereignisaufruf freigegeben.

</dd> <dt>

<span id="Transient"></span><span id="transient"></span><span id="TRANSIENT"></span>Vorübergehende
</dt> <dd>

Für vorübergehende Abonnements können Sie die [**TransientSubscriptions-Auflistung**](transientsubscriptions.md) verwenden, deren übergeordnetes Objekt das Stammkatalogobjekt ist. Vorübergehende Abonnements fordern ein Ereignis für ein bestimmtes Abonnentenobjekt an, das bereits vorhanden ist. Vorübergehende Abonnements werden im COM+-Katalog gespeichert, aber das Abonnement wird gelöscht, wenn das Ereignissystem oder Betriebssystem beendet wird. Im Gegensatz zu persistenten Abonnements sind vorübergehende Abonnements an ein bestimmtes Objekt gebunden und werden nur im Ereignissystem gespeichert. Vorübergehende Abonnements können effizienter sein als persistente Abonnements, aber Sie müssen deren Objektlebenszyklen verwalten. Informationen zum Registrieren eines vorübergehenden Abonnements finden Sie unter [Registrieren eines vorübergehenden Abonnements.](registering-a-transient-subscription.md)

</dd> <dt>

<span id="Per_user"></span><span id="per_user"></span><span id="PER_USER"></span>Pro Benutzer
</dt> <dd>

Abonnements pro Benutzer können Ereignisse nur übermitteln, wenn der Abonnent beim Computer des Ereignissystems angemeldet ist. Wenn sich der Abonnent anmeldet, aktiviert das Ereignissystem alle Abonnements, für die das *PerUser-Flag* auf **TRUE** und *UserName* auf den Namen des angemeldeten Benutzers festgelegt ist. Wenn sich der Abonnent abmeldet, sind die Abonnements deaktiviert.

Abonnements pro Benutzer sind nur gültig, wenn sich Herausgeber und Abonnent auf demselben Computer befinden. Anmeldung und Abmeldung werden nur auf dem Computer des Herausgebers erkannt– nicht auf dem Computer, auf dem sich das Abonnentenobjekt befindet.

</dd> </dl>

Das Ereignissystem verwendet Metaereignisse, um interessierten Abonnenten zu benachrichtigen, wenn Ereignisklassenobjekte oder -abonnements erstellt, geändert oder entfernt werden. Um Metaereignisse vom Ereignissystem zu empfangen, müssen Anwendungen ein Abonnement erstellen, das sich auf dem Computer des Ereignissystems befindet und die id der auslösenden Schnittstelle (IID \_ IEventObjectChange) angibt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Filtern von Ereignissen in COM+](filtering-events-in-com-.md)
</dt> <dt>

[Veröffentlichen und Übermitteln von Ereignissen in COM+](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[Das COM+-Ereignisklassenobjekt](the-com--event-class-object.md)
</dt> <dt>

[Verwenden von COM+-Ereignissen mit COM+-Komponenten in der Warteschlange](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 



