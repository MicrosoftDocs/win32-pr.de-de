---
description: Fordert an, dass der Dienst seinen Zustand auf den Dienst-Manager aktualisiert.
ms.assetid: 118156ef-ee43-4f73-af41-e295a0a850b9
ms.tgt_platform: multiple
title: InterrogateService-Methode der Win32_BaseService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.InterrogateService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 02c48dfefe0a1e504dfd40af802ea0737852c61c0cda2c5b62ceff7d9234f3ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119760400"
---
# <a name="interrogateservice-method-of-the-win32_baseservice-class"></a>InterrogateService-Methode der Win32 \_ BaseService-Klasse

Die [WMI-Klassenmethode](/windows/desktop/WmiSdk/retrieving-a-class) **InterrogateService** fordert an, dass der Dienst seinen Zustand auf den Dienst-Manager aktualisiert.

In diesem Thema wird Managed Object Format (MOF)-Syntax verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 InterrogateService();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.

<dl> <dt>

**Erfolgreich**
</dt> <dd>

0

Die Anforderung wurde akzeptiert.

</dd> <dt>

**Nicht unterstützt**
</dt> <dd>

1

Die Anforderung wird nicht unterstützt.

</dd> <dt>

**Zugriff verweigert**
</dt> <dd>

2

Der Benutzer hatte nicht den erforderlichen Zugriff.

</dd> <dt>

**Ausgeführte abhängige Dienste**
</dt> <dd>

3

Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.

</dd> <dt>

**Ungültige Dienststeuerung**
</dt> <dd>

4

Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.

</dd> <dt>

**Der Dienst kann die Steuerung nicht akzeptieren**
</dt> <dd>

5

Der angeforderte Steuerungscode kann nicht an den Dienst gesendet werden, da der Zustand des Diensts ([**Win32 \_ BaseService**](win32-baseservice.md)[**State-Eigenschaft)**](win32-baseservice.md) gleich 0, 1 oder 2 ist.

</dd> <dt>

**Dienst nicht aktiv**
</dt> <dd>

6

Der Dienst wurde nicht gestartet.

</dd> <dt>

**Timeout für Dienstanforderungen**
</dt> <dd>

7

Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.

</dd> <dt>

**Unbekannter Fehler**
</dt> <dd>

8

Interaktiver Prozess.

</dd> <dt>

**Pfad nicht gefunden**
</dt> <dd>

9

Der Verzeichnispfad zur ausführbaren Dienstdatei wurde nicht gefunden.

</dd> <dt>

**Dienst wird bereits ausgeführt**
</dt> <dd>

10

Der Dienst wird schon ausgeführt.

</dd> <dt>

**Dienstdatenbank gesperrt**
</dt> <dd>

11

Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.

</dd> <dt>

**Dienstabhängigkeit gelöscht**
</dt> <dd>

12

Eine Abhängigkeit, von der dieser Dienst abhängt, wurde aus dem System entfernt.

</dd> <dt>

**Dienstabhängigkeitsfehler**
</dt> <dd>

13

Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.

</dd> <dt>

**Dienst deaktiviert**
</dt> <dd>

14

Der Dienst wurde vom System deaktiviert.

</dd> <dt>

**Dienstanmeldung fehlgeschlagen**
</dt> <dd>

15

Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.

</dd> <dt>

**Dienst zum Löschen markiert**
</dt> <dd>

16

Dieser Dienst wird aus dem System entfernt.

</dd> <dt>

**Dienst kein Thread**
</dt> <dd>

17

Es gibt keinen Ausführungsthread für den Dienst.

</dd> <dt>

**Statuskreisabhängigkeit**
</dt> <dd>

18

Es gibt Ringabhängigkeiten beim Starten des Diensts.

</dd> <dt>

**Doppelter Name des Status**
</dt> <dd>

19

Es wird ein Dienst unter dem gleichen Namen ausgeführt.

</dd> <dt>

**Status Ungültiger Name**
</dt> <dd>

20

Der Name des Diensts enthält ungültige Zeichen.

</dd> <dt>

**Ungültiger Statusparameter**
</dt> <dd>

21

Ungültige Parameter wurden an den Dienst übergeben.

</dd> <dt>

**Status Ungültiges Dienstkonto**
</dt> <dd>

22

Das Konto, unter dem dieser Dienst ausgeführt werden soll, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Diensts.

</dd> <dt>

**Statusdienst vorhanden**
</dt> <dd>

23

Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.

</dd> <dt>

**Dienst wurde bereits angehalten**
</dt> <dd>

24

Der Dienst ist im System derzeitig angehalten.

</dd> <dt>

**Andere**
</dt> <dd>

25 4294967295

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32 \_ BaseService**](win32-baseservice.md)
</dt> </dl>

 

