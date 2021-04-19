---
description: Sie können das Logman-Tool verwenden, um Ablauf Verfolgungs Informationen für VSS-Anwendungen zu sammeln, die automatisierte System Wiederherstellung (ASR) verwenden.
ms.assetid: 872609c8-a123-40a8-96ca-58f34d37f3d8
title: Verwenden von Ablauf Verfolgungs Tools mit ASR-Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c13eee1c62cd6636eebe5bcfd35bd5abb119645
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356770"
---
# <a name="using-tracing-tools-with-asr-applications"></a>Verwenden von Ablauf Verfolgungs Tools mit ASR-Anwendungen

Sie können das Logman-Tool verwenden, um Ablauf Verfolgungs Informationen für VSS-Anwendungen zu sammeln, die [automatisierte System Wiederherstellung (ASR)](using-vss-automated-system-recovery-for-disaster-recovery.md)verwenden. Logman (logman.exe) ist ein Ablauf Verfolgungs Controller für Ablauf Verfolgungs Ereignisse und Leistungsindikatoren. Es ist in Windows XP und höheren Versionen von Windows enthalten. Oder Sie können, wenn Sie möchten, das tracelog-Tool verwenden, um die gleichen ASR-Ablauf Verfolgungs Informationen zu sammeln. TraceLog ist im Windows-Treiberkit (WDK) enthalten.

Informationen zur Verwendung von Ablauf Verfolgungs Tools mit VSS finden Sie unter [Verwenden von Ablauf Verfolgungs Tools mit VSS](using-tracing-tools-with-vss.md).

## <a name="using-logman"></a>Verwenden von logman

Im folgenden Verfahren wird beschrieben, wie Sie Logman mit der ASR-Anwendung verwenden.

**So verwenden Sie Logman mit der ASR-Anwendung**

1.  Verwenden Sie den folgenden Befehl zum Starten der Ablauf Verfolgung:

    **logman Start ASR-o** *x: \\ * * * ASR. ETL-ETS-p {6407345b-94f 2-44c8-b3db-4e076be46816} 0xFF 0xFF**

    > [!Note]  
    > Ersetzen Sie "x: \\ " durch den Pfad zu dem Verzeichnis, in dem die Ablauf Verfolgungs Protokolldatei gespeichert werden soll. Für eine optimale Leistung sollte sich die Ablauf Verfolgungs Protokolldatei auf einem Volume befinden, das nicht Teil der Schatten Kopie ist.

     

2.  Verwenden Sie den folgenden Befehl, um die Ablauf Verfolgung anzuhalten:

    **logman beendet ASR-ETS**

Die Ablauf Verfolgungs Protokolldatei ist *x \\ :* ASR. ETL.

Weitere Informationen zum Logman-Tool finden Sie unter [logman](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc753820(v=ws.11)).

## <a name="using-tracelog"></a>Verwenden von tracelog

Im folgenden Verfahren wird die Verwendung von tracelog beschrieben.

**So verwenden Sie tracelog**

1.  Erstellen Sie eine Textdatei mit dem Namen ASR. CTL, die nur den folgenden Text enthält:

    **6407345b-94f 2-44c8-b3db-4e076be46816 ASR**

2.  Verwenden Sie den folgenden Befehl zum Starten der Ablauf Verfolgung:

    **tracelog-Start ASR-f** *x: \\ * * * ASR. ETL-GUID ASR. CTL-Flag 0xFF-Level 0xFF**

    > [!Note]  
    > Ersetzen Sie "x: \\ " durch den Pfad zu dem Verzeichnis, in dem die Ablauf Verfolgungs Protokolldatei gespeichert werden soll. Für eine optimale Leistung sollte sich die Ablauf Verfolgungs Protokolldatei auf einem Volume befinden, das nicht Teil der Schatten Kopie ist.

     

3.  Verwenden Sie den folgenden Befehl, um die Ablauf Verfolgung anzuhalten:

    **tracelog-ASR Abbrechen**

Die Ablauf Verfolgungs Protokolldatei ist *x \\ :* ASR. ETL.

Weitere Informationen zum tracelog-Tool finden Sie unter [tracelog](https://msdn.microsoft.com/library/ms797927.aspx).

 

 
