---
description: Bei einem private Assembly handelt es sich um eine Assembly, die mit einer Anwendung bereitgestellt wird und für die ausschließliche Verwendung dieser Anwendung verfügbar ist.
ms.assetid: 5E0E7423-85BD-4ED0-9149-9541F4D2371F
title: Über private Assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c7ccfe8c63a8435a33085f607c2040a0a42345c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106373024"
---
# <a name="about-private-assemblies"></a>Über private Assemblys

Bei einem private Assembly handelt es sich um eine Assembly, die mit einer Anwendung bereitgestellt wird und für die ausschließliche Verwendung dieser Anwendung verfügbar ist. Das heißt, dass andere Anwendungen die private Assembly nicht gemeinsam nutzen. Private Assemblys sind eine der Methoden, die zum Erstellen [isolierter Anwendungen](isolated-applications.md)verwendet werden können. Weitere Informationen finden Sie unter Informationen [zu isolierten Anwendungen und](about-isolated-applications-and-side-by-side-assemblies.md)parallelen Assemblys.

Private Assemblys müssen so entworfen werden, dass Sie parallel mit anderen Versionen der Assembly auf dem System funktionieren. Weitere Informationen finden Sie unter [Richtlinien zum Erstellen](guidelines-for-creating-side-by-side-assemblies.md)paralleler Assemblys.

Private Assemblys müssen von einem [Assemblymanifest](assembly-manifests.md)begleitet werden. Beachten Sie, dass namens Einschränkungen gelten, wenn eine DLL als private Assembly verpackt wird, um die Art und Weise zu berücksichtigen, wie Windows nach privaten Assemblys sucht. Bei der Suche nach privaten Assemblys besteht die empfohlene Methode darin, das Assemblymanifest in die dll als Ressource einzubeziehen. In diesem Fall muss die Ressourcen-ID gleich 1 und der Name des private Assembly mit dem Namen der dll identisch sein. Wenn beispielsweise der Name der dll MICROSOFT.WINDOWS.MYSAMPLE.DLL ist, kann der Wert des Namens Attributs, der im **assemblyIdentity** -Element des Manifests verwendet wird, auch Microsoft. Windows. MySample lauten. Eine alternative Methode für die Suche nach privaten Assemblys besteht darin, das Assemblymanifest in einer separaten Datei bereitzustellen. In diesem Fall müssen sich der Name der Assembly und des zugehörigen Manifests von dem Namen der DLL unterscheiden. Beispiel: "Microsoft. Windows. mysampleasm", "Microsoft. Windows. mysampleasm. Manifest" und "Microsoft.Windows.mysample.dll". Weitere Informationen zur parallelen Suche von privaten Assemblys finden Sie unter [Assemblysuchsequenz](assembly-searching-sequence.md).

Private Assemblys werden in einem Ordner der Verzeichnisstruktur der Anwendung installiert. In der Regel ist dies der Ordner, der die ausführbare Datei der Anwendung enthält. Private Assemblys können im selben Ordner wie die Anwendung, in einem Ordner mit dem gleichen Namen wie die Assembly oder in einem sprachspezifischen Unterordner mit dem gleichen Namen wie die Assembly bereitgestellt werden. Verwenden Sie beispielsweise eine der folgenden Verzeichnisstrukturen, um eine private Assembly, Microsoft. Tools. Pop, ohne Angabe der angegebenen Sprache bereitzustellen.



| Verzeichnisstruktur                                       | BESCHREIBUNG                                                                                            |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| Appdir- \\MICROSOFT.TOOLS.POP.DLL                           | Das Manifest wird als Ressource in der DLL bereitgestellt.                                                     |
| Appdir \\ Microsoft. Tools. Pop. Manifest                      | Das Manifest wird als separate Datei bereitgestellt.                                                           |
| appdir \\ Microsoft. Hilfsmittel. Pop- \\MICROSOFT.TOOLS.POP.DLL      | Das Manifest wird als Ressource in der DLL bereitgestellt, die sich in einem Unterordner mit dem Namen der Assembly befindet. |
| Appdir \\ Microsoft. Tools. Pop \\ Microsoft. Tools. Pop. Manifest | Das Manifest wird als separate Datei in einem Unterordner mit dem Namen der Assembly bereitgestellt.                 |



 

> [!IMPORTANT]
>
> Für Versionen des Windows-Betriebssystems vor Windows 7 und Windows Server 2008 R2 müssen Native private Assemblys in dem Ordner bereitgestellt werden, der die ausführbare Datei der Anwendung enthält. Die Installation in einem sprachspezifischen Ordner oder im Ordner mit dem gleichen Namen wie die Assembly wird für Native private Assemblys nicht unterstützt.

 

Verwenden Sie eine der folgenden Verzeichnisstrukturen, um eine private Assembly, Microsoft. Tools. Pop, mit einer angegebenen Sprache bereitzustellen. Im folgenden Beispiel ist die von Microsoft. Tools. Pop verwendete Sprache Englisch (USA), und der Sprachcode ist "en-US". Sie sollten den korrekten Code der DHTML-Sprache für Ihre Assembly ersetzen.

``` syntax
appdir\en-us\Microsoft.tools.pop.DLL
appdir\en-us\Microsoft.tools.pop.MANIFEST
appdir\en-us\Microsoft.tools.pop\Microsoft.tools.pop.DLL
appdir\en-us\Microsoft.tools.pop\Microsoft.tools.pop.MANIFEST
```

Private Assemblys können von jeder Installationsmethode installiert werden, mit der die Datei der Assembly in diesen Ordner kopiert werden kann, z. b. der **xcopy** -Befehl. Weitere Informationen zum Installieren von privaten Assemblys mit dem Windows Installer finden Sie unter [Installation von Win32](../msi/installation-of-win32-assemblies.md)-Assemblys.

Private Assemblys können auch auf älteren Betriebssystemen als Windows XP installiert werden. In diesem Fall muss die Assembly registriert werden, und unter diesen Betriebssystemen wird das Manifest nicht verwendet. Eine Kopie des private Assembly wird in einem privaten Ordner installiert, um die Anwendung exklusiv zu verwenden. Eine andere Version der Assembly kann global auf dem System registriert werden und ist für jede Anwendung verfügbar, die Sie bindet. Die globale Version der Assembly kann die Version sein, die mit der Anwendung installiert wird, oder eine frühere Version. Weitere Informationen finden Sie unter [DLL/COM-Umleitung unter Windows](dll-com-redirection-on-windows.md). Eine Assembly kann auch als freigegebene Assembly für die Verwendung durch mehrere Anwendungen installiert werden. Weitere Informationen finden Sie unter frei [gegebene](/windows/desktop/Msi/shared-assemblies)Assemblys.

Beachten Sie, dass die Schritte zum Erstellen einer private Assembly identisch mit denen zum Erstellen einer freigegebenen Assembly mit zwei Ausnahmen sind:

-   Es muss kein private Assembly signiert werden, und **PublicKeyToken** ist im **assemblyIdentity-Element des Assemblymanifests** nicht erforderlich.
-   Private Assemblys können mithilfe einer beliebigen Installations Technologie im Ordner der Anwendung installiert werden. Es ist nicht erforderlich, dass private Assemblys mit dem Windows Installer installiert werden.

 

 
