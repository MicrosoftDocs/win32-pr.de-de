---
description: Ein Übergabe-Satz gibt die Protokolle an, die einem Protokoll folgen. Der Parser verwendet einen Handzettel Satz nur dann, wenn der Parser das nächste Protokoll aus den Daten in einer Protokoll Instanz identifizieren kann.
ms.assetid: d1f44646-98ee-4e3a-a81a-83d6c87c23f4
title: Angeben einer Übergabe Gruppe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9acb421963bea3ffaa70b6165c6ffceee138e38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356813"
---
# <a name="specifying-a-handoff-set"></a>Angeben einer Übergabe Gruppe

Ein Übergabe-Satz gibt die Protokolle an, die einem Protokoll folgen. Der Parser verwendet einen Handzettel Satz nur dann, wenn der Parser das nächste Protokoll aus den Daten in einer Protokoll Instanz identifizieren kann.

Das TCP-Protokoll verfügt beispielsweise über eine Port-Eigenschaft, die das Protokoll identifiziert, das dem TCP-Protokoll folgt. Der-Eigenschafts Wert 20 gibt an, dass das nächste Protokoll FTP ist. Der-Eigenschafts Wert 53 gibt an, dass das nächste Protokoll DNS ist. Da die Port-Eigenschaft das folgende Protokoll identifiziert, kann der TCP-Parser den folgenden Übergabe-Satz verwenden, um ein Handle für das Protokoll zu erhalten, das die Port-Eigenschaft angibt.

``` syntax
[TCP_HandoffSet]
  20    = FTP
  21    = FTP
  23    = TELNET
  25    = SMTP
  53    = DNS
  79    = FINGER
  80    = HTTP
  102   = ISO
  111   = RPC
  119   = NNTP
  137   = NBT, 1000
  138   = NBT, 1002
  139   = NBT, 1001
  389   = LDAP
  445   = NBT, 1001
  515   = LPR
  612   = HMMP
  613   = HMMP
  1024  = NBT, 1001
  1047  = NBT, 1001
  1362  = TDS
  1433  = TDS
  1723  = PPTP
  3020  = NBT, 1001
  3268  = LDAP
  5678  = PPTP
```

Übergabe Sätze werden in der INI-Datei des Parsers gespeichert. Beispielsweise befindet sich die vorherige TCP-handsegruppe in tcpip.ini Datei. Beachten Sie Folgendes: Wenn eine Parser-DLL mehrere Protokolle unterstützt, hat jeder Parser, der einen Handzettel Satz verwendet, seinen eigenen Speicherort in der INI-Datei.

Handoff-Set-Informationen werden während der Implementierung der Funktion " [**parameterautoinstallinfo**](parserautoinstallinfo.md) " angegeben. Der Parser kann die Protokolle angeben, die dem Parser-Protokoll vorangestellt sind, und die Protokolle, die dem Parser-Protokoll folgen. Netzwerkmonitor nimmt alle Protokolle vor, die vorangestellt sind, und fügt das parserprotokoll den folgenden Set-Abschnitten der parserini-Datei – für jedes vorherige Protokoll hinzu. Netzwerkmonitor speichert die Liste der Protokolle, die im Abschnitt Übergabe Satz der parserini-Datei befolgt werden.

In Netzwerkmonitor werden die Informationen zum handseset in der INI-Datei des Parsers gespeichert, aber der Parser greift nicht direkt auf die INI-Dateien zu. Um die Informationen im Übergabe-Satz zu verwenden, [**ruft der Parser die Funktion "**](createhandofftable.md) -Funktion" auf, um eine Übergabe-Tabelle zu erstellen. In der Regel wird die Übergabe Tabelle erstellt, wenn der Parser das Protokoll registriert. Nachdem das Protokoll registriert wurde, erstellt Netzwerkmonitor eine Übergabe-Tabelle, die vom Parser verwendet werden kann.

Der Parser verwendet seine Übergabe-Menge, wenn Daten erkannt werden. Zuerst liest der Parser den Wert der-Eigenschaft, die das nächste Protokoll identifiziert. Dann ruft der Parser den [**getprotocolfromtable**](getprotocolfromtable.md) auf, um ein Handle für das nächste Protokoll zu erhalten. Zuletzt gibt der Parser einen Zeiger auf das Handle im Parameter " *phnextprotocol* " von " [**erkenzeframe**](recognizeframe.md)" zurück.

 

 



