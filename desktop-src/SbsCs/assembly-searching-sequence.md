---
description: Wenn eine isolierte Anwendung eine Assemblyabhängigkeit angibt, sucht die Seite-an-Seite-Assembly zunächst zwischen den freigegebenen Assemblys im Ordner WinSxS.
ms.assetid: 93496631-55cc-4dd9-9a51-b748c35fd477
title: Assemblysuchsequenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc689ecb14c55f0e8a609c7e7497fce969e88b8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042492"
---
# <a name="assembly-searching-sequence"></a>Assemblysuchsequenz

Wenn eine isolierte Anwendung eine Assemblyabhängigkeit angibt, sucht die Seite-an-Seite-Assembly zunächst zwischen den frei [gegebenen](/windows/desktop/Msi/shared-assemblies) Assemblys im Ordner WinSxS. Wenn die erforderliche Assembly nicht gefunden wird, sucht Seite-an-Seite nach einer private Assembly, die in einem Ordner der Verzeichnisstruktur der Anwendung installiert ist.

[Private](/windows/desktop/Msi/private-assemblies) Assemblys können an den folgenden Speicherorten in der Verzeichnisstruktur der Anwendung bereitgestellt werden:

-   Im Ordner der Anwendung. In der Regel ist dies der Ordner, der die ausführbare Datei der Anwendung enthält.
-   In einem Unterordner im Ordner der Anwendung. Der Unterordner muss den gleichen Namen wie die Assembly haben.
-   In einem sprachspezifischen Unterordner im Ordner der Anwendung. Der Name des unter Ordners ist eine Zeichenfolge von DHTML-Sprachcodes, die eine Sprache-Kultur oder Sprache angeben.
-   In einem Unterordner eines sprachspezifischen unter Ordners im Ordner der Anwendung. Der Name des unter Ordners "höher" ist eine Zeichenfolge von DHTML-Sprachcodes, die eine Sprache-Kultur oder Sprache angeben. Der tiefere Unterordner hat denselben Namen wie die Assembly.

Wenn Sie das erste Mal nebeneinander nach einer private Assembly suchen, wird ermittelt, ob ein sprachspezifischer Unterordner in der Verzeichnisstruktur der Anwendung vorhanden ist. Wenn kein sprachspezifischer Unterordner vorhanden ist, sucht die Seite-an-Seite-private Assembly an den folgenden Speicherorten mithilfe der folgenden Sequenz.

1.  Seite-an-Seite-durchsucht den Ordner WinSxS.
2.  \\\\< > \\ appdir < *AssemblyName* # C0.DLL
3.  \\\\< > \\ appdir < *AssemblyName*>. Manifest
4.  \\\\< > \\ appdir < *AssemblyName* > \\ < *AssemblyName* # C0.DLL
5.  \\\\< > \\ appdir < *AssemblyName* > \\ < *AssemblyName*>. Manifest

Wenn ein sprachspezifischer Unterordner vorhanden ist, kann die Verzeichnisstruktur der Anwendung die private Assembly enthalten, die in mehreren Sprachen lokalisiert sind. Seite-an-Seite-durchsucht die sprachspezifischen Unterordner, um sicherzustellen, dass die Anwendung die angegebene Sprache oder die am besten verfügbare Sprache verwendet. Sprachspezifische Unterordner werden mithilfe einer Zeichenfolge von DHTML-Sprachcodes benannt, die eine Sprache-Kultur oder Sprache angeben. Wenn ein sprachspezifischer Unterordner vorhanden ist, sucht die Seite-an-Seite-private Assembly an den folgenden Speicherorten mithilfe der folgenden Sequenz.

1.  Seite-an-Seite-durchsucht den Ordner WinSxS.
2.  \\\\< > \\ appdir < *Sprache-Kultur* > \\ < *AssemblyName* # C0.DLL
3.  \\\\< > \\ appdir < *Sprache-Kultur* > \\ < *AssemblyName*>. Manifest
4.  \\\\< > \\ appdir < *Sprache-Kultur* > \\ < *AssemblyName* > \\ < *AssemblyName* # C0.DLL
5.  \\\\< > \\ appdir < *Sprache-Kultur* > \\ < *AssemblyName* > \\ < *AssemblyName*>. Manifest

Beachten Sie, dass die Seite-an-Seite-Such Sequenz eine DLL-Datei mit dem Namen der Assembly findet und beendet wird, bevor Sie nach einer Manifest-Datei mit dem Namen der Assembly sucht. Die empfohlene Vorgehensweise zum Behandeln einer private Assembly, die eine dll ist, besteht darin, das Assemblymanifest in der DLL-Datei als Ressource zu platzieren. Die Ressourcen-ID muss gleich 1 sein, und der Name des private Assembly kann mit dem Namen der dll identisch sein. Wenn beispielsweise der Name der dll MICROSOFT.WINDOWS.MYSAMPLE.DLL ist, kann der Wert des Namens Attributs, der im **assemblyIdentity-Element des Assemblymanifests** verwendet wird, auch Microsoft. Windows. MySample lauten. Als Alternative können Sie das Assemblymanifest in einer separaten Datei ablegen, aber der Name der Assembly und das zugehörige Manifest müssen sich von dem Namen der DLL unterscheiden. Beispiel: "Microsoft. Windows. mysampleasm", "Microsoft. Windows. mysampleasm. Manifest" und "MICROSOFT.WINDOWS.MYSAMPLE.DLL".

Wenn z. b. MyApp im Stammverzeichnis von Laufwerk c: installiert ist und in Französisch-Belgien MyAsm erfordert, verwendet parallel die folgende Sequenz, um nach der optimalen Näherung für eine lokalisierte Instanz von MyAsm zu suchen.

1.  Parallele Durchsuchen von WinSxS für die FR-be-Version.
2.  c: \\ myapp \\ - \\myasm.dll
3.  c: \\ myapp \\ -fr-be \\ MyAsm. Manifest
4.  c: \\ myapp \\ -fr-be \\ MyAsm- \\myasm.dll
5.  c: \\ myapp \\ -fr-be MyAsm \\ \\ . Manifest
6.  Parallele Durchsuchen von WinSxS für die FR-Version.
7.  c: \\ myapp \\ - \\myasm.dll Fr
8.  c: \\ myapp-Datei \\ \\ MyAsm. Manifest
9.  c: \\ myapp \\ - \\ MyAsm- \\myasm.dll
10. c: \\ myapp \\ - \\ MyAsm \\ MyAsm. Manifest
11. Parallele Durchsuchen von WinSxS für die en-US-Version.
12. c: \\ myapp \\ en-US \\myasm.dll
13. c: \\ myapp \\ en-US \\ MyAsm. Manifest
14. c: \\ myapp \\ en-US \\ MyAsm \\myasm.dll
15. c: \\ myapp \\ en-US \\ MyAsm \\ MyAsm. Manifest
16. Parallele Durchsuchen von WinSxS für die Version "en".
17. c: \\ myapp \\ - \\myasm.dll
18. c: \\ myapp \\ en \\ MyAsm. Manifest
19. c: \\ myapp \\ en \\ MyAsm- \\myasm.dll
20. c: \\ myapp \\ en \\ MyAsm \\ MyAsm. Manifest
21. Parallele durchsuchen WinSxS für die Version No language.
22. c: \\ myapp- \\myasm.dll
23. c: \\ myapp \\ MyAsm. Manifest
24. c: \\ myapp \\ MyAsm- \\myasm.dll
25. c: \\ myapp \\ MyAsm \\ MyAsm. Manifest

Wenn die Seite-an-Seite-Suche eine sprachneutrale Version der Assembly erreicht und eine [MUI-Version (Multilanguage User Interface)](/windows/desktop/Intl/multilingual-user-interface) von Windows auf dem System vorhanden ist, versucht nebeneinander, eine Bindung an <*AssemblyName*>. MUI herzustellen. Seite-an-Seite versucht nicht, eine Bindung an <*AssemblyName*>. MUI herzustellen, wenn die Suche eine lokalisierte Version der Assembly erreicht. Das [Assemblymanifest](assembly-manifests.md) einer sprach neutralen Assembly weist kein Language-Attribut im **assemblyIdentity** -Element auf. Wenn Seite-an-Seite eine sprachneutrale Assembly erreicht und MUI installiert ist, sucht parallel die folgenden Speicherorte mithilfe der folgenden Sequenz für <*AssemblyName*>. MUI. Parallel verwendet dieselbe Such Sequenz, wenn die Assembly Kultur neutral ist, mit dem Unterschied, <*keine sprach*> durchsucht wird.

1.  Seite-an-Seite durchsucht den Ordner WinSxS nach <*AssemblyName*>. MUI.
2.  \\\\<*Sprache des Benutzers (Kultur)* > \\ < *AssemblyName*>. MUI
3.  \\\\< > Sprache \\ des < Benutzers *AssemblyName*>. MUI
4.  \\\\<*Sprache des Systems (Kultur)* > \\ < *AssemblyName*>. MUI
5.  \\\\< > Sprache \\ des < Systems *AssemblyName*>. MUI
6.  \\\\<*keine* > \\ Sprache < *AssemblyName*>. MUI

Wenn z. b. die Seite-an-Seite-Suche den private Assembly unter c: \\ myapp \\ MyAsm \\ MyAsm. Manifest findet und MyAsm eine sprachneutrale Assembly ist. Parallel verwendet die folgende Sequenz, um nach MyAsm. mui zu suchen. Beachten Sie, dass die Seite-an-Seite nicht nach einer sprach neutralen MUI-Assembly sucht.

1.  Parallele durchsuchen WinSxS für die FR-be-Version der MUI-Assembly.
2.  c: \\ myapp \\ - \\myasm.mui.dll
3.  c: \\ myapp \\ -fr-be \\ MyAsm. MUI. Manifest
4.  c: \\ myapp \\ -fr-be \\ MyAsm- \\myasm.mui.dll
5.  c: \\ myapp \\ -fr-be MyAsm \\ \\ . MUI. Manifest
6.  Parallele durchsuchen WinSxS für die FR-Version der MUI-Assembly.
7.  c: \\ myapp \\ - \\myasm.mui.dll Fr
8.  c: \\ myapp, \\ fr \\ MyAsm. MUI. Manifest
9.  c: \\ myapp \\ - \\ MyAsm- \\myasm.mui.dll
10. c: \\ myapp-Datei \\ \\ MyAsm \\ MyAsm. MUI. Manifest
11. Parallele durchsuchen WinSxS für die en-US-Version der MUI-Assembly.
12. c: \\ myapp \\ en-US \\myasm.mui.dll
13. c: \\ myapp \\ en-US \\ MyAsm. MUI. Manifest
14. c: \\ myapp \\ en-US \\ MyAsm \\myasm.mui.dll
15. c: \\ myapp \\ en-US meinasm \\ \\ MyAsm. MUI. Manifest
16. Parallele durchsuchen WinSxS für die Version en der MUI-Assembly.
17. c: \\ myapp \\ - \\myasm.mui.dll
18. c: \\ myapp \\ en \\ MyAsm. MUI. Manifest
19. c: \\ myapp \\ en \\ MyAsm- \\myasm.mui.dll
20. c: \\ myapp \\ en \\ MyAsm \\ MyAsm. MUI. Manifest

 

 
