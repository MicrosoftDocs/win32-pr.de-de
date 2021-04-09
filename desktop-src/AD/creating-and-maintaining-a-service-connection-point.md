---
title: Erstellen und Verwalten eines Dienst Verbindungs Punkts
description: Beachten Sie beim Veröffentlichen mit einem SCP, dass Sie aktuelle Daten über die Dienst Instanz enthalten muss.
ms.assetid: 2350cb65-3439-4a5f-adc5-b71476793247
ms.tgt_platform: multiple
keywords:
- Erstellen und Verwalten eines Dienst Verbindungspunkt-AD
- Dienst Verbindungspunkt AD, erstellen und verwalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6c4ad02b92fa6567fc3b709e45f2f64ce66318
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038779"
---
# <a name="creating-and-maintaining-a-service-connection-point"></a>Erstellen und Verwalten eines Dienst Verbindungs Punkts

Beachten Sie beim Veröffentlichen mit einem SCP, dass Sie aktuelle Daten über die Dienst Instanz enthalten muss. Andernfalls werden von Clients, die an den Dienst Verbindungs Dienst gebunden sind, veraltete Daten abgerufen. Das Dienst Installationsprogramm, das einen SCP erstellt, gibt die Anfangswerte für die SCPS-Attribute an. Wenn die Dienst Instanz dann gestartet wird, muss Sie den SCP suchen und die Attributwerte ggf. aktualisieren. Auf diese Weise werden Clients die aktuellsten Daten sichergestellt.

Nach dem Erstellen des Dienst Verbindungs dienstaners führt Ihr Dienst Installationsprogramm zwei zusätzliche Schritte aus, mit denen der Dienst den SCP aktualisieren kann:

-   Legen Sie ACEs in der Sicherheits Beschreibung des SCP-Objekts fest, damit der Dienst SCP-Attribute zur Laufzeit ändern kann. Weitere Informationen und ein Codebeispiel finden Sie unter [Aktivieren des Dienst Kontos für den Zugriff auf SCP-Eigenschaften](enabling-service-account-to-access-scp-properties.md).
-   Speichern Sie die **objectGUID** des Dienst Verbindungs Diensts in der Registrierung auf dem Dienst Host Computer. Der Dienst ruft die zwischengespeicherte GUID zum Binden an den Dienst Verbindungspunkt ab, um die zugehörigen Attribute zu überprüfen und zu aktualisieren.

Das Dienst Installationsprogramm speichert die **objectGUID** des SCP-dienstanders und nicht seinen DN. Die **objectGUID** ändert sich nie, unabhängig davon, ob der Dienst Verbindungspunkt verschoben oder umbenannt wurde. Der DN kann sich ändern, wenn ein Administrator den Dienst Verbindungspunkt verschiebt oder umbenennt. Wenn Sie z. b. einen SCP als untergeordnetes Element eines Computer Objekts erstellen, ändert sich der Distinguished Name des Dienst Verbindungs Punkts, wenn der Computer umbenannt oder in eine andere Domäne oder Organisationseinheit verschoben wird.

Wenn ein Dienst Installationsprogramm einen SCP erstellt, muss er die **objectGUID** des neu erstellten Objekts lesen und in der Registrierung des Dienst Host Computers Zwischenspeichern. Verwenden Sie die [**IADs:: get \_ GUID**](/windows/desktop/ADSI/iads-property-methods) -Methode, um den **objectGUID** -Wert im Zeichen folgen Format abzurufen, das für die Bindung geeignet ist. Speichern Sie die GUID-Zeichenfolge als Wert unter dem folgenden Registrierungsschlüssel.

```
HKEY_LOCAL_MACHINE
   vendor name
      product name
```

Dabei ermitteln "Herstellername" und "Produktname" den Hersteller und das Produkt.

Wenn der Dienst gestartet wird, ruft er die zwischengespeicherte GUID-Zeichenfolge aus der Registrierung ab und verwendet diese für die Bindung an den SCP. Der Dienst liest die wichtigen SCP-Attribute und vergleicht sie mit den aktuellen Werten. Wenn die SCP-Werte veraltet sind, aktualisiert der Dienst Sie. Zum Aktualisieren von include- **Schlüsselwörtern**, **serviceBindingInformation**, **servicednsname** und **serviceDNSNameType** sind Werte, die der Dienst möglicherweise benötigt.

## <a name="examples"></a>Beispiele

-   [Skript Beispiele](script-samples-for-managing-service-connection-points.md)
-   [Code Beispiele (C/C++)](code-samples-for-managing-service-connection-points.md)

 

 