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
# <a name="specifying-a-handoff-set"></a><span data-ttu-id="533db-104">Angeben einer Übergabe Gruppe</span><span class="sxs-lookup"><span data-stu-id="533db-104">Specifying a Handoff Set</span></span>

<span data-ttu-id="533db-105">Ein Übergabe-Satz gibt die Protokolle an, die einem Protokoll folgen.</span><span class="sxs-lookup"><span data-stu-id="533db-105">A handoff set specifies the protocols that follow a protocol.</span></span> <span data-ttu-id="533db-106">Der Parser verwendet einen Handzettel Satz nur dann, wenn der Parser das nächste Protokoll aus den Daten in einer Protokoll Instanz identifizieren kann.</span><span class="sxs-lookup"><span data-stu-id="533db-106">The parser uses a handoff set only when the parser can identify the next protocol from the data in a protocol instance.</span></span>

<span data-ttu-id="533db-107">Das TCP-Protokoll verfügt beispielsweise über eine Port-Eigenschaft, die das Protokoll identifiziert, das dem TCP-Protokoll folgt.</span><span class="sxs-lookup"><span data-stu-id="533db-107">For example, the TCP protocol has a port property that identifies the protocol that follows the TCP protocol.</span></span> <span data-ttu-id="533db-108">Der-Eigenschafts Wert 20 gibt an, dass das nächste Protokoll FTP ist.</span><span class="sxs-lookup"><span data-stu-id="533db-108">A property value of 20 indicates that the next protocol is FTP.</span></span> <span data-ttu-id="533db-109">Der-Eigenschafts Wert 53 gibt an, dass das nächste Protokoll DNS ist.</span><span class="sxs-lookup"><span data-stu-id="533db-109">A property value of 53 indicates that the next protocol is DNS.</span></span> <span data-ttu-id="533db-110">Da die Port-Eigenschaft das folgende Protokoll identifiziert, kann der TCP-Parser den folgenden Übergabe-Satz verwenden, um ein Handle für das Protokoll zu erhalten, das die Port-Eigenschaft angibt.</span><span class="sxs-lookup"><span data-stu-id="533db-110">Because the port property identifies the protocol that follows, the TCP parser can use the following handoff set to get a handle for the protocol that the port property specifies.</span></span>

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

<span data-ttu-id="533db-111">Übergabe Sätze werden in der INI-Datei des Parsers gespeichert.</span><span class="sxs-lookup"><span data-stu-id="533db-111">Handoff sets are stored in the parser INI file.</span></span> <span data-ttu-id="533db-112">Beispielsweise befindet sich die vorherige TCP-handsegruppe in tcpip.ini Datei.</span><span class="sxs-lookup"><span data-stu-id="533db-112">For example, the preceding TCP handoff set is located in tcpip.ini file.</span></span> <span data-ttu-id="533db-113">Beachten Sie Folgendes: Wenn eine Parser-DLL mehrere Protokolle unterstützt, hat jeder Parser, der einen Handzettel Satz verwendet, seinen eigenen Speicherort in der INI-Datei.</span><span class="sxs-lookup"><span data-stu-id="533db-113">Note that if a parser DLL supports multiple protocols, each parser that uses a handoff set has its own location in the INI file.</span></span>

<span data-ttu-id="533db-114">Handoff-Set-Informationen werden während der Implementierung der Funktion " [**parameterautoinstallinfo**](parserautoinstallinfo.md) " angegeben.</span><span class="sxs-lookup"><span data-stu-id="533db-114">Handoff set information is specified during the implementation of the [**ParserAutoInstallInfo**](parserautoinstallinfo.md) function.</span></span> <span data-ttu-id="533db-115">Der Parser kann die Protokolle angeben, die dem Parser-Protokoll vorangestellt sind, und die Protokolle, die dem Parser-Protokoll folgen.</span><span class="sxs-lookup"><span data-stu-id="533db-115">The parser can specify the protocols that precede the parser protocol, and the protocols that follow the parser protocol.</span></span> <span data-ttu-id="533db-116">Netzwerkmonitor nimmt alle Protokolle vor, die vorangestellt sind, und fügt das parserprotokoll den folgenden Set-Abschnitten der parserini-Datei – für jedes vorherige Protokoll hinzu.</span><span class="sxs-lookup"><span data-stu-id="533db-116">Network Monitor takes all the protocols that precede, and adds the parser protocol to the follow set sections of the parser INI file — for each preceding protocol.</span></span> <span data-ttu-id="533db-117">Netzwerkmonitor speichert die Liste der Protokolle, die im Abschnitt Übergabe Satz der parserini-Datei befolgt werden.</span><span class="sxs-lookup"><span data-stu-id="533db-117">Network Monitor stores the list of protocols that follow in the handoff set section of the parser INI file.</span></span>

<span data-ttu-id="533db-118">In Netzwerkmonitor werden die Informationen zum handseset in der INI-Datei des Parsers gespeichert, aber der Parser greift nicht direkt auf die INI-Dateien zu.</span><span class="sxs-lookup"><span data-stu-id="533db-118">Network Monitor stores the handoff set information in the parser INI file, but the parser does not access the INI files directly.</span></span> <span data-ttu-id="533db-119">Um die Informationen im Übergabe-Satz zu verwenden, [**ruft der Parser die Funktion "**](createhandofftable.md) -Funktion" auf, um eine Übergabe-Tabelle zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="533db-119">To use the information in the handoff set, the parser calls the [**CreateHandoffTable**](createhandofftable.md) function to create a handoff table.</span></span> <span data-ttu-id="533db-120">In der Regel wird die Übergabe Tabelle erstellt, wenn der Parser das Protokoll registriert.</span><span class="sxs-lookup"><span data-stu-id="533db-120">Typically, the handoff table is created when the parser registers the protocol.</span></span> <span data-ttu-id="533db-121">Nachdem das Protokoll registriert wurde, erstellt Netzwerkmonitor eine Übergabe-Tabelle, die vom Parser verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="533db-121">After the protocol is registered, Network Monitor creates a handoff set table that the parser can use.</span></span>

<span data-ttu-id="533db-122">Der Parser verwendet seine Übergabe-Menge, wenn Daten erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="533db-122">The parser uses its handoff set when recognizing data.</span></span> <span data-ttu-id="533db-123">Zuerst liest der Parser den Wert der-Eigenschaft, die das nächste Protokoll identifiziert.</span><span class="sxs-lookup"><span data-stu-id="533db-123">First the parser reads the value of the property that identifies the next protocol.</span></span> <span data-ttu-id="533db-124">Dann ruft der Parser den [**getprotocolfromtable**](getprotocolfromtable.md) auf, um ein Handle für das nächste Protokoll zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="533db-124">Then the parser calls the [**GetProtocolFromTable**](getprotocolfromtable.md) to get a handle to the next protocol.</span></span> <span data-ttu-id="533db-125">Zuletzt gibt der Parser einen Zeiger auf das Handle im Parameter " *phnextprotocol* " von " [**erkenzeframe**](recognizeframe.md)" zurück.</span><span class="sxs-lookup"><span data-stu-id="533db-125">Last, the parser returns a pointer to the handle in the *phNextProtocol* parameter of [**RecognizeFrame**](recognizeframe.md).</span></span>

 

 



