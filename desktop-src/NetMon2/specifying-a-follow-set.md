---
description: Ein Folgesatz gibt die Protokolle an, die einem Protokoll folgen. Netzwerkmonitor verwendet einen Folgesatz, wenn der Parser das nächste Protokoll nicht anhand der Daten in einer Protokollinstanz identifizieren kann.
ms.assetid: 9e73c724-a540-42f8-b273-4f02c39d81c4
title: Angeben eines Folgesatzes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b11320872cc07d69f5796e344a1d5ed4dea4594e48f9697901126d915fd7b42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118363046"
---
# <a name="specifying-a-follow-set"></a>Angeben eines Folgesatzes

Ein Folgesatz gibt die Protokolle an, die einem Protokoll folgen. Netzwerkmonitor verwendet einen Folgesatz, wenn der Parser das nächste Protokoll nicht anhand der Daten in einer Protokollinstanz identifizieren kann.

Beispielsweise gibt der NetBIOS-Parser einen Folgesatz an, da die Daten im NetBIOS-Protokoll nicht identifizieren, welches Protokoll als Nächstes verwendet wird. Daher muss der NetBIOS-Parser einen Folgesatz aller Protokolle erstellen, die möglicherweise folgen.

Im folgenden Codebeispiel wird der NetBIOS-Follow-Satz in der [*dateiParser.ini*](p.md) identifiziert. Der folgende Satz enthält SMB-Protokolle (Server Message Block) und MSRPC-Protokolle (Microsoft Remote Procedure Call). Dies sind die einzigen Protokolle, die einer Instanz des NetBIOS-Protokolls folgen können.

``` syntax
[NETBIOS]
   Comment    = "Network Basic Input/Output System protocol"
   FollowSet  = SMB, MSRPC
   HelpFile   =
```

Ein Parser gibt einen Folgesatz während der Implementierung der [**ParserAutoInstallInfo-Funktion**](parserautoinstallinfo.md) an. Ein Parser kann angeben, welche Protokolle vorangestellt sind und welche Protokolle folgen. Wenn ein Parser die vorangehenden Protokolle angibt, fügt Netzwerkmonitor das Parserprotokoll den folgenden Sätzen der angegebenen Protokolle hinzu. Wenn ein Parser die folgenden Protokolle angibt, erstellt Netzwerkmonitor einen neuen Abschnitt in der datei Parser.ini, der den folgenden Satz des Parsers enthält.

 

 



