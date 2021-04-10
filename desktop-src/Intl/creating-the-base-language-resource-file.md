---
description: Erstellen der Ressourcen Datei für die Basis Sprache
ms.assetid: 770e1f4b-5258-4b6b-afa4-5c19743daaaa
title: Erstellen der Ressourcen Datei für die Basis Sprache
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b96d566625025c105e123e0e2edf9f4f20721274
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050394"
---
# <a name="creating-the-base-language-resource-file"></a>Erstellen der Ressourcen Datei für die Basis Sprache

Ressourcen für Elemente der Benutzeroberfläche werden für die grundlegende Sprache definiert, die von der Anwendung unterstützt wird, z. b. Englisch (USA). Ein Beispiel für eine Win32 PE-Ressourcen Datei ist eine RC-Datei, die mit dem RC-Compiler erstellt wurde. Ausführliche Informationen zum Erstellen von RC-Dateien finden Sie unter Informationen [zu Ressourcen Dateien](../menurc/about-resource-files.md).

Wenn Sie eine RC-Datei für die Basis Sprachen Ressourcen verwenden, haben Sie die Möglichkeit, eine Ressourcen Konfigurationsdatei für eine XML-Darstellung der Ressourcen Konfigurationsdaten zu verwenden. Informationen zum Erstellen dieser Datei finden Sie unter [Vorbereiten einer Ressourcen Konfigurationsdatei](preparing-a-resource-configuration-file.md).

Sie können auch eine nicht-Win32 PE-Datei verwenden, um Basis Sprachen Ressourcen zu definieren. Beispielsweise können Sie eine XML-Datei oder eine txt-Datei zu diesem Zweck verwenden.

> [!Note]  
> Wenn Sie Basis Sprachen Ressourcen mit einer nicht-Win32-PE-Datei definieren, können Sie den RC-Compiler nicht für die Ressourcendefinition verwenden. Stattdessen definieren Sie ein eigenes Ressourcen Format, und Ihre Anwendung muss Ihre eigene Funktionalität bereitstellen, um die erforderlichen Ressourcen zu suchen und zu laden.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vorbereiten von Ressourcen](preparing-resources.md)
</dt> <dt>

[Vorbereiten einer Ressourcen Konfigurationsdatei](preparing-a-resource-configuration-file.md)
</dt> </dl>

 

 
