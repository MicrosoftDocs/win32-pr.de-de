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
# <a name="implementing-parserautoinstallinfo"></a>Implementieren von "parameserautoinstallinfo"

Netzwerkmonitor verwendet die [**parserautoinstallinfo**](parserautoinstallinfo.md) -Exportfunktion, um einen Parser zu installieren. Wenn **parserautoinstallinfo** aufgerufen wird, gibt der Parser eine [**PF \_ parserdllinfo**](pf-parserdllinfo.md) -Struktur zurück, die alle Informationen enthält, die Netzwerkmonitor zum Installieren einer Parser-DLL benötigt.

> [!Note]  
> Netzwerkmonitor behält eine Liste vorhandener Parser in der [*Parser.ini*](p.md) Datei bei und erstellt eine separate ini-Datei für jeden installierten Parser.

 

Während des Installationsvorgangs muss die Parser-DLL Folgendes identifizieren:

-   Die Anzahl der Parser in der dll – einschließlich eines Namens und einer Kommentar Beschreibung für jeden Parser.
-   Die Protokolle, die dem parserprotokoll vorangestellt sind.
-   Die Protokolle, die dem Parser-Protokoll folgen.

> [!Note]  
> Netzwerkmonitor verwendet die vorhergehenden und folgenden Parser-Protokollinformationen, um die [*Übergabe Sätze*](h.md) zu aktualisieren und die Sätze von Parser zu [*befolgen*](f.md) , die von der Parser-DLL identifiziert werden.

 

Im folgenden Verfahren werden die erforderlichen Schritte zum Implementieren von " [**Parser autoinstallinfo**](parserautoinstallinfo.md)" beschrieben.

**So implementieren Sie "Parser autoinstallinfo"**

1.  Zuordnen einer [**PF \_ parserdllinfo**](pf-parserdllinfo.md) -Struktur mithilfe von **HeapAlloc**.
2.  Geben Sie mithilfe von **HeapFree** Arbeitsspeicher an den Heap zurück.
3.  Beachten Sie, dass dieser-Befehl auch eine [**PF \_ parserinfo**](pf-parserinfo.md) -Struktur für jeden Parser in der dll zuordnen muss.
4.  Geben Sie die Anzahl der Parser (in der Regel eine) an, die die dll im **nparser** -Member von [**PF-Parser " \_ Parser**](pf-parserdllinfo.md)" enthält.
5.  Geben Sie einen Namen, einen Kommentar und eine optionale Hilfedatei in den Elementen **szprotocolname**, **szcomment** und **szhelpfile** jeder [**PF \_**](pf-parserinfo.md) -Parameter Info-Struktur an.
6.  Geben Sie die Protokolle an, die jedem dll-Protokoll vorangestellt sind. Eine der folgenden Bedingungen gilt für einen eingehenden Übergabe-Satz.
    -   Wenn die oben genannten Protokolle feststellen können, ob Ihr Protokoll aus den Daten in den vorangehenden Protokollen folgt, legen Sie den **pwhohandsofftome** -Member von PF-Parameter [**\_ Info**](pf-parserinfo.md)fest. In diesem Fall wird Ihr Protokoll dann den [*Übergabe Sätzen*](h.md) der vorherigen Protokolle hinzugefügt.
    -   Wenn die oben genannten Protokolle nicht bestimmen können, ob Ihr Protokoll aus den Daten in den vorangehenden Protokollen folgt, legen Sie das **pwhocanvoran-** Element von PF-Parameter [**\_ Info**](pf-parserinfo.md)fest. In diesem Fall wird Ihr Protokoll den [*folgenden Protokoll Sätzen*](f.md) hinzugefügt.
7.  Geben Sie die Protokolle an, die den einzelnen dll-Protokollen entsprechen. Eine der folgenden Bedingungen gilt für eine ausgehende Folge Gruppe.
    -   Wenn Ihr Protokoll basierend auf den Daten in Ihrem Protokoll feststellen kann, welche Protokolle befolgt werden, legen Sie den **pwhodoihandoffto** -Member von PF-Parameter [**\_ Info**](pf-parserinfo.md)fest. In diesem Fall werden diese Protokolle dem [*Übergabe Satz*](h.md) ihrer Protokolle hinzugefügt.
    -   Wenn Ihr Protokoll nicht ermitteln kann, welche Protokolle auf der Grundlage von Daten in Ihrem Protokoll befolgt werden, legen Sie das **pwhocanfollowme** -Element von PF-Parameter [**\_ Info**](pf-parserinfo.md)fest. In diesem Fall werden diese Protokolle dem [*folgenden Protokoll Satz*](f.md) hinzugefügt.
8.  Gibt die [**PF- \_ parameserdllinfo**](pf-parserdllinfo.md) -Struktur an Netzwerkmonitor zurück.

Im folgenden finden Sie eine grundlegende Implementierung von " [**Parser autoinstallinfo**](parserautoinstallinfo.md)". Das Codebeispiel stammt aus dem generischen Parser, den Netzwerkmonitor bereitstellt.

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

 

 



