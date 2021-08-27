---
description: Wenn eine isolierte Anwendung eine Assemblyabhängigkeit angibt, sucht die Assembly zuerst nebeneinander unter den freigegebenen Assemblys im WinSxS-Ordner.
ms.assetid: 93496631-55cc-4dd9-9a51-b748c35fd477
title: Sequenz der Assemblysuche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 983466954d6cb9619d3fb0595c96f81fed7c9b73a29bfbf2f609b3f14203a957
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127540"
---
# <a name="assembly-searching-sequence"></a>Sequenz der Assemblysuche

Wenn eine isolierte Anwendung eine Assemblyabhängigkeit angibt, sucht die [](/windows/desktop/Msi/shared-assemblies) Assembly zuerst nebeneinander unter den freigegebenen Assemblys im WinSxS-Ordner. Wenn die erforderliche Assembly nicht gefunden wird, sucht sie nebeneinander nach einer privaten Assembly, die in einem Ordner der Verzeichnisstruktur der Anwendung installiert ist.

[Private Assemblys](/windows/desktop/Msi/private-assemblies) können an den folgenden Speicherorten in der Verzeichnisstruktur der Anwendung bereitgestellt werden:

-   Im Ordner der Anwendung. In der Regel ist dies der Ordner, der die ausführbare Datei der Anwendung enthält.
-   In einem Unterordner im Ordner der Anwendung. Der Unterordner muss den gleichen Namen wie die Assembly haben.
-   In einem sprachspezifischen Unterordner im Ordner der Anwendung. Der Name des Unterordners ist eine Zeichenfolge von DHTML-Sprachcodes, die eine Sprachkultur oder Sprache angeben.
-   In einem Unterordner eines sprachspezifischen Unterordners im Ordner der Anwendung. Der Name des höheren Unterordners ist eine Zeichenfolge von DHTML-Sprachcodes, die eine Sprachkultur oder Sprache angeben. Der untere Unterordner hat den gleichen Namen wie die Assembly.

Bei der ersten gleichzeitigen Suche nach einer privaten Assembly wird ermittelt, ob ein sprachspezifischer Unterordner in der Verzeichnisstruktur der Anwendung vorhanden ist. Wenn kein sprachspezifischer Unterordner vorhanden ist, sucht die private Assembly mithilfe der folgenden Sequenz nebeneinander an den folgenden Speicherorten.

1.  Durchsucht den Ordner WinSxS nebeneinander.
2.  \\\\<*appdir* > \\ < *assemblyname*>.DLL
3.  \\\\<*appdir* > \\ < *assemblyname*>.manifest
4.  \\\\<*appdir* > \\ <  > \\ assemblyname < *assemblyname*>.DLL
5.  \\\\<*appdir* > \\ <  > \\ assemblyname < *assemblyname*>.manifest

Wenn ein sprachspezifischer Unterordner vorhanden ist, kann die Verzeichnisstruktur der Anwendung die private Assembly enthalten, die in mehreren Sprachen lokalisiert ist. Durchsucht die sprachspezifischen Unterordner nebeneinander, um sicherzustellen, dass die Anwendung die angegebene Sprache oder die beste verfügbare Sprache verwendet. Sprachspezifische Unterordner werden mithilfe einer Zeichenfolge von DHTML-Sprachcodes benannt, die eine Sprachkultur oder Sprache angeben. Wenn ein sprachspezifischer Unterordner vorhanden ist, sucht die private Assembly mithilfe der folgenden Sequenz nebeneinander an den folgenden Speicherorten.

1.  Durchsucht den Ordner WinSxS nebeneinander.
2.  \\\\<*appdir* > \\ <  > \\ Sprachkultur < *assemblyname*>.DLL
3.  \\\\<*appdir* > \\ <  > \\ Sprachkultur < *assemblyname*>.manifest
4.  \\\\<*appdir* > \\ <  > \\ Sprachkultur <  > \\ assemblyname < *assemblyname*>.DLL
5.  \\\\<*appdir* > \\ <  > \\ Sprachkultur <  > \\ assemblyname < *assemblyname*>.manifest

Beachten Sie, dass die nebenseitige Suchsequenz eine DLL-Datei mit dem Namen der Assembly findet und beendet wird, bevor nach einer Manifestdatei mit dem Namen der Assembly gesucht wird. Die empfohlene Methode zum Behandeln einer privaten Assembly, bei der es sich um eine DLL handelt, besteht im Speichern des Assemblymanifests in der DLL-Datei als Ressource. Die Ressourcen-ID muss gleich 1 sein, und der Name der privaten Assembly kann mit dem Namen der DLL identisch sein. Wenn der Name der DLL beispielsweise MICROSOFT.WINDOWS.MYSAMPLE.DLL ist, kann der Wert des namensattributs, das im **assemblyIdentity-Element** des Assemblymanifests verwendet wird, auch Microsoft sein. Windows.mysample. Alternativ können Sie das Assemblymanifest in einer separaten Datei speichern. Der Name der Assembly und ihres Manifests muss sich jedoch vom Namen der DLL unterscheiden. Beispiel: Microsoft. Windows.mysampleAsm, Microsoft. Windows.mysampleAsm.manifest und MICROSOFT.WINDOWS.MYSAMPLE.DLL.

Wenn z. B. myapp im Stammverzeichnis von Laufwerk c: installiert ist und myasm in Französisch-Hieran erfordert, wird die folgende Sequenz verwendet, um nach der besten Näherung zu einer lokalisierten Instanz von myasm zu suchen.

1.  In WinSxS wird die fr-be-Version nebeneinander durchsucht.
2.  c: \\ myapp \\ fr-be \\myasm.dll
3.  c: \\ myapp \\ fr-be \\ myasm.manifest
4.  c: \\ myapp \\ fr-be \\ myasm \\myasm.dll
5.  c: \\ myapp \\ fr-be \\ myasm \\ myasm.manifest
6.  In WinSxS wird die Fr-Version nebeneinander durchsucht.
7.  c: \\ myapp \\ fr \\myasm.dll
8.  c: \\ myapp \\ fr \\ myasm.manifest
9.  c: \\ myapp \\ fr \\ myasm \\myasm.dll
10. c: \\ myapp \\ fr \\ myasm \\ myasm.manifest
11. In WinSxS wird die en-us-Version nebeneinander durchsucht.
12. c: \\ myapp \\ en-us \\myasm.dll
13. c: \\ myapp \\ en-us \\ myasm.manifest
14. c: \\ myapp \\ en-us \\ myasm \\myasm.dll
15. c: \\ myapp \\ en-us \\ myasm \\ myasm.manifest
16. In WinSxS wird die en-Version nebeneinander durchsucht.
17. c: \\ myapp \\ en \\myasm.dll
18. c: \\ myapp \\ en \\ myasm.manifest
19. c: \\ myapp \\ en \\ myasm \\myasm.dll
20. c: \\ myapp \\ en \\ myasm \\ myasm.manifest
21. In WinSxS wird die Sprachversion no-by-side (Keine Sprache) nebeneinander durchsucht.
22. c: \\ myapp \\myasm.dll
23. c: \\ myapp \\ myasm.manifest
24. c: \\ myapp \\ myasm \\myasm.dll
25. c: \\ myapp \\ myasm \\ myasm.manifest

Wenn die side-by-side-Suche eine sprachneutrale Version der Assembly erreicht und eine MEHRSPRACH-Version [(Multilanguage Benutzeroberfläche)](/windows/desktop/Intl/multilingual-user-interface) von Windows im System vorhanden ist, versucht sie nebeneinander, eine Bindung an <*Assemblyname*>.soll. Es wird nicht versucht, eine Bindung an <*Assemblyname*>.soll, wenn die Suche eine lokalisierte Version der Assembly erreicht. Das [Assemblymanifest](assembly-manifests.md) einer sprachneutralen Assembly enthält im **assemblyIdentity-Element kein Sprachattribut.** Wenn eine sprachneutrale Assembly nebeneinander erreicht wird und DANN installiert ist, durchsucht side-by-side die folgenden Speicherorte mithilfe der folgenden Sequenz nach <*Assemblyname*>.install. Nebeneinander wird die gleiche Suchsequenz verwendet, wenn die Assembly kulturneutral  ist, außer <keine Sprache> nicht durchsucht wird.

1.  Durchsucht den Ordner WinSxS nebeneinander nach <*Assemblyname*>.soll.
2.  \\\\<*Sprachkultur des Benutzers* > \\ < *assemblyname*>.assembly
3.  \\\\<*Sprache des Benutzers* > \\ < *assemblyname*>.assemblyname
4.  \\\\<*Sprachkultur des Systems* > \\ < *assemblyname*>.assemblyname
5.  \\\\< > \\ Systemsprache < *assemblyname*>.assembly
6.  \\\\<*keine Sprache* > \\ < *assemblyname*>.assemblyname

Wenn die suche nach einer seiteseitigen Suche beispielsweise die private Assembly unter c: \\ \\ myapp myasm \\ myasm.manifest findet und myasm eine sprachneutrale Assembly ist. Verwenden Sie dann die folgende Sequenz, um nach myasm.wpa zu suchen. Beachten Sie, dass nebeneinander nicht nach einer sprachneutralen ASSEMBLY vom Benutzer gesucht wird.

1.  Durchsucht WinSxS nebeneinander nach der fr-be-Version der ASSEMBLY MIT.
2.  c: \\ myapp \\ fr-be \\myasm.mui.dll
3.  c: \\ myapp \\ fr-be \\ myasm.manifest.manifest
4.  c: \\ myapp \\ fr-be \\ myasm \\myasm.mui.dll
5.  c: \\ myapp \\ fr-be \\ myasm \\ myasm.manifest
6.  Durchsucht WinSxS nebeneinander nach der fr-Version der ASSEMBLY MIT.
7.  c: \\ myapp \\ fr \\myasm.mui.dll
8.  c: \\ myapp \\ fr \\ myasm.manifest.manifest
9.  c: \\ myapp \\ fr \\ myasm \\myasm.mui.dll
10. c: \\ myapp \\ fr \\ myasm \\ myasm.manifest
11. Durchsucht WinSxS nebeneinander nach der en-us-Version der ASSEMBLY MIT.
12. c: \\ myapp \\ en-us \\myasm.mui.dll
13. c: \\ myapp \\ en-us \\ myasm.manifest.manifest
14. c: \\ myapp \\ en-us \\ myasm \\myasm.mui.dll
15. c: \\ myapp \\ en-us \\ myasm \\ myasm.manifest
16. In WinSxS wird die en-Version der ASSEMBLY side-by-side durchsucht.
17. c: \\ myapp \\ en \\myasm.mui.dll
18. c: \\ myapp \\ en \\ myasm.manifest.manifest
19. c: \\ myapp \\ en \\ myasm \\myasm.mui.dll
20. c: \\ myapp \\ en \\ myasm \\ myasm.manifest

 

 
