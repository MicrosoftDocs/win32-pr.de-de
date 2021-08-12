---
description: Sie können das Logman-Tool verwenden, um Ablaufverfolgungsinformationen für VSS-Anwendungen zu sammeln, die die automatisierte Systemwiederherstellung (Automated System Recovery, ASR) verwenden.
ms.assetid: 872609c8-a123-40a8-96ca-58f34d37f3d8
title: Verwenden von Ablaufverfolgungstools mit ASR-Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e2d22dbb1488b5fd60836926d3c5ef2de5913ff1cc1529fdb278773b2ccd8b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118590869"
---
# <a name="using-tracing-tools-with-asr-applications"></a>Verwenden von Ablaufverfolgungstools mit ASR-Anwendungen

Sie können das Logman-Tool verwenden, um Ablaufverfolgungsinformationen für VSS-Anwendungen zu sammeln, die die automatisierte [Systemwiederherstellung (Automated System Recovery, ASR) verwenden.](using-vss-automated-system-recovery-for-disaster-recovery.md) Logman (logman.exe) ist ein Ablaufverfolgungscontroller für Ablaufverfolgungsereignisse und Leistungsindikatoren. Sie ist in Windows XP und neueren Versionen von Windows. Wenn Sie möchten, können Sie auch das Tracelog-Tool verwenden, um dieselben ASR-Ablaufverfolgungsinformationen zu erfassen. Tracelog ist im Windows Driver Kit (WDK) enthalten.

Informationen zur Verwendung von Ablaufverfolgungstools mit VSS finden Sie unter [Verwenden von Ablaufverfolgungstools mit VSS.](using-tracing-tools-with-vss.md)

## <a name="using-logman"></a>Verwenden von Logman

Im folgenden Verfahren wird beschrieben, wie Sie Logman mit Ihrer ASR-Anwendung verwenden.

**So verwenden Sie Logman mit Ihrer ASR-Anwendung**

1.  Verwenden Sie den folgenden Befehl, um die Ablaufverfolgung zu starten:

    **logman start asr -o** *\\ x:r.etl -ets -p {6407345b-94f2-44c8-b3db-4e076be46816} 0xff 0xff**

    > [!Note]  
    > Ersetzen Sie "x: " durch den Pfad zu dem Verzeichnis, \\ in dem die Ablaufverfolgungsprotokolldatei gespeichert werden soll. Um eine optimale Leistung zu erzielen, sollte sich die Ablaufverfolgungsprotokolldatei auf einem Volume befinden, das nicht Teil der Schattenkopie ist.

     

2.  Verwenden Sie den folgenden Befehl, um die Ablaufverfolgung zu beenden:

    **logman stop asr -ets**

Die Ablaufverfolgungsprotokolldatei ist *x: \\* asr.etl.

Weitere Informationen zum Logman-Tool finden Sie unter [Logman](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc753820(v=ws.11)).

## <a name="using-tracelog"></a>Verwenden von Tracelog

Im folgenden Verfahren wird die Verwendung von Tracelog beschrieben.

**So verwenden Sie Tracelog**

1.  Erstellen Sie eine Textdatei namens asr.ctl, die nur den folgenden Text enthält:

    **6407345b-94f2-44c8-b3db-4e076be46816 asr**

2.  Verwenden Sie den folgenden Befehl, um die Ablaufverfolgung zu starten:

    **tracelog -start asr -f** *x: \\ ".asr.etl -guid asr.ctl -flag 0xff -level 0xff**

    > [!Note]  
    > Ersetzen Sie "x: " durch den Pfad zu dem Verzeichnis, \\ in dem die Ablaufverfolgungsprotokolldatei gespeichert werden soll. Um eine optimale Leistung zu erzielen, sollte sich die Ablaufverfolgungsprotokolldatei auf einem Volume befinden, das nicht Teil der Schattenkopie ist.

     

3.  Verwenden Sie den folgenden Befehl, um die Ablaufverfolgung zu beenden:

    **tracelog -stop asr**

Die Ablaufverfolgungsprotokolldatei ist *x: \\* asr.etl.

Weitere Informationen zum Tracelog-Tool finden Sie unter [Tracelog](https://msdn.microsoft.com/library/ms797927.aspx).

 

 
