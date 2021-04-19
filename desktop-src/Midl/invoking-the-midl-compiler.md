---
title: Aufrufen des Mittel l-Compilers
description: Der mittlerer l-Compiler kann Code für verschiedene Plattformen und System Releases generieren. Weitere Informationen zu vorgeschlagenen Switches und zum Generieren von Code, der für eine bestimmte Version optimiert ist, finden Sie unter/Target.
ms.assetid: 57730efa-71c3-4746-83f4-c7e327888efc
keywords:
- Mittel l compilermittell, aufrufen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b7e03abc49007b823f509acb35bd34ce6e47d80
ms.sourcegitcommit: 1e8e6e6f27c909900cfa8be58b042456331a82ad
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/15/2019
ms.locfileid: "106341270"
---
# <a name="invoking-the-midl-compiler"></a>Aufrufen des Mittel l-Compilers

Der mittlerer l-Compiler kann Code für verschiedene Plattformen und System Releases generieren. Weitere Informationen zu vorgeschlagenen Switches und zum Generieren von Code, der für eine bestimmte Version optimiert ist, finden Sie unter [**/target**](-target.md) .

Führen Sie den-compilercompiler über die Befehlszeile mit dem folgenden Befehl aus:

**Dateiname. idl** für **mittlere** *< ***Optionen*** >*

Where- *< ***Optionen*** >* stellen die Befehlszeilenoptionen dar, die Sie verwenden möchten, und filename. idl ist der Name der zu kompilierenden Mittell-Datei.

Eine vollständige Liste der kompil-Compilerschalter und-Optionen ist verfügbar, wenn Sie den Mittelwert Compiler [**/Help**](-help-.md) und/? verwenden. Mikro. Die Schalter sind nach Kategorien organisiert. Weitere Informationen finden Sie in der [Referenz zur Mittel l-Command-Line](midl-command-line-reference.md).

> [!NOTE]
> Das neue globale Flag **$ (mittlerer l- \_ Optimierung)** ist in Win32. MAK vorhanden. Wenn eine IDL-Datei mit diesem Flag kompiliert wird, kann der generierte Stub die neuesten auf der angegebenen Plattform verfügbaren RPC-Features nutzen und potenziell die Leistung und Stabilität der Anwendung verbessern. Es wird empfohlen, dass Anwendungen dieses Flag bei der Verwendung von "Mittel l" verwenden.
>
> **Mittel l** **$ (mittlere \_ Optimierung)** **...**