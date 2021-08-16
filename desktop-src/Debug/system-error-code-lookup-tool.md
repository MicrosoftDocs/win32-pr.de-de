---
description: Beschreibt die Verwendung des Microsoft-Fehlersuchetools, um Texterklärungen von Hexadezimalfehlercodes in Windows zu finden.
title: Das Microsoft-Fehlersuchtool
ms.topic: article
ms.date: 12/4/2019
ms.openlocfilehash: 534b2af92b8dc0e906bd033e8ce1f0fbd08ead0cda21406d1818a318356db613
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118405890"
---
# <a name="the-microsoft-error-lookup-tool"></a>Das Microsoft-Fehlersuchtool

Das Microsoft-Fehlersuchetool zeigt den Meldungstext an, der einem Hexadezimalstatuscode (oder einem anderen Code) zugeordnet ist. Dieser Text wird in verschiedenen Quellcodeheaderdateien von Microsoft definiert, z.B. Winerror.h, Setupapi.h usw.

Das Tool wird digital von Microsoft signiert. Im Folgenden sind die SHA256-Informationen für den Dateidownload enthalten:  

|Algorithmus |Hash |
| --- | --- |
|SHA256 |88739EC82BA16A0B4A3C83C1DD2FCA6336AD8E2A1E5F1238C085B1E86AB8834A |

> [!NOTE]
> Geschäftsumgebungen können einschränken, welche Dateien von wo aus ausgeführt werden können. Überprüfen Sie die folgenden Details, bevor Sie dieses Tool herunterladen und ausführen:
> - Müssen Sie über die Berechtigung oder eine Sicherheitsausnahme verfügen, um das Tool herunterladen oder ausführen zu können?
> - Können Sie dieses Tool auf Ihrem Computer speichern und ausführen (z. B. im Ordner "Dokumente")? Oder müssen Sie das Tool auf einem spezialisierten Computer speichern und ausführen, z. B. auf einem zentralen Dateiserver?

## <a name="usage"></a>Verbrauch

1. Laden Sie das Tool herunter, indem Sie [diesen Link](https://download.microsoft.com/download/4/3/2/432140e8-fb6c-4145-8192-25242838c542/Err_6.4.5/Err_6.4.5.exe)auswählen.
1. Wenn Sie in Schritt 1 keinen Speicherort angegeben haben, wechseln Sie zu Ihrem Downloadordner, und kopieren oder verschieben Sie die heruntergeladene Datei (Err_6.4.5.exe) in den Ordner, in dem Sie das Tool speichern. Sie müssen die Datei nicht erweitern oder installieren.
   > [!NOTE]
   > Wenn Sie die Datei kopieren oder in einen Ordner verschieben, der in der Path-Umgebungsvariable Ihres Betriebssystems aufgeführt ist, funktioniert sie an jeder Eingabeaufforderung. 

1. Öffnen Sie ein Eingabeaufforderungsfenster. Ändern Sie bei Bedarf das Verzeichnis in den Speicherort des Fehlersuchetools.
1. Führen Sie den folgenden Befehl aus:
   ```cmd
   Err_6.4.5.exe <error code>
   ```
   > [!NOTE]  
   > In diesem Befehl \<*error code*> stellt den Hexadezimalcode dar, den Sie suchen möchten.

## <a name="examples"></a>Beispiele

```cmd
C:\Tools>Err_6.4.5.exe c000021a
# for hex 0xc000021a / decimal -1073741286
 STATUS_SYSTEM_PROCESS_TERMINATED                ntstatus.h
# {Fatal System Error}
# The %hs system process terminated unexpectedly with a
# status of 0x%08x (0x%08x 0x%08x).
# The system has been shut down.
# as an HRESULT: Severity: FAILURE (1), FACILITY_NULL (0x0), Code 0x21a
# for hex 0x21a / decimal 538
 ERROR_ABIOS_ERROR                               winerror.h
# An error occurred in the ABIOS subsystem.
# 2 matches found for "c000021a"
```

```cmd
C:\Tools>Err_6.4.5.exe 7b
# for hex 0x7b / decimal 123
 INACCESSIBLE_BOOT_DEVICE                       bugcodes.h
 NMERR_SECURITY_BREACH_CAPTURE_DELETED              netmon.h
 ERROR_INVALID_NAME                       winerror.h
# The filename, directory name, or volume label syntax is
# incorrect.
# as an HRESULT: Severity: SUCCESS (0), FACILITY_NULL (0x0), Code 0x7b
# for hex 0x7b / decimal 123
 ERROR_INVALID_NAME                       winerror.h
# The filename, directory name, or volume label syntax is
# incorrect.
# 4 matches found for "7b"
```

## <a name="more-information"></a>Weitere Informationen

Beachten Sie, dass dies ein "Point-in-Time"-Tool ist. Das Microsoft Error Lookup Tool decodiert die meisten Microsoft-Fehlercodes zum Zeitpunkt der Kompilierung des Tools. Wenn neue Releases von Windows neue Ereignis- und Fehlercodes hinzufügen, müssen Sie möglicherweise eine neue Version des Fehlersuchetools herunterladen. Überprüfen Sie das Microsoft Download Center auf eine neue Version, oder lesen Sie [Fehlercodes.](system-error-codes.md)
