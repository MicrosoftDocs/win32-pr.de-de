---
description: Sie können Karten innerhalb von Lesern nachverfolgen. Diese Routinen verwenden in der Regel die Struktur "SCard \_ ReaderState" in einem Array.
ms.assetid: b26b26bf-85ff-435f-a679-7529f19b1c1b
title: Smartcard-nach Verfolgungs Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde9bebfeea2718ce634d585c2740cb510500ce3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867456"
---
# <a name="smart-card-tracking-functions"></a>Smartcard-nach Verfolgungs Funktionen

Mit den folgenden Funktionen können Sie Karten innerhalb von Lesern nachverfolgen. Diese Routinen verwenden in der Regel die Struktur " [**SCard \_ ReaderState**](/windows/desktop/api/Winscard/ns-winscard-scard_readerstatea) " in einem Array.



| Thema                                                | BESCHREIBUNG                                                                                                                            |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Scardlogecards**](/windows/desktop/api/Winscard/nf-winscard-scardlocatecardsa)         | Suchen Sie nach einer Karte, deren [*ATR-Zeichen*](../secgloss/a-gly.md) Folge mit einem angegebenen Kartennamen übereinstimmt. |
| [**ScardGetStatusChange**](/windows/desktop/api/Winscard/nf-winscard-scardgetstatuschangea) | Blockiert die Ausführung, bis die aktuelle Verfügbarkeit von Karten geändert wird.                                                                       |
| [**"SCardCancel"**](/windows/desktop/api/Winscard/nf-winscard-scardcancel)                   | Beenden Sie ausstehende Aktionen.                                                                                                         |



 

 

 
