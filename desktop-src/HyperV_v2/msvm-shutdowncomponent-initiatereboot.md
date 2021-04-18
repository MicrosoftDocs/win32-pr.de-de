---
description: Initiiert einen Neustart Vorgang des Betriebssystems auf der zugeordneten untergeordneten virtuellen Maschine.
ms.assetid: 9f3ebbaf-ee0f-4c01-8f73-1f37c08a0feb
title: Initiatereboot-Methode der Msvm_ShutdownComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ShutdownComponent.InitiateReboot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 527569e8a5d6c2bb0a54294637ae19c13f5e3af2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368138"
---
# <a name="initiatereboot-method-of-the-msvm_shutdowncomponent-class"></a>Initiatereboot-Methode der MSVM \_ shutdowncomponent-Klasse

Initiiert einen Neustart Vorgang des Betriebssystems auf der zugeordneten untergeordneten virtuellen Maschine.

Wenn 0 (null) zurückgegeben wird, wurde der Neustart erfolgreich initiiert. Jeder andere Rückgabecode weist auf eine Fehlerbedingung hin.

## <a name="syntax"></a>Syntax


```mof
uint32 InitiateReboot(
  [in] boolean Force,
  [in] string  Reason
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Erzwingen* \[ in\]
</dt> <dd>

Ein Flag, das beim Wert "true" erzwingt, dass Anwendungen geschlossen werden, obwohl nicht gespeicherte Daten vorhanden sind.

</dd> <dt>

*Grund* \[ in\]
</dt> <dd>

Der Grund für den Neustart Vorgang. Dies ist eine benutzerdefinierte Zeichenfolge.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück:

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)
</dt> <dt>

Fehler **(32768** )
</dt> <dt>

**Zugriff verweigert** (32769)
</dt> <dt>

**Nicht unterstützt** (32770)
</dt> <dt>

Der **Status ist "Unknown** " (32771).
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Ungültiger Parameter** (32773)
</dt> <dt>

Das **System wird verwendet** (32774).
</dt> <dt>

**Ungültiger Status für diesen Vorgang** (32775).
</dt> <dt>

**Falscher Datentyp** (32776).
</dt> <dt>

Das **System ist nicht verfügbar** (32777).
</dt> <dt>

**Nicht** genügend Arbeitsspeicher (32778)
</dt> <dt>

Die **Datei wurde nicht gefunden** (32779).
</dt> <dt>

**Das System ist nicht bereit** (32780).
</dt> <dt>

**Der Computer ist gesperrt und kann nicht ohne die Option "Force** " (32781) heruntergefahren werden.
</dt> <dt>

**Ein Herunterfahren des Systems wird** ausgeführt (32782).
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSVM \_ shutdowncomponent**](msvm-shutdowncomponent.md)
</dt> </dl>

 

 




