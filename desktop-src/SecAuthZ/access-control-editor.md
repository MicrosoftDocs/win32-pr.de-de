---
description: Eine Gruppe von Eigenschaftenblättern und Eigenschaftenseiten, die es dem Benutzer ermöglichen, die Komponenten eines Objektsicherheitsdeskriptors anzuzeigen und zu ändern.
ms.assetid: ca709f27-8463-4f11-92ac-2148796e640a
title: Access Control Editor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3ed7c210c747278d35537fc010c66b60f0057d9a61b407eb04e993f8928f2d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118914678"
---
# <a name="access-control-editor"></a>Access Control Editor

Der Zugriffssteuerungs-Editor ist ein Satz von Eigenschaftenblättern und Eigenschaftenseiten, mit denen der Benutzer die Komponenten der [*Sicherheitsbeschreibung*](/windows/desktop/SecGloss/s-gly)eines Objekts anzeigen und ändern kann. Der Editor besteht aus zwei Hauptteilen:

-   Eine [grundlegende Sicherheitseigenschaftenseite,](basic-security-property-page.md) die eine einfache Schnittstelle zum Bearbeiten der [*Zugriffssteuerungseinträge (ACEs)*](/windows/desktop/SecGloss/a-gly) in der [*dacl (Discretionary Access Control List)*](/windows/desktop/SecGloss/d-gly) eines Objekts bereitstellt. Diese Seite kann eine optionale Schaltfläche **Erweitert** enthalten, die das Eigenschaftenblatt für erweiterte Sicherheit anzeigt.
-   Ein [erweitertes Sicherheitseigenschaftenblatt](advanced-security-property-sheet.md) mit Eigenschaftenseiten, mit denen der Benutzer die [*Systemzugriffssteuerungsliste*](/windows/desktop/SecGloss/s-gly) (SACL) des Objekts bearbeiten, den Besitzer des Objekts ändern oder die DACL des Objekts erweitert bearbeiten kann.

Die [**CreateSecurityPage-Funktion**](/windows/desktop/api/Aclui/nf-aclui-createsecuritypage) erstellt die Eigenschaftenseite "Grundlegende Sicherheit". Sie können dann die [**PropertySheet-Funktion**](/windows/win32/api/prsht/nf-prsht-propertysheeta) oder die [**\_ PSM-ADDPAGE-Nachricht**](../controls/psm-addpage.md) verwenden, um diese Seite einem Eigenschaftenblatt hinzuzufügen.

Alternativ können Sie die [**EditSecurity-Funktion**](/windows/desktop/api/Aclui/nf-aclui-editsecurity) verwenden, um ein Eigenschaftenblatt anzuzeigen, das die Eigenschaftenseite "Grundlegende Sicherheit" enthält.

Sowohl für [**CreateSecurityPage**](/windows/desktop/api/Aclui/nf-aclui-createsecuritypage) als auch [**für EditSecurity**](/windows/desktop/api/Aclui/nf-aclui-editsecurity)muss der Aufrufer einen Zeiger auf eine Implementierung der [**ISecurityInformation-Schnittstelle**](/windows/win32/api/aclui/nn-aclui-isecurityinformation) übergeben. Der Zugriffssteuerungs-Editor ruft die Methoden dieser Schnittstelle auf, um Zugriffssteuerungsinformationen über das bearbeitete Objekt abzurufen und die Eingabe des Benutzers zurück an Ihre Anwendung zu übergeben. Die **ISecurityInformation-Methoden** haben die folgenden Zwecke:

-   So initialisieren Sie die Eigenschaftenseiten.

    Ihre Implementierung der [**GetObjectInformation-Methode**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) übergibt eine [**SI OBJECT \_ \_ INFO-Struktur**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) an den Editor. Diese Struktur gibt die Eigenschaftenseiten an, die der Editor anzeigen soll, sowie andere Informationen, die die für den Benutzer verfügbaren Bearbeitungsoptionen bestimmen.

-   Zum Bereitstellen von Sicherheitsinformationen über das objekt, das bearbeitet wird.

    Ihre [**GetSecurity-Implementierung**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getsecurity) übergibt den anfänglichen [*Sicherheitsdeskriptor*](/windows/desktop/SecGloss/s-gly) des Objekts an den Editor. Die [**Methoden GetAccessRights**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getaccessrights) und [**MapGeneric**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-mapgeneric) stellen Informationen zu den Zugriffsrechten des Objekts bereit. Die [**GetInheritTypes-Methode**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getinherittypes) stellt Informationen darüber bereit, wie die ACEs des Objekts von untergeordneten Objekten geerbt werden können.

-   So übergeben Sie die Eingabe des Benutzers zurück an Ihre Anwendung.

    Wenn der Benutzer auf **Ok** oder **Anwenden** klickt, ruft der Editor Ihre [**SetSecurity-Methode**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-setsecurity) auf, um eine Sicherheitsbeschreibung mit den Änderungen des Benutzers zurückzugeben.

 

 
