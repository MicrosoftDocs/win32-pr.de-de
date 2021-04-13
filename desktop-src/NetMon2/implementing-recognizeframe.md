---
description: Netzwerk Monitore rufen die erkenzeframe-Funktion eines Parsers auf, um zu bestimmen, ob der Parser die nicht beanspruchten Daten eines Frames erkennt.
ms.assetid: 6d0574da-f0ec-4ed9-bfb0-023dff2ac6fe
title: Implementieren von "erkenzeframe"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d970eee80a04168b3fa06b117c2c219c506da7ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348948"
---
# <a name="implementing-recognizeframe"></a><span data-ttu-id="42ab6-103">Implementieren von "erkenzeframe"</span><span class="sxs-lookup"><span data-stu-id="42ab6-103">Implementing RecognizeFrame</span></span>

<span data-ttu-id="42ab6-104">Netzwerk Monitore rufen die [**erkenzeframe**](recognizeframe.md) -Funktion eines Parsers auf, um zu bestimmen, ob der Parser die nicht beanspruchten Daten eines Frames erkennt.</span><span class="sxs-lookup"><span data-stu-id="42ab6-104">Network Monitors calls the [**RecognizeFrame**](recognizeframe.md) function of a parser to determine that the parser recognizes the unclaimed data of a frame.</span></span> <span data-ttu-id="42ab6-105">Die nicht beanspruchten Daten können sich am Anfang eines Frames befinden, aber in der Regel befinden sich nicht beanspruchte Daten in der Mitte eines Frames.</span><span class="sxs-lookup"><span data-stu-id="42ab6-105">The unclaimed data may be at the start of a frame, but typically, unclaimed data is located in the middle of a frame.</span></span> <span data-ttu-id="42ab6-106">Die folgende Abbildung zeigt nicht beanspruchte Daten, die sich in der Mitte eines Frames befinden.</span><span class="sxs-lookup"><span data-stu-id="42ab6-106">The following illustration shows unclaimed data located in the middle of a frame.</span></span>

![nicht beanspruchte Daten, die sich in der Mitte eines Frames befinden](images/recognizeframe1.png)

<span data-ttu-id="42ab6-108">Netzwerkmonitor stellt beim Aufrufen der Funktion " [**erkenzeframe**](recognizeframe.md) " die folgenden Informationen bereit:</span><span class="sxs-lookup"><span data-stu-id="42ab6-108">Network Monitor provides the following information when it calls the [**RecognizeFrame**](recognizeframe.md) function:</span></span>

-   <span data-ttu-id="42ab6-109">Ein Handle für den Frame.</span><span class="sxs-lookup"><span data-stu-id="42ab6-109">A handle to the frame.</span></span>
-   <span data-ttu-id="42ab6-110">Ein Zeiger auf den Anfang des Frames.</span><span class="sxs-lookup"><span data-stu-id="42ab6-110">A pointer to the start of the frame.</span></span>
-   <span data-ttu-id="42ab6-111">Ein Zeiger auf den Anfang der nicht beanspruchten Daten.</span><span class="sxs-lookup"><span data-stu-id="42ab6-111">A pointer to the start of the unclaimed data.</span></span>
-   <span data-ttu-id="42ab6-112">Der Mac-Wert des ersten Protokolls im Frame.</span><span class="sxs-lookup"><span data-stu-id="42ab6-112">The MAC value of the first protocol in the frame.</span></span>
-   <span data-ttu-id="42ab6-113">Die Anzahl der Bytes in den nicht beanspruchten Daten; Das heißt, die Bytes verbleiben im Frame.</span><span class="sxs-lookup"><span data-stu-id="42ab6-113">The number of bytes in the unclaimed data; that is, the bytes remaining in the frame.</span></span>
-   <span data-ttu-id="42ab6-114">Ein Handle für das vorherige Protokoll.</span><span class="sxs-lookup"><span data-stu-id="42ab6-114">A handle to the previous protocol.</span></span>
-   <span data-ttu-id="42ab6-115">Der Offset des vorherigen Protokolls.</span><span class="sxs-lookup"><span data-stu-id="42ab6-115">The offset of the previous protocol.</span></span>

<span data-ttu-id="42ab6-116">Wenn die Parser-DLL ermittelt, dass nicht beanspruchte Daten mit dem parserprotokoll beginnen, bestimmt die Parser-DLL, wo das nächste Protokoll beginnt und welches Protokoll folgt.</span><span class="sxs-lookup"><span data-stu-id="42ab6-116">When the parser DLL determines that unclaimed data starts with the parser protocol, the parser DLL determines where the next protocol starts, and which protocol follows.</span></span> <span data-ttu-id="42ab6-117">Die Parser-DLL funktioniert wie folgt:</span><span class="sxs-lookup"><span data-stu-id="42ab6-117">The parser DLL functions in the following conditional ways:</span></span>

-   <span data-ttu-id="42ab6-118">Wenn die Parser-DLL nicht beanspruchte Daten erkennt, legt die Parser-DLL den *pprotocolstatus* -Parameter fest und gibt einen Zeiger auf das nächste Protokoll im Frame oder auf **null** zurück.</span><span class="sxs-lookup"><span data-stu-id="42ab6-118">If the parser DLL recognizes unclaimed data, the parser DLL sets the *pProtocolStatus* parameter, and returns a pointer to either the next protocol in the frame, or **NULL**.</span></span> <span data-ttu-id="42ab6-119">**Null** wird zurückgegeben, wenn das aktuelle Protokoll das letzte Protokoll im Frame ist.</span><span class="sxs-lookup"><span data-stu-id="42ab6-119">**NULL** is returned if the current protocol is the last protocol in the frame.</span></span>
-   <span data-ttu-id="42ab6-120">Wenn die Parser-DLL nicht beanspruchte Daten erkennt und das folgende Protokoll identifiziert (aus den im Protokoll bereitgestellten Informationen), gibt die Parser-DLL einen Zeiger auf das Handle des nächsten Protokolls im Parameter *phnextprotocol* der Funktion zurück.</span><span class="sxs-lookup"><span data-stu-id="42ab6-120">If the parser DLL recognizes unclaimed data and identifies the protocol that follows (from information provided in the protocol), then the parser DLL returns a pointer to the handle of the next protocol in the *phNextProtocol* parameter of the function.</span></span>
-   <span data-ttu-id="42ab6-121">Wenn die Parser-DLL keine nicht beanspruchten Daten erkennt, gibt die Parser-DLL den Zeiger auf den Anfang der nicht beanspruchten Daten zurück, und Netzwerkmonitor versucht weiterhin, die nicht beanspruchten Daten zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="42ab6-121">If the parser DLL does not recognize unclaimed data, the parser DLL returns the pointer to the start of unclaimed data, and Network Monitor continues trying to parse the unclaimed data.</span></span>

<span data-ttu-id="42ab6-122">**So implementieren Sie "erkenzeframe"**</span><span class="sxs-lookup"><span data-stu-id="42ab6-122">**To implement RecognizeFrame**</span></span>

1.  <span data-ttu-id="42ab6-123">Testen Sie, um zu ermitteln, dass Sie das Protokoll erkennen.</span><span class="sxs-lookup"><span data-stu-id="42ab6-123">Test to determine that you recognize the protocol.</span></span>
2.  <span data-ttu-id="42ab6-124">Wenn Sie nicht beanspruchte Daten erkennen und wissen, welches Protokoll befolgt wird, legen Sie *pprotocolstatus* auf Protokoll \_ Status \_ Next \_ Protocol fest, legen Sie *phnextprotocol* auf einen Zeiger fest, der auf das Handle für das nächste Protokoll verweist, und geben Sie dann einen Zeiger auf das nächste Protokoll zurück.</span><span class="sxs-lookup"><span data-stu-id="42ab6-124">If you recognize unclaimed data and you know which protocol follows, set *pProtocolStatus* to PROTOCOL\_STATUS\_NEXT\_PROTOCOL, set *phNextProtocol* to a pointer that points to the handle for the next protocol, and then return a pointer to the next protocol.</span></span>

    <span data-ttu-id="42ab6-125">– oder –</span><span class="sxs-lookup"><span data-stu-id="42ab6-125">–or–</span></span>

    <span data-ttu-id="42ab6-126">Wenn Sie nicht beanspruchte Daten erkennen und nicht wissen, welches Protokoll befolgt wird, legen Sie *pprotocolstatus* auf Protokoll \_ Status erkannt fest \_ , und geben Sie dann einen Zeiger auf das nächste Protokoll zurück.</span><span class="sxs-lookup"><span data-stu-id="42ab6-126">If you recognize unclaimed data and you do not know which protocol follows, set *pProtocolStatus* to PROTOCOL\_STATUS\_RECOGNIZED, and then return a pointer to the next protocol.</span></span>

    <span data-ttu-id="42ab6-127">– oder –</span><span class="sxs-lookup"><span data-stu-id="42ab6-127">–or–</span></span>

    <span data-ttu-id="42ab6-128">Wenn Sie nicht beanspruchte Daten erkennen und Ihr Protokoll das letzte Protokoll in einem Frame ist, legen Sie *pprotocolstatus* auf "Protokoll \_ Status beansprucht" fest \_ , und geben Sie dann **null** zurück.</span><span class="sxs-lookup"><span data-stu-id="42ab6-128">If you recognize unclaimed data and your protocol is the last protocol in a frame, set *pProtocolStatus* to PROTOCOL\_STATUS\_CLAIMED, and then return **NULL**.</span></span>

    <span data-ttu-id="42ab6-129">– oder –</span><span class="sxs-lookup"><span data-stu-id="42ab6-129">–or–</span></span>

    <span data-ttu-id="42ab6-130">Wenn Sie keine nicht beanspruchten Daten erkennen, legen Sie *pprotocolstatus* auf "Protokoll \_ Status \_ nicht erkannt" fest \_ , und geben Sie dann den Zeiger zurück, der in " *pprotocol*" an Sie übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="42ab6-130">If you do not recognize unclaimed data, set *pProtocolStatus* to PROTOCOL\_STATUS\_NOT\_RECOGNIZED, and then return the pointer that is passed to you in *pProtocol*.</span></span>

<span data-ttu-id="42ab6-131">Im folgenden finden Sie eine grundlegende Implementierung von [**erkenzeframe**](recognizeframe.md).</span><span class="sxs-lookup"><span data-stu-id="42ab6-131">The following is a basic implementation of [**RecognizeFrame**](recognizeframe.md).</span></span>

``` syntax
#include <windows.h>

LPBYTE BHAPI MyProtocol_RecognizeFrame( HFRAME hFrame,
                                        LPBYTE        pMacFrame,
                                        LPBYTE        pProtocol,
                                        DWORD         MacType,
                                        DWORD         BytesLeft,
                                        HPROTOCOL     hPrevProtocol,
                                        DWORD         nPreviuosProtOffset,
                                        LPDWORD       pProtocolStatus,
                                        LPHPROTOCOL   phNextProtocol,
                                        LPDWORD       InstData)
  
  // Test unclaimed data. 
  
  // If unclaimed data is recognized, but you do not know what follows.
  *pProtocolStatus =  PROTOCOL_STATUS_RECOGNIZED;
  return pProtocol + MY_PROTOCOL_LENGTH;
  
  // If unclaimed data is recognized and you know what follows.
  *pProtocolStatus =  PROTOCOL_STATUS_NEXT_PROTOCOL;
  phNextProtocol = GetProtocolFromTable(
                                        hTable,
                                        ItemToFind,
                                        lpInstData);
  return  pProtocol + MY_PROTOCOL_LENGTH;
  
  // If unclaimed data is recognized and the protocol is the last 
  // protocol in the frame.
  *pProtocolStatus =  PROTOCOL_STATUS_CLAIMED;
  return NULL;
  
  // If the unclaimed data is not recognized.
  *pProtocolStatus =  PROTOCOL_STATUS_NOT_RECOGNIZED;
  return *pProtocol;

}
```

 

 



