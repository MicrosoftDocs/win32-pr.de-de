---
title: Lesen aus einer Datei
description: Lesen aus einer Datei
ms.assetid: 7c728304-7d05-4e28-a9bd-83b5b1af39be
keywords:
- Avifileingefo-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba1ffe866e454a898c5c3b91c7721c24f6a861ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037379"
---
# <a name="reading-from-a-file"></a>Lesen aus einer Datei

Mithilfe der [**avifileinfo**](/windows/desktop/api/Vfw/nf-vfw-avifileinfo) -Funktion können Sie Informationen zu einer geöffneten Datei abrufen. Diese Funktion füllt die [**avifileinfo**](/windows/desktop/api/Vfw/ns-vfw-avifileinfoa) -Struktur mit den folgenden Informationen aus: die maximale Datenrate, die Anzahl der Streams in der Datei, ob die Datei einen Index verwendet und ob die Datei urheberrechtlich geschützt ist.

Um ergänzende Informationen in einer AVI-Datei abzurufen, verwenden Sie die [**avifilereaddata**](/windows/desktop/api/Vfw/nf-vfw-avifilereaddata) -Funktion. Ergänzende Informationen gelten für die gesamte Datei und sind nicht in den normalen Datei Headern enthalten. Beispielsweise kann der Name des Unternehmens oder der Person, der die Urheberrechte einer Datei besitzt, zusätzliche Informationen sein. Ergänzende Informationen entsprechen nicht einem bestimmten Format. Sie kann Datei spezifisch sein. **Avifilereaddata** gibt die ergänzenden Informationen in einem von der Anwendung bereitgestellten Puffer zurück.

 

 




