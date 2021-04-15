---
title: Mittlere und Windows-Runtime Komponenten
description: Zeigt, wie Metadatendateien (. winmd) erstellt werden, die die API für benutzerdefinierte Windows-Runtime Komponenten darstellen.
ms.assetid: 7830A5DB-9696-4A93-948B-51DA46A5143C
keywords:
- Mittel l-compilermittell
- Mittel l-compilermittell, Mittel l und Windows-Runtime WinRT
- Windows-Runtime-Mittell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4edf4d40b3fc5b0a5ed8eeb9b5fd47a3b87c4543
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104517216"
---
# <a name="midlrt-and-windows-runtime-components"></a>Mittlere und Windows-Runtime Komponenten

Zeigt, wie Metadatendateien (. winmd) erstellt werden, die die API für benutzerdefinierte Windows-Runtime Komponenten darstellen.


Verwenden Sie den-compilercompiler, um Metadatendateien (. winmd) für die benutzerdefinierten Windows-Runtime Komponenten zu erstellen.

Wenn Ihre Metadatendateien generiert werden, können Sie Sie mithilfe des Hilfsprogramms "mdmerge" in ein effizienteres Paket zerlegen. Weitere Informationen finden Sie unter [mdmerge-und Metadatendateien](mdmerge-and-metadata-files.md).


Die Verwendung von "Mittell" ähnelt der Verwendung des compl-Compilers. Führen Sie in der Befehlszeile den folgenden Befehl aus:

**mittlere**  *<* **Optionen** _>_ **Dateiname. idl**

Where * < *-**Optionen** _>_ stellt die Befehlszeilenoptionen dar, die Sie verwenden möchten, und filename. idl ist der Name der zu kompilierenden IDL-Datei.


In der folgenden Liste sind die Befehls Zeilenschalter aufgeführt, die von MIDLRT.EXE verwendet werden.

<dl>

[**/Enum- \_ Klasse**](-enum-class.md)  
[**/Metadata \_ dir**](-metadata-dir.md)  
[**/nomidl**](-nomidl.md)  
[**/nomd**](-nomd.md)  
[**/NS- \_ Präfix**](-ns-prefix.md)  
[**/winmd**](-winmd.md)  
[**/WinRT**](-winrt.md)  
</dl>

Eine umfassende Liste mit den Compilerschaltern und-Optionen für den Mittelwert ist verfügbar, wenn Sie den-Compilerschalter [**/Help**](-help-.md) und/? verwenden. Mikro. Die Schalter sind nach Kategorien organisiert. Weitere Informationen finden Sie in der [Referenz zur Mittel l-Command-Line](midl-command-line-reference.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Mdmerge-und Metadatendateien](mdmerge-and-metadata-files.md)
</dt> </dl>

 

 




