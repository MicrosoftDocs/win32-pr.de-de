---
title: Verwaltung von Benachrichtigungs Handlern
description: Das MMC-Snap-in "Microsoft Active Directory-Benutzer und-Computer" bietet einen Mechanismus, mit dem Komponenten Benachrichtigungen empfangen können, wenn der Benutzer die Eigenschaften eines Objekts mithilfe des-Snap-Ins löscht, umbenannt, verschiebt oder ändert.
ms.assetid: 49dbb995-c760-4fac-a72f-d5d94afb63c7
ms.tgt_platform: multiple
keywords:
- Verwaltungs Benachrichtigungs Handler AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baa6f48f8b56ab8e4a1d64d0fe15543bfee6c09e
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103858159"
---
# <a name="administrative-notification-handlers"></a>Verwaltung von Benachrichtigungs Handlern

Das MMC-Snap-in "Microsoft Active Directory-Benutzer und-Computer" bietet einen Mechanismus, mit dem Komponenten Benachrichtigungen empfangen können, wenn der Benutzer die Eigenschaften eines Objekts mithilfe des-Snap-Ins löscht, umbenannt, verschiebt oder ändert. Die Komponente, die Benachrichtigungen empfängt, wird als "Benachrichtigungs Handler" bezeichnet.

Dies ist nützlich, wenn mehrere Objekte miteinander verknüpft sind und innerhalb desselben Containers vorhanden sein müssen. Wenn eines der verknüpften Objekte verschoben wird, wird eine Benachrichtigung an den Benachrichtigungs Handler übermittelt, und der Benachrichtigungs Handler kann die anderen verknüpften Objekte in denselben Ordner verschieben.

Wenn einer der Vorgänge ausgeführt wird und mindestens ein Benachrichtigungs Handler installiert ist, zeigt das Snap-in "Benutzer und Computer" ein Bestätigungs Dialogfeld an, in dem die Benachrichtigungs Handler und ein Kontrollkästchen für jeden Handler aufgeführt werden. Wenn das Kontrollkästchen für einen Handler aktiviert ist, wird der Handler benachrichtigt. Wenn das Kontrollkästchen nicht aktiviert ist, wird der Handler nicht benachrichtigt.

## <a name="implementing-a-notification-handler"></a>Implementieren eines Benachrichtigungs Handlers

Ein Benachrichtigungs Handler ist ein COM-Objekt, das als in-proc-Server implementiert wird. Der Benachrichtigungs Handler muss die [**idsadminnotifyhandler**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadminnotifyhandler) -Schnittstelle implementieren.

Wenn ein Ereignis auftritt, das eine Benachrichtigung auslöst, listet das Snap-in "Benutzer und Computer" die registrierten Benachrichtigungs Handler auf und erstellt jeden mithilfe der CLSID für den Handler. Nachdem der Handler erstellt wurde, ruft das Snap-in die [**idsadminnotifyhandler:: Initialize**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-initialize) -Methode auf. Die **Initialize** -Methode liefert das-Snap-in mit den Ereignissen, die der Handler empfangen soll.

Wenn das Ereignis ein Ereignis ist, das an den Benachrichtigungs Handler gesendet werden soll, ruft das Snap-in die [**idsadminnotifyhandler:: begin**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-begin) -Methode auf. Die **Begin** -Methode stellt dem-Handler das-Ereignis, die Daten über das Objekt, in dem das Ereignis auftritt, und abhängig vom Ereignis die Daten über das Objekt bereit. Die **Begin** -Methode stellt außerdem das-Snap-in mit dem Text bereit, der für den Handler im Bestätigungs Dialogfeld angezeigt werden soll.

Wenn die [**Begin**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-begin) -Methode für jeden Handler aufgerufen wurde, zeigt das Snap-in das Bestätigungs Dialogfeld an. Das Bestätigungs Dialogfeld fordert den Benutzer auf, auszuwählen, welche Handler die Benachrichtigung erhalten sollen. Wenn der Benutzer im Bestätigungs Dialogfeld die Schaltfläche **kein** Push drückt, wird keiner der Handler benachrichtigt. Wenn der Benutzer die Schaltfläche " **Ja** " drückt, erhält jeder der im Bestätigungs Dialogfeld ausgewählten Handler die Benachrichtigung. Das Snap-in sendet die Benachrichtigung an den Handler, indem die [**idsadminnotifyhandler:: notify**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-notify) -Methode aufgerufen wird.

Nachdem alle Handler benachrichtigt wurden, ruft das Snap-in die [**idsadminnotifyhandler:: End**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-end) -Methode auf. Die **End** -Methode wird immer aufgerufen, auch wenn die [**Benachrichtigungs**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-notify) Methode nicht aufgerufen wird.

## <a name="registering-a-notification-handler-in-the-windows-registry"></a>Registrieren eines Benachrichtigungs Handlers in der Windows-Registrierung

Wie bei allen com-Servern muss ein Benachrichtigungs Handler in der Windows-Registrierung registriert werden. Der Handler ist unter folgendem Schlüssel registriert:


```C++
HKEY_CLASSES_ROOT - CLSID - <CLSID>
```



**<CLSID>** die Zeichen folgen Darstellung der CLSID, die von der [**stringfromclsid**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) -Funktion erstellt wird. Unter dem **<CLSID>** Schlüssel gibt es einen **InProcServer32** -Schlüssel, der das-Objekt als 32-Bit-in-proc-Server identifiziert. Unter der **InProcServer32** -Taste wird der Speicherort der dll im Standardwert angegeben, und das Threading Modell wird im **ThreadingModel** -Wert angegeben. Alle Benachrichtigungs Handler müssen das **Apartment** Thread Modell verwenden.

## <a name="registering-a-notification-handler-with-an-active-directory-server"></a>Registrieren eines Benachrichtigungs Handlers bei einem Active Directory Server

Innerhalb Active Directory Domain Services ist die Benachrichtigung des Benachrichtigungs Handlers für ein einzelnes Gebiets Schema spezifisch. Wenn der Benachrichtigungs Handler auf alle Gebiets Schemas angewendet wird, muss er im **displaySpecifier** -Objekt in allen Gebiets Schema-subcontainern im Display Specifiers-Container registriert werden. Wenn der Benachrichtigungs Handler für ein bestimmtes Gebiets Schema lokalisiert ist, wird er im **displaySpecifier** -Objekt im unter Container dieses Gebiets Schemas registriert. Weitere Informationen über den displayspecifieres-Container und die Gebiets Schemas finden Sie unter [anzeigen](display-specifiers.md) von Bezeichner und [displaySpecifier-Containern](displayspecifiers-container.md).

Benachrichtigungs Handler werden unter dem **dsuiadminnotification** -Attribut im Container " **DS-UI-Default-Settings** " registriert. Dies ist ein mehr wertiger Unicode-Zeichen folgen Wert, bei dem jeder Wert das folgende Format erfordert:


```C++
<order number>,<CLSID>
```



" &lt; Order Number &gt; " ist eine nicht signierte Zahl, die die Position des Handlers im Bestätigungs Dialogfeld darstellt. Wenn das Bestätigungs Dialogfeld angezeigt wird, werden die Werte mithilfe eines Vergleichs der "Order Number"-Werte der einzelnen Werte sortiert &lt; &gt; . Wenn mehr als ein Wert dieselbe " &lt; Bestellnummer" aufweist &gt; , werden diese Handler in der Reihenfolge angezeigt, in der Sie vom Active Directory Server gelesen werden. Eine nicht vorhandene, d. h. eine, die nicht von anderen Werten in der-Eigenschaft verwendet wird, &lt; &gt; sollte nach Möglichkeit verwendet werden. Es gibt keine vorgeschriebene Anfangsposition, und es können Lücken in der &lt; Sequenz "Order Number" angezeigt werden &gt; .

Die " &lt; CLSID &gt; " ist die Zeichen folgen Darstellung der CLSID, die von der [**stringfromclsid**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) -Funktion erstellt wird.

 

 