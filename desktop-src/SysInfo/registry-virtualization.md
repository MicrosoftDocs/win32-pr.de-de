---
description: Die Registrierungsvirtualisierung ist eine Anwendungskompatibilitätstechnologie, mit der Schreibvorgänge für Registrierungen mit globalen Auswirkungen an benutzerspezifische Speicherorte umgeleitet werden können.
ms.assetid: dace2f65-df60-419a-8be8-ab60668e6396
title: Registrierungsvirtualisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f14d8a82a12be74d3c5f2963e8b4edf47baaa85c4a8299e4ff632284bbac83fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117763587"
---
# <a name="registry-virtualization"></a>Registrierungsvirtualisierung

*Die Registrierungsvirtualisierung* ist eine Anwendungskompatibilitätstechnologie, mit der Schreibvorgänge für Registrierungen mit globalen Auswirkungen an benutzerspezifische Speicherorte umgeleitet werden können. Diese Umleitung ist für Anwendungen transparent, die aus der Registrierung lesen oder in die Registrierung schreiben. Sie wird ab Windows Vista unterstützt.

Diese Form der Virtualisierung ist eine Zwischenanwendungskompatibilitätstechnologie. Microsoft möchte es aus zukünftigen Versionen des Windows Betriebssystems entfernen, da mehr Anwendungen mit Windows Vista und neueren Versionen von Windows kompatibel gemacht werden. Daher ist es wichtig, dass Ihre Anwendung nicht vom Verhalten der Registrierungsvirtualisierung im System abhängig wird.

Die Virtualisierung dient nur dazu, Kompatibilität für vorhandene Anwendungen bereitzustellen. Anwendungen, die für Windows Vista und höhere Versionen von Windows entwickelt wurden, sollten weder in sensible Systembereiche schreiben, noch sollten sie virtualisierungsabhängig sein, um Probleme zu beheben. Beim Aktualisieren von vorhandenem Code für die Ausführung auf Windows Vista und neueren Versionen von Windows sollten Entwickler sicherstellen, dass Anwendungen Daten nur an Benutzerstandorten oder an Computerstandorten innerhalb von %alluserprofile% speichern, die eine Zugriffssteuerungsliste (Access Control List, ACL) ordnungsgemäß verwenden.

Weitere Informationen zum Erstellen von UAC-kompatiblen Anwendungen finden Sie im [UAC-Entwicklerhandbuch.](/previous-versions/dotnet/articles/aa480150(v=msdn.10))

## <a name="virtualization-overview"></a>Virtualisierungsübersicht

Vor Windows Vista wurden Anwendungen in der Regel von Administratoren ausgeführt. Daher können Anwendungen frei auf Systemdateien und Registrierungsschlüssel zugreifen. Wenn diese Anwendungen von einem Standardbenutzer ausgeführt würden, würden sie aufgrund unzureichender Zugriffsrechte fehlschlagen. Windows Vista und höhere Versionen von Windows die Anwendungskompatibilität für diese Anwendungen verbessern, indem diese Vorgänge automatisch umgeleitet werden. Beispielsweise werden Registrierungsvorgänge für den globalen Speicher (**HKEY \_ LOCAL MACHINE \_ \\ Software**) an einen benutzerbezogenen Speicherort innerhalb des Profils des Benutzers umgeleitet, der als *virtueller Speicher* bezeichnet wird (**HKEY USERS Classes \_ \\ <User SID> \_ \\ VirtualStore Machine \\ \\ Software**).

Die Registrierungsvirtualisierung kann im Großen und Ganzen in die folgenden Typen unterteilt werden:

<dl> <dt>

<span id="Open_Registry_Virtualization"></span><span id="open_registry_virtualization"></span><span id="OPEN_REGISTRY_VIRTUALIZATION"></span>Open Registry Virtualization
</dt> <dd>

Wenn der Aufrufer keinen Schreibzugriff auf einen Schlüssel hat und versucht, den Schlüssel zu öffnen, wird der Schlüssel mit dem maximal zulässigen Zugriff für diesen Aufrufer geöffnet.

Wenn das FLAG REG \_ KEY \_ DONT \_ SILENT FAIL für den Schlüssel festgelegt \_ ist, schlägt der Vorgang fehl, und der Schlüssel wird nicht geöffnet. Weitere Informationen finden Sie unter "Steuern der Registrierungsvirtualisierung" weiter unten in diesem Thema.

</dd> <dt>

<span id="Write_Registry_Virtualization"></span><span id="write_registry_virtualization"></span><span id="WRITE_REGISTRY_VIRTUALIZATION"></span>Schreibregistrierungsvirtualisierung
</dt> <dd>

Wenn der Aufrufer keinen Schreibzugriff auf einen Schlüssel hat und versucht, einen Wert in diesen zu schreiben oder einen Unterschlüssel zu erstellen, wird der Wert in den virtuellen Speicher geschrieben.

Wenn beispielsweise ein eingeschränkter Benutzer versucht, einen Wert in den folgenden Schlüssel zu schreiben: **HKEY \_ LOCAL MACHINE \_ \\ Software** \\ *AppKey1*, leitet die Virtualisierung den Schreibvorgang an **HKEY USERS Classes \_ \\ <User SID> \_ \\ VirtualStore Machine \\ \\ Software** \\ *AppKey1* um.

</dd> <dt>

<span id="Read_Registry_Virtualization"></span><span id="read_registry_virtualization"></span><span id="READ_REGISTRY_VIRTUALIZATION"></span>Lesen der Registrierungsvirtualisierung
</dt> <dd>

Wenn der Aufrufer aus einem virtualisierten Schlüssel liest, stellt die Registrierung dem Aufrufer eine zusammengeführte Ansicht der virtualisierten Werte (aus dem virtuellen Speicher) und der nicht virtuellen Werte (aus dem globalen Speicher) bereit.

Angenommen, **HKEY \_ LOCAL \_ MACHINE \\ Software** \\ *AppKey1* enthält die beiden Werte V1 und V2, und ein eingeschränkter Benutzer schreibt einen Wert V3 in den Schlüssel. Wenn der Benutzer versucht, Werte aus diesem Schlüssel zu lesen, enthält die zusammengeführte Ansicht die Werte V1 und V2 aus dem globalen Speicher und den Wert V3 aus dem virtuellen Speicher.

Beachten Sie, dass virtuelle Werte Vorrang vor globalen Werten haben, wenn sie vorhanden sind. Im obigen Beispiel würde der Wert V3 auch dann an den Aufrufer aus dem virtuellen Speicher zurückgegeben werden, wenn der globale Speicher unter diesem Schlüssel den Wert V3 aufwiesen würde. Wenn V3 aus dem virtuellen Speicher gelöscht wird, wird V3 aus dem globalen Speicher zurückgegeben. Anders ausgedrückt: Wenn V3 aus **den HKEY \_ \\ <User SID> \_ USERS-Klassen \\ VirtualStore Machine \\ \\ Software** AppKey1 gelöscht werden \\  würde, **HKEY LOCAL \_ MACHINE \_ \\ Software** \\ *AppKey1* jedoch den Wert V3 aufwiesen, würde dieser Wert aus dem globalen Speicher zurückgegeben.

</dd> </dl>

## <a name="registry-virtualization-scope"></a>Registrierungsvirtualisierungsbereich

Die Registrierungsvirtualisierung ist nur für Folgendes aktiviert:

-   Interaktive 32-Bit-Prozesse.
-   Schlüssel in **HKEY \_ LOCAL MACHINE \_ \\ Software**.
-   Schlüssel, in die ein Administrator schreiben kann. (Wenn ein Administrator nicht in einen Schlüssel schreiben kann, wäre die Anwendung in früheren Versionen von Windows fehlgeschlagen, auch wenn sie von einem Administrator ausgeführt wurde.)

Die Registrierungsvirtualisierung ist für Folgendes deaktiviert:

-   64-Bit-Prozesse.
-   Prozesse, die nicht interaktiv sind, z. B. Dienste.

    Beachten Sie, dass die Verwendung der Registrierung als Mechanismus für die prozessübergreifende Kommunikation (Inter-Process Communication, IPC) zwischen einem Dienst (oder einem anderen Prozess, für den die Virtualisierung nicht aktiviert ist) und einer Anwendung nicht ordnungsgemäß funktioniert, wenn der Schlüssel virtualisiert ist. Wenn beispielsweise ein Antivirendienst seine Signaturdateien basierend auf einem von einer Anwendung festgelegten Wert aktualisiert, aktualisiert der Dienst nie seine Signaturdateien, da der Dienst aus dem globalen Speicher liest, die Anwendung jedoch in den virtuellen Speicher schreibt.

-   Prozesse, die die Identität eines Benutzers annehmen. Wenn ein Prozess einen Vorgang versucht, während die Identität eines Benutzers angenommen wird, wird dieser Vorgang nicht virtualisiert.
-   Kernelmodusprozesse wie Treiber.
-   Prozesse, die **requestedExecutionLevel** in ihren Manifesten angegeben haben.
-   Schlüssel und Unterschlüssel der **HKEY \_ LOCAL MACHINE Software \_ \\ \\ Classes**, **HKEY LOCAL MACHINE Software \_ Microsoft \_ \\ \\ \\ Windows** und **HKEY LOCAL MACHINE Software \_ Microsoft Windows \_ \\ \\ \\ NT**.

## <a name="controlling-registry-virtualization"></a>Steuern der Registrierungsvirtualisierung

Zusätzlich zur Steuerung der Virtualisierung auf Anwendungsebene mit **requestedExecutionLevel** im Manifest kann ein Administrator die Virtualisierung pro Schlüssel für Schlüssel in **HKEY \_ LOCAL MACHINE \_ \\ Software** aktivieren oder deaktivieren. Verwenden Sie hierzu die Option Reg.exe Befehlszeilen-Hilfsprogramm FLAGS mit den in der folgenden Tabelle aufgeführten Flags.



| Flag                         | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FEHLER BEIM NICHT \_ \_ \_ AUTOMATISCHEN \_ REGISTRIEREN DES SCHLÜSSELS | Dieses Flag deaktiviert die Open Registry-Virtualisierung. Wenn dieses Flag festgelegt ist und bei einem Schlüssel, für den virtualisierungsaktiviert ist, ein Fehler beim Öffnen auftritt, versucht die Registrierung nicht, den Schlüssel erneut zu öffnen. Wenn dieses Flag eindeutig ist, versucht die Registrierung, den Schlüssel mit DEM MAXIMAL ZULÄSSIGen Zugriff anstelle des angeforderten Zugriffs erneut zu \_ öffnen.                                                                   |
| REG \_ KEY \_ DONT \_ VIRTUALIZE   | Dieses Flag deaktiviert die Schreibregistrierungsvirtualisierung. Wenn dieses Flag festgelegt ist und ein Erstellungsschlüssel- oder Werterstellungsvorgang fehlschlägt, weil der Aufrufer nicht über ausreichende Zugriffsrechte auf den übergeordneten Schlüssel verfügt, schlägt die Registrierung den Vorgang fehl. Wenn dieses Flag eindeutig ist, versucht die Registrierung, den Schlüssel oder Wert im virtuellen Speicher zu schreiben. Der Aufrufer muss über die BERECHTIGUNG KEY \_ READ für den übergeordneten Schlüssel verfügen. |
| \_ \_ REKURSIVES FLAG DES REG-SCHLÜSSELS \_      | Wenn dieses Flag festgelegt ist, werden Registrierungsvirtualisierungsflags vom übergeordneten Schlüssel weitergegeben. Wenn dieses Flag eindeutig ist, werden Registrierungsvirtualisierungsflags nicht weitergegeben. Das Ändern dieses Flags wirkt sich nur auf neue Nachfolgerschlüssel aus, die nach dem Ändern des Flags erstellt wurden. Diese Flags für vorhandene Nachfolgerschlüssel werden nicht festgelegt oder gelöscht.                                                                  |



 

Das folgende Beispiel zeigt die Verwendung des Befehlszeilen-Hilfsprogramms Reg.exe mit der Flags-Option, um den Status der Virtualisierungsflags nach einem Schlüssel abzufragen.

``` syntax
C:\>reg flags HKLM\Software\AppKey1 QUERY

HKEY_LOCAL_MACHINE\Software\AppKey1

        REG_KEY_DONT_VIRTUALIZE: CLEAR
        REG_KEY_DONT_SILENT_FAIL: CLEAR
        REG_KEY_RECURSE_FLAG: CLEAR

The operation completed successfully.
```

Wenn die Überwachung für einen Schlüssel aktiviert ist, der virtualisiert wird, wird ein neues Virtualisierungsüberwachungsereignis generiert, um anzugeben, dass der Schlüssel virtualisiert wird (zusätzlich zu den üblichen Überwachungsereignissen). Administratoren können diese Informationen verwenden, um den Status der Virtualisierung auf ihren Systemen zu überwachen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erste Schritte mit Benutzerkontensteuerung](/previous-versions/windows/it-pro/windows-vista/cc507861(v=technet.10))
</dt> <dt>

[Grundlegendes und Konfigurieren der Benutzerkontensteuerung](/previous-versions/windows/it-pro/windows-vista/cc709628(v=ws.10))
</dt> <dt>

[Bewährte Methoden und Richtlinien für Entwickler für Anwendungen in einer Umgebung mit den geringsten Berechtigungen](/previous-versions/dotnet/articles/aa480150(v=msdn.10))
</dt> </dl>

 

 
