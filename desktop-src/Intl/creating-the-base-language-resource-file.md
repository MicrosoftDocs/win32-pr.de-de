---
description: Erstellen der Basissprachressourcendatei
ms.assetid: 770e1f4b-5258-4b6b-afa4-5c19743daaaa
title: Erstellen der Basissprachressourcendatei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72d1d254231e44d6934d3debdcddd788761b8333f687d93aabc8cbdaea342521
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117993231"
---
# <a name="creating-the-base-language-resource-file"></a>Erstellen der Basissprachressourcendatei

Ressourcen für Benutzeroberflächenelemente werden für die grundlegende Sprache definiert, die von der Anwendung unterstützt wird, z. B. Englisch (USA). Ein Beispiel für eine Win32 PE-Ressourcendatei ist eine RC-Datei, die mit dem RC-Compiler erstellt wurde. Weitere Informationen zum Erstellen von RC-Dateien finden Sie unter [Informationen zu Ressourcendateien.](../menurc/about-resource-files.md)

Wenn Sie eine RC-Datei für die Basissprachressourcen verwenden, haben Sie die Möglichkeit, eine Ressourcenkonfigurationsdatei für eine XML-Darstellung von Ressourcenkonfigurationsdaten zu verwenden. Informationen zum Erstellen dieser Datei finden Sie unter [Vorbereiten einer Ressourcenkonfigurationsdatei.](preparing-a-resource-configuration-file.md)

Sie können auch eine Nicht-Win32 PE-Datei verwenden, um Basissprachressourcen zu definieren. Beispielsweise können Sie zu diesem Zweck eine .xml- oder .txt datei verwenden.

> [!Note]  
> Wenn Sie Basissprachressourcen mit einer Nicht-Win32 PE-Datei definieren, können Sie den RC-Compiler nicht für die Ressourcendefinition verwenden. Stattdessen definieren Sie ihr eigenes Ressourcenformat, und Ihre Anwendung muss ihre eigene Funktionalität bereitstellen, um die erforderlichen Ressourcen zu finden und zu laden.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vorbereiten von Ressourcen](preparing-resources.md)
</dt> <dt>

[Vorbereiten einer Ressourcenkonfigurationsdatei](preparing-a-resource-configuration-file.md)
</dt> </dl>

 

 
