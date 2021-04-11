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
# <a name="setting-and-getting-the-timestamp-of-a-file"></a><span data-ttu-id="3e37b-103">Festlegen und erhalten des Zeitstempels einer Datei</span><span class="sxs-lookup"><span data-stu-id="3e37b-103">Setting and Getting the Timestamp of a File</span></span>

<span data-ttu-id="3e37b-104">Anwendungen können das Datum und die Uhrzeit der Erstellung, letzten Änderung oder des letzten Zugriffs auf eine Datei mithilfe der Funktionen [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) und [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime) abrufen und festlegen.</span><span class="sxs-lookup"><span data-stu-id="3e37b-104">Applications can retrieve and set the date and time a file is created, last modified, or last accessed by using the [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) and [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime) functions.</span></span> <span data-ttu-id="3e37b-105">Weitere Informationen finden Sie unter [Datei Zeiten](/windows/desktop/SysInfo/file-times).</span><span class="sxs-lookup"><span data-stu-id="3e37b-105">For more information, see [File Times](/windows/desktop/SysInfo/file-times).</span></span>

> [!Note]  
> <span data-ttu-id="3e37b-106">Nicht alle Dateisysteme können Erstellungs-und letzten Zugriffszeiten aufzeichnen, und nicht alle Dateisysteme zeichnen Sie auf die gleiche Weise auf.</span><span class="sxs-lookup"><span data-stu-id="3e37b-106">Not all file systems can record creation and last access times, and not all file systems record them in the same manner.</span></span> <span data-ttu-id="3e37b-107">Im FAT-Dateisystem hat die Erstellungszeit beispielsweise eine Auflösung von 10 Millisekunden, die Schreibzeit eine Auflösung von 2 Sekunden und die Zugriffszeit eine Auflösung von 1 Tag (wirklich das Zugriffs Datum).</span><span class="sxs-lookup"><span data-stu-id="3e37b-107">For example, on FAT file system, create time has a resolution of 10 milliseconds, write time has a resolution of 2 seconds, and access time has a resolution of 1 day (really, the access date).</span></span> <span data-ttu-id="3e37b-108">Das NTFS-Dateisystem verzögert das Update auf den Zeitpunkt des letzten Zugriffs für eine Datei um bis zu eine Stunde nach dem letzten Zugriff.</span><span class="sxs-lookup"><span data-stu-id="3e37b-108">The NTFS file system delays update to the last access time for a file by up to one hour after the last access.</span></span>

 

 

 
