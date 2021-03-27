---
description: TrueType-Schriftart Dateien enthalten Panose-Zahlen, die Anwendungen verwenden können, um eine Schriftart auszuwählen, die ihren Spezifikationen genau entspricht.
ms.assetid: 39fd56da-c744-432d-9623-92fc7d9bf5f5
title: Verwenden von Panose-Zahlen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dfa6a185e2afb05aec5fdf0e200300c7cf686a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217708"
---
# <a name="using-panose-numbers"></a>Verwenden von Panose-Zahlen

TrueType-Schriftart Dateien enthalten Panose-Zahlen, die Anwendungen verwenden können, um eine Schriftart auszuwählen, die ihren Spezifikationen genau entspricht. Das Panose-System klassifiziert Gesichter um 10 verschiedene Attribute. Weitere Informationen zu diesen Attributen finden Sie unter [**Panose**](/windows/win32/api/wingdi/ns-wingdi-panose). Eine **Panose** -Struktur ist Teil der [**outlinetextmetric**](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) -Struktur (deren Werte durch Aufrufen der [**getoutlinetextmetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) -Funktion ausgefüllt werden).

Die Panose-Attribute werden einzeln auf einer Skala bewertet. Die resultierenden Werte werden verkettet, um eine Zahl zu erhalten. Wenn diese Zahl für eine Schriftart und eine mathematische Metrik zum Messen der Entfernungen im Panose-Bereich festgelegt ist, kann eine Anwendung die nächsten Nachbarn ermitteln.

 

 



