---
description: Die Technologie für persistenten Speicher (Persistent Memory, PM) bietet Zugriff auf Byteebene auf nicht flüchtige Medien und reduziert gleichzeitig die Latenz beim Speichern oder Abrufen von Daten erheblich.
ms.assetid: 68BF6074-09CB-4D6E-8BFD-FBA297391286
title: Persistente Speicherprogrammierung in Windows – NVML-Integration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 750a05f28ca4698091f79b1004bbbb00ff69752e0ff45f2153cc4f0b7fe20a26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951050"
---
# <a name="persistent-memory-programming-in-windows---nvml-integration"></a>Persistente Speicherprogrammierung in Windows – NVML-Integration

Die Technologie für persistenten Speicher (Persistent Memory, PM) bietet Zugriff auf Byteebene auf nicht flüchtige Medien und reduziert gleichzeitig die Latenz beim Speichern oder Abrufen von Daten erheblich. Es wird eine neue Ebene zwischen dem Speicher eines Systems und dem herkömmlichen Speicher erstellt. Jedes Programm, das von abhängig ist oder mit schnellen Schreibvorgängen auf ein persistentes Medium skaliert wird, kann von PM profitieren.

In diesem Artikel wird erläutert, wie die NVML (Non-Volatile Memory Library) zur einfachen Verwendung in ein Visual Studio integriert werden kann.

> [!Note]  
> Persistenter Speicher wird manchmal auch als Storage Class Memory (SCM) bezeichnet.

 

## <a name="pm-and-nvml"></a>PM und NVML

Die erste Unterstützung für persistenten Speicher wurde in Windows Server 2016 und dem Windows 10 Anniversary Update (1607) eingeführt. Eine kurze Übersicht finden Sie in diesen beiden Channel9-Videos:

-   [Using Non-volatile Memory (NVDIMM-N) as Block Storage in Windows Server 2016 (Verwenden von permanentem Speicher [NVDIMM-N] als Blockspeicher in Windows Server 2016)](https://channel9.msdn.com/Events/Build/2016/P466)
-   [Using Non-volatile Memory (NVDIMM-N) as Byte-Addressable Storage in Windows Server 2016 (Verwenden von permanentem Speicher [NVDIMM-N] als byteadressierbaren Speicher in Windows Server 2016)](https://channel9.msdn.com/Events/Build/2016/P470)

Damit Entwickler von den Vorteilen des beständigen Speichers profitieren können, hat Microsoft auch dazu beigetragen, die NVML-Datei (Non-Volatile Memory Library, nicht flüchtige Speicherbibliothek) in die Windows. Diese Bibliothek stellt verschiedene Tools zur Verfügung, mit derenHilfe Anwendungen beständigen Arbeitsspeicher nutzen können. Sie enthält beispielsweise Code, mit dem Sie problemlos einen PM-orientierten Schlüssel-Wert-Speicher für extrem schnelle Look-Ups und Speicher erstellen können. Weitere Informationen zu NVML, einschließlich Beispielen, finden Sie unter [NVM-Bibliothek.](https://pmem.io/nvml/)

## <a name="integrating-nvml-into-a-visual-studio-project"></a>Integrieren von NVML in Visual Studio Project

1. Herunterladen von NVML-Bibliotheksdateien und -Headern

-   NVML wird auf GitHub. Sie können die Quelle entweder selbst kompilieren oder kompilierte Binärdateien direkt hier herunterladen: [NVML Version 1.2 – Windows Technical Preview](https://github.com/pmem/pmdk/releases/tag/1.2%2Bwtp1).

2. Platzieren Sie die Bibliotheksdateien und Header in einem Verzeichnis Ihrer Wahl, z.B. "C: NVML lib" bzw. \\ \\ "C: \\ NVML \\ inc".

3. Konfigurieren Sie Ihr Projekt wie folgt:

-   Öffnen Sie Ihr Visual Studio-Projekt, und klicken Projektmappen-Explorer mit der rechten Maustaste auf den Namen Ihres Projekts.
-   Öffnen Sie den Einstellungsbereich des Projekts am unteren Rand des resultierenden Popupfensters.
-   Navigieren Sie zu "Konfigurationseigenschaften -> C/C++", und fügen Sie dem Feld "Zusätzliche Includeverzeichnisse" den Ordner hinzu, in dem Sie den Header gespeichert haben (C: \\ NVML \\ inc).
-   Navigieren Sie als Nächstes zu "Konfigurationseigenschaften -> Linker", und fügen Sie dem Feld "Zusätzliche Bibliotheksverzeichnisse" den Ordner hinzu, in dem Sie die Bibliothek gespeichert haben (C: \\ NVML \\ lib).

4. Stellen Sie als Nächstes sicher, dass Sie das Projekt als Ziel Windows Server 2016 oder Windows 10 Anniversary Update:

-   Navigieren Sie zu "Konfigurationseigenschaften -> Allgemein", und legen Sie das Feld "Zielplattformversion" auf "10.0.14393.0" fest.
-   Navigieren Sie zu "Konfigurationseigenschaften -> C/C++", und fügen Sie \_ "NTDDI VERSION=NTDDI \_ WIN10 \_ RS1;" zum Feld "Präprozessor" hinzu.

5. Schließen Sie die Header in Ihren Code ein, und verknüpfen Sie sie mit den erforderlichen Bibliotheken.

-   An diesem Punkt können Sie einfach die Headerdateien, die Sie verwenden möchten, wie alle anderen Headerdateien in Ihren Code ein schließen. So verwenden Sie z. B. libpmem:
    -   add " \# include <libpmem.h>" und
    -   Fügen Sie "libpmem.lib" zu "Konfigurationseigenschaften -> Linker -> Input -> Additional Dependencies" hinzu.

An diesem Punkt können Sie die Funktionen der Bibliothek direkt in Ihrem Code aufrufen und diese nutzen.

 

 



