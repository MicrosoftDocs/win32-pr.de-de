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
# <a name="specifying-a-follow-set"></a><span data-ttu-id="90a96-104">Angeben eines folgenden Satzes</span><span class="sxs-lookup"><span data-stu-id="90a96-104">Specifying a Follow Set</span></span>

<span data-ttu-id="90a96-105">Ein nachfolgenden Satz gibt die Protokolle an, die einem Protokoll folgen.</span><span class="sxs-lookup"><span data-stu-id="90a96-105">A follow set specifies the protocols that follow a protocol.</span></span> <span data-ttu-id="90a96-106">Netzwerkmonitor verwendet einen nachfolgenden Satz, wenn der Parser das nächste Protokoll aus den Daten in einer Protokoll Instanz nicht identifizieren kann.</span><span class="sxs-lookup"><span data-stu-id="90a96-106">Network Monitor uses a follow set when the parser cannot identify the next protocol from the data in a protocol instance.</span></span>

<span data-ttu-id="90a96-107">Der NetBIOS-Parser gibt z. b. ein Resultset an, da die Daten im NetBIOS-Protokoll nicht bestimmen, welches Protokoll als Nächstes verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="90a96-107">For example, the NetBIOS parser specifies a follow set because the data in the NetBIOS protocol does not identify which protocol is next.</span></span> <span data-ttu-id="90a96-108">Folglich muss der NetBIOS-Parser einen nachfolgenden Satz aller Protokolle erstellen, die möglicherweise befolgt werden.</span><span class="sxs-lookup"><span data-stu-id="90a96-108">As a result the NetBIOS parser must create a follow set of all the protocols that may follow.</span></span>

<span data-ttu-id="90a96-109">Im folgenden Codebeispiel wird der NetBIOS-nach Verfolgungs Satz in der [*Parser.ini*](p.md) -Datei identifiziert.</span><span class="sxs-lookup"><span data-stu-id="90a96-109">The following code example identifies the NetBIOS follow set in the [*Parser.ini*](p.md) file.</span></span> <span data-ttu-id="90a96-110">Der folgende Satz enthält Server Message Block (SMB) und Microsoft Remote Procedure-Aufruf Protokolle (Msrpc).</span><span class="sxs-lookup"><span data-stu-id="90a96-110">The follow set contains server message block (SMB), and Microsoft remote procedure call (MSRPC) protocols.</span></span> <span data-ttu-id="90a96-111">Dies sind die einzigen Protokolle, die einer Instanz des NetBIOS-Protokolls folgen können.</span><span class="sxs-lookup"><span data-stu-id="90a96-111">These are the only protocols that can follow an instance of the NetBIOS protocol.</span></span>

``` syntax
[NETBIOS]
   Comment    = "Network Basic Input/Output System protocol"
   FollowSet  = SMB, MSRPC
   HelpFile   =
```

<span data-ttu-id="90a96-112">Ein Parser gibt bei der Implementierung der [**parserautoinstallinfo**](parserautoinstallinfo.md) -Funktion einen nachfolgenden Satz an.</span><span class="sxs-lookup"><span data-stu-id="90a96-112">A parser specifies a follow set during the implementation of the [**ParserAutoInstallInfo**](parserautoinstallinfo.md) function.</span></span> <span data-ttu-id="90a96-113">Ein Parser kann angeben, welche Protokolle vorangestellt sind und welche Protokolle befolgt werden.</span><span class="sxs-lookup"><span data-stu-id="90a96-113">A parser can specify which protocols precede, and which protocols follow.</span></span> <span data-ttu-id="90a96-114">Wenn ein Parser die Protokolle angibt, die vorangestellt sind, fügt Netzwerkmonitor das parserprotokoll den folgenden Sätzen der angegebenen Protokolle hinzu.</span><span class="sxs-lookup"><span data-stu-id="90a96-114">When a parser specifies the protocols that precede, Network Monitor adds the parser protocol to the follow sets of the specified protocols.</span></span> <span data-ttu-id="90a96-115">Wenn ein Parser die folgenden Protokolle angibt, erstellt Netzwerkmonitor einen neuen Abschnitt in der Parser.ini-Datei, die den folgenden parsersatz enthält.</span><span class="sxs-lookup"><span data-stu-id="90a96-115">When a parser specifies the protocols that follow, Network Monitor creates a new section in the Parser.ini file that includes the follow set of the parser.</span></span>

 

 



