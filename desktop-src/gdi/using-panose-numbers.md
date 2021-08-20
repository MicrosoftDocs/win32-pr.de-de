---
description: TrueType-Schriftartdateien enthalten PANOSE-Nummern, mit denen Anwendungen eine Schriftart auswählen können, die ihren Spezifikationen sehr genau entspricht.
ms.assetid: 39fd56da-c744-432d-9623-92fc7d9bf5f5
title: Verwenden von PANOSE-Zahlen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a974a0d1e708cac931e06e386e2df0802cbea79e5c9d499ca460d6deb5b0bab9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037458"
---
# <a name="using-panose-numbers"></a>Verwenden von PANOSE-Zahlen

TrueType-Schriftartdateien enthalten PANOSE-Nummern, mit denen Anwendungen eine Schriftart auswählen können, die ihren Spezifikationen sehr genau entspricht. Das PANOSE-System klassifiziert Gesichter nach 10 verschiedenen Attributen. Weitere Informationen zu diesen Attributen finden Sie unter [**PANOSE**](/windows/win32/api/wingdi/ns-wingdi-panose). Eine **PANOSE-Struktur** ist Teil der [**OUTLINETEXTMETRIC-Struktur**](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) (deren Werte durch Aufrufen der [**GetOutlineTextMetrics-Funktion ausgefüllt**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) werden).

Die PANOSE-Attribute werden einzeln auf einer Skala bewertet. Die resultierenden Werte werden verkettet, um eine Zahl zu erzeugen. Bei dieser Zahl für eine Schriftart und einer mathematischen Metrik zum Messen von Entfernungen im PANOSE-Raum kann eine Anwendung die nächsten Nachbarn bestimmen.

 

 



