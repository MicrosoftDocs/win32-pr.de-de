---
title: Schreiben eines Treibers zum Erfassen von FRAMES
description: In diesem Dokument wird erläutert, wie Sie einen Treiber entwickeln, der FRAMES in Windows Vista erfassen kann, bevor sie im Sendepfad komprimiert/verschlüsselt oder im Empfangspfad dekomprimiert/entschlüsselt werden.
ms.assetid: 1b3fe1b8-2b11-4aed-98e1-464b8c0821ec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b769a07811980b20ab076f60cc1e4fd7d9aa227b8eecfa44e71089bc949d0de5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789688"
---
# <a name="writing-a-driver-to-capture-ppp-frames"></a>Schreiben eines Treibers zum Erfassen von FRAMES

Wenn Point-to-Point-Protokoll Frames (FTP) über einen PPTP-Tunnel (Point-to-Point Tunneling Protocol) mit aktivierter Verschlüsselung oder über einen L2TP-Tunnel (Layer 2 Tunneling Protocol) gesendet werden, der IPSec für die Verschlüsselung verwendet, kann das typische FRAME CAPTURE-Hilfsprogramm nur FRAMES erfassen, die über ein verschlüsseltes Protokollidentitätsfeld verfügen. In diesem Dokument wird erläutert, wie Sie einen Treiber entwickeln, der FRAMES in Windows Vista erfassen kann, bevor sie im Sendepfad komprimiert/verschlüsselt oder im Empfangspfad dekomprimiert/entschlüsselt werden.

1.  Schreiben sie einen NDIS-Protokolltreiber. Weitere Informationen finden Sie unter [NDIS 6.0-Protokolltreiber](https://msdn.microsoft.com/library/ms795570.aspx) oder [NDIS-Protokolltreiber (NDIS 5.1).](https://msdn.microsoft.com/library/ms801145.aspx)
2.  Installieren Sie den Treiber mit der Hardwareidentität "ms \_ netmon". Ausführliche Anweisungen zum Installieren des Treibers mit einer bestimmten Hardwareidentität finden Sie [im Abschnitt INF-Modelle.](https://msdn.microsoft.com/library/ms794357.aspx)
    > [!Note]  
    > Jeder Windows Vista-Computer lässt die Installation nur einer Treiberentität zu, die über die Hardwareidentität "ms \_ netmon" verfügt. Um einen anderen Treiber mit dieser Identität zu installieren, muss der erste Treiber deinstalliert werden. Ein Treiber, der ohne Verwendung der \_ "ms netmon"-Hardwareidentität installiert wird, kann nicht die Bindung ausführen, die zum Erfassen von FRAMES erforderlich ist.

     

3.  Der Protokolltreiber sollte "ndiswanbh" als Bindungsschnittstelle zum Erfassen von FRAMES angeben. Ausführliche Anweisungen finden Sie unter [Angeben von Bindungsschnittstellen.](https://msdn.microsoft.com/library/aa937923.aspx)
4.  Die [ProtocolBindAdapter-Implementierung](https://msdn.microsoft.com/library/ms797311.aspx) im Treiber sollte "NdisMediumWan" als Teil des mittleren Arrays unterstützen, damit der ndiswanbh-Miniportrand mit der [NdisOpenAdapter-Funktion](https://msdn.microsoft.com/library/ms804862.aspx) geöffnet werden kann.
5.  Wenn die [Funktion ProtocolOpenAdapterComplete](https://msdn.microsoft.com/library/ms797287.aspx) mit dem Status NDIS STATUS SUCCESS aufgerufen \_ \_ wird, sollte der Protokolltreiber die [OID OID GEN \_ CURRENT PACKET \_ \_ \_ FILTER](https://msdn.microsoft.com/library/bb314089.aspx) mit den Flags [NDIS \_ PACKET TYPE \_ \_ PROMISCUOUS](https://msdn.microsoft.com/library/bb314089.aspx) und [NDIS \_ PACKET TYPE ALL \_ \_ \_ LOCAL](https://msdn.microsoft.com/library/bb314089.aspx) über diese Bindung festlegen. Sobald dies erfolgt ist, empfängt der Protokolltreiber die entschlüsselten FRAMES von der FRAMES-Rahmenebene in seiner [ProtocolReceive-Funktion.](https://msdn.microsoft.com/library/ms797274.aspx)

> [!Note]  
> Diese Informationen gelten nur für Treiber auf einem computer Windows Vista.

 

 

 




