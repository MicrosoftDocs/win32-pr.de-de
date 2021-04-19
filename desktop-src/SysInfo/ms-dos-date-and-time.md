---
description: MS-DOS-Datum und MS-DOS-Zeit sind gepackte 16-Bit-Werte, die den Monat, den Tag, das Jahr und den Tag angeben, an dem eine MS-DOS-Datei zuletzt geschrieben wurde
ms.assetid: 948e6d77-dd01-4c90-9ef0-af143972c3fa
title: Datum und Uhrzeit der MS-DOS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84d401c731c9a3f5127511e28adf846c929a89a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355516"
---
# <a name="ms-dos-date-and-time"></a><span data-ttu-id="e3789-103">Datum und Uhrzeit der MS-DOS</span><span class="sxs-lookup"><span data-stu-id="e3789-103">MS-DOS Date and Time</span></span>

<span data-ttu-id="e3789-104">**MS-DOS-Datum** und **MS-DOS-Zeit** sind gepackte 16-Bit-Werte, die den Monat, den Tag, das Jahr und den Tag angeben, an dem eine MS-DOS-Datei zuletzt geschrieben wurde</span><span class="sxs-lookup"><span data-stu-id="e3789-104">**MS-DOS date** and **MS-DOS time** are packed 16-bit values that specify the month, day, year, and time of day an MS-DOS file was last written to.</span></span> <span data-ttu-id="e3789-105">Von MS-DOS werden das Datum und die Uhrzeit aufgezeichnet, wenn eine MS-DOS-Anwendung eine Datei erstellt oder in eine Datei schreibt.</span><span class="sxs-lookup"><span data-stu-id="e3789-105">MS-DOS records the date and time whenever an MS-DOS application creates or writes to a file.</span></span> <span data-ttu-id="e3789-106">MS-DOS-Anwendungen rufen dieses Datum und die Uhrzeit mithilfe von MS-DOS</span><span class="sxs-lookup"><span data-stu-id="e3789-106">MS-DOS applications retrieve this date and time using MS-DOS functions.</span></span> <span data-ttu-id="e3789-107">Wenn Sie die [**GetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime) -Funktion verwenden, um die Datei Zeiten für die von MS-DOS erstellten Dateien abzurufen, konvertiert **GetFileTime** MS und Uhrzeiten von MS-DOS automatisch in UTC-basierte Zeiten.</span><span class="sxs-lookup"><span data-stu-id="e3789-107">When you use the [**GetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime) function to retrieve the file times for files that were created by MS-DOS, **GetFileTime** automatically converts MS-DOS dates and times to UTC-based times.</span></span>

<span data-ttu-id="e3789-108">Wenn Sie ein Datum und eine Uhrzeit für das MS-DOS festzustellen, die nicht konvertiert wurden, können Sie Sie mithilfe der [**dosdatetimetofiletime**](/windows/desktop/api/Winbase/nf-winbase-dosdatetimetofiletime) -Funktion in eine UTC-basierte Zeit konvertieren.</span><span class="sxs-lookup"><span data-stu-id="e3789-108">If you encounter an MS-DOS date and time that has not been converted, you can convert it to a UTC-based time by using the [**DosDateTimeToFileTime**](/windows/desktop/api/Winbase/nf-winbase-dosdatetimetofiletime) function.</span></span> <span data-ttu-id="e3789-109">Diese Funktion kopiert das konvertierte Datum und die konvertierte Uhrzeit in eine [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="e3789-109">This function copies the converted date and time to a [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure.</span></span> <span data-ttu-id="e3789-110">Sie können den Wert mithilfe der [**filetimededosdatetime**](/windows/desktop/api/Winbase/nf-winbase-filetimetodosdatetime) -Funktion wieder in ein MS-DOS-Datum und eine MS-DOS-Uhrzeit konvertieren.</span><span class="sxs-lookup"><span data-stu-id="e3789-110">You can convert the value back to an MS-DOS date and time by using the [**FileTimeToDosDateTime**](/windows/desktop/api/Winbase/nf-winbase-filetimetodosdatetime) function.</span></span>

 

 
