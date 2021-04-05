---
description: Manchmal ist es erforderlich, eine DLL durch eine neuere Version zu ersetzen.
ms.assetid: 82349a33-dc2c-4309-b0fc-890f230e3f2c
title: Updates der Dynamic-Link Bibliothek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a10f76103ddebc723466fb7e32a216c0c039691d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041897"
---
# <a name="dynamic-link-library-updates"></a>Updates der Dynamic-Link Bibliothek

Manchmal ist es erforderlich, eine DLL durch eine neuere Version zu ersetzen. Bevor Sie eine DLL ersetzen, führen Sie eine Versions Überprüfung durch, um sicherzustellen, dass Sie eine ältere Version durch eine neuere Version ersetzen. Es ist möglich, eine DLL zu ersetzen, die verwendet wird. Die Methode, die Sie verwenden, um die verwendeten DLLs zu ersetzen, hängt vom verwendeten Betriebssystem ab. Unter Windows XP und höher sollten Anwendungen [isolierte Anwendungen und](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal)parallele Assemblys verwenden.

Es ist nicht erforderlich, den Computer neu zu starten, wenn Sie die folgenden Schritte ausführen:

1.  Verwenden Sie die Funktion " [**fivefileex**](/windows/desktop/api/winbase/nf-winbase-movefileexa) " zum Umbenennen der zu ersetzenden dll. Geben Sie nicht die Berechtigung zum \_ kopieren \_ von Dateien an, und stellen Sie sicher, dass sich die umbenannte Datei auf demselben Volume befindet, das auch die ursprüngliche Datei enthält. Sie können die Datei auch einfach im gleichen Verzeichnis umbenennen, indem Sie Ihr eine andere Erweiterung erteilen.
2.  Kopieren Sie die neue dll in das Verzeichnis, das die umbenannte dll enthält. Alle Anwendungen verwenden nun die neue dll.
3.  Verwenden Sie " [**muvefileex**](/windows/desktop/api/winbase/nf-winbase-movefileexa) " mit "muvefile \_ Delay" \_ \_ , bis der Neustart zum Löschen der umbenannten dll

Bevor Sie diese Ersetzung durchführen, wird die ursprüngliche dll von Anwendungen verwendet, bis Sie entladen wird. Nachdem Sie die Ersetzung vorgenommen haben, verwenden Anwendungen die neue dll. Wenn Sie eine DLL schreiben, müssen Sie darauf achten, sicherzustellen, dass Sie für diese Situation vorbereitet ist, insbesondere, wenn die DLL Informationen zum globalen Status verwaltet oder mit anderen Diensten kommuniziert. Wenn die dll nicht auf eine Änderung von globalen Zustandsinformationen oder Kommunikationsprotokollen vorbereitet ist, müssen Sie beim Aktualisieren der DLL den Computer neu starten, um sicherzustellen, dass alle Anwendungen dieselbe Version der DLL verwenden.

 

 
