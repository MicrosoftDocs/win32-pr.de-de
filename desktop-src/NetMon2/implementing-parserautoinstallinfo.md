---
description: Netzwerkmonitor verwendet die Exportfunktion ParserAutoInstallInfo, um einen Parser zu installieren. Wenn ParserAutoInstallInfo aufgerufen wird, gibt der Parser eine PF \_ PARSERDLLINFO-Struktur zurück, die alle Informationen enthält, die Netzwerkmonitor zum Installieren einer Parser-DLL benötigt.
ms.assetid: 1add9988-9cb2-43f9-8ae2-32acfe21b6f3
title: Implementieren von ParserAutoInstallInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6d1c797f53ad110392fea304cc0a610fdb0f9346c745e2f7dea2bff16208e05
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119743080"
---
# <a name="implementing-parserautoinstallinfo"></a>Implementieren von ParserAutoInstallInfo

Netzwerkmonitor verwendet die Exportfunktion [**ParserAutoInstallInfo,**](parserautoinstallinfo.md) um einen Parser zu installieren. Wenn **ParserAutoInstallInfo** aufgerufen wird, gibt der Parser eine [**PF \_ PARSERDLLINFO-Struktur**](pf-parserdllinfo.md) zurück, die alle Informationen enthält, die Netzwerkmonitor zum Installieren einer Parser-DLL benötigen.

> [!Note]  
> Netzwerkmonitor speichert eine Liste vorhandener Parser in der [*Parser.ini-Datei*](p.md) und erstellt eine separate INI-Datei für jeden installierten Parser.

 

Während des Installationsvorgangs muss die Parser-DLL Folgendes identifizieren:

-   Die Anzahl der Parser in der DLL, einschließlich eines Namens und einer Kommentarbeschreibung für jeden Parser.
-   Die Protokolle, die dem Parserprotokoll vorangestellt sind.
-   Die Protokolle, die dem Parserprotokoll folgen.

> [!Note]  
> Netzwerkmonitor verwendet die obigen und folgenden Parserprotokollinformationen, um die [*Übergabesätze*](h.md) zu aktualisieren und den von der Parser-DLL identifizierten [*Parsersätzen zu folgen.*](f.md)

 

Mit dem folgenden Verfahren werden die Schritte identifiziert, die zum Implementieren von [**ParserAutoInstallInfo**](parserautoinstallinfo.md)erforderlich sind.

**So implementieren Sie ParserAutoInstallInfo**

1.  Zuordnen einer [**PF \_ PARSERDLLINFO-Struktur**](pf-parserdllinfo.md) mit **HeapAlloc**.
2.  Geben Sie mit **HeapFree** Arbeitsspeicher an den Heap zurück.
3.  Beachten Sie, dass dieser Aufruf auch eine [**PF \_ PARSERINFO-Struktur**](pf-parserinfo.md) für jeden Parser in der DLL zuordnen muss.
4.  Geben Sie die Anzahl der Parser (in der Regel eins) an, die die DLL im **nParsers-Member** von [**PF \_ PARSERDLLINFO**](pf-parserdllinfo.md)enthält.
5.  Geben Sie einen Namen, einen Kommentar und eine optionale Hilfedatei in den **Membern szProtocolName,** **szComment** und **szHelpFile** jeder [**PF \_ PARSERINFO-Struktur**](pf-parserinfo.md) an.
6.  Geben Sie die Protokolle an, die jedem DLL-Protokoll vorangestellt sind. Eine der folgenden Bedingungen gilt für einen eingehenden Übergabesatz.
    -   Wenn die vorherigen Protokolle bestimmen können, dass Ihr Protokoll den Daten in den vorherigen Protokollen folgt, legen Sie den **pWhoHandsOffToMe-Member** von [**PF \_ PARSERINFO**](pf-parserinfo.md)fest. In diesem Fall wird Ihr Protokoll dann den [*Übergabesätzen*](h.md) der vorherigen Protokolle hinzugefügt.
    -   Wenn die vorherigen Protokolle nicht ermitteln können, ob Ihr Protokoll auf daten in den vorherigen Protokollen folgt, legen Sie **pWhoCanPrecedeMe-Member** von [**PF \_ PARSERINFO**](pf-parserinfo.md)fest. In diesem Fall wird das Protokoll dann den [*folgenden Protokollsätzen*](f.md) hinzugefügt.
7.  Geben Sie die Protokolle an, die den einzelnen DLL-Protokollen folgen. Eine der folgenden Bedingungen gilt für einen ausgehenden Follow-Set.
    -   Wenn Ihr Protokoll anhand der Daten in Ihrem Protokoll bestimmen kann, welche Protokolle folgen, legen Sie den **pWhoDoIHandOffTo-Member** von [**PF \_ PARSERINFO**](pf-parserinfo.md)fest. In diesem Fall werden diese Protokolle dem [*Übergabesatz*](h.md) Ihrer Protokolle hinzugefügt.
    -   Wenn Ihr Protokoll anhand der Daten in Ihrem Protokoll nicht bestimmen kann, welche Protokolle folgen, legen Sie den **pWhoCanFollowMe-Member** von [**PF \_ PARSERINFO**](pf-parserinfo.md)fest. In diesem Fall werden diese Protokolle dem [*folgenden Satz*](f.md) Ihres Protokolls hinzugefügt.
8.  Gibt die [**\_ PARSERDLLINFO-PF-Struktur**](pf-parserdllinfo.md) an Netzwerkmonitor zurück.

Im Folgenden ist eine grundlegende Implementierung von [**ParserAutoInstallInfo .**](parserautoinstallinfo.md) Das Codebeispiel stammt aus dem generischen Parser, den Netzwerkmonitor bereitstellt.

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

 

 



