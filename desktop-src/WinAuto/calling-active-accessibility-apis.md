---
title: Aufrufen von Active Accessibility-APIs
description: Microsoft Active Accessibility stellt APIs (Application Programming Interfaces) für Clients und Server bereit.
ms.assetid: c40441d2-7294-4c76-8b42-08ed66eccb7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209a239495fddbcaf2275f095abc889295568b3c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039133"
---
# <a name="calling-active-accessibility-apis"></a>Aufrufen von Active Accessibility-APIs

Microsoft Active Accessibility stellt APIs (Application Programming Interfaces) für Clients und Server bereit. Die meisten werden in der Microsoft Active Accessibility Dynamic-Link Library, Oleacc.dll implementiert, aber [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent), [**setwineventhook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook)und [**unthookwinevent**](/windows/desktop/api/Winuser/nf-winuser-unhookwinevent) werden in user32.dll implementiert. Dies ist eine Kernkomponente des Microsoft Windows-Betriebssystems.

Auf Computern, auf denen Windows 95 oder Microsoft Windows NT 4,0 ausgeführt wird, ist Oleacc.dll und die richtige Version von user32.dll nicht installiert, da Microsoft Active Accessibility in Phasen in nachfolgende Versionen von Windows integriert wurde. Daher werden Anwendungen, die auf diesen Plattformen ausgeführt werden, mithilfe der [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion explizit mit Oleacc.dll verknüpft, anstatt sich auf Import Bibliotheken zu verlassen. Active Accessibility 1,3 unterstützt Windows 95 und Microsoft Windows NT 4,0. Frühere Versionen von Windows werden von Microsoft Active Accessibility nicht unterstützt.

Server Anwendungen verwenden die [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion, um die Adresse einer Microsoft Active Accessibility-Funktion abzurufen, und führen den Abruf dann über einen Funktionszeiger aus. Wenn eine Funktion aufgerufen wird, die in Oleacc.dll implementiert wurde, verwenden Server Anwendungen das Handle, das von [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) im Aufruf von **GetProcAddress** zurückgegeben wurde. Wenn eine in user32.dll definierte Funktion aufgerufen wird, rufen Server Anwendungen [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) auf, indem Sie "User32" angeben, und verwenden Sie das zurückgegebene Modul Handle im Aufruf von **GetProcAddress**.

Wenn eine Anwendung z. b. [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent)verwendet, ruft Sie [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) mithilfe des Modul Handles user32.dll auf, um die Adresse der Funktion zu erhalten. Wenn der-Vorgang erfolgreich ist (was bedeutet, dass diese Version von Windows Microsoft Active Accessibility unterstützt), legt die Anwendung ein Flag fest, das angibt, dass es sicher ist, **NotifyWinEvent** aufzurufen. Die von **GetProcAddress** empfangene Adresse wird in einer Funktionszeiger Variablen gespeichert und im gesamten Code verwendet.

 

 