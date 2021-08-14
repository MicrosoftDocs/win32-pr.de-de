---
title: Eigenschaftenseiten für die Verwendung mit Anzeigespezifizierern
description: Active Directory Domain Services bieten einen Mechanismus zum Hinzufügen von Seiten zum Eigenschaftenblatt, das für ein Verzeichnisobjekt aus den Active Directory-Administrator-Snap-Ins oder der Windows Shell angezeigt wird.
ms.assetid: c1dd84e2-50f9-4903-a4b5-4473515e4d0e
ms.tgt_platform: multiple
keywords:
- Anzeigespezifizierer AD, Eigenschaftenseiten für die Verwendung mit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f813223aa88dce3b8bba867139bab476416cba1932c583e2e9be591de03fc63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185184"
---
# <a name="property-pages-for-use-with-display-specifiers"></a>Eigenschaftenseiten für die Verwendung mit Anzeigespezifizierern

Active Directory Domain Services bieten einen Mechanismus zum Hinzufügen von Seiten zum Eigenschaftenblatt, das für ein Verzeichnisobjekt aus den Active Directory-Administrator-Snap-Ins oder der Windows Shell angezeigt wird. Um dem Eigenschaftenblatt eine Seite hinzuzufügen, implementieren Sie eine Eigenschaftenblatterweiterung.

## <a name="developer-audience"></a>Entwicklerzielgruppe

In dieser Dokumentation wird davon ausgegangen, dass der Reader mit com-Vorgang und Komponentenentwicklung mit C++ vertraut ist. Es ist derzeit nicht möglich, eine Active Directory-Eigenschaftenblatterweiterung mit Visual Basic zu erstellen.

## <a name="creating-an-active-directory-property-sheet-extension"></a>Erstellen einer Active Directory-Eigenschaftenblatterweiterung

Eine *Eigenschaftenblatterweiterung* ist ein COM-Prozessserver, der bestimmte Schnittstellen implementiert und bei Active Directory Domain Services registriert ist. Führen Sie die folgenden Schritte aus, um eine Eigenschaftenblatterweiterung zu erstellen.

**So erstellen Sie eine Active Directory-Eigenschaftenblatterweiterung**

1.  Erstellen Sie die Dll für die Eigenschaftenblatterweiterung. Eine Eigenschaftenblatterweiterung ist ein COM-Prozessserver, der mindestens die Schnittstellen [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) und [**IShellPropSheetExt**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) implementiert. Weitere Informationen finden Sie unter [Implementieren des COM-Objekts der Eigenschaftenseite.](implementing-the-property-page-com-object.md)
2.  Installieren Sie die Eigenschaftenblatterweiterung auf den Computern, auf denen die Eigenschaftenblatterweiterung verwendet werden soll. Erstellen Sie hierzu ein Microsoft Windows Installer-Paket für die DLL der Eigenschaftenblatterweiterung, und stellen Sie das Paket mithilfe der Gruppenrichtlinie entsprechend bereit. Weitere Informationen finden Sie unter [Verteilen Benutzeroberfläche Komponenten.](distributing-user-interface-components.md)
3.  Registrieren Sie die Eigenschaftenblatterweiterung in der Windows-Registrierung und bei Active Directory Domain Services. Weitere Informationen finden Sie unter [Registrieren des COM-Objekts der Eigenschaftenseite in einem Anzeigespezifizierer.](registering-the-property-page-com-object-in-a-display-specifier.md)

 

 