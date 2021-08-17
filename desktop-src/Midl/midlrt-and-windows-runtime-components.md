---
title: MIDLRT- und Windows Runtime-Komponenten
description: Zeigt, wie Metadatendateien (WINMD) erstellt werden, die die API für benutzerdefinierte Windows Runtime-Komponenten darstellen.
ms.assetid: 7830A5DB-9696-4A93-948B-51DA46A5143C
keywords:
- MIDL-Compiler-MIDL
- MIDL-Compiler MIDL, MIDL und Windows Runtime winrt
- Windows Runtime MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f827178216bbb7e78c16f2c11fa68b29b2eb50cfc0714a0ed53b02ce5bdc4ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642904"
---
# <a name="midlrt-and-windows-runtime-components"></a>MIDLRT- und Windows Runtime-Komponenten

Zeigt, wie Metadatendateien (WINMD) erstellt werden, die die API für benutzerdefinierte Windows Runtime-Komponenten darstellen.


Verwenden Sie den MIDLRT-Compiler, um Metadatendateien (.winmd) für Ihre benutzerdefinierten Windows Runtime-Komponenten zu erstellen.

Wenn Ihre Metadatendateien generiert werden, können Sie sie mithilfe des MDMERGE-Hilfsprogramms in einem effizienteren Paket zusammenstellen. Weitere Informationen finden Sie unter [MDMERGE und Metadatendateien.](mdmerge-and-metadata-files.md)


Die Verwendung von MIDLRT ähnelt der Verwendung des MIDL-Compilers. Führen Sie MIDLRT über die Befehlszeile mit dem folgenden Befehl aus:

**midlrt**  *<* **Optionen** _>_ **filename.idl**

wobei *<*-Optionen _>_ die Befehlszeilenoptionen darstellen, die Sie verwenden möchten, und Filename.idl der Name der zu kompilierenden IDL-Datei ist.


Die folgende Liste zeigt die Befehlszeilenschalter, die MIDLRT.EXE verwendet.

<dl>

[**\_/enum-Klasse**](-enum-class.md)  
[**/metadata \_ dir**](-metadata-dir.md)  
[**/nomidl**](-nomidl.md)  
[**/nomd**](-nomd.md)  
[**\_/ns-Präfix**](-ns-prefix.md)  
[**/winmd**](-winmd.md)  
[**/winrt**](-winrt.md)  
</dl>

Eine vollständige Liste der MIDLRT-Compilerschalter und -Optionen ist verfügbar, wenn Sie den MIDLRT-Compiler [**/help**](-help-.md) und /? verwenden. Schalter. Die Switches sind nach Kategorien organisiert. Weitere Informationen finden Sie in der [MIDL Command-Line Reference](midl-command-line-reference.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[MDMERGE- und Metadatendateien](mdmerge-and-metadata-files.md)
</dt> </dl>

 

 




