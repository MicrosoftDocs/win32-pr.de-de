---
description: Die Registrierungsvirtualisierung ist eine Anwendungs Kompatibilitäts Technologie, die es ermöglicht, Registrierungs Schreibvorgänge mit globaler Auswirkung an benutzerspezifische Speicherorte umzuleiten.
ms.assetid: dace2f65-df60-419a-8be8-ab60668e6396
title: Registrierungsvirtualisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 642bda46b43fc0b4f7efa60cfcd9e2178643811f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351611"
---
# <a name="registry-virtualization"></a>Registrierungsvirtualisierung

Die *Registrierungsvirtualisierung* ist eine Anwendungs Kompatibilitäts Technologie, die es ermöglicht, Registrierungs Schreibvorgänge mit globaler Auswirkung an benutzerspezifische Speicherorte umzuleiten. Diese Umleitung ist für Anwendungen transparent, die aus der Registrierung lesen oder in diese schreiben. Sie wird ab Windows Vista unterstützt.

Diese Form der Virtualisierung ist eine zwischen Anwendungs Kompatibilitäts Technologie. Microsoft beabsichtigt, Sie aus zukünftigen Versionen des Windows-Betriebssystems zu entfernen, da mehr Anwendungen mit Windows Vista und neueren Windows-Versionen kompatibel gemacht werden. Daher ist es wichtig, dass Ihre Anwendung nicht vom Verhalten der Registrierungsvirtualisierung im System abhängig ist.

Die Virtualisierung soll lediglich die Kompatibilität vorhandener Anwendungen gewährleisten. Anwendungen, die für Windows Vista und spätere Versionen von Windows entwickelt wurden, sollten nicht in sensible Systembereiche schreiben und sollten sich nicht auf die Virtualisierung verlassen, um Probleme zu beheben. Beim Aktualisieren von vorhandenem Code für die Ausführung unter Windows Vista und höheren Versionen von Windows sollten die Entwickler sicherstellen, dass Anwendungen nur Daten an benutzerspezifischen Speicherorten oder an Computer Standorten innerhalb von% alluserprofile% speichern, die eine Zugriffs Steuerungs Liste (ACL) ordnungsgemäß verwenden.

Weitere Informationen zum Entwickeln von UAC-kompatiblen Anwendungen finden Sie im [UAC-Entwicklerhandbuch](/previous-versions/dotnet/articles/aa480150(v=msdn.10)).

## <a name="virtualization-overview"></a>Übersicht über die Virtualisierung

Vor Windows Vista wurden Anwendungen in der Regel von Administratoren ausgeführt. Daher können Anwendungen kostenlos auf Systemdateien und Registrierungsschlüssel zugreifen. Wenn diese Anwendungen von einem Standardbenutzer ausgeführt wurden, können Sie aufgrund unzureichender Zugriffsrechte nicht ausgeführt werden. Windows Vista und spätere Versionen von Windows verbessern die Anwendungs Kompatibilität für diese Anwendungen, indem diese Vorgänge automatisch umgeleitet werden. Registrierungs Vorgänge für den globalen Speicher (**HKEY \_ local \_ Machine \\ Software**) werden z. b. an einen benutzerspezifischen Speicherort im Benutzerprofil umgeleitet, das als *virtueller Speicher* (**HKEY \_ Users \\ <User SID> \_ Classes \\ virtualstore \\ Machine \\ Software**) bezeichnet wird.

Die Registrierungsvirtualisierung kann im Allgemeinen in folgende Typen eingeteilt werden:

<dl> <dt>

<span id="Open_Registry_Virtualization"></span><span id="open_registry_virtualization"></span><span id="OPEN_REGISTRY_VIRTUALIZATION"></span>Registrierungsvirtualisierung öffnen
</dt> <dd>

Wenn der Aufrufer keinen Schreibzugriff auf einen Schlüssel hat und versucht, den Schlüssel zu öffnen, wird der Schlüssel mit dem maximal zulässigen Zugriff für diesen Aufrufer geöffnet.

Wenn das Flag "nicht unbeaufsichtigtes \_ \_ \_ \_ fehlschlagen" für den Schlüssel festgelegt ist, schlägt der Vorgang fehl, und der Schlüssel wird nicht geöffnet. Weitere Informationen finden Sie weiter unten in diesem Thema unter "Steuern der Registrierungsvirtualisierung".

</dd> <dt>

<span id="Write_Registry_Virtualization"></span><span id="write_registry_virtualization"></span><span id="WRITE_REGISTRY_VIRTUALIZATION"></span>Registrierungs-Virtualisierung schreiben
</dt> <dd>

Wenn der Aufrufer keinen Schreibzugriff auf einen Schlüssel hat und versucht, einen Wert in den Schlüssel zu schreiben oder einen Unterschlüssel zu erstellen, wird der Wert in den virtuellen Speicher geschrieben.

Wenn ein eingeschränkter Benutzer z. b. versucht, einen Wert in den folgenden Schlüssel zu schreiben: **HKEY \_ local \_ Machine \\** \\ *AppKey1*, wird der Schreibvorgang von der Virtualisierung an die **HKEY- \_ Benutzer \\ <User SID> \_ Klassen \\ virtualstore- \\ Computer \\ Software** \\ *AppKey1* umgeleitet.

</dd> <dt>

<span id="Read_Registry_Virtualization"></span><span id="read_registry_virtualization"></span><span id="READ_REGISTRY_VIRTUALIZATION"></span>Lesen der Registrierungsvirtualisierung
</dt> <dd>

Wenn der Aufrufer aus einem virtualisierten Schlüssel liest, stellt die Registrierung eine zusammengeführte Ansicht der virtualisierten Werte (aus dem virtuellen Speicher) und der nicht virtuellen Werte (aus dem globalen Speicher) für den Aufrufer dar.

Nehmen wir beispielsweise an, dass **HKEY \_ local \_ Machine \\ Software** \\ *AppKey1* die beiden Werte v1 und v2 enthält und dass ein eingeschränkter Benutzer einen Wert v3 in den Schlüssel schreibt. Wenn der Benutzer versucht, Werte aus diesem Schlüssel zu lesen, enthält die zusammengeführte Sicht die Werte v1 und v2 aus dem globalen Speicher und Wert V3 aus dem virtuellen Speicher.

Beachten Sie, dass virtuelle Werte, wenn Sie vorhanden sind, Vorrang vor globalen Werten haben. Im obigen Beispiel, auch wenn der globale Speicher unter diesem Schlüssel den Wert V3 hat, wird der Wert V3 weiterhin vom virtuellen Speicher an den Aufrufer zurückgegeben. Wenn V3 aus dem virtuellen Speicher gelöscht werden soll, wird V3 aus dem globalen Speicher zurückgegeben. Anders ausgedrückt: Wenn V3 aus **HKEY- \_ Benutzer \\ <User SID> \_ Klassen, \\ virtualstore- \\ Computer \\ Software** \\ *AppKey1* , aber **HKEY \_ local \_ Machine \\ Software** AppKey1 mit dem Wert "v3" gelöscht werden soll \\  , wird dieser Wert aus dem globalen Speicher zurückgegeben.

</dd> </dl>

## <a name="registry-virtualization-scope"></a>Gültigkeitsbereich der Registrierungs Virtualisierung

Die Registrierungsvirtualisierung ist nur für Folgendes aktiviert:

-   interaktive 32-Bit-Prozesse.
-   Schlüssel in der **lokalen HKEY- \_ \_ Computer \\ Software**.
-   Schlüssel, in die ein Administrator schreiben kann. (Wenn ein Administrator nicht in einen Schlüssel schreiben kann, würde die Anwendung auf früheren Versionen von Windows fehlgeschlagen sein, auch wenn Sie von einem Administrator ausgeführt wurde.)

Die Registrierungsvirtualisierung ist für Folgendes deaktiviert:

-   64-Bit-Prozesse.
-   Prozesse, die nicht interaktiv sind, z. b. Dienste.

    Beachten Sie, dass die Registrierung als Mechanismus für die prozessübergreifende Kommunikation (Inter-Process Communication, IPC) zwischen einem Dienst (oder einem anderen Prozess, für den keine Virtualisierung aktiviert ist) verwendet wird und eine Anwendung nicht ordnungsgemäß funktioniert, wenn der Schlüssel virtualisiert ist. Wenn beispielsweise ein Antivirendienst seine Signatur Dateien auf Grundlage eines von einer Anwendung festgelegten Werts aktualisiert, aktualisiert der Dienst seine Signatur Dateien nie, da der Dienst aus dem globalen Speicher liest, die Anwendung jedoch in den virtuellen Speicher schreibt.

-   Prozesse, die die Identität eines Benutzers annehmen. Wenn ein Prozess einen Vorgang während der Identität eines Benutzers annimmt, wird dieser Vorgang nicht virtualisiert.
-   Kernel Modus-Prozesse, z. b. Treiber.
-   Prozesse, für die **requestedExecutionLevel** in ihren Manifesten angegeben ist.
-   Schlüssel und Unterschlüssel von **HKEY \_ - \_ \\ Software \\ Klassen für lokale Computer**, **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows** und **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows NT**.

## <a name="controlling-registry-virtualization"></a>Steuern der Registrierungsvirtualisierung

Zusätzlich zur Steuerung der Virtualisierung auf Anwendungsebene, indem **requestedExecutionLevel** im Manifest verwendet wird, kann ein Administrator die Virtualisierung auf Schlüssel Basis für Schlüssel in der **\_ lokalen \_ Computer \\ Software von HKEY** aktivieren bzw. deaktivieren. Verwenden Sie hierzu die Option Flags für Reg.exe Befehlszeilen-Hilfsprogramm mit den Flags, die in der folgenden Tabelle aufgeführt sind.



| Flag                         | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| REG \_ - \_ Schlüssel \_ \_ nicht unbeaufsichtigt | Dieses Flag deaktiviert die öffnende Registrierungsvirtualisierung. Wenn dieses Flag festgelegt ist und ein Öffnungsvorgang für einen Schlüssel mit aktivierter Virtualisierung fehlschlägt, versucht die Registrierung nicht, den Schlüssel erneut zu öffnen. Wenn dieses Flag eindeutig ist, versucht die Registrierung, den Schlüssel mit maximal zulässiger Zugriffsberechtigung erneut zu öffnen, \_ anstatt auf den angeforderten Zugriff zuzugreifen.                                                                   |
| REG- \_ Schlüssel nicht \_ \_ virtualisieren   | Mit diesem Flag wird die Serialisierung der Schreib Registrierung deaktiviert. Wenn dieses Flag festgelegt ist und ein Vorgang zum Erstellen eines Schlüssels oder eines festgelegten Werts fehlschlägt, weil der Aufrufer nicht über ausreichende Zugriffsrechte für den übergeordneten Schlüssel verfügt, schlägt die Registrierung fehl. Wenn dieses Flag eindeutig ist, versucht die Registrierung, den Schlüssel oder Wert im virtuellen Speicher zu schreiben. Der Aufrufer muss über die Berechtigung zum Lesen des Schlüssels \_ für den übergeordneten Schlüssel verfügen. |
| REG \_ Key \_ recurse- \_ Flag      | Wenn dieses Flag festgelegt ist, werden registrierungsvirtualisierungsflags aus dem übergeordneten Schlüssel weitergegeben. Wenn dieses Flag eindeutig ist, werden die registrierungsvirtualisierungsflags nicht weitergegeben. Das Ändern dieses Flags wirkt sich nur auf neue Nachfolger Schlüssel aus, die erstellt werden, nachdem das Flag geändert wurde. Diese Flags für vorhandene Nachfolger Schlüssel werden nicht festgelegt oder deaktiviert.                                                                  |



 

Das folgende Beispiel zeigt die Verwendung des Befehlszeilen Dienstprogramms Reg.exe mit der Flags-Option, um den Status der virtualisierungsflags für einen Schlüssel abzufragen.

``` syntax
C:\>reg flags HKLM\Software\AppKey1 QUERY

HKEY_LOCAL_MACHINE\Software\AppKey1

        REG_KEY_DONT_VIRTUALIZE: CLEAR
        REG_KEY_DONT_SILENT_FAIL: CLEAR
        REG_KEY_RECURSE_FLAG: CLEAR

The operation completed successfully.
```

Wenn die Überwachung für einen Schlüssel aktiviert ist, der virtualisiert wird, wird ein neues virtualisierungsprüfungs-Ereignis generiert, das angibt, dass der Schlüssel virtualisiert wird (zusätzlich zu den üblichen Überwachungs Ereignissen). Administratoren können diese Informationen verwenden, um den Status der Virtualisierung auf Ihren Systemen zu überwachen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einstieg in die Benutzerkontensteuerung](/previous-versions/windows/it-pro/windows-vista/cc507861(v=technet.10))
</dt> <dt>

[Verstehen und Konfigurieren der Benutzerkontensteuerung](/previous-versions/windows/it-pro/windows-vista/cc709628(v=ws.10))
</dt> <dt>

[Bewährte Methoden für Entwickler und Richtlinien für Anwendungen in einer Umgebung mit geringsten Rechten](/previous-versions/dotnet/articles/aa480150(v=msdn.10))
</dt> </dl>

 

 
