---
description: Ein Übergabesatz gibt die Protokolle an, die einem Protokoll folgen. Der Parser verwendet einen Übergabesatz nur, wenn der Parser das nächste Protokoll aus den Daten in einer Protokollinstanz identifizieren kann.
ms.assetid: d1f44646-98ee-4e3a-a81a-83d6c87c23f4
title: Angeben eines Übergabesatzes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c2f3f7d559c83e3c56bc6ea202b3a0e339dbc1b76d93fc2af1b73f5a2c60c4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778350"
---
# <a name="specifying-a-handoff-set"></a>Angeben eines Übergabesatzes

Ein Übergabesatz gibt die Protokolle an, die einem Protokoll folgen. Der Parser verwendet einen Übergabesatz nur, wenn der Parser das nächste Protokoll aus den Daten in einer Protokollinstanz identifizieren kann.

Das TCP-Protokoll verfügt beispielsweise über eine Porteigenschaft, die das Protokoll identifiziert, das dem TCP-Protokoll folgt. Der Eigenschaftswert 20 gibt an, dass das nächste Protokoll FTP ist. Der Eigenschaftswert 53 gibt an, dass das nächste Protokoll DNS ist. Da die port-Eigenschaft das folgende Protokoll identifiziert, kann der TCP-Parser den folgenden Übergabesatz verwenden, um ein Handle für das Protokoll abzurufen, das von der Porteigenschaft angegeben wird.

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

Übergabesätze werden in der PARSER-INI-Datei gespeichert. Der vorangehende TCP-Übergabesatz befindet sich beispielsweise in tcpip.ini Datei. Beachten Sie Folgendes: Wenn eine Parser-DLL mehrere Protokolle unterstützt, verfügt jeder Parser, der einen Übergabesatz verwendet, über einen eigenen Speicherort in der INI-Datei.

Informationen zum Übergabesatz werden während der Implementierung der [**ParserAutoInstallInfo-Funktion**](parserautoinstallinfo.md) angegeben. Der Parser kann die Protokolle angeben, die dem Parserprotokoll vorangehen, und die Protokolle, die dem Parserprotokoll folgen. Netzwerkmonitor verwendet alle vorherigen Protokolle und fügt das Parserprotokoll den folgenden Abschnitten der PARSER-INI-Datei hinzu – für jedes vorhergehende Protokoll. Netzwerkmonitor speichert die Liste der Protokolle, die im Abschnitt handoff set der Parser-INI-Datei folgen.

Netzwerkmonitor speichert die Informationen zum Übergabesatz in der PARSER-INI-Datei, aber der Parser greift nicht direkt auf die INI-Dateien zu. Um die Informationen im Übergabesatz zu verwenden, ruft der Parser die [**CreateHandoffTable-Funktion**](createhandofftable.md) auf, um eine Übergabetabelle zu erstellen. In der Regel wird die Übergabetabelle erstellt, wenn der Parser das Protokoll registriert. Nachdem das Protokoll registriert wurde, erstellt Netzwerkmonitor eine Übergabesatztabelle, die der Parser verwenden kann.

Der Parser verwendet seinen Übergabesatz beim Erkennen von Daten. Zuerst liest der Parser den Wert der Eigenschaft, die das nächste Protokoll identifiziert. Anschließend ruft der Parser die [**GetProtocolFromTable**](getprotocolfromtable.md) auf, um ein Handle für das nächste Protokoll abzurufen. Schließlich gibt der Parser einen Zeiger auf das Handle im *parameter phNextProtocol* von [**RecognizeFrame**](recognizeframe.md)zurück.

 

 



