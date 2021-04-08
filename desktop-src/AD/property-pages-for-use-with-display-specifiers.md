---
title: Eigenschaften Seiten für die Verwendung mit Anzeige spezifiken
description: Active Directory Domain Services bieten einen Mechanismus zum Hinzufügen von Seiten zu dem Eigenschaften Blatt, das für ein Verzeichnis Objekt aus den Active Directory Verwaltungs-Snap-Ins oder der Windows-Shell angezeigt wird.
ms.assetid: c1dd84e2-50f9-4903-a4b5-4473515e4d0e
ms.tgt_platform: multiple
keywords:
- Anzeige spezifiker anzeigen, Eigenschaften Seiten für die Verwendung mit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c204f4d378e66cda5bc02684cb51cc707ba3d6f2
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103858131"
---
# <a name="property-pages-for-use-with-display-specifiers"></a>Eigenschaften Seiten für die Verwendung mit Anzeige spezifiken

Active Directory Domain Services bieten einen Mechanismus zum Hinzufügen von Seiten zu dem Eigenschaften Blatt, das für ein Verzeichnis Objekt aus den Active Directory Verwaltungs-Snap-Ins oder der Windows-Shell angezeigt wird. Um dem Eigenschaften Blatt eine Seite hinzuzufügen, implementieren Sie eine Eigenschaften Blatt Erweiterung.

## <a name="developer-audience"></a>Entwicklerzielgruppe

In dieser Dokumentation wird davon ausgegangen, dass der Reader mit der com-Operation und-Komponentenentwicklung mit C++ vertraut ist. Es ist derzeit nicht möglich, eine Active Directory Eigenschaften Blatt Erweiterung mit Visual Basic zu erstellen.

## <a name="creating-an-active-directory-property-sheet-extension"></a>Erstellen einer Active Directory-Eigenschaften Blatt Erweiterung

Eine *Eigenschaften Blatt Erweiterung* ist ein com-in-proc-Server, der bestimmte Schnittstellen implementiert und bei Active Directory Domain Services registriert ist. Führen Sie die folgenden Schritte aus, um eine Eigenschaften Blatt Erweiterung zu erstellen.

**So erstellen Sie eine Active Directory-Eigenschaften Blatt Erweiterung**

1.  Erstellen Sie die Eigenschaften Blatt-Erweiterungs-DLL. Eine Eigenschaften Blatt Erweiterung ist ein com-in-proc-Server, der mindestens die [**ishellextinit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) -und [**ishellpropsheetext**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) -Schnittstellen implementiert. Weitere Informationen finden Sie unter [Implementieren des COM-Objekts der Eigenschaften Seite](implementing-the-property-page-com-object.md).
2.  Installieren Sie die Eigenschaften Blatt Erweiterung auf den Computern, auf denen die Eigenschaften Blatt Erweiterung verwendet werden soll. Zu diesem Zweck erstellen Sie ein Microsoft Windows Installer Paket für die DLL-Datei der Eigenschafts Blatt Erweiterung und stellen das Paket entsprechend mithilfe der Gruppenrichtlinie bereit. Weitere Informationen finden Sie unter [Verteilen von Benutzeroberflächen Komponenten](distributing-user-interface-components.md).
3.  Registrieren Sie die Erweiterung des Eigenschaften Blatts in der Windows-Registrierung und mit Active Directory Domain Services. Weitere Informationen finden Sie unter [Registrieren des COM-Objekts der Eigenschaften Seite in einem Anzeigespezifizierer](registering-the-property-page-com-object-in-a-display-specifier.md).

 

 