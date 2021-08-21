---
title: Nachverfolgen geänderter Bereiche einer Datei
description: Nachverfolgen geänderter Bereiche einer Datei
ms.assetid: 756881E9-EFD0-42FE-9B1C-4A2EF1998D71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6998d2706cd4d8bdb4e94b95fd0e617dbbf4e3a1b288d33dbcebe5528d544c07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117852027"
---
# <a name="tracking-modified-ranges-of-a-file"></a>Nachverfolgen geänderter Bereiche einer Datei

## <a name="platforms"></a>Plattformen

**Clients –** Windows 8.1 (alle SKUs)  
**Server –** Windows Server 2012 R2  

## <a name="description"></a>Beschreibung

Das NTFS-Team (NT File System) hat Windows ein neues Feature hinzugefügt. Das USN-Journal gibt beim Schließen einen DATENSATZ mit der Updatesequenznummer (USN) aus, der geänderte Bereiche für eine Datei enthält. Der neue Eintragstyp USN \_ RECORD \_ V4 wurde eingeführt, um diese geänderten Bereiche einer Datei aufzuzeichnen.

Das Feature ist standardmäßig nicht aktiviert. Benutzer müssen einen FSCTL-Befehl (File System Control) aufrufen, um ihn zu aktivieren. Da jedoch andere Windows Komponenten die Bereichsnachverfolgung aktivieren können, werden Benutzer und Entwickler möglicherweise feststellen, dass das Feature immer aktiviert ist. Windows können Entwickler das USN-Journal abfragen, um herauszufinden, ob die Bereichsnachverfolgung aktiviert ist.

Die MSDN-Dokumentation wird zu einem späteren Zeitpunkt bereitgestellt, um Entwickler anzuweisen, auf USN \_ RECORD \_ V4-Datensätze zuzugreifen.

## <a name="manifestation"></a>Manifestation

Alle vorhandenen Anwendungen, die das USN Journal verwenden, funktionieren weiterhin ohne Kompatibilitätsprobleme gut.

 

 




