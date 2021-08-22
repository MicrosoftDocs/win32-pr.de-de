---
description: Eine private Assembly ist eine Assembly, die mit einer Anwendung bereitgestellt wird und für die exklusive Verwendung dieser Anwendung verfügbar ist.
ms.assetid: 5E0E7423-85BD-4ED0-9149-9541F4D2371F
title: Informationen zu privaten Assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c785b30ca8654071a9816aaf9a11ecc69a029f605d06f39f44a6a490a2a7aef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142613"
---
# <a name="about-private-assemblies"></a>Informationen zu privaten Assemblys

Eine private Assembly ist eine Assembly, die mit einer Anwendung bereitgestellt wird und für die exklusive Verwendung dieser Anwendung verfügbar ist. Das heißt, dass andere Anwendungen die private Assembly nicht gemeinsam nutzen. Private Assemblys sind eine der Methoden, die zum Erstellen [isolierter Anwendungen](isolated-applications.md)verwendet werden können. Weitere Informationen finden Sie unter [Informationen zu isolierten Anwendungen und nebeneinander verwendeten Assemblys.](about-isolated-applications-and-side-by-side-assemblies.md)

Private Assemblys müssen so entworfen werden, dass sie nebeneinander mit anderen Versionen der Assembly auf dem System funktionieren. Weitere Informationen finden Sie unter [Guidelines for Creating Side-by-side Assemblies](guidelines-for-creating-side-by-side-assemblies.md).

Private Assemblys müssen von einem [Assemblymanifest](assembly-manifests.md)begleitet werden. Beachten Sie, dass beim Packen einer DLL als private Assembly Namenseinschränkungen gelten, um die Art und Weise zu berücksichtigen, wie Windows nach privaten Assemblys sucht. Bei der Suche nach privaten Assemblys wird empfohlen, das Assemblymanifest als Ressource in die DLL einzufügen. In diesem Fall muss die Ressourcen-ID gleich 1 sein, und der Name der privaten Assembly kann mit dem Namen der DLL übereinstimmen. Wenn der Name der DLL beispielsweise MICROSOFT.WINDOWS.MYSAMPLE.DLL ist, kann der Wert des namensattributs, das im **assemblyIdentity-Element** des Manifests verwendet wird, auch Microsoft sein. Windows.mysample. Eine alternative Methode zum Suchen nach privaten Assemblys besteht darin, das Assemblymanifest in einer separaten Datei bereitzustellen. In diesem Fall müssen sich der Name der Assembly und ihr Manifest vom Namen der DLL unterscheiden. Beispiel: Microsoft. Windows.mysampleAsm, Microsoft. Windows.mysampleAsm.manifest und Microsoft.Windows.mysample.dll. Weitere Informationen dazu, wie nebeneinander nach privaten Assemblys sucht, finden Sie unter [Assemblysuchsequenz.](assembly-searching-sequence.md)

Private Assemblys werden in einem Ordner der Verzeichnisstruktur der Anwendung installiert. In der Regel ist dies der Ordner, der die ausführbare Datei der Anwendung enthält. Private Assemblys können im selben Ordner wie die Anwendung, in einem Ordner mit dem gleichen Namen wie die Assembly oder in einem sprachspezifischen Unterordner mit dem gleichen Namen wie die Assembly bereitgestellt werden. Verwenden Sie beispielsweise eine der folgenden Verzeichnisstrukturen, um eine private Assembly, Microsoft.tools.pop, ohne Angabe der Sprache bereitzustellen.



| Verzeichnisstruktur                                       | Beschreibung                                                                                            |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| \\APPDIR-MICROSOFT.TOOLS.POP.DLL                           | Das Manifest wird als Ressource in der DLL bereitgestellt.                                                     |
| Appdir \\ Microsoft.Tools.Pop.MANIFEST                      | Das Manifest wird als separate Datei bereitgestellt.                                                           |
| APPDIR \\ MICROSOFT. Werkzeuge. \\ POP-MICROSOFT.TOOLS.POP.DLL      | Das Manifest wird als Ressource in der DLL bereitgestellt, die sich in einem Unterordner mit dem Namen der Assembly befindet. |
| Appdir \\ Microsoft.Tools.Pop \\ Microsoft.Tools.Pop.MANIFEST | Das Manifest wird als separate Datei in einem Unterordner mit dem Namen der Assembly bereitgestellt.                 |



 

> [!IMPORTANT]
>
> Für Versionen des Windows Betriebssystems vor Windows 7 und Windows Server 2008 R2 müssen native private Assemblys in dem Ordner bereitgestellt werden, der die ausführbare Datei der Anwendung enthält. Die Installation in einem sprachspezifischen Ordner oder in dem Ordner mit demselben Namen wie die Assembly wird für native private Assemblys nicht unterstützt.

 

Verwenden Sie eine der folgenden Verzeichnisstrukturen, um eine private Assembly, Microsoft.tools.pop, mit einer angegebenen Sprache bereitzustellen. Im folgenden Beispiel ist die von Microsoft.Tools.Pop verwendete Sprache Englisch (USA), und der Sprachcode lautet en-us. Ersetzen Sie die Assembly durch den richtigen DHTML-Sprachcode.

``` syntax
appdir\en-us\Microsoft.tools.pop.DLL
appdir\en-us\Microsoft.tools.pop.MANIFEST
appdir\en-us\Microsoft.tools.pop\Microsoft.tools.pop.DLL
appdir\en-us\Microsoft.tools.pop\Microsoft.tools.pop.MANIFEST
```

Private Assemblys können mit jeder Installationsmethode installiert werden, die die Assemblydatei in diesen Ordner kopieren kann, z. B. den **xcopy-Befehl.** Weitere Informationen zum Installieren privater Assemblys mithilfe des Windows Installers finden Sie unter [Installation von Win32-Assemblys.](../msi/installation-of-win32-assemblies.md)

Private Assemblys können auch auf Betriebssystemen vor Windows XP installiert werden. In diesem Fall muss die Assembly registriert werden, und unter diesen Betriebssystemen wird das Manifest nicht verwendet. Eine Kopie der privaten Assembly wird zur exklusiven Verwendung der Anwendung in einem privaten Ordner installiert. Eine andere Version der Assembly kann global auf dem System registriert und für jede Anwendung verfügbar sein, die an sie gebunden ist. Die globale Version der Assembly kann die Version sein, die mit der Anwendung oder einer früheren Version installiert wurde. Weitere Informationen finden Sie unter [DLL/COM-Umleitung auf Windows](dll-com-redirection-on-windows.md). Eine Assembly kann auch als freigegebene Assembly für die Verwendung durch mehrere Anwendungen installiert werden. Weitere Informationen finden Sie unter [Freigegebene Assemblys.](/windows/desktop/Msi/shared-assemblies)

Beachten Sie, dass die Schritte zum Erstellen einer privaten Assembly mit denen zum Erstellen einer freigegebenen Assembly mit zwei Ausnahmen identisch sind:

-   Eine private Assembly muss nicht signiert werden, und **publickeyToken** ist im **assemblyIdentity-Element** des Assemblymanifests nicht erforderlich.
-   Private Assemblys können mithilfe einer beliebigen Installationstechnologie im Ordner der Anwendung installiert werden. Private Assemblys müssen nicht mit dem Windows Installer installiert werden.

 

 
