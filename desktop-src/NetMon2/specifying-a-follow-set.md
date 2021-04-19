---
description: Ein nachfolgenden Satz gibt die Protokolle an, die einem Protokoll folgen. Netzwerkmonitor verwendet einen nachfolgenden Satz, wenn der Parser das nächste Protokoll aus den Daten in einer Protokoll Instanz nicht identifizieren kann.
ms.assetid: 9e73c724-a540-42f8-b273-4f02c39d81c4
title: Angeben eines folgenden Satzes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b9e36268be82d2fed7c3d0c56a078e41dff1733
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359877"
---
# <a name="specifying-a-follow-set"></a>Angeben eines folgenden Satzes

Ein nachfolgenden Satz gibt die Protokolle an, die einem Protokoll folgen. Netzwerkmonitor verwendet einen nachfolgenden Satz, wenn der Parser das nächste Protokoll aus den Daten in einer Protokoll Instanz nicht identifizieren kann.

Der NetBIOS-Parser gibt z. b. ein Resultset an, da die Daten im NetBIOS-Protokoll nicht bestimmen, welches Protokoll als Nächstes verwendet werden soll. Folglich muss der NetBIOS-Parser einen nachfolgenden Satz aller Protokolle erstellen, die möglicherweise befolgt werden.

Im folgenden Codebeispiel wird der NetBIOS-nach Verfolgungs Satz in der [*Parser.ini*](p.md) -Datei identifiziert. Der folgende Satz enthält Server Message Block (SMB) und Microsoft Remote Procedure-Aufruf Protokolle (Msrpc). Dies sind die einzigen Protokolle, die einer Instanz des NetBIOS-Protokolls folgen können.

``` syntax
[NETBIOS]
   Comment    = "Network Basic Input/Output System protocol"
   FollowSet  = SMB, MSRPC
   HelpFile   =
```

Ein Parser gibt bei der Implementierung der [**parserautoinstallinfo**](parserautoinstallinfo.md) -Funktion einen nachfolgenden Satz an. Ein Parser kann angeben, welche Protokolle vorangestellt sind und welche Protokolle befolgt werden. Wenn ein Parser die Protokolle angibt, die vorangestellt sind, fügt Netzwerkmonitor das parserprotokoll den folgenden Sätzen der angegebenen Protokolle hinzu. Wenn ein Parser die folgenden Protokolle angibt, erstellt Netzwerkmonitor einen neuen Abschnitt in der Parser.ini-Datei, die den folgenden parsersatz enthält.

 

 



