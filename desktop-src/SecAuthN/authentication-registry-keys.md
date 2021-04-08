---
description: Wenn ein Netzwerkanbieter installiert wird, sollte Ihre Anwendung die in diesem Thema beschriebenen Registrierungsschlüssel und-Werte erstellen.
ms.assetid: cc5a4a7b-02b5-4ecd-967c-de0656f00846
title: Registrierungsschlüssel für die Authentifizierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ee2e42febe7516060dd61a7b751a33dcf62cb9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959968"
---
# <a name="authentication-registry-keys"></a>Registrierungsschlüssel für die Authentifizierung

Wenn ein Netzwerkanbieter installiert wird, sollte Ihre Anwendung die in diesem Thema beschriebenen Registrierungsschlüssel und-Werte erstellen. Diese Schlüssel und Werte stellen dem MPR Informationen zu den Netzwerkanbietern bereit, die auf dem System installiert sind. Die MPR prüft diese Schlüssel beim Start und lädt die gefundenen DLLs für den Netzwerkanbieter.

Bevor Sie eine Reihe von Schlüsseln erstellen, die Informationen über Ihren Netzwerkanbieter enthalten, sollten Sie den Namen Ihres Netzwerk Anbieters dem **Bestell** Schlüssel hinzufügen. Dieser Schlüssel ist ein Unterschlüssel des folgenden Schlüssels:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Control
            NetworkProvider
```

Der **Bestell** Schlüssel enthält einen einzelnen Wert, **ProviderOrder**, der die installierten Anbieter auflistet und die Reihenfolge angibt, in der Sie während des Vorgangs ausprobiert werden sollen, der die Anbieter durchläuft, bis ein akzeptier barer Anbieter gefunden wird.

Der **ProviderOrder** -Wert enthält eine durch Trennzeichen getrennte Liste von Schlüsselnamen. Jeder Schlüssel Name in **ProviderOrder** identifiziert einen Netzwerkanbieter. Wenn MPR die Anbieter durchläuft, werden diese in der Reihenfolge aufgerufen, in der Sie in der Liste angezeigt werden.

Der in **ProviderOrder** festgelegte Anbieter Name sollte auch als Name des Registrierungsschlüssels verwendet werden, der Informationen zu diesem Anbieter enthält. Die anbieterspezifischen Registrierungsschlüssel werden als Unterschlüssel des folgenden Schlüssels erstellt:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
```

Anders ausgedrückt: die in **ProviderOrder** angegebenen Anbieter Namen sind der Pfad zur Registrierung der Netzwerkanbieter spezifischen Schlüssel relativ zum folgenden Pfad:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
```

Wenn Ihr Netzwerkanbieter Dienst installiert ist, sollte die Installationsanwendung einen Schlüssel wie folgt hinzufügen:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            ProviderName
```

Dabei steht *providerName* für den Namen des Netzwerk Anbieters, der im **ProviderOrder** -Wert des **Auftrags** Schlüssels angegeben ist. Der **Gruppen** Wert unter dem *providerName* -Schlüssel sollte auf "Network Provider" festgelegt werden. Dadurch wird der Dienst als in der Netzwerkanbieter Gruppe festgelegt.

Sie müssen auch einen Unterschlüssel von *providerName*, **Network Provider**, erstellen. Dieser Schlüssel enthält die folgenden Werte, die den Netzwerkanbieter beschreiben.



| Wert                       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Name**<br/>         | Enthält den Namen des Anbieters. Dieser Name wird dem Benutzer als Name des Netzwerks in den Dialogfeldern zum Durchsuchen angezeigt und sollte mit dem Feld **lpprovider** , das in den Strukturen von " [**nettresource**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) " zurückgegeben wird, identisch sein. Dieser Name muss eine Variation des Produkt namens sein, vorzugsweise mit einem Hinweis auf das Unternehmen, sodass er eindeutig und eindeutig ist. "MS-LanMan" ist beispielsweise ein guter Name, während "the net" eine schlechte Wahl wäre.<br/> |
| **ProviderPath**<br/> | Enthält den vollständigen Pfad der dll, die den Netzwerkanbieter implementiert. MPR ruft [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) auf diesem Pfad auf.<br/>                                                                                                                                                                                                                                                                                                                                |



 

Die folgenden Werte werden nur von Netzwerkanbietern verwendet, die die Funktionen für die Verwaltung von Anmelde Informationen, [**nplogonnotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) und [**nppasswordchangenotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify), unterstützen.



| Wert                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Klasse**<br/>               | Ein **DWORD** , das die Klasse oder den Typ der Anbieter Funktionalität identifiziert, die dieser Anbieter unterstützt. Werte können ggf. durch den **or** -Operator verknüpft werden. Gültige Werte hierfür sind "WN \_ Network \_ Class", "WN \_ Credential \_ Class", "WN \_ Primary \_ Authent \_ Class" und "WN \_ Service Class" \_ .<br/> Obwohl ein Anbieter möglicherweise die primäre Authenticator-Funktionalität unterstützt, wird ein weiterer Mittelwert verwendet, um zu bestimmen, welcher Authentifikator primär ist.<br/> **Windows XP/2000:** Das wechseln primärer Authentifikatoren wird nicht unterstützt, daher wird dieser Wert ignoriert. <br/> |
| **Authentproviderpath**<br/> | Dies ist der voll qualifizierte Dateiname für die dll, von der die Funktionen zur Verwaltung von Anmelde Informationen exportiert werden. Dieser Wert ist nur nützlich (aber nicht erforderlich), wenn der Anbieter als Anmelde Informations \_ Klasse oder primärer \_ Authent- \_ Klassen Anbieter identifiziert wird. Wenn dieser Wert für einen Anbieter dieser Klasse nicht vorhanden ist, wird erwartet, dass die Anmelde Informations Verwaltungsfunktionen aus der durch den ProviderPath-Wert identifizierten dll exportiert werden. Dieser Wert wird nur verwendet, wenn es wünschenswert ist, die Netzwerkfunktionen und die Funktionen der Anmelde Informationsverwaltung in separaten DLLs zu verpacken.<br/>  |



 

Zusätzlich zu den Werten, die zum Registrieren von Netzwerkanbietern und Anmelde Informations Managern verwendet werden, können Sie der Registrierung einen Wert hinzufügen, um eine DLL für den Empfang von Verbindungs Benachrichtigungen zu registrieren. Erstellen Sie hierzu \_ \_ den Wert reg Expand SZ unter folgendem Schlüssel:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Control
            NetworkProvider
               Notifyees
```

Dieser Wert sollte den Pfad zu einer DLL angeben, die die [Verbindungs Benachrichtigungs-API](connection-notification-api.md)implementiert. Der Name dieses Werts kann beliebig sein, solange er nicht mit bereits vorhandenen Wertnamen in Konflikt steht.

## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt die Registrierungsschlüssel für ein System, das zwei Netzwerkanbieter installiert hat: "LanmanWorkstation" und "anothernetzvc". Anothernetzvc ist auch eine Anmelde Informationsverwaltung. Im Beispiel sind die Schlüsselnamen fett formatiert, und Wertnamen sind kursiv formatiert.

**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **Network Provider** \\ **Order**

*ProviderOrder* = "LanmanWorkstation, anothernetzvc"

**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **Network Provider** \\ **notififyees**

*Mynotifyapp* = "c: \\ Connect \\connect.dll"

**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **LanmanWorkstation**\\

*Group* = "Network Provider"

**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **LanmanWorkstation** \\ **Network Provider**

*Name* = "NT LanMan"*ProviderPath* = "ntlanman.dll"

*Class* = 0x00000001 (WN- \_ Netzwerk \_ Klasse)

**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **anothernetzvc**\\

*Group* = "Network Provider"

**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **anothernetzwerkvc** \\ **Network Provider**

*Name* = "ein anderes Netzwerk"*ProviderPath* = "c: \\ andere \\anet.dll"

*Class* = 0x00000003 (WN- \_ Netzwerk \_ Klasse \| WN \_ Credential \_ Class)

*Authentproviderpath* = "c: \\ andere \\anetCM.dll"

 

