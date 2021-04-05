---
description: Glossar der Netzwerkmonitor Begriffe, die mit dem Buchstaben "P" beginnen.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 321398fb-683f-4fb1-b6b7-c7826811cacd
title: P (Netzwerkmonitor)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44a95ed739acb6f4a59cf8c7a7edb760547f6469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041833"
---
# <a name="p-network-monitor"></a>P (Netzwerkmonitor)

<dl> <dt>

<span id="_netmon_packet_gly"></span><span id="_NETMON_PACKET_GLY"></span>**Lohn**
</dt> <dd>

Siehe [*Frame*](f.md).

</dd> <dt>

<span id="_netmon_parser_gly"></span><span id="_NETMON_PARSER_GLY"></span>**Parser**
</dt> <dd>

Eine Komponente, die ein bestimmtes Protokoll in einer verzögerten Erfassung erkennt. Jeder Parser kann ein Protokoll erkennen. Eine Parser-DLL kann jedoch mehrere Parser enthalten. Wird auch als Protokoll Parser bezeichnet.

</dd> <dt>

<span id="_netmon_parser.ini_gly"></span><span id="_NETMON_PARSER.INI_GLY"></span>**parser.ini**
</dt> <dd>

Eine Netzwerkmonitor Initialisierungsdatei, die eine Liste aller installierten Parser enthält. Für jeden Parser gibt es eine Kommentar Zeichenfolge, in der der Parser, der folgende Satz des Parsers und alle dem Parser zugeordneten Hilfedateien beschrieben werden. Die INI-Datei des Parsers wird aktualisiert, wenn Netzwerkmonitor **parserautoinstallinfo** aufruft oder wenn die Parser-DLL " **kreatehandofftable**" aufruft.

</dd> <dt>

<span id="_netmon_perfmon_gly"></span><span id="_NETMON_PERFMON_GLY"></span>**Perfmon**
</dt> <dd>

Ein Software Tool, mit dem Sie Netzwerk leistungsbezogene Variablen anzeigen können, die die Aktivität eines Prozesses identifizieren.

</dd> <dt>

<span id="_netmon_promiscuous_mode_gly"></span><span id="_NETMON_PROMISCUOUS_MODE_GLY"></span>**gemischten-Modus**
</dt> <dd>

Ein Zustand, in dem eine Netzwerkadapter Karte alle Frames kopiert, die über das Netzwerk übergeben werden, unabhängig von der Zieladresse an einen lokalen Puffer. In diesem Modus können Netzwerkmonitor den gesamten Netzwerk Datenverkehr erfassen und anzeigen.

</dd> <dt>

<span id="_netmon_property_gly"></span><span id="_NETMON_PROPERTY_GLY"></span>**Property**
</dt> <dd>

Ein Protokoll Element in einem Parser, das ein Datenfeld in einem Frame beschreibt, der mit diesem Protokoll gesendet wird.

</dd> <dt>

<span id="_netmon_property_database_gly"></span><span id="_NETMON_PROPERTY_DATABASE_GLY"></span>**Eigenschaften Datenbank**
</dt> <dd>

Eine interne Datenbank, die alle Eigenschaften definiert, die von einem bestimmten Protokoll unterstützt werden. Die Eigenschaften Datenbank enthält eine **PropertyInfo** -Struktur für jede Eigenschaft, die der Parser definiert. Netzwerkmonitor verwendet die Informationen in der Datenbank, wenn eine Eigenschafts Definition an eine Instanz der Eigenschaft angefügt wird, und wenn die Eigenschaften Daten formatiert werden, die im Detailbereich der Netzwerkmonitor Benutzeroberfläche angezeigt werden.

</dd> <dt>

<span id="_netmon_protocol_level_gly"></span><span id="_NETMON_PROTOCOL_LEVEL_GLY"></span>**Protokollebene**
</dt> <dd>

Eine logische Gruppierung von Protokoll Eigenschaften.

</dd> </dl>

 

 



