---
title: Desktop-Gadgets entfernt
description: Desktop-Gadgets entfernt
ms.assetid: 0074204B-F568-4F9B-A0F7-3E330B91E4CD
keywords:
- Gadgets
- Desktop-Gadgets
- Windows Seitenleiste
- Seitenleiste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f254c4794c93c6afeeec9374e7c1c73f7d538c82b343ffaea984369a72231deb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707010"
---
# <a name="desktop-gadgets-removed"></a>Desktop-Gadgets entfernt

## <a name="platforms"></a>Plattformen

 **Clients** – Windows 8  
**Server** – Windows Server 2012  



## <a name="description"></a>Beschreibung

Aus Funktionalitätssicht wurden Gadgets bereits als veraltet eingestuft und werden durch neue Livekacheln und Apps ausgegliedert. Gadgets stellen auch ein Sicherheitsrisiko für Benutzer dar. Als Plattform sind Sicherheitsrisiken vorhanden, sodass auch unbedenkliche Gadgets ausgenutzt werden können. Daher haben wir uns entschieden, Gadgets vollständig aus dem Betriebssystem zu entfernen, um Windows 8 als unser modernes und sicherstes Betriebssystem zu erhalten. Windows 7 Benutzer mit Gadgets auf ihrem Desktop werden benachrichtigt, und Gadgets werden deinstalliert.

## <a name="manifestation"></a>Manifestation

Desktop-Gadgets sind auf dem Windows Desktop nicht verfügbar.

## <a name="mitigation"></a>Minderung

Die Desktop-Gadgets-API und die Ordnerstruktur bleiben für Windows 8 erhalten. Anwendungen, die Gadgets programmgesteuert mit dieser API installieren und ausführen, werden weiterhin ohne Fehler ausgeführt (obwohl die Gadgets selbst nicht ausgeführt werden).

## <a name="solution"></a>Lösung

Desktop-App-Entwickler sollten in ihren Installationsprogrammen keine Gadgets packen. Diese Gadgets nehmen nur Speicherplatz für den Benutzer in Anspruch und können nicht im System ausgeführt werden.

## <a name="tests"></a>Tests

Entwickler können die Kompatibilität dieser Änderung testen, indem sie die optionale Komponente für Desktop-Gadgets in Windows 7 deaktivieren. Führen Sie die folgenden Schritte aus, um Gadgets auf einem pc Windows 7 zu deaktivieren:

1.  Navigieren Sie im Systemsteuerung zu Windows Features aktivieren oder deaktivieren.
2.  Deaktivieren Sie das Kontrollkästchen neben "Windows Gadget Platform".
3.  Klicken Sie auf OK, und befolgen Sie alle zusätzlichen Anweisungen auf dem Bildschirm.

## <a name="resources"></a>Ressourcen

[Sicherheitsrisiken in Gadgets können Remotecodeausführung ermöglichen](https://support.microsoft.com/kb/2719662)

 

 




