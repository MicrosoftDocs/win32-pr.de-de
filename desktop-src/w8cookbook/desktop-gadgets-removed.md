---
title: Desktop-Mini Anwendungen entfernt
description: Desktop-Mini Anwendungen entfernt
ms.assetid: 0074204B-F568-4F9B-A0F7-3E330B91E4CD
keywords:
- Geschenken
- Desktop Gadgets
- Windows-Rand Leiste
- Seitenleiste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c37c058a75aca82d7727566041af4c30f3bb474
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "104391105"
---
# <a name="desktop-gadgets-removed"></a>Desktop-Mini Anwendungen entfernt

## <a name="platforms"></a>Plattformen

 **Clients** -Windows 8  
**Server** -Windows Server 2012  



## <a name="description"></a>BESCHREIBUNG

Aus Funktionalitäts Sicht wurden Gadgets bereits als veraltet markiert und werden von neuen Live-Kacheln und-apps ausgegeben. Mini Anwendungen stellen auch ein Sicherheitsrisiko für Benutzer dar. Als Plattform gibt es Sicherheitsrisiken, sodass selbst gutartige Gadgets ausgenutzt werden könnten. Um Windows 8 als modernes und sicheres Betriebssystem zu unterstützen, haben wir daher entschieden, Gadgets vollständig aus dem Betriebssystem zu entfernen. Windows 7-Benutzer mit Mini Anwendungen auf Ihrem Desktop werden benachrichtigt, und Gadgets werden deinstalliert.

## <a name="manifestation"></a>Ausstrahlung

Desktop Gadgets sind auf dem Windows-Desktop nicht verfügbar.

## <a name="mitigation"></a>Minderung

Die Desktop Gadgets-API und die Ordnerstruktur bleiben für Windows 8 vorhanden. Anwendungen, die Gadgets mithilfe dieser API Programm gesteuert installieren und ausführen, werden weiterhin ohne Fehler ausgeführt (obwohl die Gadgets selbst dies nicht tun werden).

## <a name="solution"></a>Lösung

Entwickler von Desktop-Apps sollten Gadgets nicht in ihren Installationsprogrammen verpacken. Diese Mini Anwendungen belegen nur Speicherplatz für den Benutzer und können nicht im System ausgeführt werden.

## <a name="tests"></a>Tests

Entwickler können die Kompatibilität dieser Änderung testen, indem Sie die optionale Komponente für Desktop Gadgets in Windows 7 deaktivieren. Um Mini Anwendungen auf einem Windows 7-PC zu deaktivieren, führen Sie die folgenden Schritte aus:

1.  Navigieren Sie in der Systemsteuerung zum Aktivieren oder Deaktivieren von Windows-Features.
2.  Deaktivieren Sie das Kontrollkästchen neben "Windows Gadget Platform".
3.  Klicken Sie auf OK, und befolgen Sie alle zusätzlichen Anweisungen auf dem Bildschirm.

## <a name="resources"></a>Ressourcen

[Sicherheitsanfälligkeiten in Gadgets können Remote Code Ausführung ermöglichen](https://support.microsoft.com/kb/2719662)

 

 




