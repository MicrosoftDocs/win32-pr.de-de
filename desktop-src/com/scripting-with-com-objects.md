---
title: Skripterstellung mit COM-Objekten
description: Skripterstellung mit COM-Objekten
ms.assetid: d99a561b-67dc-4fc9-adfa-cd7350eb16ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f2b00380a14db2d254675a5826b61f262e8cfe8
ms.sourcegitcommit: 8c981a2f4149b4a9d605ffb71fefda8d82bc696e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2019
ms.locfileid: "103717664"
---
# <a name="scripting-with-com-objects"></a>Skripterstellung mit COM-Objekten

Eine *Skriptsprache* ist eine Programmiersprache, die zur Laufzeit von einer *Skript-Engine* analysiert wird, einer Komponente, die in dieser Sprache geschriebene Skripts in Computercode übersetzt. Jede Skript-Engine übersetzt eine bestimmte Skriptsprache. Ein *Skript Host* ist eine Anwendung, z. b. ein Webbrowser, die eine Skript-Engine zum Ausführen von Skripts hostet. Wenn Ihr Skript Host com unterstützt, können Sie Skripts schreiben, die COM-Objekte verwenden. In den folgenden Themen wird das Skripting von Hosts beschrieben, die COM-Objekte, gängige Skriptsprachen und die Übersetzung zwischen Skriptsprachen unterstützen.

Eine Skriptsprache unterscheidet sich von einer kompilierten Sprache darin, dass Sie zur Laufzeit in Computercode übersetzt wird. Dies bedeutet, dass bei jedem Ausführen eines Skripts die Skript-Engine zuerst den Code analysiert und dann ausführt. Im Gegensatz dazu werden kompilierte Sprachen, wie z. b. C++, während der Kompilierung einmal in Computercode übersetzt. Wenn Sie eine kompilierte Anwendung ausführen, führt das Betriebssystem einfach den vorkompilierten Code aus.

Da eine Skript-Engine jedes Mal, wenn Sie ausgeführt wird, ein Skript neu erstellen muss, sind Skriptsprachen in der Regel langsamer und weniger effizient als die vorkompilierten Entsprechungen. Der Vorteil von Skripts ist jedoch, dass Sie einfach zu schreiben und zu warten sind. Skriptsprachen sind in der Regel einfacher als vorkompilierte Sprachen, und wenn sich ein Skript ändert, muss es nicht erneut kompiliert werden. Für kleinere und schnell veränderliche Anwendungen, z. b. Webseiten, sind Skriptsprachen ideal.

Es gibt mehrere Host Umgebungen, in denen Sie Skripts schreiben können, die COM-Objekte verwenden, wie im folgenden beschrieben:

-   [Einbetten von COM-Objekten in Webseiten](embedding-com-objects-in-web-pages.md)
-   [Verwenden von COM-Objekten in Active Server Seiten](using-com-objects-in-active-server-pages.md)
-   [Verwenden von COM-Objekten in Windows Script Host](using-com-objects-in-windows-script-host.md)
-   [Skripterstellung für COM-Objekte in benutzerdefinierten Anwendungen](scripting-com-objects-in-custom-applications.md)

In jeder der oben erwähnten Host Umgebungen analysiert und führt eine Skript-Engine das Skript aus. Da die Engine für jede Skriptsprache eine separate Komponente ist, können Sie eine neue Skriptsprache zu einer Umgebung hinzufügen, indem Sie eine neue Engine hinzufügen.

Die am häufigsten verwendeten Skriptsprachen sind:

-   Microsoft Visual Basic Scripting Edition (VBScript), eine Teilmenge der Visual Basic.
-   JavaScript, die Netscape Scripting Language, früher als LiveScript bezeichnet.
-   Microsoft JScript Development Software, die Microsoft-Implementierung der ECMA 262-Sprachspezifikation.

Microsoft stellt Skript-Engines für JScript und VBScript bereit. Andere Softwareunternehmen stellen ActiveX-Skript-Engines für Sprachen wie z. b. Perl Script, Pscript, Python und andere bereit.

Weitere Informationen finden Sie in der [ECMA 262-Sprachspezifikation](https://www.ecma-international.org/publications/standards/Ecma-262.htm).

Beachten Sie, dass die meisten Skriptsprachen, z. b. VBScript und JScript, nicht auf Dateien zugreifen oder diese ändern können. Diese Unfähigkeit hindert das Skript daran, Daten auf Client Computern zu ändern. Für COM-Objekte gelten jedoch keine Einschränkungen. Nachdem Sie auf Client Computern heruntergeladen und installiert wurden, können Sie alle Standard Anwendungs Aktionen ausführen. Daher sollten Benutzer ActiveX-Steuerelemente nur aus vertrauenswürdigen Quellen herunterladen und ausführen.

Informationen zum Übersetzen zwischen Skriptsprachen finden Sie in den folgenden Themen:

-   [Übersetzen in VBScript](translating-to-vbscript.md)
-   [Übersetzen in JScript](translating-to-jscript.md)
-   [Übersetzen in JavaScript](translating-to-javascript.md)

 

 




