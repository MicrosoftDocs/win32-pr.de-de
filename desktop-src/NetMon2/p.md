---
description: Glossar mit Netzwerkmonitor Begriffen, die mit dem Buchstaben P beginnen.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 321398fb-683f-4fb1-b6b7-c7826811cacd
title: P (Netzwerkmonitor)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0de258a4394ae13ca71a62d90fd9ee9218862ab7845c7300fcfe509a3a286f34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555470"
---
# <a name="p-network-monitor"></a>P (Netzwerkmonitor)

<dl> <dt>

<span id="_netmon_packet_gly"></span><span id="_NETMON_PACKET_GLY"></span>**Paket**
</dt> <dd>

Weitere Informationen [*finden Sie unter Frame*](f.md).

</dd> <dt>

<span id="_netmon_parser_gly"></span><span id="_NETMON_PARSER_GLY"></span>**Parser**
</dt> <dd>

Eine Komponente, die ein bestimmtes Protokoll in einer verzögerten Erfassung erkennt. Jeder Parser kann ein Protokoll erkennen. Eine Parser-DLL kann jedoch mehrere Parser enthalten. Wird auch als Protokollparser bezeichnet.

</dd> <dt>

<span id="_netmon_parser.ini_gly"></span><span id="_NETMON_PARSER.INI_GLY"></span>**parser.ini**
</dt> <dd>

Eine Netzwerkmonitor Initialisierungsdatei, die eine Liste aller installierten Parser enthält. Für jeden Parser gibt es eine Kommentarzeichenfolge, die den Parser, den folgenden Satz des Parsers und alle dem Parser zugeordneten Hilfedateien beschreibt. Die PARSER-INI-Datei wird aktualisiert, wenn Netzwerkmonitor **ParserAutoInstallInfo** aufruft oder wenn die Parser-DLL **CreateHandoffTable aufruft.**

</dd> <dt>

<span id="_netmon_perfmon_gly"></span><span id="_NETMON_PERFMON_GLY"></span>**Perfmon**
</dt> <dd>

Ein Softwaretool, mit dem Sie leistungsbezogene Variablen für das Netzwerk anzeigen können, die die Aktivität eines Prozesses identifizieren.

</dd> <dt>

<span id="_netmon_promiscuous_mode_gly"></span><span id="_NETMON_PROMISCUOUS_MODE_GLY"></span>**Promiscuous-Modus**
</dt> <dd>

Ein Zustand, in dem eine Netzwerkadapterkarte alle Frames kopiert, die über das Netzwerk übergeben werden, unabhängig von der Zieladresse in einen lokalen Puffer. In diesem Modus können Netzwerkmonitor Netzwerkdatenverkehr erfassen und anzeigen.

</dd> <dt>

<span id="_netmon_property_gly"></span><span id="_NETMON_PROPERTY_GLY"></span>**Eigenschaft**
</dt> <dd>

Ein Protokollelement in einem Parser, das ein Datenfeld innerhalb eines Frames beschreibt, das mit diesem Protokoll gesendet wird.

</dd> <dt>

<span id="_netmon_property_database_gly"></span><span id="_NETMON_PROPERTY_DATABASE_GLY"></span>**Eigenschaftendatenbank**
</dt> <dd>

Eine interne Datenbank, die alle Eigenschaften definiert, die von einem bestimmten Protokoll unterstützt werden. Die Eigenschaftendatenbank enthält eine **PROPERTYINFO-Struktur** für jede Eigenschaft, die der Parser definiert. Netzwerkmonitor verwendet die Informationen in der Datenbank, wenn eine Eigenschaftendefinition an eine Instanz der -Eigenschaft angefügt wird, und wenn die Eigenschaftsdaten formatiert werden, die im Detailbereich der benutzeroberfläche Netzwerkmonitor werden.

</dd> <dt>

<span id="_netmon_protocol_level_gly"></span><span id="_NETMON_PROTOCOL_LEVEL_GLY"></span>**Protokollebene**
</dt> <dd>

Eine logische Gruppierung von Protokolleigenschaften.

</dd> </dl>

 

 



