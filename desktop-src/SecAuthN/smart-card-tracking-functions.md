---
description: Lassen Sie Karten innerhalb von Lesern nachverfolgen. Diese Routinen verwenden in der Regel die SCARD \_ READERSTATE-Struktur innerhalb eines Arrays.
ms.assetid: b26b26bf-85ff-435f-a679-7529f19b1c1b
title: Smartcard-Nachverfolgungsfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 581b81ce357cf683d29c1a86d48993c16b7f363635b8e6e3c7e0f2a6ad0900f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118917340"
---
# <a name="smart-card-tracking-functions"></a>Smartcard-Nachverfolgungsfunktionen

Mit den folgenden Funktionen können Sie Karten innerhalb von Readern nachverfolgen. Diese Routinen verwenden in der Regel die [**SCARD \_ READERSTATE-Struktur**](/windows/desktop/api/Winscard/ns-winscard-scard_readerstatea) innerhalb eines Arrays.



| Thema                                                | BESCHREIBUNG                                                                                                                            |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**SCardLocateCards**](/windows/desktop/api/Winscard/nf-winscard-scardlocatecardsa)         | Suchen Sie nach einer Karte, [*deren ATR-Zeichenfolge*](../secgloss/a-gly.md) einem angegebenen Kartennamen entspricht. |
| [**SCardGetStatusChange**](/windows/desktop/api/Winscard/nf-winscard-scardgetstatuschangea) | Blockiert die Ausführung, bis sich die aktuelle Verfügbarkeit von Karten ändert.                                                                       |
| [**SCardCancel**](/windows/desktop/api/Winscard/nf-winscard-scardcancel)                   | Beenden ausstehender Aktionen.                                                                                                         |



 

 

 
