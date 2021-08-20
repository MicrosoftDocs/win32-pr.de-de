---
title: Administrative Benachrichtigungshandler
description: Das Microsoft Active Directory-Benutzer und -Computer MMC-Snap-In bietet einen Mechanismus, mit dem Komponenten Benachrichtigungen empfangen können, wenn der Benutzer die Eigenschaften eines Objekts mithilfe des Snap-Ins löscht, umbenennt, verschiebt oder ändert.
ms.assetid: 49dbb995-c760-4fac-a72f-d5d94afb63c7
ms.tgt_platform: multiple
keywords:
- Ad administrative Benachrichtigungshandler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ebe2e92edd9a2630963d7dda6d84e6c323743ef5d37687927502c62b32ec592
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118024660"
---
# <a name="administrative-notification-handlers"></a>Administrative Benachrichtigungshandler

Das Microsoft Active Directory-Benutzer und -Computer MMC-Snap-In bietet einen Mechanismus, mit dem Komponenten Benachrichtigungen empfangen können, wenn der Benutzer die Eigenschaften eines Objekts mithilfe des Snap-Ins löscht, umbenennt, verschiebt oder ändert. Die Komponente, die die Benachrichtigungen empfängt, wird als "Benachrichtigungshandler" bezeichnet.

Dies ist nützlich, wenn mehrere Objekte miteinander verknüpft sind und innerhalb desselben Containers vorhanden sein müssen. Wenn eines der verknüpften Objekte verschoben wird, wird dem Benachrichtigungshandler eine Benachrichtigung bereitgestellt, und der Benachrichtigungshandler kann die anderen verknüpften Objekte in denselben Ordner verschieben.

Wenn einer der Vorgänge ausgeführt wird und mindestens ein Benachrichtigungshandler installiert ist, zeigt das Snap-In Benutzer und Computer ein Bestätigungsdialogfeld an, in dem die Benachrichtigungshandler und ein Kontrollkästchen für jeden Handler aufgeführt sind. Wenn das Kontrollkästchen für einen Handler aktiviert ist, wird der Handler benachrichtigt. Wenn das Kontrollkästchen nicht aktiviert ist, wird der Handler nicht benachrichtigt.

## <a name="implementing-a-notification-handler"></a>Implementieren eines Benachrichtigungshandlers

Ein Benachrichtigungshandler ist ein COM-Objekt, das als Prozessserver implementiert wird. Der Benachrichtigungshandler muss die [**IDsAdminNotifyHandler-Schnittstelle**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadminnotifyhandler) implementieren.

Wenn ein Ereignis auftritt, das eine Benachrichtigung verursacht, listet das Snap-In Benutzer und Computer die registrierten Benachrichtigungshandler auf und erstellt jeden mithilfe der CLSID für den Handler. Nachdem der Handler erstellt wurde, ruft das Snap-In die [**IDsAdminNotifyHandler::Initialize-Methode**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-initialize) auf. Die **Initialize-Methode** stellt das Snap-In mit den Ereignissen zur Verfügung, die der Handler empfangen soll.

Wenn das Ereignis an den Benachrichtigungshandler gesendet werden soll, ruft das Snap-In die [**IDsAdminNotifyHandler::Begin-Methode**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-begin) auf. Die **Begin-Methode** stellt dem Handler das ereignisaufgehende Ereignis, Daten zum Objekt, auf dem das Ereignis auftritt, und abhängig vom Ereignis Daten dazu bereit, was das Objekt werden soll. Die **Begin-Methode** stellt auch das Snap-In mit dem Text bereit, der für den Handler im Bestätigungsdialogfeld angezeigt werden soll.

Wenn die [**Begin-Methode**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-begin) für jeden Handler aufgerufen wurde, zeigt das Snap-In das Bestätigungsdialogfeld an. Im Bestätigungsdialogfeld wird der Benutzer aufgefordert, auszuwählen, welche Handler die Benachrichtigung erhalten. Wenn der Benutzer im Bestätigungsdialogfeld die Schaltfläche No push **(Kein** Push) drückt, wird keiner der Handler benachrichtigt. Wenn der Benutzer die Schaltfläche **Ja** drückt, erhält jeder der im Bestätigungsdialogfeld ausgewählten Handler die Benachrichtigung. Das Snap-In sendet die Benachrichtigung an den Handler, indem die [**IDsAdminNotifyHandler::Notify-Methode**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-notify) aufgerufen wird.

Nachdem alle Handler benachrichtigt wurden, ruft das Snap-In die [**IDsAdminNotifyHandler::End-Methode**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-end) auf. Die **End-Methode** wird immer aufgerufen, auch wenn die [**Notify-Methode**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-notify) nicht aufgerufen wird.

## <a name="registering-a-notification-handler-in-the-windows-registry"></a>Registrieren eines Benachrichtigungshandlers in der Windows Registry

Wie alle COM-Server muss ein Benachrichtigungshandler in der Windows Registrierung registriert werden. Der Handler wird unter dem folgenden Schlüssel registriert:


```C++
HKEY_CLASSES_ROOT - CLSID - <CLSID>
```



**<CLSID>** ist die Zeichenfolgendarstellung der CLSID, die von der [**StringFromCLSID-Funktion**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) erzeugt wird. Unter dem **<CLSID>** Schlüssel befindet sich ein **InProcServer32-Schlüssel,** der das Objekt als 32-Bit-Prozessserver identifiziert. Unter dem **InProcServer32-Schlüssel** wird der Speicherort der DLL im Standardwert angegeben, und das Threadingmodell wird im **ThreadingModel-Wert** angegeben. Alle Benachrichtigungshandler  müssen das Apartment-Threadingmodell verwenden.

## <a name="registering-a-notification-handler-with-an-active-directory-server"></a>Registrieren eines Benachrichtigungshandlers bei einem Active Directory-Server

Innerhalb Active Directory Domain Services ist die Registrierung des Benachrichtigungshandlers spezifisch für ein Gebietsschema. Wenn der Benachrichtigungshandler für alle Gebietsschemas gilt, muss er im **displaySpecifier-Objekt** in allen Gebietsschemauntercontainern im Container DisplaySpecifiers registriert werden. Wenn der Benachrichtigungshandler für ein bestimmtes Gebietsschema lokalisiert ist, wird er im **displaySpecifier-Objekt** im Untercontainer dieses Gebietsschemas registriert. Weitere Informationen zum DisplaySpecifiers-Container und den Gebietsschemas finden Sie unter [Anzeigespezifizierer](display-specifiers.md) und [DisplaySpecifiers-Container.](displayspecifiers-container.md)

Benachrichtigungshandler werden unter dem **dsUIAdminNotification-Attribut** im **Container DS-UI-Default-Einstellungen** registriert. Dies ist ein mehrwertiger Unicode-Zeichenfolgenwert, bei dem jeder Wert das folgende Format erfordert:


```C++
<order number>,<CLSID>
```



Die &lt; Bestellnummer &gt; ist eine Zahl ohne Vorzeichen, die die Position des Handlers im Bestätigungsdialogfeld darstellt. Wenn das Bestätigungsdialogfeld angezeigt wird, werden die Werte mithilfe eines Vergleichs der "Bestellnummer" jedes Werts &lt; &gt; sortiert. Wenn mehr als ein Wert über die gleiche &lt; "Bestellnummer" &gt; verfügt, werden diese Handler in der Reihenfolge angezeigt, in der sie vom Active Directory-Server gelesen werden. Ein nicht vorhandener , d. h. einer, der nicht von anderen Werten in der -Eigenschaft verwendet &lt; wird, " Bestellnummer &gt; ", sollte nach Möglichkeit verwendet werden. Es gibt keine vorgeschriebene Anfangsposition, und Lücken können in der &lt; Sequenz "Bestellnummer" angezeigt &gt; werden.

&lt;"CLSID" &gt; ist die Zeichenfolgendarstellung der CLSID, die von der [**StringFromCLSID-Funktion**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) erzeugt wird.

 

 