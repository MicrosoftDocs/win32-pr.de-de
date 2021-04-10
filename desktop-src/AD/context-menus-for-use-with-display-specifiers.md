---
title: Kontextmenüs für die Verwendung mit Anzeige spezifiken
description: Die Active Directory-Verwaltungs-MMC-Snap-Ins und Windows 2000 Shell bieten einen Mechanismus zum Hinzufügen eines Elements zum Kontextmenü, das für Objekte in Active Directory Domain Services angezeigt wird.
ms.assetid: 0b0691f5-321d-4f22-b39c-bc528db9e707
ms.tgt_platform: multiple
keywords:
- Anzeige spezifiker anzeigen, Kontextmenüs für
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f28fbf703f17ea5c0fa7938365d485998be77e8d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103948585"
---
# <a name="context-menus-for-use-with-display-specifiers"></a>Kontextmenüs für die Verwendung mit Anzeige spezifiken

Die Active Directory-Verwaltungs-MMC-Snap-Ins und Windows 2000 Shell bieten einen Mechanismus zum Hinzufügen eines Elements zum Kontextmenü, das für Objekte in Active Directory Domain Services angezeigt wird. Ein Kontextmenü Element kann hinzugefügt werden, indem ein com-in-proc-Server implementiert wird, der als *Kontextmenüerweiterung* bezeichnet wird. Es kann auch ein Kontextmenü Element hinzugefügt werden, das jede mit der [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) -API gestartete Datei aufruft, z. b. eine Anwendungs-oder Webseiten-URL. Dies wird als *statisches Kontextmenü Element* bezeichnet.

## <a name="developer-audience"></a>Entwicklerzielgruppe

In dieser Dokumentation wird davon ausgegangen, dass der Reader mit der com-Operation und-Komponentenentwicklung mit C++ vertraut ist. Es ist derzeit nicht möglich, eine Active Directory Domain Services Kontextmenüerweiterung mithilfe von Microsoft Visual Basic zu erstellen.

## <a name="extending-the-context-menu-with-a-context-menu-extension"></a>Erweitern des Kontextmenüs mit einer Kontextmenüerweiterung

Eine Kontextmenüerweiterung ist ein com-in-proc-Server, der bestimmte Schnittstellen implementiert und bei Active Directory Domain Services registriert ist.

**So erstellen und installieren Sie eine Kontextmenüerweiterung**

1.  Erstellen Sie die Kontextmenü-Erweiterungs-DLL. Eine Kontextmenüerweiterung ist ein com-in-proc-Server, der mindestens die Schnittstellen [**ishellextinit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) und [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) implementiert. Weitere Informationen finden Sie unter [Implementieren des Kontextmenü-com-Objekts](implementing-the-context-menu-com-object.md).
2.  Installieren Sie die Erweiterung des Kontextmenü Blatts auf Computern, auf denen die Kontextmenüerweiterung verwendet wird. Dies wird erreicht, indem ein Microsoft Windows Installer Paket für die Erweiterung der Kontextmenüerweiterung erstellt und das Paket entsprechend mithilfe der Gruppenrichtlinie bereitgestellt wird. Weitere Informationen finden Sie unter [Verteilen von Benutzeroberflächen Komponenten](distributing-user-interface-components.md).
3.  Registrieren Sie die Kontextmenüerweiterung in der Windows-Registrierung und mit Active Directory Domain Services. Weitere Informationen finden Sie unter [Registrieren des Kontextmenü-com-Objekts in einem Anzeige Spezifizierer](registering-the-context-menu-com-object-in-a-display-specifier.md).

## <a name="extending-the-context-menu-with-a-static-context-menu-item"></a>Erweitern des Kontextmenüs mit einem statischen Kontextmenü Element

Ein statisches Kontextmenü Element kann verwendet werden, um alle mit der [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) -API gestarteten Dateien aufzurufen, z. b. eine Anwendungs-oder Webseiten-URL. Um dies zu erreichen, muss das statische Kontextmenü Element für eine bestimmte Objektklasse registriert werden, damit das statische Kontextmenü Element dem Kontextmenü von Objekten dieser Klasse hinzugefügt wird. Weitere Informationen finden Sie unter [Registrieren eines statischen Kontextmenü Elements](registering-a-static-context-menu-item.md).

 

 