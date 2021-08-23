---
description: Anwendungen können das Datum und die Uhrzeit der Erstellung, letzten Änderung oder des letzten Zugriffes einer Datei mithilfe der Funktionen GetFileTime und SetFileTime abrufen und festlegen.
ms.assetid: f8930be6-7c2a-4e50-a7a1-d25f6e2a3951
title: Festlegen und Abrufen des Zeitstempels einer Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67e98bd87ae8224ecbebc46e5f9d0ed71ad3522097fb865afc0d16e53a828812
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015128"
---
# <a name="setting-and-getting-the-timestamp-of-a-file"></a>Festlegen und Abrufen des Zeitstempels einer Datei

Anwendungen können das Datum und die Uhrzeit der Erstellung, letzten Änderung oder des letzten Zugriffes einer Datei mithilfe der [**Funktionen GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) und [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime) abrufen und festlegen. Weitere Informationen finden Sie unter [Dateizeiten.](/windows/desktop/SysInfo/file-times)

> [!Note]  
> Nicht alle Dateisysteme können Erstellungs- und letzte Zugriffszeiten aufzeichnen, und nicht alle Dateisysteme zeichnen sie auf die gleiche Weise auf. Beispielsweise hat die Erstellungszeit im FAT-Dateisystem eine Auflösung von 10 Millisekunden, die Schreibzeit eine Auflösung von 2 Sekunden und die Zugriffszeit eine Auflösung von 1 Tag (tatsächlich das Zugriffsdatum). Das NTFS-Dateisystem verzögert die Aktualisierung auf den letzten Zugriffszeitzeit für eine Datei um bis zu eine Stunde nach dem letzten Zugriff.

 

 

 
