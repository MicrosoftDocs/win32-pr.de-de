---
title: Ändern von Benachrichtigungen in Active Directory Domain Services
description: Active Directory Domain Services einen Mechanismus bereitstellen, mit dem eine Client Anwendung bei einem Domänen Controller registriert werden soll, um Änderungs Benachrichtigungen zu empfangen.
ms.assetid: 27f6c7c1-b32e-457a-9be5-47836d097ab1
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee564727cfbcb2bfdb367f822fdc137bca7c4e37
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038800"
---
# <a name="change-notifications-in-active-directory-domain-services"></a>Ändern von Benachrichtigungen in Active Directory Domain Services

Active Directory Domain Services einen Mechanismus bereitstellen, mit dem eine Client Anwendung bei einem Domänen Controller registriert werden soll, um Änderungs Benachrichtigungen zu empfangen. Zu diesem Zweck gibt der Client das LDAP-Änderungs Benachrichtigungs Steuerelement in einem asynchronen LDAP-Suchvorgang an. Der Client gibt auch die folgenden Suchparameter an.



| Parameter             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `Scope`<br/>      | Geben Sie entweder die **LDAP- \_ Bereichs \_ Basis** an, um nur das Objekt zu überwachen, oder **LDAP \_ Scope \_ onelevel** , um die unmittelbar untergeordneten Elemente des Objekts zu überwachen, ohne das Objekt selbst einzuschließen Geben Sie keine **LDAP- \_ Bereichs \_ Teilstruktur** an. Obwohl der Teilstruktur Bereich unterstützt wird, wenn das Basisobjekt der Stamm eines Namens Kontexts ist, kann sich seine Verwendung stark auf die Serverleistung auswirken, da er jedes Mal eine LDAP-Suchergebnis Meldung generiert, wenn ein Objekt im namens Kontext geändert wird. Sie können keine **LDAP- \_ Bereichs \_ Teilstruktur** für eine beliebige Unterstruktur angeben.<br/> |
| Filter<br/>     | Geben Sie einen Suchfilter für "(objectClass = \* )" an. Dies bedeutet, dass Sie Benachrichtigungen für Änderungen an einem beliebigen Objekt im angegebenen Bereich erhalten.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                |
| Attribute<br/> | Gibt eine Liste der Attribute an, die zurückgegeben werden sollen, wenn eine Änderung auftritt. Beachten Sie, dass Sie Benachrichtigungen erhalten, wenn ein beliebiges Attribut geändert wird, nicht nur die angegebenen Attribute.<br/>                                                                                                                                                                                                                                                                                                                                                                               |



 

Sie können bis zu fünf Benachrichtigungs Anforderungen bei einer einzelnen LDAP-Verbindung registrieren. Sie müssen über einen dedizierten Thread verfügen, der auf die Benachrichtigungen wartet und Sie schnell verarbeitet. Wenn Sie die LDAP- \_ Such \_ Funktion "ext" zum Registrieren einer Benachrichtigungs Anforderung aufruft, gibt die Funktion eine Nachrichten-ID zurück, die diese Anforderung identifiziert. Anschließend verwenden Sie die [**LDAP- \_ Ergebnis**](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result) Funktion, um auf Änderungs Benachrichtigungen zu warten. Wenn eine Änderung auftritt, sendet der Server Ihnen eine LDAP-Nachricht, die die Nachrichten-ID für die Benachrichtigungs Anforderung enthält, die die Benachrichtigung generiert hat. Dies bewirkt, dass die **LDAP- \_ Ergebnis** Funktion mit Suchergebnissen zurückgibt, durch die das geänderte Objekt identifiziert wird.

Die Client Anwendung muss den ursprünglichen Status des überwachten Objekts bestimmen. Zu diesem Zweck müssen Sie zuerst die Benachrichtigungs Anforderung registrieren und dann den aktuellen Status lesen.

Die Client Anwendung muss außerdem die Ursache der Änderung ermitteln. Bei einer Basisebene-Suche tritt eine Benachrichtigung auf, wenn sich ein beliebiges Attribut ändert oder wenn das Objekt gelöscht oder verschoben wird. Bei einer einstufigen Suche tritt eine Benachrichtigung auf, wenn ein untergeordnetes Objekt erstellt, gelöscht, verschoben oder geändert wird. Beachten Sie, dass durch das Verschieben oder Umbenennen eines Objekts in der Hierarchie oberhalb eines Zielobjekts keine Benachrichtigung generiert wird, obwohl sich der Distinguished Name des Ziels als Ergebnis geändert hat. Wenn Sie z. b. Änderungen an den untergeordneten Objekten in einem Container überwachen, erhalten Sie keine Benachrichtigungen, wenn der Container selbst verschoben oder umbenannt wird.

Wenn der Client die Suchergebnisse verarbeitet, kann er die LDAP \_ Get DN-Funktion verwenden, \_ um den Distinguished Name des geänderten Objekts zu erhalten. Verlassen Sie sich nicht auf gekennzeichnete Namen, um die nach verfolgten Objekte zu identifizieren, da sich Distinguished Names ändern können. Fügen Sie stattdessen das **objectGUID** -Attribut in die Liste der abzurufenden Attribute ein. Die **objectGUID** jedes Objekts bleibt unverändert, unabhängig davon, wo das Objekt innerhalb der Gesamtstruktur des Unternehmens verschoben wird.

Wenn ein Objekt innerhalb des Suchbereichs gelöscht wird, empfängt der Client eine Änderungs Benachrichtigung, und das **isDeleted** -Attribut des Objekts ist auf **true** festgelegt. In diesem Fall melden die Suchergebnisse den neuen Distinguished Name des Objekts im Container "Gelöschte Objekte" der Partition. Es ist nicht erforderlich, das Tombstone-Steuerelement ([LDAP- \_ Server \_ Show \_ deleted \_ OID](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid)) anzugeben, um Benachrichtigungen zu Objekt Löschungen zu erhalten. Weitere Informationen finden Sie unter [Abrufen von gelöschten Objekten](retrieving-deleted-objects.md).

Wenn ein Client eine Benachrichtigungs Anforderung registriert hat, empfängt der Client weiterhin Benachrichtigungen, bis die Verbindung getrennt wird oder der Client die Suche durch Aufrufen der LDAP-Abbruch \_ Funktion verlässt. Wenn der Client oder der Server die Verbindung trennt, z. b. wenn der Server ausfällt, wird die Benachrichtigungs Anforderung beendet. Wenn der Client die Verbindung wiederherstellt, muss er sich erneut für Benachrichtigungen registrieren und dann den aktuellen Zustand der relevanten Objekte lesen, falls Änderungen aufgetreten sind, während der Client getrennt wurde.

Der Client kann den Wert des **uSNChanged** -Attributs eines Objekts verwenden, um zu bestimmen, ob der aktuelle Zustand des Objekts auf dem Server die neuesten Änderungen widerspiegelt, die der Client empfangen hat. Das System erhöht das Attribut "-Attribut" für ein Objekt, wenn das Objekt verschoben **oder geändert wird** . Wenn z. b. der Server ausfällt und die Verzeichnis Partition aus einer Sicherung wieder hergestellt wird, spiegelt das Replikat des Servers eines Objekts möglicherweise keine Änderungen wider, die zuvor an den Client gemeldet wurden. in diesem Fall ist der Wert von "" auf dem Server niedriger als der Wert **, der vom** Client gespeichert wird.

Weitere Informationen und ein Codebeispiel, in dem das LDAP-Änderungs Benachrichtigungs Steuerelement in einem asynchronen LDAP-Suchvorgang verwendet wird, finden Sie unter [Beispielcode für den Empfang von Änderungs Benachrichtigungen](example-code-for-receiving-change-notifications.md).

Weitere Informationen zur Verwendung der LDAP-Änderungs Benachrichtigungs Steuerung finden Sie unter [Übersicht über Änderungsnachverfolgung Techniken](overview-of-change-tracking-techniques.md).

 

