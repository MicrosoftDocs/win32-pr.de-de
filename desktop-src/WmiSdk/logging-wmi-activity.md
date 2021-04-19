---
description: Die WMI-Protokolldateien werden nicht mehr unterstützt.
ms.assetid: 4ba80063-7aa6-42df-a620-1b366b795034
ms.tgt_platform: multiple
title: Protokollieren der WMI-Aktivität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6ced8645eb7ad9005e6ba751d011ae7f0ccb3dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348126"
---
# <a name="logging-wmi-activity"></a>Protokollieren der WMI-Aktivität

Die WMI-Protokolldateien werden nicht mehr unterstützt. Ab Windows Vista verwendet WMI die [Ereignis Ablauf Verfolgung für Windows (Event Tracing for Windows, etw](/windows/desktop/ETW/event-tracing-portal)) und Ereignisse, die über die **Ereignisanzeige** -Benutzeroberfläche oder das Befehlszeilen Tool wevtutil verfügbar sind. Weitere Informationen finden Sie unter der ETW-Anbieter und in der Befehlszeilen Dokumentation von [wevutil](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc732848(v=ws.11)) .

In diesem Thema werden die folgenden Abschnitte erläutert:

-   [WMI-Protokolldateien vor Windows Vista](#wmi-log-files-before-windows-vista)
-   [Protokollieren von Aktivitäten für WMI-Kernkomponenten vor Windows Vista](#logging-activities-for-wmi-core-components-before-windows-vista)
-   [Protokollieren von Aktivitäten für WMI-Anbieter Komponenten vor Windows Vista](#logging-activities-for-wmi-provider-components-before-windows-vista)
-   [Zugehörige Themen](#related-topics)

## <a name="wmi-log-files-before-windows-vista"></a>WMI-Protokolldateien vor Windows Vista

Die von WMI und verschiedenen Anbietern erstellten Protokolldateien zeichnen auf: Ereignisse, Ablauf Verfolgungs-oder Diagnosedaten, Fehler und verschiedene Aktivitäten. Nur Administratoren verfügen über Lesezugriff auf den WMI-Protokoll Ordner unter% windir% \\ system32 \\ WBEM \\ Logs.

Nur WMI-Kernkomponenten oder WMI-Anbieter schreiben in Protokolldateien. Sie können die Daten in diesen Protokollen nur zu Diagnose Zwecken lesen oder anzeigen. Sie können eigene Protokolldateien im WMI-Protokoll Verzeichnis erstellen und speichern.

## <a name="logging-activities-for-wmi-core-components-before-windows-vista"></a>Protokollieren von Aktivitäten für WMI-Kernkomponenten vor Windows Vista

Diese Dateien enthalten kein konsistentes Format, das zum programmgesteuerten Lesen geeignet ist. Weitere Informationen zu bestimmten Protokollen finden Sie unter [WMI-Protokolldateien](wmi-log-files.md).

Protokollierungs Aktivitäten für WMI-Kernkomponenten treten auf, wenn die folgenden Registrierungsschlüssel festgelegt sind:

-   Protokolliergrad

    Änderungen am Registrierungs Wert der Protokollierungsebene treten sofort in Kraft. Der WMI-Dienst muss nicht neu gestartet werden.

    **HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **Logging** = 2

    In der folgenden Liste sind die Protokolliergrade aufgelistet, die in der Registrierung definiert werden können.

    

    | Protokolliergrad | BESCHREIBUNG               |
    |---------------|---------------------------|
    | 0             | Keine Protokollierung                |
    | 1             | Nur Fehler protokollieren           |
    | 2             | Ausführliche Protokollierung (Standard) |

    

     

-   Speicherort der Protokolldatei

    Damit Änderungen am Speicherort der Protokolldatei wirksam werden, starten Sie den WMI-Dienst neu.

    **HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **Logging Directory** =% windir% \\ system32 \\ WBEM \\ Logs

-   Maximale Protokolldatei Größe in Bytes

    **HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM**- \\ **Protokolldatei maximale Größe** = 65536

Sie können diese Registrierungsschlüssel Werte über den Registrierungs-Editor oder über das WMI-Snap-in für die Microsoft Management Console ändern.

**So legen Sie den Protokolliergrad für WMI vor Windows Vista fest**

1.  Klicken Sie im **Startmenü** auf **Ausführen**.
2.  Geben Sie **Wmimgmt. msc ein.**
3.  Klicken Sie im Menü **Aktion** auf **Eigenschaften**.
4.  Legen Sie auf der Registerkarte **Protokollierung** den Protokolliergrad auf **deaktiviert**, **aktiviert** **oder ausführlich** fest.
5.  Geben Sie unter **Speicherort:** den Pfad zum Protokolldatei Ordner und in **Maximale Größe (Bytes)** ein, und legen Sie die maximale Größe (in Bytes) der Protokolldatei fest.

Weitere Informationen zum Festlegen der Eigenschaften der Protokolldatei finden Sie in der Online Hilfe für die WMI-Steuerungsanwendung.

## <a name="logging-activities-for-wmi-provider-components-before-windows-vista"></a>Protokollieren von Aktivitäten für WMI-Anbieter Komponenten vor Windows Vista

Wenn die Protokollierung für WMI-Kernkomponenten aktiviert ist, wird die Protokollierung auch für jeden Anbieter mit Protokollierungsfunktionen aktiviert.

In der folgenden Liste sind die erforderlichen Werte aufgeführt.

<dl> <dt>

<span id="File"></span><span id="file"></span><span id="FILE"></span>**Datei**
</dt> <dd>

Vollständiger Pfad und Dateiname der Protokolldatei. Der Standardwert ist% windir% \\ system32 \\ WBEM \\ Logs. Der **Typ** mit dem Namen value muss auf = File festgelegt werden, damit dieser benannte Wert verwendet werden soll.

</dd> <dt>

<span id="Level"></span><span id="level"></span><span id="LEVEL"></span>**Geringen**
</dt> <dd>

Eine logische 32-Bit-Maske, die den Typ der Debugausgabe definiert, die vom Anbieter generiert wurde. Dieser Wert ist vom Anbieter abhängig. Der Standardwert ist 0 (null).

</dd> <dt>

<span id="MaxFileSize"></span><span id="maxfilesize"></span><span id="MAXFILESIZE"></span>**MaxFileSize**
</dt> <dd>

Maximale Dateigröße (in Bytes) der Protokolldatei. Dieser ganzzahlige Wert muss zwischen 1024 und 2 ^ 32-1 liegen. Wenn die Dateigröße diesen Wert überschreitet, wird die Datei in **~ filename** umbenannt, und eine neue, leere Protokolldatei wird erstellt. Der erforderliche Speicherplatz für die Protokolldatei ist zweimal der Wert von **MaxFileSize**. Der Standardwert ist 65.535.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Sorte**
</dt> <dd>

Kann auf = File oder = Debugger festgelegt werden. Wenn auf = File festgelegt, werden die Ablauf Verfolgungs Informationen in die Protokolldatei geschrieben, die in der **Datei** mit dem Namen value angegeben ist. Der Standardwert ist = File.

</dd> </dl>

Verwenden Sie z. b. die folgenden Registrierungsschlüssel Werte, um Abfragen zu protokollieren und Instanzaufrufe vom Ansichts Anbieter zu erhalten. Das Protokoll befindet sich im Protokoll Ordner und ist die Standarddatei Größe.

**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM**- \\ **Anbieter** \\ **Protokollieren** \\ **viewprovider**- \\ **Datei** = C: \\ Windows \\ system32 \\ WBEM \\ Logs \\ viewprovider. log

**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM**- \\ **Anbieter** \\ **Protokollieren** \\ **viewprovider**- \\ **Ebene** = 2

**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM**- \\ **Anbieter** \\ **Protokollieren** \\ **viewprovider** \\ **MaxFileSize** = 65535

**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM**- \\ **Anbieter** \\ **Protokollieren** \\ **viewprovider** \\ **Type** = file

> [!Note]  
> Für Ihre eigenen Anbieter mit Protokollierungsfunktionen müssen Sie die erforderlichen Registrierungsschlüssel und-Werte schreiben, um die Protokollierung zu aktivieren.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Problembehandlung](wmi-troubleshooting.md)
</dt> <dt>

[WMI-Protokolldateien](wmi-log-files.md)
</dt> <dt>

[WMI-Fehler Behebungs Klassen](wmi-troubleshooting-classes.md)
</dt> <dt>

[WMI-Ablauf Verfolgung](tracing-wmi-activity.md)
</dt> </dl>

 

 
