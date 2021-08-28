---
title: Administrative Benachrichtigungshandler
description: Das Microsoft Active Directory-Benutzer und -Computer MMC-Snap-In bietet einen Mechanismus, mit dem Komponenten Benachrichtigungen empfangen können, wenn der Benutzer die Eigenschaften eines Objekts mithilfe des Snap-Ins löscht, umbenennt, verschiebt oder ändert.
ms.assetid: 49dbb995-c760-4fac-a72f-d5d94afb63c7
ms.tgt_platform: multiple
keywords:
- Administrative Benachrichtigungshandler AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08d89627cdb15cc7ea15f4b56e3a6ec90eafbe6a
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122879891"
---
# <a name="administrative-notification-handlers"></a>Administrative Benachrichtigungshandler

Das Microsoft Active Directory-Benutzer und -Computer MMC-Snap-In bietet einen Mechanismus, mit dem Komponenten Benachrichtigungen empfangen können, wenn der Benutzer die Eigenschaften eines Objekts mithilfe des Snap-Ins löscht, umbenennt, verschiebt oder ändert. Die Komponente, die die Benachrichtigungen empfängt, wird als "Benachrichtigungshandler" bezeichnet.

Dies ist nützlich, wenn mehrere Objekte miteinander verknüpft sind und innerhalb desselben Containers vorhanden sein müssen. Wenn eines der verknüpften Objekte verschoben wird, wird dem Benachrichtigungshandler eine Benachrichtigung bereitgestellt, und der Benachrichtigungshandler kann die anderen verknüpften Objekte in denselben Ordner verschieben.

Wenn einer der Vorgänge ausgeführt wird und mindestens ein Benachrichtigungshandler installiert ist, zeigt das Snap-In Benutzer und Computer ein Bestätigungsdialogfeld an, in dem die Benachrichtigungshandler und ein Kontrollkästchen für jeden Handler aufgeführt sind. Wenn das Kontrollkästchen für einen Handler aktiviert ist, wird der Handler benachrichtigt. Wenn das Kontrollkästchen nicht aktiviert ist, wird der Handler nicht benachrichtigt.

## <a name="implementing-a-notification-handler"></a>Implementieren eines Benachrichtigungshandlers

Ein Benachrichtigungshandler ist ein COM-Objekt, das als In-Proc-Server implementiert wird. Der Benachrichtigungshandler muss die [**IDsAdminNotifyHandler-Schnittstelle**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadminnotifyhandler) implementieren.

Wenn ein Ereignis auftritt, das eine Benachrichtigung verursacht, listet das Snap-In Benutzer und Computer die registrierten Benachrichtigungshandler auf und erstellt jeden mithilfe der CLSID für den Handler. Nachdem der Handler erstellt wurde, ruft das Snap-In die [**IDsAdminNotifyHandler::Initialize-Methode**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-initialize) auf. Die **Initialize-Methode** stellt das Snap-In mit den Ereignissen zur Verfügung, die der Handler empfangen soll.

Wenn das Ereignis an den Benachrichtigungshandler gesendet werden soll, ruft das Snap-In die [**IDsAdminNotifyHandler::Begin-Methode**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-begin) auf. Die **Begin-Methode** stellt dem Handler das auftretende Ereignis, Daten über das Objekt, auf dem das Ereignis auftritt, und, je nach Ereignis, Daten darüber, was das Objekt wird, zur Seite. Die **Begin-Methode** stellt auch das Snap-In mit dem Text zur Seite, der für den Handler im Bestätigungsdialogfeld angezeigt werden soll.

Wenn die [**Begin-Methode**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-begin) für jeden Handler aufgerufen wurde, zeigt das Snap-In das Bestätigungsdialogfeld an. Im Bestätigungsdialogfeld wird der Benutzer aufgefordert, auszuwählen, welche Handler die Benachrichtigung erhalten. Wenn der Benutzer  im Bestätigungsdialogfeld die Schaltfläche Nein drückt, wird keiner der Handler benachrichtigt. Wenn der Benutzer die Schaltfläche **Ja** drückt, erhält jeder der im Bestätigungsdialogfeld ausgewählten Handler die Benachrichtigung. Das Snap-In sendet die Benachrichtigung durch Aufrufen der [**IDsAdminNotifyHandler::Notify-Methode an den Handler.**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-notify)

Nachdem alle Handler benachrichtigt wurden, ruft das Snap-In die [**IDsAdminNotifyHandler::End-Methode**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-end) auf. Die **End-Methode** wird immer aufgerufen, auch wenn die [**Notify-Methode**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-notify) nicht aufgerufen wird.

## <a name="registering-a-notification-handler-in-the-windows-registry"></a>Registrieren eines Benachrichtigungshandlers in der Windows Registrierung

Wie alle COM-Server muss auch ein Benachrichtigungshandler in der Windows werden. Der Handler wird unter dem folgenden Schlüssel registriert:


```C++
HKEY_CLASSES_ROOT - CLSID - <CLSID>
```



**&lt; CLSID &gt; ist** die Zeichenfolgendarstellung der CLSID, die von der [**StringFromCLSID-Funktion erzeugt**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) wird. Unter dem **&lt; &gt; CLSID-Schlüssel** befindet sich ein **InProcServer32-Schlüssel,** der das Objekt als 32-Bit-In-Proc-Server identifiziert. Unter dem **InProcServer32-Schlüssel** wird der Speicherort der DLL im Standardwert und das Threadingmodell im **ThreadingModel-Wert** angegeben. Alle Benachrichtigungshandler müssen das **Apartmentthreadingmodell** verwenden.

## <a name="registering-a-notification-handler-with-an-active-directory-server"></a>Registrieren eines Benachrichtigungshandlers bei einem Active Directory-Server

Innerhalb Active Directory Domain Services ist die Registrierung des Benachrichtigungshandlers für ein einzelnes Locale spezifisch. Wenn der Benachrichtigungshandler für alle Locales gilt, muss er im **displaySpecifier-Objekt** in allen Untercontainern des Locale-Objekts im DisplaySpecifiers-Container registriert werden. Wenn der Benachrichtigungshandler für ein bestimmtes Locale lokalisiert wird, wird er im **displaySpecifier-Objekt** im Untercontainer dieses Locales registriert. Weitere Informationen zum DisplaySpecifiers-Container und den -Locales finden Sie unter [Display Specifiers](display-specifiers.md) and DisplaySpecifiers Container ( Anzeigespezifizierer und [DisplaySpecifiers-Container).](displayspecifiers-container.md)

Benachrichtigungshandler werden unter dem **dsUIAdminNotification-Attribut** im **Container DS-UI-Default-Einstellungen** registriert. Dies ist ein mehrwertigen Unicode-Zeichenfolgenwert, bei dem jeder Wert das folgende Format erfordert:


```C++
<order number>,<CLSID>
```



Die &lt; "Bestellnummer" ist eine Zahl ohne Vorzeichen, die die Position des Handlers &gt; im Bestätigungsdialogfeld darstellt. Wenn das Bestätigungsdialogfeld angezeigt wird, werden die Werte anhand eines Vergleichs der Bestellnummer jedes &lt; Werts &gt; sortiert. Wenn mehr als ein Wert über die gleiche "Bestellnummer" verfügt, werden diese Handler in der Reihenfolge angezeigt, in der sie vom &lt; &gt; Active Directory-Server gelesen werden. Wenn möglich, sollte ein nicht vorhandener ,, der nicht von anderen Werten in der -Eigenschaft verwendet wird, " &lt; Bestellnummer &gt; " verwendet werden. Es gibt keine vorgeschriebene Anfangsposition, und Lücken können in der Sequenz " &lt; Bestellnummer &gt; " auftreten.

&lt;"CLSID" &gt; ist die Zeichenfolgendarstellung der CLSID, die von der [**StringFromCLSID-Funktion erzeugt**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) wird.

 

 
