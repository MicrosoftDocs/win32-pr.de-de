---
title: MIDL-Compilerfehler und -Warnungen
description: Bei Verwendung des MIDL-Compilers können Fehler und Warnungen durch eine falsche Verwendung der Befehlszeilenschalter oder durch den Inhalt der IDL- und ACF-Dateien verursacht werden.
ms.assetid: 5c8d5a28-e559-4893-932f-b2306aefa932
keywords:
- Microsoft Interface Definition Language MIDL , Referenz
- MIDL-Compiler MIDL , Fehler
- Compiler MIDL , Fehler
- Fehler MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f6c2dfd830a1240e2af107eb4a3f1799eafcd0de35ccec7f3756b3e9de5bbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146403"
---
# <a name="midl-compiler-errors-and-warnings"></a>MIDL-Compilerfehler und -Warnungen

Bei Verwendung des MIDL-Compilers können Fehler und Warnungen durch eine falsche Verwendung der Befehlszeilenschalter oder durch den Inhalt der IDL- und ACF-Dateien verursacht werden. Wenn der Fehler auf eine nicht ordnungsgemäße Eingabe der Befehlszeilenschalter verursacht wird, kann in einer Fehler- oder Warnmeldung der Name mindestens eines MIDL-Compilermodusschalters angegeben werden. Sie können z. B. bestimmte ACF-Attribute in eine IDL-Datei einfgen, wenn Sie den Schalter **/app \_ config** verwenden. Diese IDL-Datei generiert jedoch einen Fehler, wenn Sie kompilieren, ohne den Konfigurationsschalter **/app \_ zu** verwenden.

Fehler in den IDL- und ACF-Dateien lassen sich in zwei Kategorien unterteilen: Fehler, die vom Präprozessor erfasst werden, und Fehler, die vom Compiler erkannt werden. In diesem Abschnitt werden die MIDL-Präprozessor- und Compilerfehlermeldungen aufgeführt. Außerdem werden die Formate und Ursachen beschrieben.

-   [Fehler- und Warnmeldungsformate](error-and-warning-message-formats.md)
-   [Präprozessorfehler](preprocessor-errors.md)
-   [Compilerfehler](compiler-errors.md)

 

 




