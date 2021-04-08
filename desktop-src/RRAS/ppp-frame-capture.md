---
title: Schreiben eines Treibers zum Erfassen von PPP-Frames
description: In diesem Dokument wird erläutert, wie Sie einen Treiber entwickeln, der PPP-Frames in Windows Vista erfassen kann, bevor diese im sendepfad komprimiert/verschlüsselt werden oder nachdem Sie im Empfangs Pfad dekomprimiert/entschlüsselt wurden.
ms.assetid: 1b3fe1b8-2b11-4aed-98e1-464b8c0821ec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d592596674cd64af5122303afefcfc81026dad27
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104038607"
---
# <a name="writing-a-driver-to-capture-ppp-frames"></a>Schreiben eines Treibers zum Erfassen von PPP-Frames

Wenn Point-to-Point-Protokoll (PPP)-Rahmen über einen PPTP-Tunnel (Point-to-Point-Tunneling-Protokoll) mit aktivierter Verschlüsselung oder über einen L2TP-Tunnel (Layer 2 Tunneling Protocol) gesendet werden, der IPSec für die Verschlüsselung verwendet, kann das typische PPP-Frame Erfassungs Dienstprogramm nur PPP-Frames erfassen, die über ein verschlüsseltes Protokoll Identitäts Feld verfügen. In diesem Dokument wird erläutert, wie Sie einen Treiber entwickeln, der PPP-Frames in Windows Vista erfassen kann, bevor diese im sendepfad komprimiert/verschlüsselt werden oder nachdem Sie im Empfangs Pfad dekomprimiert/entschlüsselt wurden.

1.  Schreiben eines NDIS-Protokoll Treibers. Weitere Informationen finden Sie unter [NDIS 6,0-Protokoll Treiber](https://msdn.microsoft.com/library/ms795570.aspx) oder [NDIS-Protokoll Treiber (NDIS 5,1)](https://msdn.microsoft.com/library/ms801145.aspx).
2.  Installieren Sie den Treiber mit der Hardware Identität "MS \_ netmon". Ausführliche Anweisungen zum Installieren des Treibers mit einer bestimmten Hardware Identität finden Sie im [Abschnitt INF-Modelle](https://msdn.microsoft.com/library/ms794357.aspx).
    > [!Note]  
    > Jeder Windows Vista-Computer lässt die Installation von nur einer Treiber Entität zu, die über die \_ Hardware Identität "MS netmon" verfügt. Zum Installieren eines weiteren Treibers mit dieser Identität muss der erste Treiber deinstalliert werden. Ein Treiber, der ohne Verwendung der \_ Hardware Identität "MS netmon" installiert wird, kann die für die Erfassung von PPP-Frames erforderliche Bindung nicht ausführen.

     

3.  Der Protokoll Treiber sollte "ndiswanbh" als Bindungsschnittstelle zum Erfassen von PPP-Frames angeben. Ausführliche Anweisungen finden Sie unter [Angeben von bindungsschnittstellen](https://msdn.microsoft.com/library/aa937923.aspx).
4.  Die [protocolbindadapter](https://msdn.microsoft.com/library/ms797311.aspx) -Implementierung im Treiber sollte "ndismediumwan" als Teil des mittelgroßen Arrays unterstützen, sodass der ndiswanbh-miniportedge mithilfe der [ndisopenadapter](https://msdn.microsoft.com/library/ms804862.aspx) -Funktion geöffnet werden kann.
5.  Wenn die [protocolopenadaptercomplete](https://msdn.microsoft.com/library/ms797287.aspx) -Funktion mit dem Status "NDIS-Status erfolgreich" aufgerufen wird \_ \_ , sollte der Protokoll Treiber die OID-ID des [ \_ \_ aktuellen \_ Paket \_ Filters](https://msdn.microsoft.com/library/bb314089.aspx) mit den Flags " [ \_ \_ \_ Promiscuous](https://msdn.microsoft.com/library/bb314089.aspx) " und " [NDIS \_ Packet \_ Type \_ All \_ local](https://msdn.microsoft.com/library/bb314089.aspx) over this Binding" festlegen. Sobald dies erfolgt ist, empfängt der Protokoll Treiber die entschlüsselten PPP-Frames von der PPP-Frame Schicht in seiner [protocolreceive](https://msdn.microsoft.com/library/ms797274.aspx) -Funktion.

> [!Note]  
> Diese Informationen gelten nur für Treiber auf einem Windows Vista-Computer.

 

 

 




