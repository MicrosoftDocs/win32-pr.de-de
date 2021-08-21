---
title: Lesen aus einer Datei
description: Lesen aus einer Datei
ms.assetid: 7c728304-7d05-4e28-a9bd-83b5b1af39be
keywords:
- AVIFileInfo-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab95186b1ec8913623b0ab02e0d2bc5556302d4dcd03f7737ac12c5872b9f2fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371686"
---
# <a name="reading-from-a-file"></a>Lesen aus einer Datei

Sie können Informationen zu einer geöffneten Datei mithilfe der [**FUNKTION AVIFileInfo**](/windows/desktop/api/Vfw/nf-vfw-avifileinfo) abrufen. Diese Funktion füllt die [**AVIFILEINFO-Struktur**](/windows/desktop/api/Vfw/ns-vfw-avifileinfoa) mit Informationen wie der maximalen Datenrate, der Anzahl der Datenströme in der Datei, der Verwendung eines Index in der Datei und der Frage, ob die Datei urheberrechtlich geschützt ist.

Verwenden Sie die [**FUNKTION AVIFileReadData,**](/windows/desktop/api/Vfw/nf-vfw-avifilereaddata) um ergänzende Informationen in einer AVI-Datei abzurufen. Ergänzende Informationen gelten für die gesamte Datei und sind nicht in den normalen Dateiheadern enthalten. Beispielsweise kann der Name des Unternehmens oder der Person, die die Copyrights einer Datei besitzt, ergänzende Informationen sein. Ergänzende Informationen haben kein bestimmtes Format. kann dateispezifisch sein. **AVIFileReadData gibt** die ergänzenden Informationen in einem von der Anwendung bereitgestellten Puffer zurück.

 

 




