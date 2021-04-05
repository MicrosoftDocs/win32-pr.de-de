---
title: Verwenden von Visual Studio
description: Microsoft Visual Studio 6,0 stellt eine Projektdatei für die einzelnen Beispiele bereit.
ms.assetid: 8da6affd-a881-4dc4-a2e6-d35f655c69fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5b32359a29d14a6cd5a4d08d015a6598ade376d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707295"
---
# <a name="using-visual-studio"></a>Verwenden von Visual Studio

Microsoft Visual Studio 6,0 stellt eine Projektdatei für die einzelnen Beispiele bereit. Diese Datei enthält die DSP-Erweiterung. Außerdem wird eine Arbeitsbereichs Datei "allsamp. DSW" im Hauptverzeichnis bereitgestellt, sodass Sie alle Beispiele in Visual Studio gleichzeitig kompilieren können.

> [!Note]  
> Die folgenden Anweisungen sind für Microsoft Visual Studio 6,0 geschrieben. Die Befehle können sich in früheren und späteren Versionen von Visual Studio unterscheiden.

 

Wenn Sie das entsprechende Projekt für ein Beispiel laden möchten, können Sie Visual Studio an der Eingabeaufforderung im Verzeichnis des Beispiels ausführen, wie im folgenden Beispiel gezeigt. Sie müssen den Namen des Beispielprojekts für ersetzen **<project name>** .

**Msdev <project name> . DSP**

Sie können auch einfach auf die DSP-Datei im Windows-Explorer doppelklicken, um den Arbeitsbereich eines Beispiels in Visual Studio zu laden. In Visual Studio können Sie dann die C++-Klassen der Beispiel Quelle durchsuchen und im Allgemeinen die anderen edit-compile-Debug-Vorgänge durchführen.

Als Teil des Platform Software Development Kit (SDK) erfordert die Kompilierung dieser Beispiele in Visual Studio die ordnungsgemäße Einstellung von Verzeichnis Pfaden in Visual Studio. Führen Sie die folgenden Schritte aus, um die Verzeichnispfade festzulegen:

-   Führen Sie Microsoft Visual Studio (Visual C++) aus.
-   Wählen Sie **im Menü Extras** die **Option Optionen...** aus.
-   Wählen Sie im Dialogfeld **Optionen** die Registerkarte **Verzeichnisse** aus.
-   Wählen Sie in der Dropdown Liste **Verzeichnisse anzeigen für** die Option **ausführbare Dateien** aus, und geben Sie den Pfad für das Verzeichnis bin für Ihr installiertes Platform SDK ein (z. b. C: \\ Program Files \\ Microsoft SDK \\ bin). Klicken Sie auf die Schaltfläche mit dem Pfeil nach oben, um den neu eingegebenen Pfad so zu verschieben, dass er der erste Eintrag in der Liste **Verzeichnisse** ist.
-   Wählen Sie in der Dropdown Liste **Verzeichnisse anzeigen für** die Option **Dateien einschließen** aus, und geben Sie den Includeverzeichnis Pfad für Ihr installiertes Plattform-SDK ein (z. b. C: \\ Programmdateien \\ Microsoft SDK \\ include). Klicken Sie auf die Schaltfläche mit dem Pfeil nach oben, um den neu eingegebenen Pfad so zu verschieben, dass er der erste Eintrag in der Liste **Verzeichnisse** ist.
-   Wählen Sie in der Dropdown Liste **Verzeichnisse anzeigen für** die Option **Bibliotheksdateien** aus, und geben Sie den Verzeichnispfad Verzeichnis für Ihr installiertes Platform SDK ein (z. b. C: \\ Program Files \\ Microsoft SDK \\ lib). Klicken Sie auf die Schaltflächen nach oben, um den neu eingegebenen Pfad so zu verschieben, dass er der erste Eintrag in der Liste **Verzeichnisse** ist.
-   Klicken Sie im Dialogfeld **Optionen** auf die Schaltfläche OK, um die Einstellungen abzuschließen.

Von dort aus können Sie den Editor, den Debugger und die Projektfunktionen zum Bearbeiten, kompilieren, verknüpfen und Debuggen verwenden.

Andere visuelle IDES können auch problemlos eines ihrer systemeigenen Projekt Makefiles generieren, wenn die vorhandenen Quelldateien eines Code Beispiels vorhanden sind. Wenn Sie eine solche IDE verwenden, kann das Erstellen eines solchen systemeigenen Projekt Makefile sehr nützlich sein, da es eine Möglichkeit bietet, die C++-Klassen des Programms zu durchsuchen. Weitere Informationen zur Verwendung externer Makefiles oder zum Erstellen eines systemeigenen Projekts Makefile mithilfe eines Satzes vorhandener Quelldateien finden Sie in der IDE-Dokumentation.

Abgesehen von der Abhängigkeit von dem allgemeinen Code in den gleich geordneten apputil-, Inc-und lib-Verzeichnissen sind viele Codebeispiele eigenständig. Erstellen Sie apputil, bevor Sie andere Codebeispiele erstellen. Einige Beispiele, die später in der Sequenz verwendet werden, funktionieren möglicherweise mit den kompilierten Ergebnissen früherer Beispiele. Diese Codebeispiel Abhängigkeiten sind wie folgt:

-   Beliebig: das Erstellen eines beliebigen Code Beispiels erfordert vor der Erstellung von apputil.
-   Dlluser: Build oder Run erfordert vorherige Build von dllskel.
-   Comuser: Erstellen oder ausführen erfordert vor der Erstellung von comobj.
-   Dllservice: der Buildvorgang muss vor der Registrierung erstellt werden.
-   Dllclien: Ausführen erfordert vorheriger Build von dllservice.
-   Licservice: der Buildvorgang muss vor der Registrierung erstellt werden.
-   Licclien: "Run" erfordert vorherige Erstellung von "licservice" und "dllservice".
-   Marshal: für den Build ist ein vorheriger Registrierungs Build erforderlich.
-   Locservice: Erstellen oder ausführen erfordert vor dem Erstellen von Register und Mars Hallen.
-   Locclien: Ausführen erfordert vorheriger Build von locservice.
-   Aptservice: Erstellen oder ausführen erfordert vor dem Erstellen von Register und Mars Hallen.
-   Aptclien: Run erfordert vorherige Erstellung von aptservice.
-   Remclien: für die Erstellung oder den Testlauf müssen vor dem Erstellen von Register und Mars Hallen auf dem lokalen Computer (Client Computer) die Ausführen erfordert vorherige Erstellung von Register, Mars Hall und aptservice auf einem Remote Computer (Server).
-   Freservice: der Buildvorgang muss vor der Registrierung erstellt werden.
-   "F": "Run" erfordert vorherige Erstellung von "freservice".
-   Sparen: der Build benötigt einen früheren Buildvorgang für das Register.
-   "Konclien: Ausführen" erfordert vor der Erstellung der Einsparung.
-   Stoservice: der Buildvorgang muss vor der Registrierung erstellt werden.
-   Stoclien: Run erfordert vorherige Erstellung von stoservice.
-   Perserve: der Buildvorgang muss vor der Registrierung erstellt werden.
-   Pertext: für den Build ist ein vorheriger Registrierungs Build erforderlich.
-   Perdraw: der Buildvorgang muss vor der Registrierung erstellt werden.
-   Perclien: Run erfordert vorherige Erstellung von perservice, pertext und perdraw.
-   Dcdmarsh: der Buildvorgang muss vor der Registrierung erstellt werden.
-   Dcdservice: Erstellen oder ausführen erfordert vor der Erstellung von Register und dcdmarsh.
-   Dcomdraw: für die Erstellung oder den Testlauf müssen vorherige Buildschritte und dcdmarsh auf dem lokalen Computer (Client) ausgeführt werden. Ausführen erfordert vorherige Erstellung von Register, dcdmarsh und dcomdraw auf einem Remote Computer (Server).

 

 




