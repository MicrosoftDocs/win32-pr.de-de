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
# <a name="p-network-monitor"></a><span data-ttu-id="4cd24-103">P (Netzwerkmonitor)</span><span class="sxs-lookup"><span data-stu-id="4cd24-103">P (Network Monitor)</span></span>

<dl> <dt>

<span data-ttu-id="4cd24-104"><span id="_netmon_packet_gly"></span><span id="_NETMON_PACKET_GLY"></span>**Lohn**</span><span class="sxs-lookup"><span data-stu-id="4cd24-104"><span id="_netmon_packet_gly"></span><span id="_NETMON_PACKET_GLY"></span>**packet**</span></span>
</dt> <dd>

<span data-ttu-id="4cd24-105">Siehe [*Frame*](f.md).</span><span class="sxs-lookup"><span data-stu-id="4cd24-105">See [*frame*](f.md).</span></span>

</dd> <dt>

<span data-ttu-id="4cd24-106"><span id="_netmon_parser_gly"></span><span id="_NETMON_PARSER_GLY"></span>**Parser**</span><span class="sxs-lookup"><span data-stu-id="4cd24-106"><span id="_netmon_parser_gly"></span><span id="_NETMON_PARSER_GLY"></span>**parser**</span></span>
</dt> <dd>

<span data-ttu-id="4cd24-107">Eine Komponente, die ein bestimmtes Protokoll in einer verzögerten Erfassung erkennt.</span><span class="sxs-lookup"><span data-stu-id="4cd24-107">A component that detects a specific protocol in a delayed capture.</span></span> <span data-ttu-id="4cd24-108">Jeder Parser kann ein Protokoll erkennen.</span><span class="sxs-lookup"><span data-stu-id="4cd24-108">Each parser can detect one protocol.</span></span> <span data-ttu-id="4cd24-109">Eine Parser-DLL kann jedoch mehrere Parser enthalten.</span><span class="sxs-lookup"><span data-stu-id="4cd24-109">However, one parser DLL may contain multiple parsers.</span></span> <span data-ttu-id="4cd24-110">Wird auch als Protokoll Parser bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="4cd24-110">Also called a protocol parser.</span></span>

</dd> <dt>

<span data-ttu-id="4cd24-111"><span id="_netmon_parser.ini_gly"></span><span id="_NETMON_PARSER.INI_GLY"></span>**parser.ini**</span><span class="sxs-lookup"><span data-stu-id="4cd24-111"><span id="_netmon_parser.ini_gly"></span><span id="_NETMON_PARSER.INI_GLY"></span>**parser.ini**</span></span>
</dt> <dd>

<span data-ttu-id="4cd24-112">Eine Netzwerkmonitor Initialisierungsdatei, die eine Liste aller installierten Parser enthält.</span><span class="sxs-lookup"><span data-stu-id="4cd24-112">A Network Monitor initialization file that contains a list of all the installed parsers.</span></span> <span data-ttu-id="4cd24-113">Für jeden Parser gibt es eine Kommentar Zeichenfolge, in der der Parser, der folgende Satz des Parsers und alle dem Parser zugeordneten Hilfedateien beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="4cd24-113">For each parser there is a comment string that describes the parser, the follow set of the parser, and any Help file associated with the parser.</span></span> <span data-ttu-id="4cd24-114">Die INI-Datei des Parsers wird aktualisiert, wenn Netzwerkmonitor **parserautoinstallinfo** aufruft oder wenn die Parser-DLL " **kreatehandofftable**" aufruft.</span><span class="sxs-lookup"><span data-stu-id="4cd24-114">The parser INI file is updated when Network Monitor calls **ParserAutoInstallInfo**, or when the parser DLL calls **CreateHandoffTable**.</span></span>

</dd> <dt>

<span data-ttu-id="4cd24-115"><span id="_netmon_perfmon_gly"></span><span id="_NETMON_PERFMON_GLY"></span>**Perfmon**</span><span class="sxs-lookup"><span data-stu-id="4cd24-115"><span id="_netmon_perfmon_gly"></span><span id="_NETMON_PERFMON_GLY"></span>**Perfmon**</span></span>
</dt> <dd>

<span data-ttu-id="4cd24-116">Ein Software Tool, mit dem Sie Netzwerk leistungsbezogene Variablen anzeigen können, die die Aktivität eines Prozesses identifizieren.</span><span class="sxs-lookup"><span data-stu-id="4cd24-116">A software tool that allows you to view network performance-related variables that identify the activity of a process.</span></span>

</dd> <dt>

<span data-ttu-id="4cd24-117"><span id="_netmon_promiscuous_mode_gly"></span><span id="_NETMON_PROMISCUOUS_MODE_GLY"></span>**gemischten-Modus**</span><span class="sxs-lookup"><span data-stu-id="4cd24-117"><span id="_netmon_promiscuous_mode_gly"></span><span id="_NETMON_PROMISCUOUS_MODE_GLY"></span>**promiscuous mode**</span></span>
</dt> <dd>

<span data-ttu-id="4cd24-118">Ein Zustand, in dem eine Netzwerkadapter Karte alle Frames kopiert, die über das Netzwerk übergeben werden, unabhängig von der Zieladresse an einen lokalen Puffer.</span><span class="sxs-lookup"><span data-stu-id="4cd24-118">A state in which a network adapter card copies all the frames that pass over the network, regardless of the destination address to a local buffer.</span></span> <span data-ttu-id="4cd24-119">In diesem Modus können Netzwerkmonitor den gesamten Netzwerk Datenverkehr erfassen und anzeigen.</span><span class="sxs-lookup"><span data-stu-id="4cd24-119">This mode enables Network Monitor to capture and display all network traffic.</span></span>

</dd> <dt>

<span data-ttu-id="4cd24-120"><span id="_netmon_property_gly"></span><span id="_NETMON_PROPERTY_GLY"></span>**Property**</span><span class="sxs-lookup"><span data-stu-id="4cd24-120"><span id="_netmon_property_gly"></span><span id="_NETMON_PROPERTY_GLY"></span>**property**</span></span>
</dt> <dd>

<span data-ttu-id="4cd24-121">Ein Protokoll Element in einem Parser, das ein Datenfeld in einem Frame beschreibt, der mit diesem Protokoll gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="4cd24-121">A protocol element in a parser that describes a data field within a frame that is sent by using that protocol.</span></span>

</dd> <dt>

<span data-ttu-id="4cd24-122"><span id="_netmon_property_database_gly"></span><span id="_NETMON_PROPERTY_DATABASE_GLY"></span>**Eigenschaften Datenbank**</span><span class="sxs-lookup"><span data-stu-id="4cd24-122"><span id="_netmon_property_database_gly"></span><span id="_NETMON_PROPERTY_DATABASE_GLY"></span>**property database**</span></span>
</dt> <dd>

<span data-ttu-id="4cd24-123">Eine interne Datenbank, die alle Eigenschaften definiert, die von einem bestimmten Protokoll unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="4cd24-123">An internal database that defines all the properties that a specific protocol supports.</span></span> <span data-ttu-id="4cd24-124">Die Eigenschaften Datenbank enthält eine **PropertyInfo** -Struktur für jede Eigenschaft, die der Parser definiert.</span><span class="sxs-lookup"><span data-stu-id="4cd24-124">The property database contains a **PROPERTYINFO** structure for each property that the parser defines.</span></span> <span data-ttu-id="4cd24-125">Netzwerkmonitor verwendet die Informationen in der Datenbank, wenn eine Eigenschafts Definition an eine Instanz der Eigenschaft angefügt wird, und wenn die Eigenschaften Daten formatiert werden, die im Detailbereich der Netzwerkmonitor Benutzeroberfläche angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="4cd24-125">Network Monitor uses the information in the database when it attaches a property definition to an instance of the property, and when it formats the property data that is displayed in the details pane of the Network Monitor UI.</span></span>

</dd> <dt>

<span data-ttu-id="4cd24-126"><span id="_netmon_protocol_level_gly"></span><span id="_NETMON_PROTOCOL_LEVEL_GLY"></span>**Protokollebene**</span><span class="sxs-lookup"><span data-stu-id="4cd24-126"><span id="_netmon_protocol_level_gly"></span><span id="_NETMON_PROTOCOL_LEVEL_GLY"></span>**protocol level**</span></span>
</dt> <dd>

<span data-ttu-id="4cd24-127">Eine logische Gruppierung von Protokoll Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4cd24-127">A logical grouping of protocol properties.</span></span>

</dd> </dl>

 

 



