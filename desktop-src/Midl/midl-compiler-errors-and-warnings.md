---
title: Compilerfehler und-Warnungen
description: Bei Verwendung des compl-Compilers können Fehler und Warnungen durch eine nicht ordnungsgemäße Verwendung der Befehls Zeilenschalter oder durch den Inhalt der IDL-und ACF-Dateien verursacht werden.
ms.assetid: 5c8d5a28-e559-4893-932f-b2306aefa932
keywords:
- Microsoft Interface Definition Language-Mittell, Referenz
- Mittel l compilermittell, Fehler
- compilermittell, Fehler
- Fehler-Mittell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ae531528f83f3731b4449c7aba012f3228edd9a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855192"
---
# <a name="midl-compiler-errors-and-warnings"></a>Compilerfehler und-Warnungen

Bei Verwendung des compl-Compilers können Fehler und Warnungen durch eine nicht ordnungsgemäße Verwendung der Befehls Zeilenschalter oder durch den Inhalt der IDL-und ACF-Dateien verursacht werden. Wenn der Fehler darauf zurückzuführen ist, dass die Befehls Zeilenschalter nicht ordnungsgemäß eingegeben werden, kann in einer Fehler-oder Warnmeldung der Name eines oder mehrerer Mittell-compilermodusschalter angegeben werden. Beispielsweise können Sie bestimmte ACF-Attribute in eine IDL-Datei einschließen, wenn Sie den Schalter/**App \_ config** verwenden. diese IDL-Datei generiert jedoch einen Fehler, wenn Sie ohne den Schalter/**App- \_ Konfiguration** verwenden.

Fehler in den IDL-und ACF-Dateien werden in zwei Kategorien unterteilt: Fehler, die vom Präprozessor abgefangen wurden, und Fehler, die vom Compiler erkannt werden. In diesem Abschnitt werden die-präprozessorfehlermeldungen und-Compilerfehlermeldungen aufgeführt. Außerdem werden ihre Formate und Gründe beschrieben.

-   [Formate für Fehler-und Warnmeldungen](error-and-warning-message-formats.md)
-   [Präprozessorfehler](preprocessor-errors.md)
-   [Compilerfehler](compiler-errors.md)

 

 




