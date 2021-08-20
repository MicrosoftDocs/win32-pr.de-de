---
description: Initiiert einen Neustart des Betriebssystems auf dem zugeordneten untergeordneten virtuellen Computer.
ms.assetid: 9f3ebbaf-ee0f-4c01-8f73-1f37c08a0feb
title: InitiateReboot-Methode der Msvm_ShutdownComponent Klasse
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
ms.openlocfilehash: 20ec6e4522f4a9060ced517b5f9944177a98dfa5455c35e15285921467ed4620
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950489"
---
# <a name="initiatereboot-method-of-the-msvm_shutdowncomponent-class"></a>InitiateReboot-Methode der Msvm \_ ShutdownComponent-Klasse

Initiiert einen Neustart des Betriebssystems auf dem zugeordneten untergeordneten virtuellen Computer.

Wenn 0 (null) zurückgegeben wird, wurde der Neustart erfolgreich initiiert. Jeder andere Rückgabecode gibt einen Fehlerzustand an.

## <a name="syntax"></a>Syntax


```mof
uint32 InitiateReboot(
  [in] boolean Force,
  [in] string  Reason
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Force* \[ In\]
</dt> <dd>

Ein Flag, das bei TRUE erzwingt, dass Anwendungen geschlossen werden, obwohl nicht gespeicherte Daten gespeichert wurden.

</dd> <dt>

*Ursache* \[ In\]
</dt> <dd>

Der Grund für den Neustartvorgang. Dies ist eine benutzerdefinierte Zeichenfolge.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück:

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Überprüfte Methodenparameter – Auftrag gestartet** (4096)
</dt> <dt>

**Fehler** (32768)
</dt> <dt>

**Zugriff verweigert** (32769)
</dt> <dt>

**Nicht unterstützt** (32770)
</dt> <dt>

**Status ist unbekannt** (32771)
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Ungültiger** Parameter (32773)
</dt> <dt>

**System wird verwendet** (32774)
</dt> <dt>

**Ungültiger Zustand für diesen Vorgang** (32775)
</dt> <dt>

**Falscher Datentyp** (32776)
</dt> <dt>

**System ist nicht verfügbar** (32777)
</dt> <dt>

**Nicht genügend Arbeitsspeicher** (32778)
</dt> <dt>

**Datei nicht gefunden** (32779)
</dt> <dt>

**Das System ist nicht bereit** (32780)
</dt> <dt>

**Der Computer ist gesperrt und kann nicht ohne die** Force-Option heruntergefahren werden (32781).
</dt> <dt>

**Ein Herunterfahren des Systems wird in Bearbeitung** (32782)
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msvm \_ ShutdownComponent**](msvm-shutdowncomponent.md)
</dt> </dl>

 

 




