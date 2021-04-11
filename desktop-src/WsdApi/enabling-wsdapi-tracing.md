---
description: WSDAPI-Protokolle enthalten Debuginformationen, die verwendet werden können, um die Grundursache von WSDAPI-Anwendungsfehlern zu finden.
ms.assetid: 28b4c032-1c9a-4b3a-9a6a-2948456572b2
title: Aktivieren der WSDAPI-Ablauf Verfolgung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 951f8ddfee6043cc662a456c70960e78ed1a3625
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042052"
---
# <a name="enabling-wsdapi-tracing"></a>Aktivieren der WSDAPI-Ablauf Verfolgung

WSDAPI-Protokolle enthalten Debuginformationen, die verwendet werden können, um die Grundursache von WSDAPI-Anwendungsfehlern zu finden. Wenn die Ablauf Verfolgung aktiviert ist, werden die Protokollierungs Informationen in einer ETL-Datei an einem vom Benutzer angegebenen Speicherort gespeichert. Diese ETL-Datei kann zur Fehlerursachen Analyse an den Microsoft-Entwickler Support gesendet werden. Weitere Informationen zum Kontaktieren des Supports finden Sie unter [https://support.microsoft.com](https://support.microsoft.com) .

Diese Prozedur muss zweimal ausgeführt werden: einmal auf dem Client und einmal auf dem Host.

**So aktivieren Sie die WSDAPI-Ablauf Verfolgung**

1.  Erstellen Sie mit Notepad oder einem anderen Text-Editor eine Textdatei mit folgendem Text:

    ``` syntax
    "{480217a9-f824-4bd4-bbe8-f371caaf9a0d}" 0xFF 0xFF
    "{649e3596-2620-4d58-a01f-17aefe8185db}" 0xFF 0xFF
    "{96ab095a-9519-4f5c-81ee-c510b0a45463}" 0xFF 0xFF
    "{f9be9c98-10db-4318-bb61-cb0ddea08bf7}" 0xFF 0xFF
    "{db1d0418-105a-4c77-9a25-8f96a19716a4}" 0xFF 0xFF
    "{7e2dbfc7-41e8-4987-bca7-76cadfad765f}" 0xFF 0xFF
    "{8b20d3e4-581f-4a27-8109-df01643a7a93}" 0xFF 0xFF
    "{6d04bf88-60a5-4d02-bc5c-94a20ba490ec}" 0xFF 0xFF
    "{75454210-b231-4fea-b2b4-2cc66d7ae8aa}" 0xFF 0xFF
    "{e176aa66-5cc8-4321-9624-f9c1d2b7bf06}" 0xFF 0xFF
    "{836767a6-af31-4938-b4c0-ef86749a9aef}" 0xFF 0xFF
    ```

2.  Speichern Sie die Textdatei unter, `C:\temp\traceguids.txt` und schließen Sie dann die Datei.
3.  Öffnen Sie ein Eingabeaufforderungsfenster mit erhöhten Rechten.
4.  Führen Sie den folgenden Befehl aus: **logman.exe Create Trace wsdlog-o c: \\ Temp \\ WSD**
5.  Führen Sie den folgenden Befehl aus: **logman.exe Update wsdlog-PF c: \\ Temp \\traceguids.txt**
6.  Führen Sie den folgenden Befehl aus: **logman.exe wsdlog starten** .
7.  Reproduzieren Sie den Fehler Durchstarten des Hosts und Clients oder durch Drücken von F5 im Netzwerk-Explorer.

**So deaktivieren Sie die WSDAPI-Ablauf Verfolgung**

1.  Öffnen Sie ein Eingabeaufforderungsfenster mit erhöhten Rechten.
2.  Führen Sie den folgenden Befehl aus: **logman.exe "wsdlog Abbrechen** ".

Nachdem der Anwendungsfehler aufgezeichnet wurde, können die \* ETL-Dateien an den Microsoft-Support gesendet werden. Diese Dateien befinden sich in `C:\temp\wsd_*.etl` .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WSDAPI-Diagnose Prozeduren](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Ersten Schritte mit der WSDAPI-Problembehandlung](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[https://support.microsoft.com](https://support.microsoft.com)
</dt> </dl>

 

 



