---
title: Preferredserverbitness
description: Legt die bevorzugte Architektur (32-Bit oder 64-Bit) für diesen com-Server fest.
ms.assetid: ef770039-1624-4256-aa09-1443695c1a1f
keywords:
- "' Preferredserverbitness '-Registrierungs Wert com"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 107a8c5b1504c5a59ca2ab178cd46236335d44ca
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316545"
---
# <a name="preferredserverbitness"></a>Preferredserverbitness

Legt die bevorzugte Architektur (32-Bit oder 64-Bit) für diesen com-Server fest.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      PreferredServerBitness = value
```

## <a name="remarks"></a>Bemerkungen

Dies ist ein **reg \_ DWORD** -Wert, der nur in 64-Bit-Versionen von Windows verfügbar ist.



| Wert | BESCHREIBUNG                                                                                                                                                                                                |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | Vergleichen Sie die Serverarchitektur mit der Client Architektur. Wenn der Client z. b. 32-Bit ist, verwenden Sie eine 32-Bit-Version des Servers, sofern verfügbar. Wenn dies nicht der Fall ist, schlägt die Aktivierungs Anforderung des Clients fehl. |
| 2     | Verwenden Sie eine 32-Bit-Version des Servers. Wenn keine vorhanden ist, tritt bei der Aktivierungs Anforderung des Clients ein Fehler auf.                                                                                                      |
| 3     | Verwenden Sie eine 64-Bit-Version des Servers. Wenn keine vorhanden ist, tritt bei der Aktivierungs Anforderung des Clients ein Fehler auf.                                                                                                      |



 

Wenn dieser Wert nicht vorhanden ist, gilt Folgendes:

-   Wenn auf dem Computer, auf dem der Server gehostet wird, Windows XP oder Windows Server 2003 ohne SP1 oder höher ausgeführt wird, wird com eine 64-Bit-Version des Servers bevorzugen, sofern verfügbar. Andernfalls wird eine 32-Bit-Version des Servers aktiviert.
-   Wenn auf dem Computer, auf dem der Server gehostet wird, Windows Server 2003 mit SP1 oder höher ausgeführt wird, versucht com, die Serverarchitektur mit der Client Architektur zu vergleichen. Anders ausgedrückt: bei einem 32-Bit-Client aktiviert com einen 32-Bit-Server, falls verfügbar. Andernfalls wird eine 64-Bit-Version des Servers aktiviert. Bei einem 64-Bit-Client aktiviert com einen 64-Bit-Server, falls verfügbar. Andernfalls wird ein 32-Bit-Server aktiviert.

Der Client kann auch seine eigene Architektur Einstellung über den CLSCTX \_ \_ \_ -32-Bit \_ -Server und CLSCTX aktivieren \_ \_ 64 Bit- \_ \_ Serverflags angeben. diese überschreiben die bevorzugte Servereinstellung. Weitere Informationen und ein Diagramm möglicher Interaktionen zwischen Client-und Serverarchitektur Einstellungen finden Sie unter [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)
</dt> </dl>

 

 