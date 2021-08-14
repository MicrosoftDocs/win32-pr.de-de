---
description: Die Registrierungsvirtualisierung ist eine Technologie zur Anwendungskompatibilität, mit der Schreibvorgänge in Registrierungen, die globale Auswirkungen haben, an benutzerspezifische Speicherorte umgeleitet werden können.
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

*Die Registrierungsvirtualisierung* ist eine Technologie zur Anwendungskompatibilität, mit der Schreibvorgänge in Registrierungen, die globale Auswirkungen haben, an benutzerspezifische Speicherorte umgeleitet werden können. Diese Umleitung ist für Anwendungen transparent, die aus der Registrierung lesen oder in diese schreiben. Dies wird ab Windows Vista unterstützt.

Diese Form der Virtualisierung ist eine Zwischentechnologie zur Anwendungskompatibilität. Microsoft möchte es aus zukünftigen Versionen des Windows-Betriebssystems entfernen, da weitere Anwendungen mit Windows Vista und neueren Versionen von Windows. Daher ist es wichtig, dass Ihre Anwendung nicht vom Verhalten der Registrierungsvirtualisierung im System abhängig wird.

Virtualisierung dient nur dazu, Kompatibilität für vorhandene Anwendungen zu gewährleisten. Anwendungen, die für Windows Vista und neuere Versionen von Windows entwickelt wurden, sollten weder in sensible Systembereiche schreiben noch auf Virtualisierung angewiesen sein, um Probleme zu beheben. Beim Aktualisieren von vorhandenem Code für die Ausführung unter Windows Vista und neueren Versionen von Windows sollten Entwickler sicherstellen, dass Anwendungen Daten nur an Benutzerstandorten oder an Computerstandorten in %alluserprofile% speichern, die eine Zugriffssteuerungsliste (Access Control List, ACL) ordnungsgemäß verwenden.

Weitere Informationen zum Erstellen von UAC-konformen Anwendungen finden Sie im [UAC-Entwicklerhandbuch.](/previous-versions/dotnet/articles/aa480150(v=msdn.10))

## <a name="virtualization-overview"></a>Virtualisierungsübersicht

Vor der Windows Vista wurden Anwendungen in der Regel von Administratoren ausgeführt. Daher können Anwendungen frei auf Systemdateien und Registrierungsschlüssel zugreifen. Wenn diese Anwendungen von einem Standardbenutzer ausgeführt würden, würden sie aufgrund unzureichender Zugriffsrechte fehlschlagen. Windows Vista und spätere Versionen von Windows die Anwendungskompatibilität für diese Anwendungen verbessern, indem diese Vorgänge automatisch umgeleitet werden. Beispielsweise werden Registrierungsvorgänge für den globalen Speicher (**HKEY \_ LOCAL MACHINE \_ \\ Software**) an einen benutzerspezifischen Speicherort innerhalb des Profils des Benutzers umgeleitet, das als virtueller Speicher **(HKEY \_ USERS Classes \\ <User SID> \_ \\ VirtualStore Machine \\ \\ Software)** bekannt *ist.*

Die Registrierungsvirtualisierung kann in die folgenden Typen unterteilt werden:

<dl> <dt>

<span id="Open_Registry_Virtualization"></span><span id="open_registry_virtualization"></span><span id="OPEN_REGISTRY_VIRTUALIZATION"></span>Open Registry Virtualization
</dt> <dd>

Wenn der Aufrufer keinen Schreibzugriff auf einen Schlüssel hat und versucht, den Schlüssel zu öffnen, wird der Schlüssel mit dem maximal zulässigen Zugriff für diesen Aufrufer geöffnet.

Wenn das REG KEY DONT SILENT FAIL-Flag für den Schlüssel festgelegt ist, schlägt der Vorgang \_ \_ \_ \_ fehl, und der Schlüssel wird nicht geöffnet. Weitere Informationen finden Sie unter "Steuern der Registrierungsvirtualisierung" weiter unten in diesem Thema.

</dd> <dt>

<span id="Write_Registry_Virtualization"></span><span id="write_registry_virtualization"></span><span id="WRITE_REGISTRY_VIRTUALIZATION"></span>Schreibregistrierungsvirtualisierung
</dt> <dd>

Wenn der Aufrufer keinen Schreibzugriff auf einen Schlüssel hat und versucht, einen Wert in ihn zu schreiben oder einen Unterschlüssel zu erstellen, wird der Wert in den virtuellen Speicher geschrieben.

Wenn ein eingeschränkter Benutzer beispielsweise versucht, einen Wert in den folgenden Schlüssel zu schreiben: **HKEY \_ LOCAL MACHINE \_ \\ Software** AppKey1, leitet die Virtualisierung den Schreibvorgang an \\ die **HKEY \_ \\ <User SID> \_ USERS-Klassen \\ VirtualStore Machine \\ \\ Software** \\ *AppKey1 um.*

</dd> <dt>

<span id="Read_Registry_Virtualization"></span><span id="read_registry_virtualization"></span><span id="READ_REGISTRY_VIRTUALIZATION"></span>Lesen der Registrierungsvirtualisierung
</dt> <dd>

Wenn der Aufrufer aus einem virtualisierten Schlüssel liest, zeigt die Registrierung dem Aufrufer eine zusammengeführte Ansicht der virtualisierten Werte (aus dem virtuellen Speicher) und der nicht virtuellen Werte (aus dem globalen Speicher) an.

Angenommen, **HKEY \_ LOCAL \_ MACHINE \\ Software** \\ *AppKey1* enthält die beiden Werte V1 und V2, und ein eingeschränkter Benutzer schreibt einen Wert V3 in den Schlüssel. Wenn der Benutzer versucht, Werte aus diesem Schlüssel zu lesen, enthält die zusammengeführte Ansicht die Werte V1 und V2 aus dem globalen Speicher und den Wert V3 aus dem virtuellen Speicher.

Beachten Sie, dass virtuelle Werte Vorrang vor globalen Werten haben, wenn sie vorhanden sind. Im obigen Beispiel würde der Wert V3 auch dann an den Aufrufer aus dem virtuellen Speicher zurückgegeben, wenn der globale Speicher den Wert V3 unter diesem Schlüssel hätte. Wenn V3 aus dem virtuellen Speicher gelöscht werden würde, würde V3 aus dem globalen Speicher zurückgegeben. Anders ausgedrückt: Wenn V3 aus **den HKEY \_ USERS-Klassen \\ <User SID> \_ \\ VirtualStore Machine \\ \\ Software** AppKey1 gelöscht werden würde, \\  **aber HKEY LOCAL MACHINE \_ \_ \\ Software** \\ *AppKey1* den Wert V3 auftrat, würde dieser Wert aus dem globalen Speicher zurückgegeben.

</dd> </dl>

## <a name="registry-virtualization-scope"></a>Registrierungsvirtualisierungsbereich

Die Registrierungsvirtualisierung ist nur für Folgendes aktiviert:

-   Interaktive 32-Bit-Prozesse.
-   Schlüssel in **HKEY \_ LOCAL MACHINE \_ \\ Software**.
-   Schlüssel, in die ein Administrator schreiben kann. (Wenn ein Administrator nicht in einen Schlüssel schreiben kann, wäre die Anwendung in früheren Versionen von Windows fehlgeschlagen, selbst wenn sie von einem Administrator ausgeführt wurde.)

Die Registrierungsvirtualisierung ist für Folgendes deaktiviert:

-   64-Bit-Prozesse.
-   Prozesse, die nicht interaktiv sind, z. B. Dienste.

    Beachten Sie, dass die Registrierung als Mechanismus für die prozessübergreifende Kommunikation (Inter-Process Communication, IPC) zwischen einem Dienst (oder einem anderen Prozess, für den keine Virtualisierung aktiviert ist) und einer Anwendung nicht ordnungsgemäß funktioniert, wenn der Schlüssel virtualisiert wird. Wenn beispielsweise ein Antivirendienst seine Signaturdateien basierend auf einem von einer Anwendung festgelegten Wert aktualisiert, aktualisiert der Dienst seine Signaturdateien nie, da der Dienst aus dem globalen Speicher liest, die Anwendung jedoch in den virtuellen Speicher schreibt.

-   Prozesse, die die Identität eines Benutzers angenommen haben. Wenn ein Prozess beim Identitätswechsel eines Benutzers einen Vorgang versucht, wird dieser Vorgang nicht virtualisiert.
-   Kernelmodusprozesse wie Treiber.
-   Prozesse, die **requestedExecutionLevel** in ihren Manifesten angegeben haben.
-   Schlüssel und Unterschlüssel der **HKEY \_ LOCAL \_ \\ MACHINE-Softwareklassen, \\** **HKEY \_ LOCAL MACHINE Software \_ Microsoft \\ \\ \\ Windows** und **HKEY LOCAL MACHINE Software \_ Microsoft Windows \_ \\ \\ \\ NT**.

## <a name="controlling-registry-virtualization"></a>Steuern der Registrierungsvirtualisierung

Zusätzlich zur Steuerung der Virtualisierung auf Anwendungsebene mit **requestedExecutionLevel** im Manifest kann ein Administrator die Virtualisierung für Schlüssel in HKEY LOCAL MACHINE Software pro Schlüssel aktivieren oder **\_ \_ \\ deaktivieren.** Verwenden Sie hierzu die Option Reg.exe-Befehlszeilen-Hilfsprogramm FLAGS mit den in der folgenden Tabelle aufgeführten Flags.



| Flag                         | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| REG \_ KEY \_ DONT \_ SILENT \_ FAIL | Dieses Flag deaktiviert die Virtualisierung der offenen Registrierung. Wenn dieses Flag festgelegt ist und bei einem geöffneten Vorgang für einen Schlüssel mit aktivierter Virtualisierung ein Fehler auftritt, versucht die Registrierung nicht, den Schlüssel erneut zu öffnen. Wenn dieses Flag eindeutig ist, versucht die Registrierung, den Schlüssel mit DEM MAXIMAL ZULÄSSIGen Zugriff anstelle des angeforderten \_ Zugriffs erneut zu öffnen.                                                                   |
| REG \_ KEY \_ DONT \_ VIRTUALIZE   | Dieses Flag deaktiviert die Schreibregistrierungsvirtualisierung. Wenn dieses Flag festgelegt ist und ein Vorgang zum Erstellen eines Schlüssels oder eines festgelegten Werts fehlschlägt, weil der Aufrufer nicht über ausreichende Zugriffsrechte für den übergeordneten Schlüssel verfügt, schlägt die Registrierung mit dem Vorgang fehl. Wenn dieses Flag eindeutig ist, versucht die Registrierung, den Schlüssel oder Wert in den virtuellen Speicher zu schreiben. Der Aufrufer muss über das Schlüsselleserecht \_ für den übergeordneten Schlüssel verfügen. |
| REG \_ KEY \_ RECURSE-FLAG \_      | Wenn dieses Flag festgelegt ist, werden Registrierungsvirtualisierungsflags vom übergeordneten Schlüssel propagiert. Wenn dieses Flag eindeutig ist, werden Registrierungsvirtualisierungsflags nicht propagiert. Das Ändern dieses Flags wirkt sich nur auf neue nach der Änderung des Flags erstellte nachabsteigende Schlüssel aus. Diese Flags werden für vorhandene absteigende Schlüssel nicht festgelegt oder wieder löschen.                                                                  |



 

Im folgenden Beispiel wird die Verwendung des Befehlszeilenprogramms Reg.exe flags mit der FLAGS-Option zum Abfragen des Zustands der Virtualisierungsflags für einen Schlüssel veranschaulicht.

``` syntax
C:\>reg flags HKLM\Software\AppKey1 QUERY

HKEY_LOCAL_MACHINE\Software\AppKey1

        REG_KEY_DONT_VIRTUALIZE: CLEAR
        REG_KEY_DONT_SILENT_FAIL: CLEAR
        REG_KEY_RECURSE_FLAG: CLEAR

The operation completed successfully.
```

Wenn die Überwachung für einen Schlüssel aktiviert wird, der virtualisiert wird, wird ein neues Virtualisierungsüberwachungsereignis generiert, um anzugeben, dass der Schlüssel virtualisiert wird (zusätzlich zu den üblichen Überwachungsereignissen). Administratoren können diese Informationen verwenden, um den Status der Virtualisierung auf ihren Systemen zu überwachen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erste Schritte mit Benutzerkontensteuerung](/previous-versions/windows/it-pro/windows-vista/cc507861(v=technet.10))
</dt> <dt>

[Grundlegendes zur Benutzerkontensteuerung und -konfiguration](/previous-versions/windows/it-pro/windows-vista/cc709628(v=ws.10))
</dt> <dt>

[Bewährte Methoden und Richtlinien für Entwickler für Anwendungen in einer Umgebung mit geringsten Berechtigungen](/previous-versions/dotnet/articles/aa480150(v=msdn.10))
</dt> </dl>

 

 
