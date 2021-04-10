---
description: 'Abonnement Daten befinden sich im Abonnement-com+-Katalog. Ein Abonnement kann entweder mithilfe des Verwaltungs Tools Komponenten Dienste oder Programm gesteuert über die icomadmincatalog:: installcomponent-Schnittstelle erstellt werden.'
ms.assetid: 190e88f3-1d87-4c27-9451-0a633cbae829
title: Abonnements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9973eb76fc22354f1a2fc8e381c90cf5be1efee3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214138"
---
# <a name="subscriptions"></a>Abonnements

Abonnement Daten befinden sich im Abonnement-com+-Katalog. Ein Abonnement kann entweder mithilfe des Verwaltungs Tools Komponenten Dienste oder Programm gesteuert über die [**icomadmincatalog:: installcomponent**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installcomponent) -Schnittstelle erstellt werden.

Die [**Abonnement**](subscriptionsforcomponent.md) -Auflistung wird verwendet, um Informationen zu Abonnements hinzuzufügen, zu löschen oder zu ändern. Die " **abonneptionsforcomponent** "-Auflistung ist eine untergeordnete Sammlung einer Komponente. Wenn Sie ein Abonnement hinzufügen möchten, müssen Sie die **Abonnement** -Auflistung der Komponente und die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -Methode verwenden, um der Auflistung einen Eintrag hinzuzufügen. Zum Einrichten der verschiedenen Eigenschaften des Abonnement Objekts verwenden Sie die [**value**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_value) -Eigenschaft. Um die Änderungen zu speichern, verwenden Sie " [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) " für das Objekt " **subscribe ptionsforcomponent** Collection".

Sie können auch das Verwaltungs Tool Komponenten Dienste verwenden, um einige, aber nicht alle der Abonnement Eigenschaften zu ändern. Abonnements geben die folgenden Informationen an:

-   Identität und Speicherort des Abonnenten
-   Bereitstellungsmethode
-   Zu über liegende Ereignis Methoden
-   Ereignis Klassenobjekt und PublisherID-Eigenschaft einer Ereignis Klassen Komponente, von der der Abonnent Ereignisse empfangen möchte

Abonnements sind unabhängig von Ereignis Klassen Objekten vorhanden. Sie können ein Abonnement deaktivieren, indem Sie die Eigenschaft aktiviert auf false festlegen. Ein deaktiviertes Abonnement wird nicht durch COM+-Ereignisse aufgerufen.

Die drei Arten von Abonnements lauten wie folgt:

<dl> <dt>

<span id="Persistent"></span><span id="persistent"></span><span id="PERSISTENT"></span>Hartnäck
</dt> <dd>

Persistente Abonnements befinden sich im com+-Katalog und sind unabhängig von der Lebensdauer des Abonnenten. Persistente Abonnements überstehen einen Systemneustart. Im Allgemeinen wird ein dauerhaftes Abonnement erstellt, wenn eine Anwendung auf dem Computer eines Abonnenten installiert und entfernt wird, wenn die Anwendung entfernt wird. Nachdem ein dauerhaftes Abonnement erstellt wurde, aktiviert com+-Ereignisse den Abonnenten jedes Mal, wenn ein Ereignis an ihn übermittelt werden soll.

Wenn ein Verleger instanziiert und einen- [Ereignis Klassen](the-com--event-class-object.md) Objekt aufruft, sucht das-Objekt im com+-Katalog nach allen permanenten Abonnements und erstellt eine neue Instanz der einzelnen-Objekte. Der Erstellungs Prozess kann entweder direkt oder über einen Moniker für in der Warteschlange befindliche Komponenten erfolgen. Geben Sie das Abonnenten Objekt von der Eigenschaft "Abonnement [**Name**](subscriptionsforcomponent.md) " des Abonnements an. Abonnenten Objekte, die von einem permanenten Abonnement erstellt werden, werden immer nach jedem Ereignis aufrufter freigegeben.

</dd> <dt>

<span id="Transient"></span><span id="transient"></span><span id="TRANSIENT"></span>Gliches
</dt> <dd>

Bei vorübergehenden Abonnements können Sie die [**transientabonnements**](transientsubscriptions.md) -Auflistung verwenden, deren übergeordnetes Objekt das Stamm Katalog Objekt ist. Vorübergehende Abonnements fordern ein Ereignis für ein bestimmtes Abonnenten Objekt an, das bereits vorhanden ist. Vorübergehende Abonnements werden im com+-Katalog gespeichert, aber das Abonnement wird gelöscht, wenn das Ereignis System oder das Betriebssystem beendet wird. Im Gegensatz zu permanenten Abonnements sind vorübergehende Abonnements an ein bestimmtes Objekt gebunden und nur im-Ereignis System gespeichert. Vorübergehende Abonnements können effizienter als persistente Abonnements sein, aber Sie müssen deren Objekt Lebenszyklen verwalten. Informationen zum Registrieren eines vorübergehenden Abonnements finden Sie unter [Registrieren eines vorübergehenden](registering-a-transient-subscription.md)Abonnements.

</dd> <dt>

<span id="Per_user"></span><span id="per_user"></span><span id="PER_USER"></span>Pro Benutzer
</dt> <dd>

Pro-Benutzer-Abonnements können Ereignisse nur dann übermitteln, wenn der Abonnent am Computer des Ereignis Systems angemeldet ist. Wenn sich der Abonnent anmeldet, aktiviert das Ereignis System alle Abonnements, für die das *peruser* -Flag auf **true** festgelegt ist, und *username* wird auf den Namen des angemeldeten Benutzers festgelegt. Wenn der Abonnent sich abmeldet, werden die Abonnements deaktiviert.

Pro-Benutzer-Abonnements sind nur wirksam, wenn sich der Verleger und der Abonnent auf demselben Computer befinden. Das anmelden und Abmelden wird nur auf dem Computer des Verlegers erkannt – nicht auf dem Computer, auf dem sich das Abonnenten Objekt befindet.

</dd> </dl>

Das Ereignis System verwendet Metadatenereignisse, um interessierte Abonnenten zu benachrichtigen, wenn Ereignis Klassen Objekte oder-Abonnements erstellt, geändert oder entfernt werden. Um Meta-Ereignisse aus dem Ereignis System zu empfangen, müssen Anwendungen ein Abonnement erstellen, das sich auf dem Computer des Ereignis Systems befindet und die auslösenden Schnittstellen-ID (IID \_ ieventobjectchange) angibt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Filtern von Ereignissen in com+](filtering-events-in-com-.md)
</dt> <dt>

[Veröffentlichen und Bereitstellung von Ereignissen in com+](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[Das com+-Ereignis Klassenobjekt](the-com--event-class-object.md)
</dt> <dt>

[Verwenden von COM+-Ereignissen mit COM+-Komponenten in der Warteschlange](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 



