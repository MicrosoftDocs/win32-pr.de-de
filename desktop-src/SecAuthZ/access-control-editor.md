---
description: Ein Satz von Eigenschaftenblättern und Eigenschaftenseiten, mit denen der Benutzer die Komponenten eines Objektsicherheitsdeskriptors anzeigen und ändern kann.
ms.assetid: ca709f27-8463-4f11-92ac-2148796e640a
title: Access Control-Editor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3ed7c210c747278d35537fc010c66b60f0057d9a61b407eb04e993f8928f2d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118914678"
---
# <a name="access-control-editor"></a>Access Control-Editor

Der Zugriffssteuerungs-Editor ist ein Satz von Eigenschaftenblättern und Eigenschaftenseiten, mit denen der Benutzer die Komponenten der Sicherheitsbeschreibung eines Objekts anzeigen [*und ändern kann.*](/windows/desktop/SecGloss/s-gly) Der Editor besteht aus zwei Hauptteilen:

-   Eine [grundlegende Sicherheitseigenschaftsseite,](basic-security-property-page.md) die eine einfache Schnittstelle zum Bearbeiten der Zugriffssteuerungseinträge (ACCESS [*Control Entries,*](/windows/desktop/SecGloss/a-gly) ACEs) in der DACL [*(Discretionary Access Control List)*](/windows/desktop/SecGloss/d-gly) eines Objekts bietet. Diese Seite kann eine optionale Schaltfläche **Erweitert enthalten,** die das Eigenschaftenblatt für erweiterte Sicherheit anzeigt.
-   Ein [](advanced-security-property-sheet.md) erweitertes Sicherheitseigenschaftsblatt mit Eigenschaftenseiten, mit denen der Benutzer die Systemzugriffssteuerungsliste [](/windows/desktop/SecGloss/s-gly) (SACL) des Objekts bearbeiten, den Besitzer des Objekts ändern oder die DACL des Objekts erweitert bearbeiten kann.

Die [**CreateSecurityPage-Funktion**](/windows/desktop/api/Aclui/nf-aclui-createsecuritypage) erstellt die grundlegende Sicherheitseigenschaftsseite. Sie können dann die [**PropertySheet-Funktion**](/windows/win32/api/prsht/nf-prsht-propertysheeta) oder die [**PSM \_ ADDPAGE-Meldung**](../controls/psm-addpage.md) verwenden, um diese Seite einem Eigenschaftenblatt hinzuzufügen.

Alternativ können Sie die [**EditSecurity-Funktion**](/windows/desktop/api/Aclui/nf-aclui-editsecurity) verwenden, um ein Eigenschaftenblatt anzuzeigen, das die grundlegende Sicherheitseigenschaftsseite enthält.

Sowohl für [**CreateSecurityPage als**](/windows/desktop/api/Aclui/nf-aclui-createsecuritypage) auch [**für EditSecurity**](/windows/desktop/api/Aclui/nf-aclui-editsecurity)muss der Aufrufer einen Zeiger auf eine Implementierung der [**ISecurityInformation-Schnittstelle**](/windows/win32/api/aclui/nn-aclui-isecurityinformation) übergeben. Der Zugriffssteuerungs-Editor ruft die Methoden dieser Schnittstelle auf, um Zugriffssteuerungsinformationen über das zu bearbeitende Objekt abzurufen und die Eingabe des Benutzers an Ihre Anwendung zurück zu übergeben. Die **ISecurityInformation-Methoden** haben die folgenden Zwecke:

-   So initialisieren Sie die Eigenschaftenseiten.

    Ihre Implementierung der [**GetObjectInformation-Methode**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) übergibt eine [**SI OBJECT \_ \_ INFO-Struktur**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) an den Editor. Diese Struktur gibt die Eigenschaftenseiten an, die der Editor anzeigen soll, und andere Informationen, die die bearbeitungsoptionen bestimmen, die dem Benutzer zur Verfügung stehen.

-   Zum Bereitstellen von Sicherheitsinformationen über das objekt, das bearbeitet wird.

    Ihre [**GetSecurity-Implementierung**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getsecurity) übergibt den anfänglichen [*Sicherheitsdeskriptor*](/windows/desktop/SecGloss/s-gly) des Objekts an den Editor. Die [**Methoden GetAccessRights**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getaccessrights) [**und MapGeneric**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-mapgeneric) stellen Informationen zu den Zugriffsrechten des Objekts zur Verfügung. Die [**GetInheritTypes-Methode**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getinherittypes) enthält Informationen dazu, wie die ACEs des Objekts von untergeordneten Objekten geerbt werden können.

-   Um die Eingabe des Benutzers an Ihre Anwendung zurück zu übergeben.

    Wenn der Benutzer auf **Ok** oder **Anwenden** klickt, ruft der Editor Ihre [**SetSecurity-Methode**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-setsecurity) auf, um einen Sicherheitsdeskriptor zurück zu übergeben, der die Änderungen des Benutzers enthält.

 

 
