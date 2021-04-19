---
description: Beschreibt, wie Sie mit dem Microsoft Error Lookup-Tool Texterklärungen von hexadezimalen Fehlercodes in Windows finden.
title: Das Microsoft-Tool zur Fehlersuche
ms.topic: article
ms.date: 12/4/2019
ms.openlocfilehash: e39b5623458fc176f5ecc81eae71212ba279945c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342985"
---
# <a name="the-microsoft-error-lookup-tool"></a>Das Microsoft-Tool zur Fehlersuche

Das Microsoft-Tool für die Fehlersuche zeigt den Meldungs Text an, der einem hexadezimalen Statuscode (oder anderem Code) zugeordnet ist. Dieser Text wird in verschiedenen Microsoft-Quell Code Headern definiert, wie z. b. "Winerror. h", "Setupapi. h" usw.

Das Tool wird von Microsoft digital signiert. Im folgenden finden Sie die SHA256-Informationen zum Herunterladen von Dateien:  

|Algorithmus |Hash |
| --- | --- |
|SHA256 |88739ec82ba16a0b4a3c83c1dd2f ca6336ad8e2a1e5b1238c085b1e86ab8834a |

> [!NOTE]
> Geschäftsumgebungen können einschränken, welche Dateien ausgeführt werden können und von wo aus. Bevor Sie dieses Tool herunterladen und ausführen, überprüfen Sie die folgenden Details:
> - Müssen Sie über eine Berechtigung oder eine Sicherheits Ausnahme verfügen, damit das Tool heruntergeladen oder ausgeführt werden kann?
> - Können Sie dieses Tool auf Ihrem Computer speichern und ausführen (z. b. im Ordner "Dokumente")? Oder müssen Sie das Tool auf einem spezialisierten Computer, z. b. einem zentralen Dateiserver, speichern und ausführen?

## <a name="usage"></a>Verbrauch

1. Wählen Sie [diesen Link](https://download.microsoft.com/download/4/3/2/432140e8-fb6c-4145-8192-25242838c542/Err_6.4.5/Err_6.4.5.exe)aus, um das Tool herunterzuladen.
1. Wenn Sie in Schritt 1 keinen Speicherort angegeben haben, navigieren Sie zu Ihrem Downloadordner, und kopieren oder verschieben Sie die heruntergeladene Datei (Err_6.4.5.exe) in den Ordner, in dem Sie das Tool speichern. Sie müssen die Datei nicht erweitern oder installieren.
   > [!NOTE]
   > Wenn Sie die Datei in einen Ordner kopieren oder verschieben, der in der **path** -Umgebungsvariable Ihres Betriebssystems aufgeführt ist, funktioniert Sie an jeder Eingabeaufforderung.

1. Öffnen Sie ein Eingabeaufforderungsfenster. Ändern Sie ggf. das Verzeichnis in den Speicherort des Tools für die Fehlersuche.
1. Führen Sie den folgenden Befehl aus:
   ```cmd
   Err_6.4.5.exe <error code>
   ```
   > [!NOTE]  
   > In diesem Befehl \<*error code*> stellt den Hexadezimal Code dar, den Sie suchen möchten.

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

Beachten Sie, dass es sich hierbei um ein "Point-in-Time"-Tool handelt. Das Microsoft Error Lookup-Tool decodiert die meisten Microsoft-Fehlercodes ab dem Zeitpunkt, an dem das Tool kompiliert wurde. Wenn neue Versionen von Windows neue Ereignis-und Fehlercodes hinzufügen, müssen Sie möglicherweise eine neue Version des Tools für die Fehlersuche herunterladen. Überprüfen Sie das Microsoft Download Center auf eine neue Version, oder sehen Sie sich die [Fehler Codes](system-error-codes.md)an.
