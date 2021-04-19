---
title: Überwachen des Fortschritts von Kompressoren und Dekompressoren
description: Überwachen des Fortschritts von Kompressoren und Dekompressoren
ms.assetid: 6507be44-1916-46b2-bae3-c4fe633cdc5a
keywords:
- Videokomprimierungs-Manager (VCM), Überwachung
- VCM (Videokomprimierungs-Manager), Überwachung
- Icsetstatusproc-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39ef5449e8d4e985217ee60f075d22b16dcc5c3b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338193"
---
# <a name="monitoring-the-progress-of-compressors-and-decompressors"></a>Überwachen des Fortschritts von Kompressoren und Dekompressoren

Die Anwendung kann den Fortschritt eines langwierigen Vorgangs überwachen, der von einem Kompressor oder Dekompressor durchgeführt wird, indem Sie die Adresse einer Rückruffunktion sendet. Sie können die [**icsetstatusproc**](/windows/desktop/api/Vfw/nf-vfw-icsetstatusproc) -Funktion verwenden, um die Adresse an den Kompressor oder Dekompressor zu senden. Wenn der-Kompressor oder der Dekompressor diese Adresse empfängt, sendet er Statusmeldungen an die-Funktion. Diese Meldungen geben an, ob der Vorgang gestartet, angehalten, bereitstellt oder fortgesetzt wird.

 

 




