---
title: Arrays und Zeiger
description: Der Remoteprozeduraufruf (Remote Procedure Call, RPC) ist für Entwickler größtenteils transparent.
ms.assetid: 5ad5a51d-a821-44a5-bbc3-14409cb42cb4
keywords:
- Rpc-Aufruf einer Remoteprozedur , beschrieben, Arrays und Zeiger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26cc588d4db7cb222ec0fb2689bf645a2a7ed0e12b632392264d480c26777531
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073500"
---
# <a name="arrays-and-pointers"></a>Arrays und Zeiger

Der Remoteprozeduraufruf (Remote Procedure Call, RPC) ist für Entwickler größtenteils transparent. Um diese Transparenz zu erreichen, überträgt der Clientstub sowohl den Zeiger als auch das Datenobjekt, auf das er zeigt, an den Server. Wenn die Remoteprozedur die Daten ändert, muss der Server die neuen Daten zurück an den Client übertragen, damit der Client die neuen Daten über die ursprünglichen Daten kopieren kann.

Im Allgemeinen verhält sich ein Remoteprozeduraufruf wie ein lokaler Prozeduraufruf. Wenn ein Zeiger ein Parameter ist, kann die Remoteprozedur auf das Datenobjekt zugreifen, auf das der Zeiger verweist, auf die gleiche Weise wie eine lokale Prozedur.

Da Client- und Serverprogramme in unterschiedlichen Adressräumen ausgeführt werden, müssen Entwickler midl-Attribute (Microsoft Interface Definition Language) verwenden, um zu beschreiben, wie Array- und Zeigerdaten zwischen dem Client und dem Server übertragen werden. Dieser Abschnitt enthält eine Übersicht über die Verwendung von Arrays und Zeigern in verteilten Anwendungen in den folgenden Themen:

-   [Arrays und RPC](arrays-and-rpc.md)
-   [Zeiger und RPC](pointers-and-rpc.md)
-   [Verwenden von Arrays, Zeichenfolgen und Zeigern](using-arrays-strings-and-pointers.md)

 

 




