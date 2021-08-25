---
description: 'Mit den folgenden Funktionen kann eine Anwendung einen Gerätekontext speichern, wiederherstellen und zurücksetzen: SaveDC, RestoreDC und ResetDC.'
ms.assetid: 22837876-2665-49c6-908e-80e107fc09f4
title: Speichern, Wiederherstellen und Zurücksetzen eines Gerätekontexts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 434ef484fecee17251a31616e396ee0fa66b381bc30cf858575f4455ca36a1ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965250"
---
# <a name="saving-restoring-and-resetting-a-device-context"></a>Speichern, Wiederherstellen und Zurücksetzen eines Gerätekontexts

Die folgenden Funktionen ermöglichen einer Anwendung das Speichern, Wiederherstellen und Zurücksetzen eines Gerätekontexts: [**SaveDC,**](/windows/desktop/api/Wingdi/nf-wingdi-savedc) [**RestoreDC**](/windows/desktop/api/Wingdi/nf-wingdi-restoredc)und [**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca). Die SaveDC-Funktion zeichnet auf einem speziellen GDI-Stapel die Grafikobjekte des aktuellen Domänencontrollers sowie deren Attribute und Grafikmodi auf. Eine Zeichnungsanwendung kann diese Funktion aufrufen, bevor ein Benutzer mit dem Zeichnen beginnt, und den ursprünglichen Zustand der Anwendung speichern, um eine saubere Tafel für den Benutzer zu erhalten. Um zu diesem ursprünglichen Zustand zurückzukehren, ruft die Anwendung die RestoreDC-Funktion auf.

[**ResetDC wird**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca) bereitgestellt, um die Dc-Daten des Druckers zurückzusetzen. Eine Anwendung ruft diese Funktion auf, um die Papierausrichtung, die Papiergröße, den Ausgabeskalierungsfaktor, die Anzahl der zu druckenden Kopien, die Papierquelle (oder den Papierbehälter), den Duplexmodus und so weiter zurückzusetzen. In der Regel ruft eine Anwendung diese Funktion auf, nachdem ein Benutzer eine der Druckeroptionen geändert hat und das System eine [**WM \_ DEVMODECHANGE-Nachricht ausgegeben**](wm-devmodechange.md) hat.

 

 



