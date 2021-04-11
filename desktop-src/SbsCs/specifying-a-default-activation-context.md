---
description: Angeben eines Standard Aktivierungs Kontexts
ms.assetid: 4d9a8552-7098-458d-a592-45524871cce5
title: Angeben eines Standard Aktivierungs Kontexts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32cf0225a8e4290a09f7e6524a4b3ef47f9c4c4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960550"
---
# <a name="specifying-a-default-activation-context"></a>Angeben eines Standard Aktivierungs Kontexts

Wenn Ihre Anwendung oder Komponente einen neuen Prozess erstellt, sucht Windows nach einem Standard Anwendungs Manifest. Beachten Sie, dass ein Manifest, das als Ressource in der Anwendung enthalten ist, Vorrang vor einem externen Manifest hat. Der Standard Aktivierungs Kontext ist der erste Aktivierungs Kontext, der aktiv ist, bevor ein anderer Aktivierungs Kontext aktiviert wird. Dieser Aktivierungs Kontext ist immer aktiv, es sei denn, Sie aktivieren andere Kontexte. Wenn Sie \_ \_ beim Kompilieren der Anwendung oder Komponente die Isolations Funktion aktiviert definieren, können Aufrufe wie [**cokreatinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)und [**kreatewindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) die automatische Kontext Verwaltung durchführen.

Das Lade Modul ermöglicht es einer Anwendung, Ihren Standard Aktivierungs Kontext mit zwei Methoden anzugeben. Sie können die Manifestressource in den Ressourcen der ausführbaren Datei ablegen, die das Lade Programm findet. Dies entspricht dem Platzieren der Manifest-Datei in der Ressourcen Tabelle der ausführbaren Datei. Sie können das Manifest in einer Datei mit dem Namen *myapp*. exe platzieren. Das Manifest befindet sich im gleichen Verzeichnis wie *myapp*. exe, und das Lade Modul findet es bei der Suche nach *myapp*. exe.

Wenn Sie keine dieser Methoden verwenden, beginnt die Anwendung mit dem standardmäßigen Aktivierungs Kontext des Systems, der einen minimalen Satz von Assemblys enthält.

Eine bessere Methode der automatischen Kontext Verwaltung ist die Kompilierung der Anwendung mit \_ \_ aktiviertem Isolations fähigen aktivierten. Die empfohlene Methode besteht darin, diese in der Befehlszeile des Compilers für das gesamte Projekt festzulegen, das erstellt wird, anstatt in einzelnen Quelldateien oder Headern festgelegt zu werden. Dadurch erkennen die meisten Win32-APIs Aktivierungs Kontexte und deren Verwaltung. Anstatt eine eigene Aktivierungs Kontext Verwaltung durchführen zu müssen, müssen Sie einfach ein Manifest in der Ressourcen Tabelle unter Ressourcen-ID isolationaware \_ Manifest \_ Resource \_ ID (numerischer Wert 2) vom Typ RT- \_ Manifest (numerischer Wert 24) platzieren. Funktionen wie z. b. " [**kreatewindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)", " [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)" und " [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) " aktivieren diesen Kontext vor dem eigentlichen aufrufen automatisch.

Beachten Sie, dass Sie bei der Kompilierung mit aktivierter Isolations Funktion " \_ \_ definiert" nicht auch Ihre eigene Aktivierungs Kontext Verwaltung ausführen können. Wenn die Isolations Funktion \_ \_ aktiviert ist, ignoriert Windows jede dynamische Aktivierungs Kontext Erstellung, die Ihre Anwendung möglicherweise versucht, zwischen [**activateactctx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) -und up- [**Window**](/windows/win32/api/winuser/nf-winuser-createwindowa) -aufrufen zu arbeiten. Dies bedeutet, dass \_ \_ das Manifest eine vollständige Liste aller Assemblys enthält, die für die Komponente erforderlich sind, wenn Ihre Anwendung Isolations fähig verwendet.

 

 
