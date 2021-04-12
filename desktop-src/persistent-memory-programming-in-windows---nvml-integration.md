---
description: Die Technologie für persistente Speicher (PM) bietet Zugriff auf bytebene auf nicht flüchtige Medien und reduziert gleichzeitig die Latenz beim Speichern oder Abrufen von Daten.
ms.assetid: 68BF6074-09CB-4D6E-8BFD-FBA297391286
title: Persistente Speicher Programmierung in Windows-nvml-Integration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c9f033963a8fecded8943eb053781d05a78d568
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218111"
---
# <a name="persistent-memory-programming-in-windows---nvml-integration"></a>Persistente Speicher Programmierung in Windows-nvml-Integration

Die Technologie für persistente Speicher (PM) bietet Zugriff auf bytebene auf nicht flüchtige Medien und reduziert gleichzeitig die Latenz beim Speichern oder Abrufen von Daten. Es wird eine neue Ebene zwischen dem Arbeitsspeicher des Systems und dem herkömmlichen Speicher erstellt. Jedes Programm, das von einem persistenten Medium abhängig ist oder mit diesem skaliert werden kann, kann von pm profitieren.

In diesem Artikel wird erläutert, wie die nicht flüchtige Speicher Bibliothek (nvml) zur einfachen Verwendung in ein Visual Studio-Projekt integriert werden kann.

> [!Note]  
> Persistenter Speicher wird manchmal auch als Speicher Klassen Speicher (SCM) bezeichnet.

 

## <a name="pm-and-nvml"></a>PM und nvml

Die erste Unterstützung für permanenten Speicher wurde in Windows Server 2016 und Windows 10 Anniversary Update (1607) eingeführt. Eine kurze Übersicht finden Sie in den folgenden beiden channel9-Videos:

-   [Using Non-volatile Memory (NVDIMM-N) as Block Storage in Windows Server 2016 (Verwenden von permanentem Speicher [NVDIMM-N] als Blockspeicher in Windows Server 2016)](https://channel9.msdn.com/Events/Build/2016/P466)
-   [Using Non-volatile Memory (NVDIMM-N) as Byte-Addressable Storage in Windows Server 2016 (Verwenden von permanentem Speicher [NVDIMM-N] als byteadressierbaren Speicher in Windows Server 2016)](https://channel9.msdn.com/Events/Build/2016/P470)

Damit Entwickler die Vorteile der persistenten Speicher Angebote nutzen können, hat Microsoft auch zu den Bemühungen beigetragen, die nicht flüchtige Speicher Bibliothek (nvml) in Windows zu unterstützen. Diese Bibliothek bietet verschiedene Tools, mit denen Anwendungen persistente Speicher fähig werden. Sie enthält z. b. Code, mit dem Sie problemlos einen PM-fähigen Schlüssel-Wert-Speicher für extrem schnelle Suche und Speicher erstellen können. Weitere Informationen zu nvml, einschließlich Beispielen, finden Sie in der [NVM-Bibliothek](https://pmem.io/nvml/).

## <a name="integrating-nvml-into-a-visual-studio-project"></a>Integrieren von nvml in ein Visual Studio-Projekt

1. Herunterladen der nvml-Bibliotheksdateien und-Header

-   Nvml wird auf GitHub verwaltet. Sie können entweder die Quelle selbst kompilieren oder nur kompilierte Binärdateien direkt von hier herunterladen: [nvml Version 1,2-Windows Technical Preview](https://github.com/pmem/pmdk/releases/tag/1.2%2Bwtp1).

2. Platzieren Sie die Bibliotheksdateien und Header in einem Verzeichnis Ihrer Wahl, z. b.: "c: \\ nvml \\ lib" und "c: \\ nvml \\ Inc".

3. Konfigurieren Sie das Projekt wie folgt:

-   Öffnen Sie das Visual Studio-Projekt, und klicken Sie in der Projektmappen-Explorer mit der rechten Maustaste auf den Namen Ihres Projekts.
-   Öffnen Sie den Einstellungsbereich des Projekts am unteren Rand des resultierenden Popup Fensters.
-   Navigieren Sie zu "Konfigurations Eigenschaften-> C/C++", und fügen Sie den Ordner, in dem Sie den Header (C: \\ nvml \\ Inc) gespeichert haben, dem Feld "Zusätzliche Includeverzeichnisse" hinzu.
-   Navigieren Sie als nächstes zu "Konfigurations Eigenschaften-> Linker", und fügen Sie den Ordner, in dem Sie die Bibliothek (C: \\ nvml \\ lib) gespeichert haben, in das Feld "zusätzliche Bibliotheks Verzeichnisse" ein.

4. Stellen Sie als nächstes sicher, dass Sie das Projekt für Windows Server 2016 oder Windows 10 Anniversary Update als Ziel festlegen:

-   Navigieren Sie zu "Konfigurations Eigenschaften-> Allgemein", und legen Sie das Feld "Ziel Platt Form Version" auf "10.0.14393.0" und
-   Navigieren Sie zu "Konfigurations Eigenschaften-> C/C++", und fügen Sie \_ \_ \_ dem Feld "Preprocessor" den Wert "ntddi Version = ntddi WIN10 RS1;" hinzu.

5. Schließen Sie die Header in Ihren Code ein, und verknüpfen Sie die erforderlichen Bibliotheken.

-   An diesem Punkt können Sie einfach die Header Dateien, die Sie in Ihrem Code verwenden möchten, wie alle anderen Header Dateien einschließen. Verwenden Sie beispielsweise, um libpmem zu verwenden:
    -   Fügen Sie " \# include <libpmem. h>" und
    -   Fügen Sie "libpmem. lib" zu "Konfigurations Eigenschaften-> Linker-> Eingabe > zusätzliche Abhängigkeiten" hinzu.

An diesem Punkt können Sie die Funktionen der Bibliothek direkt im Code aufzurufen und Sie nutzen.

 

 



