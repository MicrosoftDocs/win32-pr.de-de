---
title: Aufrufen von Active Accessibility-APIs
description: Microsoft Active Accessibility stellt APIs (Application Programming Interfaces) sowohl für Clients als auch für Server bereit.
ms.assetid: c40441d2-7294-4c76-8b42-08ed66eccb7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6a54bc297af42546a081c3478ef109be137d8af19a37ea39415e8b0d2c06ccc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122240"
---
# <a name="calling-active-accessibility-apis"></a>Aufrufen von Active Accessibility-APIs

Microsoft Active Accessibility stellt APIs (Application Programming Interfaces) sowohl für Clients als auch für Server bereit. Die meisten werden in der dynamic-link-Bibliothek Microsoft Active Accessibility Oleacc.dll implementiert, aber [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent), [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook)und [**UnhookWinEvent**](/windows/desktop/api/Winuser/nf-winuser-unhookwinevent) werden in user32.dll implementiert. Dies ist eine Kernkomponente des Betriebssystems Microsoft Windows.

Auf Computern, auf denen Windows 95 oder Microsoft Windows NT 4.0 ausgeführt wird, sind keine Oleacc.dll und die richtige Version von user32.dll installiert, da Microsoft Active Accessibility phasenweise in die nachfolgenden Versionen von Windows integriert wurde. Daher verknüpfen Anwendungen, die auf diesen Plattformen ausgeführt werden, explizit mit Oleacc.dll zur Laufzeit, indem sie die [**LoadLibrary-Funktion**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) verwenden, anstatt sich auf Importbibliotheken zu verlassen. Active Accessibility 1.3 unterstützt Windows 95 und Microsoft Windows NT 4.0. Frühere Versionen von Windows werden von Microsoft Active Accessibility nicht unterstützt.

Serveranwendungen verwenden die [**GetProcAddress-Funktion,**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) um die Adresse einer Microsoft Active Accessibility Funktion abzurufen und dann den Aufruf über einen Funktionszeiger vorzunehmen. Beim Aufrufen einer Funktion, die in Oleacc.dll implementiert wurde, verwenden Serveranwendungen das handle, das von [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) im Aufruf von **GetProcAddress** zurückgegeben wird. Wenn eine in user32.dll definierte Funktion aufgerufen wird, rufen Serveranwendungen [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) unter Angabe von "USER32" auf und verwenden das zurückgegebene Modulhandle im Aufruf von **GetProcAddress**.

Wenn eine Anwendung beispielsweise [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent)verwendet, ruft sie [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) mithilfe des Modulhandle von user32.dll auf, um die Adresse der Funktion abzurufen. Wenn der Aufruf erfolgreich ist (d. h., diese Version von Windows unterstützt Microsoft Active Accessibility), legt die Anwendung ein Flag fest, das angibt, dass **notifyWinEvent** sicher aufgerufen werden kann. Die von **GetProcAddress empfangene** Adresse wird in einer Funktionszeigervariablen gespeichert und im gesamten Code verwendet.

 

 