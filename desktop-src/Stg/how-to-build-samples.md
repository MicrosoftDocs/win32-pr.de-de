---
title: Erstellen von Beispielen
description: Um ein com-Beispiel zu erstellen, muss die Computerumgebung zum Erstellen von Microsoft Win32 C++-Anwendungen eingerichtet werden.
ms.assetid: c62b8b4d-a9d2-4587-8bb6-7b2c30d1c00d
keywords:
- Erstellen von Beispielen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 593d3465d3ebcc32a6768dd8b2dffe1f0a653d07
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2020
ms.locfileid: "106341916"
---
# <a name="how-to-build-samples"></a>Erstellen von Beispielen

Um ein com-Beispiel zu erstellen, muss die Computerumgebung zum Erstellen von Microsoft Win32 C++-Anwendungen eingerichtet werden.

## <a name="preparing-a-computer-to-create-com-samples"></a>Vorbereiten eines Computers zum Erstellen von com-Beispielen

Die Computerumgebung muss mit einem ordnungsgemäß installierten 32-Bit-C++ Compiler, Linker und Ressourcen Compiler eingerichtet werden, die mit Microsoft Visual C++ 4. x oder höher und einem ordnungsgemäß installierten Windows SDK kompatibel sind. Es empfiehlt sich, die Windows SDK zuletzt zu installieren. Der Windows SDK stellt. h include-und. lib-Bibliotheksdateien bereit, die für die in den Beispielen codierte com-Funktionalität erforderlich sind.

Zum erfolgreichen Ausführen der remclien-, freservice-und Freclien-Beispiele sind System Einrichtungen erforderlich, die in den Windows-Betriebssystemen verfügbar sind: Windows Server 2003, Windows XP, Windows 2000 oder Windows NT 4,0. Die remclien-, freservice-und f reclien-Beispiele werden zwar erstellt, aber nicht auf den Betriebssystemen Windows Me, Windows 98 oder Windows 95 ausgeführt werden, es sei denn, DCOM (DCOM) und die kostenlose Thread-com sind Teil des Betriebssystems. Diese Unterstützung ist für die Betriebssysteme Windows Me, Windows 98 und Windows 95 im DCOM95 Add on verfügbar. DCOM95 kann zurzeit durch den [Download von Microsoft](https://www.microsoft.com/download/details.aspx?id=31661)abgerufen werden.

Jedes Beispiel Verzeichnis enthält die erforderlichen Quelldateien, um das Beispiel zu erstellen und auszuführen. Das übergeordnete Beispiel Verzeichnis enthält eine Makeall.bat-Datei, die Sie von der Eingabeaufforderung aus ausführen können, um alle Codebeispiele in der Verzweigung unten zu erstellen. Weitere Informationen finden Sie in der Makeall.bat-Datei. Wenn Ihre Umgebung zum Erstellen von Win32 C++-Anwendungen eingerichtet ist, können Sie einfach Makeall.bat aus dem Verzeichnis ausführen, in dem es sich befindet, um alle Codebeispiele in der folgenden Verzweigung zu erstellen. Makeall stellt die korrekte Reihenfolge für den Build sicher, sodass alle Codebeispiel Abhängigkeiten erfüllt sind.

Das Hauptverzeichnis verfügt auch über ein Makefile, das alle Lernprogramm-Codebeispiele mit ähnlichen Optionen erstellt, die von Makeall.bat unterstützt werden. Weitere Informationen finden Sie in diesem Makefile. Dieses Makefile geht davon aus, dass der gesamte Code Samples-Branch als Teil der Windows SDK installiert wird. Derzeit hat dieser Speicherort einen ähnlichen Pfad wie *d: \\ MSSDK \\ Samples \\ com \\ tutsamp*, wobei D: das Installations Laufwerk darstellt. Wenn Sie den Tutorial-Code Sample Branch (z. b. das com-Verzeichnis com und seine Unterverzeichnisse) an einen anderen Speicherort außerhalb des Windows SDK extrahiert haben (oder wenn Sie den Beispielsatz als separaten Download von der Microsoft-Website erhalten haben), verwenden Sie Makeall.bat, um alle Beispiele in der Verzweigung zu kompilieren. Im Allgemeinen wird Makeall.bat empfohlen. Außerdem wird eine Logmall.bat Datei bereitgestellt. Dies erfolgt genauso wie bei der makeall-Batchdatei, mit der Ausnahme, dass Sie die gesamte Kompilierungs Ausgabe in Datei Errorlog.txt im Hauptverzeichnis des Tutorials protokolliert.

Zwei Batch Dateien, Regall.bat und Unregall.bat, werden auch im Hauptverzeichnis bereitgestellt, um alle com-Server in der tutorialcode-Beispiel Reihe zu registrieren und die Registrierung aufzuheben. Führen Sie Regall.bat-Datei aus dem Hauptverzeichnis aus, um alle Server zu registrieren. Führen Sie Unregall.bat auf die gleiche Weise aus, um die Registrierung aller Server aufzuheben. Diese Batch Dateien erfordern einen früheren Build der Codebeispiele "Register", "Marshal", "dllservice", "licservice", "locservice", "aptservice", "freservice" und " Wenn Sie einen normalen Build der Codebeispiele durchführen, werden die Server von Makefiles automatisch registriert. In diesem Fall ist es nicht erforderlich, die "Regall"-Batchdatei auszuführen.

Führen Sie die Batchdatei Cleanall.bat aus, um vollständige vollständig alle com-Lernprogramm Beispiele auszuführen.

> [!WARNING]
> Diese Batchdatei löscht alle Visual Studio-Projektdateien und anderen temporären Arbeitsdateien, die in den Beispielen Visual C++ erstellt wurden. Alle in den Codebeispielen für das Tutorial erstellten com-Server werden in der Registrierung aufgehoben. Alle ausführbaren exe-und dll-Dateien werden gelöscht. Alle Debugsymboldateien werden gelöscht. Dateien, die in einer Vielzahl von Buildumgebungen generiert werden, werden ebenfalls gelöscht.

 

Führen Sie "makeall Clean" aus, um eine schnellere, aber präzisetere Bereinigung aller Codebeispiele auszuführen. Dieser Reinigungsvorgang versucht nicht, so umfassend wie Cleanall.bat zu sein. Die OBJ-Dateien werden gelöscht, die Ausgabe Binärdateien werden jedoch beibehalten. Die Registrierung der com-Server in der Registrierung wird nicht aufgehoben.

Diese Beispiel Reihe wurde als integraler Bestandteil der Windows SDK, daher geht die Lernprogramm Darstellung davon aus, dass eine Umgebung mit der ordnungsgemäßen Windows SDK ordnungsgemäß installiert ist.

Allerdings können Releases der Microsoft Visual C++ Version 4,0 und höher auch die für die Kompilierung erforderlichen Bibliotheksdateien ". h" und ". lib" enthalten. In solchen Fällen ist die Installation des Windows SDK möglicherweise nicht erforderlich, um die Beispiele zu kompilieren.

Weitere Informationen und ausführliche Beispiele für Builddetails finden Sie unter:

[Einrichten der Umgebung](environment-setup.md)

[Makefiles](makefiles.md)

[Verwenden von Visual Studio](using-visual-studio.md)

[Extrahieren der Code Beispiele](extracting-the-code-samples.md)

[Codierungsstil Konventionen](coding-style-conventions.md)

 

 




