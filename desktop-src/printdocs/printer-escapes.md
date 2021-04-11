---
description: Die Drucker Escapezeichen werden von Windows-Geräten mit 16-Bit-Zugriff auf spezielle Geräte bereitgestellt.
ms.assetid: 4bdd1d47-8cf4-4088-aec8-88193e71a828
title: Drucker Escapezeichen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59463c4201e97c5ac1ec689a772581fab28314b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216631"
---
# <a name="printer-escapes"></a>Drucker Escapezeichen

Die Drucker Escapezeichen werden von Windows-Geräten mit 16-Bit-Zugriff auf spezielle Geräte bereitgestellt. Die meisten dieser Escapezeichen sind veraltet, aber einige werden bereitgestellt, um das Portieren von Windows-basierten 16-Bit-Anwendungen zu vereinfachen. GDI unterstützt einen kompletten Satz von Pfad Funktionen, die von Anwendungen anstelle der Escapezeichen zum Zeichnen von Pfaden auf beliebigen Geräten verwendet werden können. Eine Liste der Funktionen, die einige der Escapezeichen ersetzen, finden Sie in der [**Escape**](/windows/desktop/api/Wingdi/nf-wingdi-escape) -Funktion.

Von den 64 ursprünglichen Drucker Escapezeichen können nur **queryescsupport** und **Passthrough** verwendet werden.

Es ist auch eine erweiterte escapefunktion mit dem Namen " [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)" vorhanden. Diese Funktion ermöglicht Anwendungen den Zugriff auf Funktionen eines bestimmten Geräts, das nicht direkt über GDI verfügbar ist.

 

 



