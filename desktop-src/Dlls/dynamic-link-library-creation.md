---
description: Zum Erstellen einer Dynamic-Link Bibliothek (dll) müssen Sie eine oder mehrere Quell Code Dateien und möglicherweise eine Linker-Datei zum Exportieren der Funktionen erstellen.
ms.assetid: b66ea0e8-84c3-40be-bf02-765b9dd61f9f
title: Dynamic-Link Bibliotheks Erstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c12d296b1494cfcedcdfa823eb1a3dd4d408427a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753777"
---
# <a name="dynamic-link-library-creation"></a>Dynamic-Link Bibliotheks Erstellung

Zum Erstellen einer Dynamic-Link Bibliothek (dll) müssen Sie eine oder mehrere Quell Code Dateien und möglicherweise eine Linker-Datei zum Exportieren der Funktionen erstellen. Wenn Sie zulassen möchten, dass Anwendungen, die Ihre DLL verwenden, dynamische Verknüpfungen der Ladezeit verwenden, müssen Sie auch eine Import Bibliothek erstellen.

## <a name="creating-source-files"></a>Erstellen von Quelldateien

Die Quelldateien für eine DLL enthalten exportierte Funktionen und Daten, interne Funktionen und Daten sowie eine optionale [Einstiegspunkt Funktion](dynamic-link-library-entry-point-function.md) für die dll. Sie können beliebige Entwicklungs Tools verwenden, die die Erstellung von Windows-basierten DLLs unterstützen.

Wenn die dll von einer Multithreadanwendung verwendet werden kann, sollten Sie die dll als "Thread sicher" festlegen. Sie müssen den Zugriff auf alle globalen Daten der dll synchronisieren, um Daten Beschädigungen zu vermeiden. Außerdem müssen Sie sicherstellen, dass Sie nur mit Bibliotheken verknüpft sind, die Thread sicher sind. Microsoft Visual C++ enthält z. b. mehrere Versionen der C-Lauf Zeit Bibliothek, die nicht Thread sicher und zwei sind.

## <a name="exporting-functions"></a>Exportieren von Funktionen

Wie Sie angeben, welche Funktionen in einer DLL exportiert werden sollen, hängt von den Tools ab, die Sie für die Entwicklung verwenden. Einige Compiler ermöglichen es Ihnen, eine Funktion direkt im Quellcode zu exportieren, indem Sie einen-Modifizierer in der Funktionsdeklaration verwenden. In anderen Zeiten müssen Sie Exporte in einer Datei angeben, die Sie an den Linker übergeben.

Beispiels Visual C++ Weise gibt es zwei Möglichkeiten zum Exportieren von DLL-Funktionen: mit dem declspec-Modifizierer [**\_ \_ (dllexport)**](https://msdn.microsoft.com/library/3y1sfaz2(v=VS.71).aspx) oder mit einer Modul Definitionsdatei (. def). Wenn Sie den **\_ \_ declspec (dllexport)** -Modifizierer verwenden, ist es nicht erforderlich, eine DEF-Datei zu verwenden. Weitere Informationen finden Sie unter [Exportieren aus einer DLL](/cpp/build/exporting-from-a-dll?view=vs-2019).

## <a name="creating-an-import-library"></a>Erstellen einer Import Bibliothek

Eine Import Bibliotheksdatei (. lib) enthält Informationen, die der Linker zum Auflösen externer Verweise auf exportierte DLL-Funktionen benötigt, damit das System die angegebene DLL-Datei und die exportierten DLL-Funktionen zur Laufzeit finden kann. Sie können eine Import Bibliothek für die dll erstellen, wenn Sie die dll erstellen.

Weitere Informationen finden Sie unter [aufbauen einer Import Bibliothek und einer Export Datei](/cpp/build/reference/building-an-import-library-and-export-file?view=vs-2019).

## <a name="using-an-import-library"></a>Verwenden einer Import Bibliothek

Wenn Sie z. b. die Funktion "up [**Window**](/windows/win32/api/winuser/nf-winuser-createwindowa) " aufrufen möchten, müssen Sie Ihren Code mit der Import Bibliothek user32. lib verknüpfen. Der Grund hierfür ist **, dass sich** "" in einer System-DLL mit dem Namen "User32.dll" befindet, und User32. lib ist die Import Bibliothek, mit der die Aufrufe der exportierten Funktionen in User32.dll im Code aufgelöst werden. Der Linker erstellt eine Tabelle, die die Adresse der einzelnen Funktionsaufrufe enthält. Aufrufe von Funktionen in einer DLL werden korrigiert, wenn die dll geladen wird. Während das System den Prozess initialisiert, wird User32.dll geladen, da der Prozess von exportierten Funktionen in dieser DLL abhängt, und die Einträge in der Funktions Adress Tabelle werden aktualisiert. Alle Aufrufe von " **kreatewindow** " rufen die aus User32.dll exportierte Funktion auf.

Weitere Informationen finden Sie unter [Verknüpfen mit einer DLL](/previous-versions/d14wsce5(v=vs.140)).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer einfachen Dynamic Link Library](creating-a-simple-dynamic-link-library.md)
</dt> <dt>

[DLLs (Visual C++)](/cpp/build/dlls-in-visual-cpp?view=vs-2019)
</dt> </dl>

 

 
