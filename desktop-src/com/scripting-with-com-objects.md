---
title: Skripterstellung mit COM-Objekten
description: Skripterstellung mit COM-Objekten
ms.assetid: d99a561b-67dc-4fc9-adfa-cd7350eb16ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c40d94ddd0316d3a921d5d1ecd4591775700c967008ad801cdd8439a341dd9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117918381"
---
# <a name="scripting-with-com-objects"></a>Skripterstellung mit COM-Objekten

Eine *Skriptsprache* ist eine Programmiersprache, die zur Laufzeit von einer *Skript-Engine* analysiert wird, einer Komponente, die in dieser Sprache geschriebene Skripts in Computercode übersetzt. Jede Skript-Engine übersetzt eine bestimmte Skriptsprache. Ein *Skripthost* ist eine Anwendung, z. B. ein Webbrowser, die eine Skript-Engine zum Ausführen von Skripts hostet. Wenn Ihr Skripthost COM unterstützt, können Sie Skripts schreiben, die COM-Objekte verwenden. In den folgenden Themen werden Skripthosts beschrieben, die COM-Objekte unterstützen, allgemeine Skriptsprachen und die Übersetzung zwischen Skriptsprachen.

Eine Skriptsprache unterscheidet sich von einer kompilierten Sprache darin, dass sie zur Laufzeit in Computercode übersetzt wird. Dies bedeutet, dass jedes Mal, wenn Sie ein Skript ausführen, die Skript-Engine zuerst den Code analysiert und dann ausführt. Im Gegensatz dazu werden kompilierte Sprachen wie C++ einmal während der Kompilierung in Computercode übersetzt. Wenn Sie eine kompilierte Anwendung ausführen, führt das Betriebssystem einfach den vorkompilierten Code aus.

Da eine Skript-Engine bei jeder Ausführung ein Skript neu prüfen muss, sind Skriptsprachen in der Regel langsamer und weniger effizient als ihre vorkompilierten Entsprechungen. Der Vorteil von Skripts ist jedoch, dass sie einfach zu schreiben und zu verwalten sind. Skriptsprachen sind in der Regel einfacher als vorkompilierte Sprachen, und wenn sich ein Skript ändert, muss es nicht erneut kompiliert werden. Für einfache und sich schnell ändernde Anwendungen wie Webseiten sind Skriptsprachen ideal.

Es gibt mehrere Hostumgebungen, in denen Sie Skripts schreiben können, die COM-Objekte verwenden, wie im Folgenden beschrieben:

-   [Einbetten von COM-Objekten in Webseiten](embedding-com-objects-in-web-pages.md)
-   [Verwenden von COM-Objekten in Active Server Pages](using-com-objects-in-active-server-pages.md)
-   [Verwenden von COM-Objekten in Windows Skripthost](using-com-objects-in-windows-script-host.md)
-   [Skripterstellung für COM-Objekte in benutzerdefinierten Anwendungen](scripting-com-objects-in-custom-applications.md)

In jeder der zuvor erwähnten Hostumgebungen analysiert eine Skript-Engine das Skript und führt es aus. Da die Engine für jede Skriptsprache eine separate Komponente ist, können Sie einer Umgebung eine neue Skriptsprache hinzufügen, indem Sie eine neue Engine hinzufügen.

Die am häufigsten verwendeten Skriptsprachen sind:

-   Microsoft Visual Basic Scripting Edition (VBScript), eine Teilmenge von Visual Basic.
-   JavaScript, die Netscape-Skriptsprache, früher als LiveScript bekannt.
-   Microsoft JScript Entwicklungssoftware, die Microsoft-Implementierung der ECMA 262-Sprachspezifikation.

Microsoft stellt Skript-Engines für JScript und VBScript bereit. Andere Softwareunternehmen stellen ActiveX Skript-Engines für Sprachen wie PerlScript, PScript, Python und andere bereit.

Weitere Informationen finden Sie in der [ECMA 262-Sprachspezifikation.](https://www.ecma-international.org/publications/standards/Ecma-262.htm)

Beachten Sie, dass die meisten Skriptsprachen wie VBScript und JScript nicht auf Dateien zugreifen oder diese ändern können. Diese Unfähigkeit verhindert, dass das Skript Daten auf Clientcomputern ändert. COM-Objekte weisen jedoch keine solchen Einschränkungen auf. Nachdem sie heruntergeladen und auf Clientcomputern installiert wurden, können sie eine beliebige Standardanwendungsaktion ausführen. Daher sollten Benutzer nur ActiveX Steuerelemente aus vertrauenswürdigen Quellen herunterladen und ausführen.

Informationen zum Übersetzen zwischen Skriptsprachen finden Sie in den folgenden Themen:

-   [Übersetzen in VBScript](translating-to-vbscript.md)
-   [Übersetzen in JScript](translating-to-jscript.md)
-   [Übersetzen in JavaScript](translating-to-javascript.md)

 

 




