---
description: Wenn die Anwendung mit ganzen Wörtern umgeht, werden gültige Positionen für die Einfügemarke durch den Wert des fwordstopp-Members der \_ logattr-Skript Struktur gekennzeichnet. Dieser Wert wird abgerufen, indem scriptbreak aufgerufen wird.
ms.assetid: c9bbfb51-727a-45ff-8450-774bc106f9f7
title: Verwenden von Wort Break Points
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b9cf68d5c90b6e93a6e6f15706ec357c7a33b23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218684"
---
# <a name="using-word-break-points"></a>Verwenden von Wort Break Points

Wenn die Anwendung mit ganzen Wörtern umgeht, werden gültige Positionen für die Einfügemarke durch den Wert des **fwordstopp** -Members der [**\_ logattr-Skript**](/windows/win32/api/usp10/ns-usp10-script_logattr) Struktur gekennzeichnet. Dieser Wert wird abgerufen, indem [**scriptbreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak)aufgerufen wird.

Gültige Positionen für den Umbruch von Zeilen zwischen Wörtern werden durch den von [**scriptbreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak)abgerufenen **fsoft Break** -Wert markiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von uniscri](using-uniscribe.md)
</dt> </dl>

 

 



