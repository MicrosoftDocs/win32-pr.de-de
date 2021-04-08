---
title: RPC-Engine (RPC)
description: Die Engine für das Remote Prozedur Aufruf (RPC) Network Data Darstellung (NDR) ist das marshallingmodul der RPC-und DCOM-Komponenten.
ms.assetid: E452AA27-053D-4032-868B-CF2D5C0D4BE0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bf7ba92a74d2d7dc8c394c561f65337db13af99
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104039964"
---
# <a name="rpc-ndr-engine-rpc"></a>RPC-Engine (RPC)

Die Engine für das Remote Prozedur Aufruf (RPC) Network Data Darstellung (NDR) ist das marshallingmodul der RPC-und DCOM-Komponenten. Die NDR-Engine behandelt alle stubbezogenen Probleme eines Remote Aufrufes. Als Prozess wird das NDR-Marshalling durch den C-Code von mit mittlerer l generierten Stub, von einem Mittelwert-JIT-typgenerator oder durch von anderen Tools generierte Stub-und manuell geschriebene Stub-Vorgänge gesteuert. Die NDR-Engine steuert wiederum die zugrunde liegende Laufzeit (DCOM oder RPC), die mit bestimmten Transporten kommuniziert.

Obwohl es sich bei Stubs um C-Code handelt, die von mittlerer l generiert werden, wird empfohlen, Stubs als nicht transparent zu behandeln, und es wird dringend davon abgeraten, etwas innerhalb des Stubs zu ändern Das Verhalten ist nicht definiert, wenn diese NDR-Routinen außerhalb des Kontexts aufgerufen werden.

Die RPC-Engine-Engine wird in den folgenden Themen ausführlicher beschrieben:

-   [Übertragungs Syntax und NDR64](transfer-syntax-and-ndr64.md)
-   [RPC-Zeichen folgen im Format](rpc-ndr-format-strings.md)
-   [RPC-NDR-Schnittstellenreferenz](rpc-ndr-interface-reference.md)

 

 




