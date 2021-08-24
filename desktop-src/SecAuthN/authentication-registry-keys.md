---
description: Wenn ein Netzwerkanbieter installiert wird, sollte Ihre Anwendung die registrierungsschlüssel und -werte erstellen, die in diesem Thema beschrieben werden.
ms.assetid: cc5a4a7b-02b5-4ecd-967c-de0656f00846
title: Authentifizierungsregistrierungsschlüssel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3c245cdb27a0d661e7e6df82ed0d1d0ed35a59ea05bf74bf98ebd39ba3dc791
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883680"
---
# <a name="authentication-registry-keys"></a>Authentifizierungsregistrierungsschlüssel

Wenn ein Netzwerkanbieter installiert wird, sollte Ihre Anwendung die registrierungsschlüssel und -werte erstellen, die in diesem Thema beschrieben werden. Diese Schlüssel und Werte stellen dem MPR Informationen zu den auf dem System installierten Netzwerkanbietern bereit. Die MPR überprüft diese Schlüssel beim Starten und lädt die gefundenen Netzwerkanbieter-DLLs.

Bevor Sie einen Satz von Schlüsseln zum Speichern von Informationen zu Ihrem Netzwerkanbieter erstellen, sollten Sie dem **Bestellschlüssel** den Namen Ihres Netzwerkanbieters hinzufügen. Dieser Schlüssel ist ein Unterschlüssel des folgenden Schlüssels:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Control
            NetworkProvider
```

Der **Bestellschlüssel** enthält einen einzelnen Wert, **ProviderOrder**, der die installierten Anbieter auflistet und die Reihenfolge angibt, in der sie bei Vorgängen versucht werden sollen, die Anbieter durchlaufen, bis ein akzeptierenden Anbieter gefunden wird.

Der **ProviderOrder-Wert** enthält eine durch Trennzeichen getrennte Liste von Schlüsselnamen. Jeder Schlüsselname in **ProviderOrder** identifiziert einen Netzwerkanbieter. Wenn MPR durch die Anbieter zyklen, werden sie in der Reihenfolge angezeigt, in der sie in dieser Liste angezeigt werden.

Der in **ProviderOrder** festgelegte Anbietername sollte auch als Name des Registrierungsschlüssels verwendet werden, der Informationen zu diesem Anbieter enthält. Die anbieterspezifischen Registrierungsschlüssel werden als Unterschlüssel des folgenden Schlüssels erstellt:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
```

Anders ausgedrückt: Die in **ProviderOrder** angegebenen Anbieternamen sind der Pfad zur Registrierung der netzwerkanbieterspezifischen Schlüssel relativ zum folgenden Pfad:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
```

Wenn der Netzwerkanbieterdienst installiert ist, sollte die Installationsanwendung einen Schlüssel wie folgt hinzufügen:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            ProviderName
```

Dabei ist *ProviderName* der Name des Netzwerkanbieters, wie im **ProviderOrder-Wert** des **Bestellschlüssels** angegeben. Der **Group-Wert** unter dem *ProviderName-Schlüssel* sollte auf "NetworkProvider" festgelegt werden. Dadurch wird der Dienst als in der Netzwerkanbietergruppe identifiziert.

Sie müssen auch einen Unterschlüssel von *ProviderName*, **networkprovider** erstellen. Dieser Schlüssel enthält die folgenden Werte, die den Netzwerkanbieter beschreiben.



| Wert                       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Name**<br/>         | Enthält den Namen des Anbieters. Dieser Name wird dem Benutzer als Name des Netzwerks in den Dialogfeldern zum Durchsuchen angezeigt und sollte mit dem **lpProvider-Feld** übereinstimmen, das in [**NETRESOURCE-Strukturen**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) zurückgegeben wird. Dieser Name sollte eine Variation des Produktnamens sein, vorzugsweise mit einem Hinweis auf das Unternehmen, damit er klar und eindeutig ist. "MS-LanMan" ist beispielsweise ein guter Name, während "The Net" eine schlechte Wahl wäre.<br/> |
| **ProviderPath**<br/> | Enthält den vollständigen Pfad der DLL, die den Netzwerkanbieter implementiert. MPR ruft [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) für diesen Pfad auf.<br/>                                                                                                                                                                                                                                                                                                                                |



 

Die folgenden Werte werden nur von Netzwerkanbietern verwendet, die die Anmeldeinformationsverwaltungsfunktionen [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) und [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify)unterstützen.



| Wert                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Klasse**<br/>               | Ein **DWORD,** das die Klasse oder den Typ der Anbieterfunktionalität identifiziert, die dieser Anbieter unterstützt. Werte können ggf. vom **OR-Operator** verknüpft werden. Gültige Werte hierfür sind WN \_ NETWORK \_ CLASS, WN \_ CREDENTIAL \_ CLASS, WN \_ PRIMARY \_ AUTHENT \_ CLASS und WN SERVICE \_ \_ CLASS.<br/> Obwohl ein Anbieter primäre Authentifikatorfunktionen unterstützen kann, wird eine andere Möglichkeit verwendet, um zu bestimmen, welcher Authentifikator primär ist.<br/> **Windows XP/2000:** Das Wechseln primärer Authentifikatoren wird nicht unterstützt, sodass dieser Wert ignoriert wird. <br/> |
| **AuthentProviderPath**<br/> | Dies ist der vollqualifizierte Dateiname für die DLL, die die Anmeldeinformationsverwaltungsfunktionen exportiert. Dieser Wert ist nur nützlich (aber nicht erforderlich), wenn der Anbieter als CREDENTIAL \_ CLASS- oder PRIMARY \_ AUTHENT \_ CLASS-Anbieter identifiziert wird. Wenn dieser Wert für einen Anbieter dieser Klasse nicht vorhanden ist, wird erwartet, dass die Anmeldeinformationsverwaltungsfunktionen aus der DLL exportiert werden, die durch den ProviderPath-Wert identifiziert wird. Dieser Wert wird nur verwendet, wenn es wünschenswert ist, die Netzwerkfunktionen und die Anmeldeinformations-Manager-Funktionen in separaten DLLs zu packen.<br/>  |



 

Zusätzlich zu den Werten, die zum Registrieren von Netzwerkanbietern und Anmeldeinformations-Managern verwendet werden, können Sie der Registrierung einen Wert hinzufügen, um eine DLL für den Empfang von Verbindungsbenachrichtigungen zu registrieren. Erstellen Sie hierzu einen REG \_ EXPAND \_ SZ-Wert unter dem folgenden Schlüssel:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Control
            NetworkProvider
               Notifyees
```

Dieser Wert sollte den Pfad zu einer DLL angeben, die die [Verbindung Benachrichtigungs-API](connection-notification-api.md)implementiert. Der Name dieses Werts kann beliebig sein, solange er nicht mit bereits vorhandenen Wertnamen in Konflikt steht.

## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt die Registrierungsschlüssel für ein System, auf dem zwei Netzwerkanbieter installiert sind: LanmanWorkStation und AnotherNetSvc. AnotherNetSvc ist auch ein Anmeldeinformations-Manager. Im Beispiel sind Schlüsselnamen fett formatiert und Wertnamen kursiv.

**HKEY \_ LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Control** \\ **NetworkProvider-Reihenfolge** \\ 

*ProviderOrder* = "LanmanWorkStation,AnotherNetSvc"

**HKEY \_ LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Control** \\ **NetworkProvider** \\ **Notifyees**

*MyNotifyApp* = "c: \\ connect \\connect.dll"

**HKEY \_ LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Services** \\ **LanmanWorkStation**\\

*Group* = "NetworkProvider"

**HKEY \_ LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Services** \\ **LanmanWorkStation** \\ **NetworkProvider**

*Name* = "NT LanMan"*ProviderPath* = "ntlanman.dll"

*Klasse* = 0x00000001 (WN-NETZWERKKLASSE) \_ \_

**HKEY \_ LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Services** \\ **AnotherNetSvc**\\

*Group* = "NetworkProvider"

**HKEY \_ LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Services** \\ **AnotherNetSvc** \\ **NetworkProvider**

*Name* = "Another Network"*ProviderPath* = "c: \\ another \\anet.dll"

*Klasse* = 0x00000003 (WN-NETZWERKKLASSE \_ \_ \| WN \_ CREDENTIAL \_ CLASS)

*AuthentProviderPath* = "c: \\ another \\anetCM.dll"

 

