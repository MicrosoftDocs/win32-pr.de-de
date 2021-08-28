---
title: Verwenden von Visual Studio
description: Der Einfachheit halber stellt Microsoft Visual Studio 6.0 eine Projektdatei für jedes Beispiel bereit.
ms.assetid: 8da6affd-a881-4dc4-a2e6-d35f655c69fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ee6edc1b19cb0e56495c8af6f96d28e4d255e40d53161671f52a1a7d27939f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796850"
---
# <a name="using-visual-studio"></a>Verwenden von Visual Studio

Der Einfachheit halber stellt Microsoft Visual Studio 6.0 eine Projektdatei für jedes Beispiel bereit. Diese Datei hat die DSP-Erweiterung. Eine Allsamp.dsw-Arbeitsbereichsdatei wird auch im Hauptverzeichnis bereitgestellt, sodass Sie alle Beispiele aus Visual Studio gleichzeitig kompilieren können.

> [!Note]  
> Die folgenden Anweisungen sind für Microsoft Visual Studio 6.0 geschrieben. Die Befehle können sich in früheren und späteren Versionen von Visual Studio unterscheiden.

 

Um das entsprechende Projekt für ein Beispiel zu laden, können Sie Visual Studio an der Eingabeaufforderung im Verzeichnis des Beispiels ausführen, wie im folgenden Beispiel gezeigt. Sie müssen den Beispielprojektnamen durch **<project name>** ersetzen.

**msdev <project name> .dsp**

Sie können auch einfach auf die DSP-Datei im Windows-Explorer doppelklicken, um den Arbeitsbereich eines Beispiels in Visual Studio zu laden. Innerhalb Visual Studio können Sie dann die C++-Klassen der Beispielquelle durchsuchen und im Allgemeinen die anderen Vorgänge zum Bearbeiten/Kompilieren und Debuggen ausführen.

Im Rahmen des Platform Software Development Kit (SDK) erfordert die Kompilierung dieser Beispiele aus Visual Studio die ordnungsgemäße Festlegung von Verzeichnispfaden in Visual Studio. Führen Sie die folgenden Schritte aus, um die Verzeichnispfade festzulegen:

-   Führen Sie Microsoft Visual Studio (Visual C++) aus.
-   Wählen Sie **optionen...** im Menü **Extras** aus.
-   Wählen Sie im Dialogfeld **Optionen** die Registerkarte **Verzeichnisse** aus.
-   Wählen Sie in der Dropdownliste **Verzeichnisse anzeigen für** die Option **Ausführbare Dateien** aus, und geben Sie den BIN-Verzeichnispfad für Ihr installiertes Plattform-SDK ein (z. B. C: Programme Microsoft \\ SDK \\ \\ Bin). Klicken Sie auf die Schaltfläche mit dem Pfeil nach oben, um diesen neu eingegebenen Pfad so zu verschieben, dass er der erste Eintrag in der Liste **Verzeichnisse** ist.
-   Wählen Sie in der Dropdownliste **Verzeichnisse anzeigen für** die Option **Dateien einschließen** aus, und geben Sie den Verzeichnispfad INCLUDE für Ihr installiertes Plattform-SDK ein (z. B. C: \\ Microsoft \\ SDK-Include für \\ Programme). Klicken Sie auf die Schaltfläche mit dem Pfeil nach oben, um diesen neu eingegebenen Pfad so zu verschieben, dass er der erste Eintrag in der Liste **Verzeichnisse** ist.
-   Wählen Sie in der Dropdownliste **Verzeichnisse anzeigen für** die Option **Bibliotheksdateien** aus, und geben Sie den LIB-Verzeichnispfad für Ihr installiertes Plattform-SDK ein (z. B. C: \\ Programme Microsoft SDK \\ \\ Lib). Klicken Sie auf die Pfeilschaltflächen nach oben, um diesen neu eingegebenen Pfad so zu verschieben, dass er der erste Eintrag in der Liste **Verzeichnisse** ist.
-   Klicken Sie im Dialogfeld **Optionen** auf die Schaltfläche OK, um die Einstellungen abzuschließen.

Dort können Sie editor, debugger und project facilities zum Bearbeiten, Kompilieren, Verknüpfen und Debuggen verwenden.

Andere visuelle IDEs können auch problemlos eines ihrer nativen Projekt-Makefiles generieren, wenn die vorhandenen Quelldateien eines Codebeispiels vorhanden sind. Wenn Sie eine solche IDE verwenden, kann das Generieren eines solchen nativen Projekt-Makefiles sehr sinnvoll sein, da es eine Möglichkeit bietet, die C++-Klassen des Programms zu durchsuchen. Weitere Informationen zur Verwendung externer Makefiles oder zum Erstellen eines nativen Projekt-Makefiles mithilfe eines Satzes vorhandener Quelldateien finden Sie in der IDE-Dokumentation.

Abgesehen von der Abhängigkeit vom allgemeinen Code in den nebengeordneten Verzeichnissen APPUTIL, INC und LIB sind viele Codebeispiele eigenständig. Erstellen Sie APPUTIL, bevor Sie andere Codebeispiele erstellen. Einige Beispiele später in der Sequenz funktionieren möglicherweise mit den kompilierten Ergebnissen früherer Beispiele. Diese Codebeispielabhängigkeiten sind wie folgt:

-   Beliebig: Für das Erstellen eines Codebeispiels ist ein vorheriger Build von APPUTIL erforderlich.
-   DLLUSER: Build oder Ausführung erfordert vor dem Build von DLLSKEL.
-   COMUSER: Build oder Ausführung erfordert vor dem Build von COMOBJ.
-   DLLSERVE: Für den Build ist ein vorheriger Build von REGISTER erforderlich.
-   DLLCLIEN: Für die Ausführung ist ein vorheriger Build von DLLSERVE erforderlich.
-   LICSERVE: Der Build erfordert vor dem Build von REGISTER.
-   LICCLIEN: Für die Ausführung ist ein vorheriger Build von LICSERVE und DLLSERVE erforderlich.
-   MARSHAL: Für den Build ist ein vorheriger Build von REGISTER erforderlich.
-   LOCSERVE: Build- oder Ausführungsanforderungen vor dem Build von REGISTER und MARSHAL.
-   LOCCLIEN: Ausführung erfordert vor dem Build von LOCSERVE.
-   APTSERVE: Für das Erstellen oder Ausführen ist ein vorheriger Build von REGISTER und MARSHAL erforderlich.
-   APTCLIEN: Für die Ausführung ist ein vorheriger Build von APTSERVE erforderlich.
-   REMCLIEN: Build- oder Ausführungsanforderungen müssen vor dem Build von REGISTER und MARSHAL auf dem lokalen (Client-)Computer erstellt werden. Für die Ausführung ist ein vorheriger Build von REGISTER, MARSHAL und APTSERVE auf einem Remotecomputer (Servercomputer) erforderlich.
-   FRESERVE: Für den Build ist ein vorheriger Build von REGISTER erforderlich.
-   FRECLIEN: Für die Ausführung ist ein vorheriger Build von FRESERVE erforderlich.
-   CONSERVE: Für den Build ist ein vorheriger Build von REGISTER erforderlich.
-   CONCLIEN: Für die Ausführung ist ein vorheriger Build von CONSERVE erforderlich.
-   STOSERVE: Für den Build ist ein vorheriger Build von REGISTER erforderlich.
-   STOCLIEN: Für die Ausführung ist ein vorheriger Build von STOSERVE erforderlich.
-   PERSERVE: Für den Build ist ein vorheriger Build von REGISTER erforderlich.
-   PERTEXT: Für den Build ist ein vorheriger Build von REGISTER erforderlich.
-   PERDRAW: Für den Build ist ein vorheriger Build von REGISTER erforderlich.
-   PERCLIEN: Für die Ausführung ist ein vorheriger Build von PERSERVE, PERTEXT und PERDRAW erforderlich.
-   DCDMARSH: Für den Build ist ein vorheriger Build von REGISTER erforderlich.
-   DCDSERVE: Build- oder Ausführungsanforderungen müssen vor dem Build von REGISTER und DCDMARSH erstellt werden.
-   DCOMDRAW: Build- oder Ausführungsanforderungen müssen vor dem Build von REGISTER und DCDMARSH auf dem lokalen Computer (Client) erstellt werden. Für die Ausführung ist ein vorheriger Build von REGISTER, DCDMARSH und DCOMDRAW auf einem Remotecomputer (Servercomputer) erforderlich.

 

 




