---
description: Jede physische Anzeige wird durch ein Monitorhandle vom Typ HMONITOR dargestellt.
ms.assetid: c43c1401-52d3-485e-a418-205df5737040
title: HMONITOR und der Gerätekontext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afb727457c388710b19d8f22bef8f65d76e9d8c5c27b0ec7dfcbf55a4acea3b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558750"
---
# <a name="hmonitor-and-the-device-context"></a>HMONITOR und der Gerätekontext

Jede physische Anzeige wird durch ein Monitorhandle vom Typ **HMONITOR** dargestellt. Ein gültiger **HMONITOR** ist garantiert ungleich NULL. Eine physische Anzeige weist den gleichen **HMONITOR** auf, solange sie Teil des Desktops ist. Wenn eine **WM \_ DISPLAYCHANGE-Nachricht** gesendet wird, kann jeder Monitor vom Desktop entfernt werden, weshalb **HMONITOR** ungültig wird oder seine Einstellungen geändert wurden. Daher sollte eine Anwendung überprüfen, ob alle **HMONITORS** gültig sind, wenn diese Nachricht gesendet wird.

Jede Funktion, die einen Anzeigegerätekontext (DC) zurückgibt, gibt normalerweise einen DC für den primären Monitor zurück. Verwenden Sie die Funktion [**EnumDisplayMonitors,**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) um den DC für einen anderen Monitor abzurufen. Alternativ können Sie den Gerätenamen aus der [**GetMonitorInfo-Funktion**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa) verwenden, um mit [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca)einen DC zu erstellen. Wenn die Funktion, z. B. [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) oder [**BeginPaint,**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)jedoch einen DC für ein Fenster erhält, das mehr als eine Anzeige umfasst, umfasst der DC auch die beiden Anzeigen.

 

 



