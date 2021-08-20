---
title: Pixelformatfunktionen
description: Die folgenden Windows-Funktionen verwalten Pixelformate.
ms.assetid: 78a6be75-72f6-4aef-a6bc-5f052c6fe2e9
keywords:
- WGL-Funktionen, Pixelformat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46c4b82a2b6cd91dd007cecf78065fa0c01204ecf468017ec7e121bd764c9ff2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119486330"
---
# <a name="pixel-format-functions"></a>Pixelformatfunktionen

Die folgenden Windows-Funktionen verwalten Pixelformate.



| Windows Funktion                                               | Beschreibung                                                                                                                                                           |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)                 | Abrufen des Pixelformats des Gerätekontexts, das dem angegebenen Pixelformat am nächsten kommt.                                                                      |
| [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)                       | Legt das aktuelle Pixelformat eines Gerätekontexts auf das Pixelformat fest, das von einem Pixelformatindex angegeben wird.                                                                   |
| [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)                       | Erhält den Pixelformatindex des aktuellen Pixelformats eines Gerätekontexts.                                                                                            |
| [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)             | Bei einem Gerätekontext und einem Pixelformatindex füllt eine [**PIXELFORMATDESCRIPTOR-Datenstruktur**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) mit den Eigenschaften des Pixelformats auf. |
| [**GetEnhMetaFilePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getenhmetafilepixelformat) | Ruft Pixelformatinformationen für eine erweiterte Metadatei ab.                                                                                                          |



 

Die [**ChoosePixelFormat-Funktion**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat) gibt einen einbasierten Pixelformatindex zurück, der die beste Übereinstimmung aus den unterstützten Pixelformaten des Gerätekontexts identifiziert.

Die [**SetPixelFormat-Funktion**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat) identifiziert das gewünschte Format mithilfe eines 1-basierten Pixelformatindexes. In der Regel rufen Sie **ChoosePixelFormat** auf, um ein Pixelformat mit der besten Übereinstimmung zu finden, und rufen dann **SetPixelFormat** mit dem Ergebnis **von ChoosePixelFormat auf.**

Wenn Sie **SetPixelFormat für einen Gerätekontext** aufrufen, der auf ein Fenster verweist, ändert **SetPixelFormat** auch das Pixelformat des Fensters. Das mehrfache Festlegen des Pixelformats eines Fensters kann zu erheblichen Schwierigkeiten für den Fenster-Manager und für Multithreadanwendungen führen, sodass dies nicht zulässig ist. Sie können das Pixelformat eines Fensters nur einmal festlegen. Danach kann das Pixelformat des Fensters nicht mehr geändert werden.

Die [**GetPixelFormat-Funktion**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat) gibt einen indexbasierten Pixelformatindex zurück.

Die [**DescribePixelFormat-Funktion**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) verwendet Folgendes als Parameter:

-   Ein Handle für einen Gerätekontext
-   Ein Index im Pixelformat
-   Ein Zeiger auf eine [**PIXELFORMATDESCRIPTOR-Datenstruktur**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor)

Die [**DescribePixelFormat-Funktion**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) gibt zurück, wenn die Member von **PIXELFORMATDESCRIPTOR** entsprechend festgelegt sind.

Die **GetEnhMetaFilePixelFormat-Funktion** gibt die Größe des Pixelformats einer Metadatei zurück und ruft die Pixelformatinformationen der Metadatei ab.

 

 




