---
description: Netzwerkmonitor verwendet die parserautoinstallinfo-Exportfunktion, um einen Parser zu installieren. Wenn parserautoinstallinfo aufgerufen wird, gibt der Parser eine PF \_ parserdllinfo-Struktur zurück, die alle Informationen enthält, die Netzwerkmonitor zum Installieren einer Parser-DLL benötigt.
ms.assetid: 1add9988-9cb2-43f9-8ae2-32acfe21b6f3
title: Implementieren von "parameserautoinstallinfo"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d79a9ba5036673acb076be9f3634dae7556b5bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360781"
---
# <a name="implementing-parserautoinstallinfo"></a><span data-ttu-id="57879-104">Implementieren von "parameserautoinstallinfo"</span><span class="sxs-lookup"><span data-stu-id="57879-104">Implementing ParserAutoInstallInfo</span></span>

<span data-ttu-id="57879-105">Netzwerkmonitor verwendet die [**parserautoinstallinfo**](parserautoinstallinfo.md) -Exportfunktion, um einen Parser zu installieren.</span><span class="sxs-lookup"><span data-stu-id="57879-105">Network Monitor uses the [**ParserAutoInstallInfo**](parserautoinstallinfo.md) export function to install a parser.</span></span> <span data-ttu-id="57879-106">Wenn **parserautoinstallinfo** aufgerufen wird, gibt der Parser eine [**PF \_ parserdllinfo**](pf-parserdllinfo.md) -Struktur zurück, die alle Informationen enthält, die Netzwerkmonitor zum Installieren einer Parser-DLL benötigt.</span><span class="sxs-lookup"><span data-stu-id="57879-106">When **ParserAutoInstallInfo** is called, the parser returns a [**PF\_PARSERDLLINFO**](pf-parserdllinfo.md) structure containing all the information that Network Monitor needs to install a parser DLL.</span></span>

> [!Note]  
> <span data-ttu-id="57879-107">Netzwerkmonitor behält eine Liste vorhandener Parser in der [*Parser.ini*](p.md) Datei bei und erstellt eine separate ini-Datei für jeden installierten Parser.</span><span class="sxs-lookup"><span data-stu-id="57879-107">Network Monitor keeps a list of existing parsers in the [*Parser.ini*](p.md) file, and creates a separate INI file for each installed parser.</span></span>

 

<span data-ttu-id="57879-108">Während des Installationsvorgangs muss die Parser-DLL Folgendes identifizieren:</span><span class="sxs-lookup"><span data-stu-id="57879-108">During the installation process, the parser DLL must identify the following:</span></span>

-   <span data-ttu-id="57879-109">Die Anzahl der Parser in der dll – einschließlich eines Namens und einer Kommentar Beschreibung für jeden Parser.</span><span class="sxs-lookup"><span data-stu-id="57879-109">The number of parsers in the DLL—including a name and comment description for each parser.</span></span>
-   <span data-ttu-id="57879-110">Die Protokolle, die dem parserprotokoll vorangestellt sind.</span><span class="sxs-lookup"><span data-stu-id="57879-110">The protocols that precede the parser protocol.</span></span>
-   <span data-ttu-id="57879-111">Die Protokolle, die dem Parser-Protokoll folgen.</span><span class="sxs-lookup"><span data-stu-id="57879-111">The protocols that follow the parser protocol.</span></span>

> [!Note]  
> <span data-ttu-id="57879-112">Netzwerkmonitor verwendet die vorhergehenden und folgenden Parser-Protokollinformationen, um die [*Übergabe Sätze*](h.md) zu aktualisieren und die Sätze von Parser zu [*befolgen*](f.md) , die von der Parser-DLL identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="57879-112">Network Monitor uses the preceding and following parser protocol information to update the [*handoff sets*](h.md) and [*follow sets*](f.md) of parsers that your parser DLL identifies.</span></span>

 

<span data-ttu-id="57879-113">Im folgenden Verfahren werden die erforderlichen Schritte zum Implementieren von " [**Parser autoinstallinfo**](parserautoinstallinfo.md)" beschrieben.</span><span class="sxs-lookup"><span data-stu-id="57879-113">The following procedure identifies the steps necessary to implement [**ParserAutoInstallInfo**](parserautoinstallinfo.md).</span></span>

<span data-ttu-id="57879-114">**So implementieren Sie "Parser autoinstallinfo"**</span><span class="sxs-lookup"><span data-stu-id="57879-114">**To implement ParserAutoInstallInfo**</span></span>

1.  <span data-ttu-id="57879-115">Zuordnen einer [**PF \_ parserdllinfo**](pf-parserdllinfo.md) -Struktur mithilfe von **HeapAlloc**.</span><span class="sxs-lookup"><span data-stu-id="57879-115">Allocate a [**PF\_PARSERDLLINFO**](pf-parserdllinfo.md) structure using **HeapAlloc**.</span></span>
2.  <span data-ttu-id="57879-116">Geben Sie mithilfe von **HeapFree** Arbeitsspeicher an den Heap zurück.</span><span class="sxs-lookup"><span data-stu-id="57879-116">Return memory to the heap using **HeapFree**.</span></span>
3.  <span data-ttu-id="57879-117">Beachten Sie, dass dieser-Befehl auch eine [**PF \_ parserinfo**](pf-parserinfo.md) -Struktur für jeden Parser in der dll zuordnen muss.</span><span class="sxs-lookup"><span data-stu-id="57879-117">Be aware that this call must also allocate a [**PF\_PARSERINFO**](pf-parserinfo.md) structure for each parser in the DLL.</span></span>
4.  <span data-ttu-id="57879-118">Geben Sie die Anzahl der Parser (in der Regel eine) an, die die dll im **nparser** -Member von [**PF-Parser " \_ Parser**](pf-parserdllinfo.md)" enthält.</span><span class="sxs-lookup"><span data-stu-id="57879-118">Specify the number of parsers (typically one) that the DLL contains in the **nParsers** member of [**PF\_PARSERDLLINFO**](pf-parserdllinfo.md).</span></span>
5.  <span data-ttu-id="57879-119">Geben Sie einen Namen, einen Kommentar und eine optionale Hilfedatei in den Elementen **szprotocolname**, **szcomment** und **szhelpfile** jeder [**PF \_**](pf-parserinfo.md) -Parameter Info-Struktur an.</span><span class="sxs-lookup"><span data-stu-id="57879-119">Specify a name, comment, and optional Help file in the **szProtocolName**, **szComment**, and **szHelpFile** members of each [**PF\_PARSERINFO**](pf-parserinfo.md) structure.</span></span>
6.  <span data-ttu-id="57879-120">Geben Sie die Protokolle an, die jedem dll-Protokoll vorangestellt sind.</span><span class="sxs-lookup"><span data-stu-id="57879-120">Specify the protocols that precede each DLL protocol.</span></span> <span data-ttu-id="57879-121">Eine der folgenden Bedingungen gilt für einen eingehenden Übergabe-Satz.</span><span class="sxs-lookup"><span data-stu-id="57879-121">One of the following conditions applies to an incoming handoff set.</span></span>
    -   <span data-ttu-id="57879-122">Wenn die oben genannten Protokolle feststellen können, ob Ihr Protokoll aus den Daten in den vorangehenden Protokollen folgt, legen Sie den **pwhohandsofftome** -Member von PF-Parameter [**\_ Info**](pf-parserinfo.md)fest.</span><span class="sxs-lookup"><span data-stu-id="57879-122">If the preceding protocols can determine that your protocol follows from data in the preceding protocols, set the **pWhoHandsOffToMe** member of [**PF\_PARSERINFO**](pf-parserinfo.md).</span></span> <span data-ttu-id="57879-123">In diesem Fall wird Ihr Protokoll dann den [*Übergabe Sätzen*](h.md) der vorherigen Protokolle hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="57879-123">In this case, your protocol is then added to the [*handoff sets*](h.md) of the preceding protocols.</span></span>
    -   <span data-ttu-id="57879-124">Wenn die oben genannten Protokolle nicht bestimmen können, ob Ihr Protokoll aus den Daten in den vorangehenden Protokollen folgt, legen Sie das **pwhocanvoran-** Element von PF-Parameter [**\_ Info**](pf-parserinfo.md)fest.</span><span class="sxs-lookup"><span data-stu-id="57879-124">If the preceding protocols cannot determine that your protocol follows from data in the preceding protocols, set **pWhoCanPrecedeMe** member of [**PF\_PARSERINFO**](pf-parserinfo.md).</span></span> <span data-ttu-id="57879-125">In diesem Fall wird Ihr Protokoll den [*folgenden Protokoll Sätzen*](f.md) hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="57879-125">In this case, the your protocol is then added to the [*follow sets*](f.md) of the protocols.</span></span>
7.  <span data-ttu-id="57879-126">Geben Sie die Protokolle an, die den einzelnen dll-Protokollen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57879-126">Specify the protocols that follow each DLL protocol.</span></span> <span data-ttu-id="57879-127">Eine der folgenden Bedingungen gilt für eine ausgehende Folge Gruppe.</span><span class="sxs-lookup"><span data-stu-id="57879-127">One of the following conditions applies to an outgoing follow-set.</span></span>
    -   <span data-ttu-id="57879-128">Wenn Ihr Protokoll basierend auf den Daten in Ihrem Protokoll feststellen kann, welche Protokolle befolgt werden, legen Sie den **pwhodoihandoffto** -Member von PF-Parameter [**\_ Info**](pf-parserinfo.md)fest.</span><span class="sxs-lookup"><span data-stu-id="57879-128">If your protocol can determine which protocols follow based on data in your protocol, set the **pWhoDoIHandOffTo** member of [**PF\_PARSERINFO**](pf-parserinfo.md).</span></span> <span data-ttu-id="57879-129">In diesem Fall werden diese Protokolle dem [*Übergabe Satz*](h.md) ihrer Protokolle hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="57879-129">In this case, the these protocols are added to the [*handoff set*](h.md) of your protocols.</span></span>
    -   <span data-ttu-id="57879-130">Wenn Ihr Protokoll nicht ermitteln kann, welche Protokolle auf der Grundlage von Daten in Ihrem Protokoll befolgt werden, legen Sie das **pwhocanfollowme** -Element von PF-Parameter [**\_ Info**](pf-parserinfo.md)fest.</span><span class="sxs-lookup"><span data-stu-id="57879-130">If your protocol cannot determine which protocols follow based on data in your protocol, set the **pWhoCanFollowMe** member of [**PF\_PARSERINFO**](pf-parserinfo.md).</span></span> <span data-ttu-id="57879-131">In diesem Fall werden diese Protokolle dem [*folgenden Protokoll Satz*](f.md) hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="57879-131">In this case, these protocols are added to the [*follow set*](f.md) of your protocol.</span></span>
8.  <span data-ttu-id="57879-132">Gibt die [**PF- \_ parameserdllinfo**](pf-parserdllinfo.md) -Struktur an Netzwerkmonitor zurück.</span><span class="sxs-lookup"><span data-stu-id="57879-132">Return the [**PF\_PARSERDLLINFO**](pf-parserdllinfo.md) structure to Network Monitor.</span></span>

<span data-ttu-id="57879-133">Im folgenden finden Sie eine grundlegende Implementierung von " [**Parser autoinstallinfo**](parserautoinstallinfo.md)".</span><span class="sxs-lookup"><span data-stu-id="57879-133">The following is a basic implementation of [**ParserAutoInstallInfo**](parserautoinstallinfo.md).</span></span> <span data-ttu-id="57879-134">Das Codebeispiel stammt aus dem generischen Parser, den Netzwerkmonitor bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="57879-134">The code example is taken from the generic parser that Network Monitor provides.</span></span>

``` syntax
#include <windows.h>

PPF_PARSERDLLINFO WINAPI ParserAutoInstallInfo() 
{

  /////////////////////////////////////////////////////////////////
  //
  // Allocate memory for PF_PARSERDLLINFO structure.
  //
  /////////////////////////////////////////////////////////////////
  PPF_PARSERDLLINFO pParserDllInfo; 
  PPF_PARSERINFO    pParserInfo;
  DWORD NumProtocols;
        DWORD NumParsers;
        DWORD NumFollows;
  NumParsers = 1;
  
  pParserDllInfo = (PPF_PARSERDLLINFO)HeapAlloc( GetProcessHeap(),
                                                 HEAP_ZERO_MEMORY,
                                                 sizeof( PF_PARSERDLLINFO ) +
                                                 NumParsers * sizeof( PF_PARSERINFO) );
  if( pParserDllInfo == NULL)
  {
    return NULL;
  }
  

    
  /////////////////////////////////////////////////////////////////
  //
  // Specify the number of parsers in the DLL.
  //
  /////////////////////////////////////////////////////////////////
  
  pParserDllInfo->nParsers = NumParsers;
  

  /////////////////////////////////////////////////////////////////
  // 
  // Specify the name, comment, and Help file for each protocol.
  // 
  /////////////////////////////////////////////////////////////////
  pParserInfo = &(pParserDllInfo->ParserInfo[0]);
  sprintf_s( pParserInfo->szProtocolName, MAX_PROTOCOL_NAME_LEN, 
    "TestProtocol" );
  sprintf_s( pParserInfo->szComment, MAX_PROTOCOL_COMMENT_LEN,
    "Test protocol for SDK" );
  sprintf_s( pParserInfo->szHelpFile, MAX_PATH, "");
  

  
  /////////////////////////////////////////////////////////////////
  //
  // Specify preceding protocols.
  //
  /////////////////////////////////////////////////////////////////
  PPF_HANDOFFSET    pHandoffSet;
  PPF_HANDOFFENTRY  pHandoffEntry;
  
  // Allocate PF_HANDOFFSET structure.
  NumHandoffs = 1;                   
  pHandoffSet = (PPF_HANDOFFSET)HeapAlloc( GetProcessHeap(),
                                           HEAP_ZERO_MEMORY,
                                           sizeof( PF_HANDOFFSET ) +
                                           NumHandoffs * sizeof( PF_HANDOFFENTRY) );
  if( pHandoffSet == NULL )
  {
     return pParserDllInfo;
  }

  // Fill in handoff set
  pParserInfo->pWhoHandsOffToMe = pHandoffSet;
  pHandoffSet->nEntries = NumHandoffs;

  // TCP PORT FFFF
  pHandoffEntry = &(pHandoffSet->Entry[0]);
  sprintf_s( pHandoffEntry->szIniFile, MAX_PATH, "TCPIP.INI" );
  sprintf_s( pHandoffEntry->szIniSection, MAX_PATH, "TCP_HandoffSet" );
  sprintf_s( pHandoffEntry->szProtocol, MAX_PROTOCOL_NAME_LEN, 
    "BLRPLATE" );
  pHandoffEntry->dwHandOffValue =        0xFFFF;
  pHandoffEntry->ValueFormatBase =       HANDOFF_VALUE_FORMAT_BASE_DECIMAL;    
  
  

  /////////////////////////////////////////////////////////////////
  //
  // Specify the following protocols.
  //
  /////////////////////////////////////////////////////////////////
  PPF_FOLLOWSET     pFollowSet;
  PPF_FOLLOWENTRY   pFollowEntry;
 
  // Allocate PF_FOLLOWSET structure
  NumFollows = 1;
  pFollowSet = (PPF_FOLLOWSET)HeapAlloc( GetProcessHeap(),
                                         HEAP_ZERO_MEMORY,
                                         sizeof( PF_FOLLOWSET ) +
                                         NumFollows * sizeof( PF_FOLLOWENTRY) );
  if( pFollowSet == NULL )
  {
    return pParserDllInfo;
  }

  // Fill in the follow set
  pParserInfo->pWhoCanFollowMe = pFollowSet;
  pFollowSet->nEntries = NumFollows;

  // Add SMB
  pFollowEntry = &(pFollowSet->Entry[0]);
  sprintf_s( pFollowEntry->szProtocol, MAX_PROTOCOL_NAME_LEN, "SMB" );
  


  /////////////////////////////////////////////////////////////////
  //
  // Return the PF_PARSERDLLINFO structure.
  //
  /////////////////////////////////////////////////////////////////
  return pParserDllInfo;

}
```

 

 



