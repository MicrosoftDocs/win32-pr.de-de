---
description: Anwendungen können das Datum und die Uhrzeit der Erstellung, letzten Änderung oder des letzten Zugriffs auf eine Datei mithilfe der Funktionen GetFileTime und SetFileTime abrufen und festlegen.
ms.assetid: f8930be6-7c2a-4e50-a7a1-d25f6e2a3951
title: Festlegen und erhalten des Zeitstempels einer Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34735994dd3017662f517a8c0a57be1d5c0e3096
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214768"
---
# <a name="setting-and-getting-the-timestamp-of-a-file"></a>Festlegen und erhalten des Zeitstempels einer Datei

Anwendungen können das Datum und die Uhrzeit der Erstellung, letzten Änderung oder des letzten Zugriffs auf eine Datei mithilfe der Funktionen [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) und [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime) abrufen und festlegen. Weitere Informationen finden Sie unter [Datei Zeiten](/windows/desktop/SysInfo/file-times).

> [!Note]  
> Nicht alle Dateisysteme können Erstellungs-und letzten Zugriffszeiten aufzeichnen, und nicht alle Dateisysteme zeichnen Sie auf die gleiche Weise auf. Im FAT-Dateisystem hat die Erstellungszeit beispielsweise eine Auflösung von 10 Millisekunden, die Schreibzeit eine Auflösung von 2 Sekunden und die Zugriffszeit eine Auflösung von 1 Tag (wirklich das Zugriffs Datum). Das NTFS-Dateisystem verzögert das Update auf den Zeitpunkt des letzten Zugriffs für eine Datei um bis zu eine Stunde nach dem letzten Zugriff.

 

 

 
