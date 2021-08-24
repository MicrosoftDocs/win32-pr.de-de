---
description: Um eine Dynamic-Link Library (DLL) zu erstellen, müssen Sie eine oder mehrere Quellcodedateien und möglicherweise eine Linkerdatei zum Exportieren der Funktionen erstellen.
ms.assetid: b66ea0e8-84c3-40be-bf02-765b9dd61f9f
title: Dynamic-Link-Bibliothekserstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89047e24fe61483b3ac807b59abc114206a00f9df18566b5fb02947268fbd792
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650450"
---
# <a name="dynamic-link-library-creation"></a>Dynamic-Link-Bibliothekserstellung

Um eine Dynamic-Link Library (DLL) zu erstellen, müssen Sie eine oder mehrere Quellcodedateien und möglicherweise eine Linkerdatei zum Exportieren der Funktionen erstellen. Wenn Sie beabsichtigen, Anwendungen, die Ihre DLL verwenden, die dynamische Verknüpfung zur Ladezeit zu erlauben, müssen Sie auch eine Importbibliothek erstellen.

## <a name="creating-source-files"></a>Erstellen von Quelldateien

Die Quelldateien für eine DLL enthalten exportierte Funktionen und Daten, interne Funktionen und Daten sowie eine optionale [Einstiegspunktfunktion](dynamic-link-library-entry-point-function.md) für die DLL. Sie können alle Entwicklungstools verwenden, die die Erstellung Windows-basierten DLLs unterstützen.

Wenn Ihre DLL von einer Multithreadanwendung verwendet werden kann, sollten Sie die DLL threadsicher machen. Sie müssen den Zugriff auf alle globalen Daten der DLL synchronisieren, um Datenbeschädigungen zu vermeiden. Sie müssen auch sicherstellen, dass Sie nur mit Bibliotheken verknüpfen, die ebenfalls threadsicher sind. Beispielsweise enthält Microsoft Visual C++ mehrere Versionen der C-Laufzeitbibliothek, eine, die nicht threadsicher ist, und zwei, die sind.

## <a name="exporting-functions"></a>Exportieren von Funktionen

Wie Sie angeben, welche Funktionen in einer DLL exportiert werden sollen, hängt von den Tools ab, die Sie für die Entwicklung verwenden. Einige Compiler ermöglichen es Ihnen, eine Funktion direkt im Quellcode zu exportieren, indem Sie einen Modifizierer in der Funktionsdeklaration verwenden. In anderen Fällen müssen Sie Exporte in einer Datei angeben, die Sie an den Linker übergeben.

Wenn Sie beispielsweise Visual C++ verwenden, gibt es zwei Möglichkeiten, DLL-Funktionen zu exportieren: mit dem Modifizierer [**\_ \_ declspec(dllexport)**](https://msdn.microsoft.com/library/3y1sfaz2(v=VS.71).aspx) oder mit einer Moduldefinitionsdatei (.def). Wenn Sie den Modifizierer **\_ \_ declspec(dllexport)** verwenden, ist es nicht erforderlich, eine DEF-Datei zu verwenden. Weitere Informationen finden Sie unter [Exportieren aus einer DLL.](/cpp/build/exporting-from-a-dll?view=vs-2019)

## <a name="creating-an-import-library"></a>Erstellen einer Importbibliothek

Eine Importbibliotheksdatei (.lib) enthält Informationen, die der Linker benötigt, um externe Verweise auf exportierte DLL-Funktionen aufzulösen, damit das System die angegebene DLL und die exportierten DLL-Funktionen zur Laufzeit finden kann. Sie können eine Importbibliothek für Ihre DLL erstellen, wenn Sie die DLL erstellen.

Weitere Informationen finden Sie unter [Erstellen einer Importbibliothek und Exportieren einer Datei.](/cpp/build/reference/building-an-import-library-and-export-file?view=vs-2019)

## <a name="using-an-import-library"></a>Verwenden einer Importbibliothek

Um beispielsweise die [**CreateWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-createwindowa) aufzurufen, müssen Sie Ihren Code mit der Importbibliothek User32.lib verknüpfen. Der Grund dafür ist, dass **sich CreateWindow** in einer System-DLL namens User32.dll befindet und User32.lib die Importbibliothek ist, die zum Auflösen der Aufrufe exportierter Funktionen in User32.dll im Code verwendet wird. Der Linker erstellt eine Tabelle, die die Adresse jedes Funktionsaufrufs enthält. Aufrufe von Funktionen in einer DLL werden korrigiert, wenn die DLL geladen wird. Während das System den Prozess initialisiert, lädt es User32.dll, da der Prozess von exportierten Funktionen in dieser DLL abhängt, und aktualisiert die Einträge in der Funktionsadresstabelle. Alle Aufrufe von **CreateWindow** rufen die aus User32.dll exportierte Funktion auf.

Weitere Informationen finden Sie unter [Implizites Verknüpfen mit einer DLL.](/previous-versions/d14wsce5(v=vs.140))

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer einfachen Dynamic Link Library](creating-a-simple-dynamic-link-library.md)
</dt> <dt>

[DLLs (Visual C++)](/cpp/build/dlls-in-visual-cpp?view=vs-2019)
</dt> </dl>

 

 
