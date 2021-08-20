---
title: Kontextmenüs für die Verwendung mit Anzeigespezifizierern
description: Die Active Directory-MMC-Snap-Ins und die Windows 2000-Shell bieten einen Mechanismus zum Hinzufügen eines Elements zum Kontextmenü, das für Objekte in Active Directory Domain Services angezeigt wird.
ms.assetid: 0b0691f5-321d-4f22-b39c-bc528db9e707
ms.tgt_platform: multiple
keywords:
- Anzeigespezifizierer AD, Kontextmenüs für
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b55b530797f1ac43456606d0fecf30e7641bf10399fb3c074135a3e0c49fd0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118021707"
---
# <a name="context-menus-for-use-with-display-specifiers"></a>Kontextmenüs für die Verwendung mit Anzeigespezifizierern

Die Active Directory-MMC-Snap-Ins und die Windows 2000-Shell bieten einen Mechanismus zum Hinzufügen eines Elements zum Kontextmenü, das für Objekte in Active Directory Domain Services angezeigt wird. Ein Kontextmenüelement kann hinzugefügt werden, indem ein COM-Prozessserver implementiert wird, der als *Kontextmenüerweiterung* bezeichnet wird. Es kann auch ein Kontextmenüelement hinzugefügt werden, das jede Datei aufruft, die mit der [**ShellExecute-API**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) gestartet wurde, z. B. eine Anwendung oder Webseiten-URL. Dies wird als *statisches Kontextmenüelement* bezeichnet.

## <a name="developer-audience"></a>Entwicklerzielgruppe

In dieser Dokumentation wird davon ausgegangen, dass der Reader mit com-Vorgang und Komponentenentwicklung mit C++ vertraut ist. Es ist derzeit nicht möglich, mit microsoft Visual Basic eine Active Directory Domain Services Kontextmenüerweiterung zu erstellen.

## <a name="extending-the-context-menu-with-a-context-menu-extension"></a>Erweitern des Kontextmenüs mit einer Kontextmenüerweiterung

Eine Kontextmenüerweiterung ist ein COM-Prozessserver, der bestimmte Schnittstellen implementiert und bei Active Directory Domain Services registriert ist.

**So erstellen und installieren Sie eine Kontextmenüerweiterung**

1.  Erstellen Sie die Kontextmenüerweiterungs-DLL. Eine Kontextmenüerweiterung ist ein COM-Prozessserver, der mindestens die [**Schnittstellen IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) und [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) implementiert. Weitere Informationen finden Sie unter [Implementieren des KONTEXTMENÜ-COM-Objekts.](implementing-the-context-menu-com-object.md)
2.  Installieren Sie die Kontextmenüblatterweiterung auf Computern, auf denen die Kontextmenüerweiterung verwendet wird. Dies wird erreicht, indem ein Microsoft Windows Installer-Paket für die Kontextmenüerweiterungs-DLL erstellt und das Paket mithilfe der Gruppenrichtlinie entsprechend bereitgestellt wird. Weitere Informationen finden Sie unter [Verteilen von Benutzeroberfläche-Komponenten.](distributing-user-interface-components.md)
3.  Registrieren Sie die Kontextmenüerweiterung in der Windows-Registrierung und bei Active Directory Domain Services. Weitere Informationen finden Sie unter [Registrieren des COM-Kontextmenüobjekts in einem Anzeigespezifizierer.](registering-the-context-menu-com-object-in-a-display-specifier.md)

## <a name="extending-the-context-menu-with-a-static-context-menu-item"></a>Erweitern des Kontextmenüs mit einem statischen Kontextmenüelement

Ein statisches Kontextmenüelement kann verwendet werden, um jede Datei aufzurufen, die mit der [**ShellExecute-API**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) gestartet wurde, z. B. eine Anwendung oder Webseiten-URL. Um dies zu erreichen, muss das statische Kontextmenüelement für eine bestimmte Objektklasse registriert werden, damit das statische Kontextmenüelement dem Kontextmenü der Objekte dieser Klasse hinzugefügt wird. Weitere Informationen finden Sie unter [Registrieren eines statischen Kontextmenüelements.](registering-a-static-context-menu-item.md)

 

 