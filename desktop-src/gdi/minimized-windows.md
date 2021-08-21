---
description: Das System reduziert das Hauptfenster einer Anwendung (überlappender Stil) auf ein minimiertes Fenster, wenn der Benutzer im Fenstermenü auf Minimieren klickt oder die Anwendung die ShowWindow-Funktion aufruft und einen Wert wie SW \_ MINIMIZE angibt.
ms.assetid: a52dba49-e4ec-45e2-a00f-211a58e28773
title: Minimierte Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d9633c3bcba452e4708c6a48557fe547eff03c4e2a6801e3669da2faa768272
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118760030"
---
# <a name="minimized-windows"></a>Minimierte Windows

Das System reduziert das Hauptfenster einer Anwendung (überlappender Stil) auf ein minimiertes Fenster, wenn der Benutzer im Fenstermenü auf Minimieren klickt oder die Anwendung die [**ShowWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-showwindow) aufruft und einen Wert wie SW \_ MINIMIZE angibt. Die Minimierung eines Fensters beschleunigt die Systemleistung, indem die Arbeitsmenge reduziert wird, die eine Anwendung beim Aktualisieren des Hauptfensters tun muss.

Für eine typische Anwendung zeichnet das System ein Symbol, das als Klassensymbol bezeichnet wird, wenn das Fenster minimiert wird, und bezeichnet das Symbol mit dem Namen des Fensters. Das Klassensymbol, ein statisches Bild, das die Anwendung darstellt, wird von der Anwendung beim Registrieren der Fensterklasse angegeben. Die Anwendung weist dem **hIcon-Member** von [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) vor dem Aufruf von RegisterClass ein Handle [**zum Klassensymbol zu.**](/windows/win32/api/winuser/nf-winuser-registerclassa) Die Anwendung kann die [**LoadIcon-Funktion**](/windows/win32/api/winuser/nf-winuser-loadicona) verwenden, um das Symbolhand handle abzurufen.

 

 
