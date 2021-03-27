---
description: Das System reduziert das Hauptfenster einer Anwendung (Überlappendes Format) in ein minimiertes Fenster, wenn der Benutzer im Menü "Fenster" auf "minimieren" klickt, oder die Anwendung die Funktion "ShowWindow" aufruft und einen Wert wie z \_ . b. SW
ms.assetid: a52dba49-e4ec-45e2-a00f-211a58e28773
title: Minimierte Fenster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c792a90dba2526b6d09fabf8281fc74ebfe96667
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754377"
---
# <a name="minimized-windows"></a>Minimierte Fenster

Das System reduziert das Hauptfenster einer Anwendung (Überlappendes Format) in ein minimiertes Fenster, wenn der Benutzer im Menü "Fenster" auf "minimieren" klickt, oder die Anwendung die Funktion " [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) " aufruft und einen Wert wie z \_ . b. SW Durch das Minimieren eines Fensters wird die Systemleistung beschleunigt, indem die Arbeitsschritte reduziert werden, die eine Anwendung beim Aktualisieren des Hauptfensters ausführen muss.

Bei einer typischen Anwendung zeichnet das System ein Symbol, das als Klassen Symbol bezeichnet wird, wenn das Fenster minimiert wird, wobei das Symbol mit dem Namen des Fensters beschriftet wird. Das Klassen Symbol, ein statisches Bild, das die Anwendung darstellt, wird von der Anwendung beim Registrieren der Fenster Klasse angegeben. Die Anwendung weist dem Klassen Symbol dem **HICON** -Member von [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) ein Handle zu, bevor [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa)aufgerufen wird. Die Anwendung kann die [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) -Funktion verwenden, um das Symbol Handle abzurufen.

 

 
