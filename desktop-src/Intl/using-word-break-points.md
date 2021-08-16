---
description: Wenn die Anwendung ganze Wörter verwendet, werden gültige Positionen für das Caret-Zeichen durch den Wert des fWordStop-Members der SCRIPT \_ LOGATTR-Struktur gekennzeichnet. Dieser Wert wird durch einen Aufruf von ScriptBreak abgerufen.
ms.assetid: c9bbfb51-727a-45ff-8450-774bc106f9f7
title: Verwenden von Wörterpausenpunkten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 733d761d15299e02fbfb84d541a7ceba5d4d77a9b57e0280bfeedee24532d8cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146863"
---
# <a name="using-word-break-points"></a>Verwenden von Wörterpausenpunkten

Wenn die Anwendung ganze Wörter verwendet, werden gültige Positionen für das Caret-Zeichen durch den Wert des **fWordStop-Members** der [**SCRIPT \_ LOGATTR-Struktur**](/windows/win32/api/usp10/ns-usp10-script_logattr) gekennzeichnet. Dieser Wert wird abgerufen, indem [**ScriptBreak aufgerufen wird.**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak)

Gültige Positionen für zeilenbrechende Zeilen zwischen Wörtern werden durch den **fSoftBreak-Wert** markiert, der von [**ScriptBreak abgerufen wird.**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 



