---
description: Die von 16-Bit-Windows bereitgestellten Drucker-Escapezeichen lassen den Zugriff auf spezielle Gerätefeatures zu.
ms.assetid: 4bdd1d47-8cf4-4088-aec8-88193e71a828
title: Drucker-Escapen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dd8bc842e60ca0019fc523b27a4657e66a623cda4802bfdb489213b694fd432
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119711560"
---
# <a name="printer-escapes"></a>Drucker-Escapen

Die von 16-Bit-Windows bereitgestellten Drucker-Escapezeichen lassen den Zugriff auf spezielle Gerätefeatures zu. Die meisten dieser Escapezeichen sind veraltet, aber einige werden bereitgestellt, um die Portierung von 16-Bit-Windows-basierten Anwendungen zu vereinfachen. GDI unterstützt einen vollständigen Satz von Pfadfunktionen, die Anwendungen anstelle der Escapes verwenden können, um Pfade auf jedem Gerät zu zeichnen. Eine Liste der Funktionen, die einige der Escapes ersetzen, finden Sie unter Der [**Escape-Funktion.**](/windows/desktop/api/Wingdi/nf-wingdi-escape)

Von den 64 ursprünglichen Drucker-Escapedateien können nur **QUERYESCSUPPORT** und **PASSTHROUGH** verwendet werden.

Es gibt auch eine erweiterte Escapefunktion namens [**ExtEscape.**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) Mit dieser Funktion können Anwendungen auf Funktionen eines bestimmten Geräts zugreifen, die nicht direkt über GDI verfügbar sind.

 

 



