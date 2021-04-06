---
title: Mdmerge-und Metadatendateien
description: Verfasst mehrere Metadatendateien (. winmd) in einer Reihe von Ausgabe Metadatendateien, basierend auf dem Namespace.
ms.assetid: A3203627-82DF-4744-BBBC-53D13F30210E
keywords:
- metadata
- winmd-Datei
- Windows-Metadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2d91f8c7506dd80fd2477beb61c5b99a26b05b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947449"
---
# <a name="mdmerge-and-metadata-files"></a>Mdmerge-und Metadatendateien

Verfasst mehrere Metadatendateien (. winmd) in einer Reihe von Ausgabe Metadatendateien, basierend auf dem Namespace.

## <a name="usage"></a>Verbrauch

Führen Sie mdmerge über die Befehlszeile mit dem folgenden Befehl aus:

**mdmerge** - *< ***Optionen***>*

Where- *< ***Optionen*** >* stellt die Befehlszeilenoptionen dar, die Sie verwenden möchten.

Generieren Sie Metadatendateien für die benutzerdefinierten Windows-Runtime Komponenten mithilfe des complrt-Compilers. Weitere Informationen finden Sie unter " [Mittel LRT-und Windows-Runtime Komponenten](midlrt-and-windows-runtime-components.md).

## <a name="command-line-switches"></a>Befehlszeilenschalter

Die folgende Liste zeigt die Befehls Zeilenschalter, die von mdmerge verwendet werden.

<dl>

[**/i**](-mdmerge-i.md)  
[**/Metadata \_ dir**](-mdmerge-metadata-dir.md)  
[**/n**](-mdmerge-n.md)  
[**/o**](-mdmerge-o.md)  
[**/partial**](-mdmerge-partial.md)  
[**/v**](-mdmerge-v.md)  
</dl>

Eine komplette Liste der mdmerge-Compilerschalter und-Optionen ist verfügbar, wenn Sie das **-h** und **/?** Mikro.

## <a name="remarks"></a>Bemerkungen

Die metadatenkomposition ermöglicht, dass mehrere IDL-Dateien Definitionen für Windows-Runtime Komponenten im gleichen Namespace enthalten. Dadurch werden alle Typen in einem Namespace innerhalb einer einzelnen IDL-Datei definiert.

Wahrscheinlich verfügen Sie über zahlreiche Windows-Runtime Komponenten, die von ihren apps verwendet werden. Wenn Sie den letzten Schritt ausführen, um bereitstell Bare Windows-Runtime Metadatenassemblys zu erstellen, können Sie mdmerge so konfigurieren, dass Komponenten aus mehreren metadatenverzeichnissen zusammengeführt werden, z. b. mit dem System (% Windows% \\ system32 \\ winmetadata), den Foundation-Typen und dem Buildverzeichnis Ihres aktuellen Projekts. Alle erforderlichen Typen werden mit den richtigen, bereitstell baren Metadatenassemblys zusammengeführt, die Sie für den Windows Store verpacken können.

Mit der [**/n**](-mdmerge-n.md) -Option können Sie die unterstützte Namespace Tiefe für das Verfassen von Metadatenassemblys angeben. Dadurch wird die Konfiguration einer aktiven Teilung für Ihre Windows-Runtime Komponenten ermöglicht, sodass anstelle von vielen nur eine einzelne winmd-Datei gepackt wird. Dies reduziert die Ladezeiten und Datei-e/a, die von Ihren Windows Store-Apps benötigt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Mittlere und Windows-Runtime Komponenten](midlrt-and-windows-runtime-components.md)
</dt> </dl>

 

 




