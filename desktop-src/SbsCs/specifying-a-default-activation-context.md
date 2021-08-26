---
description: Angeben eines Standardaktivierungskontexts
ms.assetid: 4d9a8552-7098-458d-a592-45524871cce5
title: Angeben eines Standardaktivierungskontexts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1598e0a111b358a783b940a5c036d63eef348740ff2467d3ed78720c6a5210
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119977140"
---
# <a name="specifying-a-default-activation-context"></a>Angeben eines Standardaktivierungskontexts

Wenn Ihre Anwendung oder Komponente einen neuen Prozess erstellt, sucht Windows nach einem Standardanwendungsmanifest. Beachten Sie, dass ein Manifest, das als Ressource in der Anwendung enthalten ist, Vorrang vor einem externen Manifest hat. Der Standardaktivierungskontext ist der erste Aktivierungskontext, der aktiv ist, bevor ein anderer Aktivierungskontext aktiviert wurde. Dieser Aktivierungskontext ist immer aktiv, es sei denn, Sie aktivieren andere Kontexte. Wenn Sie \_ ISOLATION AWARE \_ ENABLED beim Kompilieren Ihrer Anwendung oder Komponente definieren, können Aufrufe wie [**CoCreateInstance,**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)und [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) eine automatische Kontextverwaltung durchführen.

Das Ladeprogramm ermöglicht einer Anwendung, ihren Standardaktivierungskontext mit zwei Methoden anzugeben. Sie können die Manifestdatei in den Ressourcen der ausführbaren Datei speichern, und das Ladeprogramm findet sie. Dies entspricht dem Speichern der Manifestdatei in der Ressourcentabelle der ausführbaren Datei. Sie können das Manifest in einer Datei namens *Myapp*.exe platzieren. Manifest im gleichen Verzeichnis wie *Myapp*.exe, und das Ladeprogramm findet es, während es nach *Myapp*.exe sucht.

Wenn Sie keine dieser Methoden verwenden, beginnt die Anwendung mit dem Standardaktivierungskontext des Systems, der einen minimalen Satz von Assemblys enthält.

Eine bessere Möglichkeit zur Verwendung der automatischen Kontextverwaltung besteht darin, Ihre Anwendung mit definierter ISOLATION AWARE ENABLED zu \_ kompilieren. \_ Die empfohlene Methode besteht darin, dies in der Befehlszeile des Compilers für das gesamte Projekt festzulegen, das erstellt wird, anstatt in einzelnen Quelldateien oder Headern festgelegt zu werden. Dadurch werden die meisten Win32-APIs über Aktivierungskontexte und deren Verwaltung informiert. Anstatt eine eigene Aktivierungskontextverwaltung durchführen zu müssen, müssen Sie einfach ein Manifest in Ihrer Ressourcentabelle unter Ressourcen-ID ISOLATIONAWARE \_ MANIFEST \_ RESOURCE ID \_ (numerischer Wert 2) des Typs RT \_ MANIFEST (numerischer Wert 24) platzieren. Funktionen wie [**CreateWindow,**](/windows/win32/api/winuser/nf-winuser-createwindowa) [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)und [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) aktivieren diesen Kontext dann automatisch, bevor der tatsächliche Aufruf erfolgt.

Beachten Sie, dass Sie bei der Kompilierung mit definierter ISOLATION \_ AWARE ENABLED nicht auch eine eigene \_ Aktivierungskontextverwaltung durchführen können. Wenn ISOLATION \_ AWARE \_ ENABLED definiert ist, ignoriert Windows alle dynamischen Aktivierungskontexterstellungen, die Ihre Anwendung zwischen [**ActivateActCtx-**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) und [**CreateWindow-Aufrufen**](/windows/win32/api/winuser/nf-winuser-createwindowa) durchführen kann. Wenn Ihre Anwendung ISOLATION AWARE ENABLED verwendet, \_ \_ müssen Sie also sicherstellen, dass das Manifest eine vollständige Liste aller Assemblys enthält, die von der Komponente benötigt werden.

 

 
