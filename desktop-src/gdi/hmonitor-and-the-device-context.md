---
description: Jede physische Anzeige wird durch ein Monitor Handle des Typs Hmonitor dargestellt.
ms.assetid: c43c1401-52d3-485e-a418-205df5737040
title: Hmonitor und der Gerätekontext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7da397af45b906a626f79f7b934b78aaad481f9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993982"
---
# <a name="hmonitor-and-the-device-context"></a>Hmonitor und der Gerätekontext

Jede physische Anzeige wird durch ein Monitor Handle des Typs **Hmonitor** dargestellt. Ein gültiger **Hmonitor** ist garantiert ungleich NULL. Eine physische Anzeige hat denselben **Hmonitor** , solange Sie Teil des Desktops ist. Wenn eine " **WM \_ displaychange** "-Meldung gesendet wird, kann jeder Monitor vom Desktop entfernt werden, sodass der zugehörige **Hmonitor** ungültig wird oder seine Einstellungen geändert werden. Daher sollte eine Anwendung überprüfen, ob alle **hmonitors** gültig sind, wenn diese Nachricht gesendet wird.

Jede Funktion, die einen Anzeigegeräte Kontext (DC) zurückgibt, gibt normalerweise einen Domänen Controller für den primären Monitor zurück. Verwenden Sie die Funktion " [**enumdisplaymonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) ", um den DC für einen anderen Monitor zu erhalten. Oder Sie können den Gerätenamen aus der [**getmonitorinfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa) -Funktion verwenden, um einen Domänen Controller mit " [**kreatedc**](/windows/desktop/api/Wingdi/nf-wingdi-createdca)" zu erstellen. Wenn die Funktion, wie z. b. [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) oder [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint), jedoch einen Domänen Controller für ein Fenster erhält, das mehr als eine Anzeige umfasst, wird der Domänen Controller auch die beiden anzeigen überspannen.

 

 



