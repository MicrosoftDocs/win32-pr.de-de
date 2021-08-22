---
title: Erstellen von Beispielen
description: Zum Erstellen eines COM-Beispiels muss die Computerumgebung zum Erstellen von Microsoft Win32 C++-Anwendungen eingerichtet werden.
ms.assetid: c62b8b4d-a9d2-4587-8bb6-7b2c30d1c00d
keywords:
- Erstellen von Beispielen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 782a75bb54127191757a515244d439bbff9570c96f4e0bb2ac603477bedb96a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663120"
---
# <a name="how-to-build-samples"></a>Erstellen von Beispielen

Zum Erstellen eines COM-Beispiels muss die Computerumgebung zum Erstellen von Microsoft Win32 C++-Anwendungen eingerichtet werden.

## <a name="preparing-a-computer-to-create-com-samples"></a>Vorbereiten eines Computers zum Erstellen von COM-Beispielen

Die Computerumgebung muss mit einem ordnungsgemäß installierten 32-Bit-C++-Compiler, Linker und Ressourcencompiler eingerichtet werden, der mit Microsoft Visual C++ 4.x oder höher kompatibel ist, sowie mit einem ordnungsgemäß installierten Windows SDK. Es ist am besten, das Windows SDK zu installieren. Das Windows SDK stellt H-Include- und LIB-Bibliotheksdateien bereit, die für die in den Beispielen codierte COM-Funktionalität erforderlich sind.

Zum erfolgreichen Ausführen der Remclien-, Freserve- und Freclien-Beispiele sind Systemeinrichtung erforderlich, die in den Windows-Betriebssystemen verfügbar sind: Windows Server 2003, Windows XP, Windows 2000 oder Windows NT 4.0. Die Remclien-, Freserve- und Freclien-Beispiele erstellen die Betriebssysteme Windows Me, Windows 98 oder Windows 95, es sei denn, Distributed COM (DCOM) und Freethread-COM sind Teil des Betriebssystems. Diese Unterstützung ist für die Betriebssysteme Windows Me, Windows 98 und Windows 95 im DCOM95-Add-On verfügbar. DCOM95 kann derzeit von [Microsoft heruntergeladen werden.](https://www.microsoft.com/download/details.aspx?id=31661)

Jedes Beispielverzeichnis verfügt über die erforderlichen Quelldateien zum Erstellen und Ausführen des Beispiels. Das übergeordnete Beispielverzeichnis verfügt über eine Makeall.bat Datei, die Sie über die Eingabeaufforderung ausführen können, um alle Codebeispiele im folgenden Branch zu erstellen. Weitere Informationen finden Sie in der Makeall.bat Datei. Wenn Ihre Umgebung zum Erstellen von Win32 C++-Anwendungen eingerichtet ist, können Sie einfach Makeall.bat aus dem Verzeichnis ausführen, in dem sie sich befindet, um alle Codebeispiele im folgenden Branch zu erstellen. Makeall stellt die richtige Reihenfolge für den Build sicher, sodass alle Codebeispielabhängigkeiten erfüllt werden.

Das Hauptverzeichnis verfügt auch über ein Makefile, mit dem alle Tutorialcodebeispiele mit ähnlichen Optionen erstellt werden wie von Makeall.bat. Weitere Informationen finden Sie in diesem Makefile. Bei diesem Makefile wird davon ausgegangen, dass der gesamte Branch für Codebeispiele als Teil des Windows SDK installiert ist. Derzeit hat dieser Speicherort einen Pfad ähnlich *D: \\ MSSDK \\ SAMPLES COM \\ \\ TUTSAMP,* wobei D: das Installationslaufwerk darstellt. Wenn Sie den Branch des Tutorialcodebeispiels (z. B. das COM-Verzeichnis COM und seine Unterverzeichnisse) an einen anderen Speicherort außerhalb des Windows SDK extrahiert haben (oder wenn Sie den Beispielsatz als separaten Download von der Microsoft-Website erhalten haben), verwenden Sie Makeall.bat, um alle Beispiele im Branch zu kompilieren. Im Allgemeinen wird Makeall.bat empfohlen. Eine Logmall.bat wird ebenfalls bereitgestellt. Er funktioniert genauso wie die Makeall-Batchdatei, protokolliert jedoch alle Kompilierungsausgabe Errorlog.txt im Hauptverzeichnis des Tutorials.

Zwei Batchdateien, Regall.bat und Unregall.bat, werden auch im Hauptverzeichnis bereitgestellt, um alle COM-Server in der Tutorialcodebeispielreihe zu registrieren und die Registrierung zu aufheben. Um alle Server zu registrieren, führen Sie Regall.bat aus dem Hauptverzeichnis aus. Um die Registrierung aller Server zu aufheben, führen Unregall.bat auf die gleiche Weise aus. Diese Batchdateien erfordern einen vorherigen Build der Codebeispiele REGISTER, MARSHAL, DLLSERVE, LICSERVE, LOCSERVE, APTSERVE, FRESERVE und CONSERVE. Wenn Sie einen normalen Build der Codebeispiele ausführen, registrieren die Server-Makefiles die Server automatisch. In diesem Fall ist es nicht erforderlich, die Batchdatei "Still" ausführen.

Führen Sie Cleanall.bat Batchdatei aus, um eine vollständige Bereinigung aller COM-Tutorialbeispiele durchzuführen.

> [!WARNING]
> Diese Batchdatei löscht alle Visual Studio Projektdateien und andere temporäre Arbeitsdateien, die von Visual C++ in den Beispielen erstellt wurden. Die Registrierung aller COM-Server, die in den Codebeispielen des Tutorials erstellt wurden, wird in der Registrierung aufgehoben. Alle ausführbaren EXE- und .dll werden gelöscht. Alle Debugsymboldateien werden gelöscht. Dateien, die in einer Vielzahl von Buildumgebungen generiert werden, werden ebenfalls gelöscht.

 

Führen Sie "Makeall Clean" aus, um eine schnellere, aber mäßigere Bereinigung aller Codebeispiele durchzuführen. Dieser Bereinigungsvorgang ist nicht so umfassend wie der von Cleanall.bat. Die OBJ-Dateien werden gelöscht, die Ausgabebinärdateien werden jedoch beibehalten. Die Registrierung der COM-Server in der Registrierung wird nicht aufgehoben.

Diese Beispielreihe stammt aus einem integralen Bestandteil des Windows SDK. Daher wird in der Tutorialerzählung von einer Umgebung ausgegangen, in der das Windows SDK ordnungsgemäß installiert ist.

Releases von version Microsoft Visual C++ 4.0 und höher können jedoch auch die H-Include- und LIB-Bibliotheksdateien bereitstellen, die für die Kompilierung erforderlich sind. In solchen Fällen ist die Installation des Windows SDK möglicherweise nicht erforderlich, um die Beispiele zu kompilieren.

Weitere Informationen und vollständige Buildbeispieldetails finden Sie unter:

[Umgebungseinrichtung](environment-setup.md)

[Makefiles](makefiles.md)

[Verwenden von Visual Studio](using-visual-studio.md)

[Extrahieren der Codebeispiele](extracting-the-code-samples.md)

[Konventionen für Codierungsstile](coding-style-conventions.md)

 

 




