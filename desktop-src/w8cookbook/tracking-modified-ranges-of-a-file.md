---
title: Nachverfolgen von geänderten Bereichen einer Datei
description: Nachverfolgen von geänderten Bereichen einer Datei
ms.assetid: 756881E9-EFD0-42FE-9B1C-4A2EF1998D71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 664e7a5c0a9148471d2a1a28f2881e1c375089c1
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "106337878"
---
# <a name="tracking-modified-ranges-of-a-file"></a>Nachverfolgen von geänderten Bereichen einer Datei

## <a name="platforms"></a>Plattformen

**Clients:** Windows 8.1 (alle SKUs)  
**Server:** Windows Server 2012 R2  

## <a name="description"></a>BESCHREIBUNG

Das NTFS-Team (NT File System) hat Windows ein neues Feature hinzugefügt. Das Daten Journal gibt einen Update Sequenznummern-Datensatz (Update Sequence Number, d) mit geänderten Bereichen für eine Datei nach dem Schließen aus. Ein neuer Daten Recordtyp wurde \_ eingeführt, \_ um die geänderten Bereiche einer Datei aufzuzeichnen.

Die Funktion ist standardmäßig nicht aktiviert. Benutzer müssen einen Befehl für die Dateisystem Steuerung (FSCTL) aufrufen, um Sie zu aktivieren. Da jedoch andere Windows-Komponenten die Bereichs Überwachung aktivieren können, können Benutzer und Entwickler erkennen, dass die Funktion immer aktiviert ist. Mit Windows können Entwickler das Anwendungs Journal Abfragen, um herauszufinden, ob die Bereichs Überwachung aktiviert ist.

Die MSDN-Dokumentation wird zu einem späteren Zeitpunkt bereitgestellt, um Entwicklern den Zugriff auf die \_ \_ Datensätze der Datensätze von Datensätzen in der Version Version

## <a name="manifestation"></a>Ausstrahlung

Alle vorhandenen Anwendungen, die das Anwendungs Journal verwenden, funktionieren weiterhin problemlos ohne Kompatibilitätsprobleme.

 

 




