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
# <a name="ms-dos-date-and-time"></a>Datum und Uhrzeit der MS-DOS

**MS-DOS-Datum** und **MS-DOS-Zeit** sind gepackte 16-Bit-Werte, die den Monat, den Tag, das Jahr und den Tag angeben, an dem eine MS-DOS-Datei zuletzt geschrieben wurde Von MS-DOS werden das Datum und die Uhrzeit aufgezeichnet, wenn eine MS-DOS-Anwendung eine Datei erstellt oder in eine Datei schreibt. MS-DOS-Anwendungen rufen dieses Datum und die Uhrzeit mithilfe von MS-DOS Wenn Sie die [**GetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime) -Funktion verwenden, um die Datei Zeiten für die von MS-DOS erstellten Dateien abzurufen, konvertiert **GetFileTime** MS und Uhrzeiten von MS-DOS automatisch in UTC-basierte Zeiten.

Wenn Sie ein Datum und eine Uhrzeit für das MS-DOS festzustellen, die nicht konvertiert wurden, können Sie Sie mithilfe der [**dosdatetimetofiletime**](/windows/desktop/api/Winbase/nf-winbase-dosdatetimetofiletime) -Funktion in eine UTC-basierte Zeit konvertieren. Diese Funktion kopiert das konvertierte Datum und die konvertierte Uhrzeit in eine [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) -Struktur. Sie können den Wert mithilfe der [**filetimededosdatetime**](/windows/desktop/api/Winbase/nf-winbase-filetimetodosdatetime) -Funktion wieder in ein MS-DOS-Datum und eine MS-DOS-Uhrzeit konvertieren.

 

 
