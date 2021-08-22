---
title: MDMERGE- und Metadatendateien
description: Erstellt mehrere Metadatendateien (.winmd) basierend auf dem Namespace in einer Reihe von Ausgabemetadatendateien.
ms.assetid: A3203627-82DF-4744-BBBC-53D13F30210E
keywords:
- metadata
- winmd-Datei
- Windows-Metadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a065a8ff93485728b1c5c4c0c7b43de88e3844a8a013f07caee8d85d76d721d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119252430"
---
# <a name="mdmerge-and-metadata-files"></a>MDMERGE- und Metadatendateien

Erstellt mehrere Metadatendateien (.winmd) basierend auf dem Namespace in einer Reihe von Ausgabemetadatendateien.

## <a name="usage"></a>Verbrauch

Führen Sie MDMERGE über die Befehlszeile mit dem folgenden Befehl aus:

**mdmerge**  *<* **Optionen**_>_

wobei *<*-Optionen _>_ die Befehlszeilenoptionen darstellen, die Sie verwenden möchten.

Generieren Sie Metadatendateien für Ihre benutzerdefinierten Windows Runtime-Komponenten mithilfe des MIDLRT-Compilers. Weitere Informationen finden Sie unter [MIDLRT und Windows Runtime-Komponenten.](midlrt-and-windows-runtime-components.md)

## <a name="command-line-switches"></a>Befehlszeilenschalter

Die folgende Liste zeigt die Befehlszeilenschalter, die MDMERGE verwendet.

<dl>

[**/i**](-mdmerge-i.md)  
[**/metadata \_ dir**](-mdmerge-metadata-dir.md)  
[**/n**](-mdmerge-n.md)  
[**/o**](-mdmerge-o.md)  
[**/partial**](-mdmerge-partial.md)  
[**/v**](-mdmerge-v.md)  
</dl>

Eine vollständige Liste der MDMERGE-Compilerschalter und -Optionen ist verfügbar, wenn Sie **-h** und **/? verwenden.** Schalter.

## <a name="remarks"></a>Hinweise

Die Metadatenkomposition ermöglicht es mehreren IDL-Dateien, Definitionen für Windows Runtime-Komponenten im gleichen Namespace zu enthalten. Dadurch können Sie nicht alle Typen in einem Namespace innerhalb einer einzelnen IDL-Datei definieren.

Wahrscheinlich verfügen Sie über zahlreiche Windows Runtime-Komponenten, die Ihre Apps verwenden. Wenn Sie den letzten Schritt ausführen, um bereitstellbare Windows Runtime-Metadatenassemblys zu erstellen, können Sie MDMERGE so konfigurieren, dass Komponenten aus mehreren Metadatenverzeichnissen zusammengeführt werden, z. B. diejenigen, die mit dem System installiert sind (%WINDOWS% \\ system32 \\ WinMetadata), Ihre Basistypen und das Buildverzeichnis Ihres aktuellen Projekts. Alle erforderlichen Typen werden in die richtigen, bereitstellbaren Metadatenassemblys zusammengeführt, die Sie für die Windows Store packen können.

Sie können die Option [**/n**](-mdmerge-n.md) verwenden, um die unterstützte Namespacetiefe für das Zusammenstellen von Metadatenassemblys anzugeben. Dies ermöglicht das Konfigurieren einer hot-Aufteilung für Ihre Windows Runtime-Komponenten, sodass nur eine winmd-Datei gepackt wird und nicht viele. Dies reduziert die Ladezeiten und Datei-E/A,die für Ihre Windows Store-Apps erforderlich sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[MIDLRT- und Windows Runtime-Komponenten](midlrt-and-windows-runtime-components.md)
</dt> </dl>

 

 




