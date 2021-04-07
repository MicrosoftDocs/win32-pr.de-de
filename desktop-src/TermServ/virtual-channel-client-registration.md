---
title: Client Registrierung des virtuellen Kanals
description: Der Name der Client-DLL muss in der Registrierung gespeichert werden.
ms.assetid: bf84b2f4-55c2-45fd-bba7-8ff3efe4b1fd
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcd7ecf128f125f6f25202bf683f8aa55ae4f257
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727896"
---
# <a name="virtual-channel-client-registration"></a>Client Registrierung des virtuellen Kanals

Der Name der Client-DLL muss in der Registrierung gespeichert werden.

Fügen Sie in der Registrierung einen Unterschlüssel zu einem der folgenden Speicherorte hinzu:

**HKEY \_ Aktuelle \_** \\ **Software Software** \\ **Microsoft** \\ **Terminal Server Client** \\ **Standard**- \\ **AddIns**

**HKEY \_ Aktuelle \_ Benutzer** \\ **Software** \\ **Microsoft** \\ **Terminal Server Client** \\ **Connection** \\  -Add-ins

> [!Note]  
> Im Registrierungs Pfad stellt *Connection* den Namen einer Verbindung im Verbindungs-Manager dar.

 

Einträge unter dem **\\ Standardschlüssel \\ AddIns** gelten für alle Verbindungen. Einträge unter dem Schlüssel für die **\\ ***Verbindungs***- \\ AddIns** gelten nur für die durch die *Verbindung* identifizierte Verbindung. Verbindungen können mithilfe des Verbindungs-Managers erstellt und verwaltet werden.

Dem Unterschlüssel kann ein beliebiger Name zugewiesen werden. Er muss einen **reg \_ SZ** -oder **reg \_ Expand \_** -Wert enthalten, der optional einen **reg \_ DWORD** -Wert enthalten kann. Die Syntax des " **reg \_ SZ** "-oder " **reg \_ Expand \_** "-Werts lautet wie folgt.

``` syntax
Name = DLLname
```

Wenn " **Name** " ein reg-Wert "reg" ist, kann er nicht erweiterte Umgebungsvariablen enthalten, die zur Laufzeit erweitert werden. **\_ \_**

Der Wert von " *dllName* " kann ein voll qualifizierter Pfad sein. Wenn *dllName* keinen Pfad enthält, wird die Standard-dll-Suchstrategie verwendet. Weitere Informationen finden Sie im Abschnitt "Hinweise" für [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya).

 

 