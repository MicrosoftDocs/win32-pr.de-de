---
description: Ein Satz von Eigenschaften Blättern und Eigenschaften Seiten, mit denen der Benutzer die Komponenten einer Sicherheits Beschreibung eines Objekts anzeigen und ändern kann.
ms.assetid: ca709f27-8463-4f11-92ac-2148796e640a
title: Access Control-Editor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65117fe086b6a374dbd973f2cb657ec9c19cc3a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349918"
---
# <a name="access-control-editor"></a>Access Control-Editor

Der Zugriffs Steuerungs-Editor ist ein Satz von Eigenschaften Blättern und Eigenschaften Seiten, mit denen der Benutzer die Komponenten der [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly)eines Objekts anzeigen und ändern kann. Der Editor besteht aus zwei Hauptteilen:

-   Eine [grundlegende Sicherheitseigenschaften Seite](basic-security-property-page.md) , die eine einfache Schnittstelle zum Bearbeiten der [*Zugriffs Steuerungs Einträge*](/windows/desktop/SecGloss/a-gly) (ACEs) in der freigegebenen [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL) eines Objekts bereitstellt. Diese Seite kann eine optionale Schaltfläche " **erweitert** " enthalten, die das Eigenschaften Blatt "Erweiterte Sicherheit" anzeigt.
-   Ein erweitertes [Sicherheitseigenschaften Blatt](advanced-security-property-sheet.md) mit Eigenschaften Seiten, mit deren Hilfe der Benutzer die [*System Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/s-gly) (SACL) des Objekts bearbeiten, den Besitzer des Objekts ändern oder eine erweiterte Bearbeitung der DACL des Objekts ausführen kann.

Die [**Funktion "**](/windows/desktop/api/Aclui/nf-aclui-createsecuritypage) Funktion erstellen" erstellt die Eigenschaften Seite "grundlegende Sicherheit". Anschließend können Sie die [**PropertySheet**](/windows/win32/api/prsht/nf-prsht-propertysheeta) -Funktion oder die [**PSM- \_ addPage**](../controls/psm-addpage.md) -Nachricht verwenden, um diese Seite zu einem Eigenschaften Blatt hinzuzufügen.

Alternativ können Sie die [**EditSecurity**](/windows/desktop/api/Aclui/nf-aclui-editsecurity) -Funktion verwenden, um ein Eigenschaften Blatt anzuzeigen, das die Eigenschaften Seite grundlegende Sicherheit enthält.

Sowohl für " [**kreatesecuritypage**](/windows/desktop/api/Aclui/nf-aclui-createsecuritypage) " als auch für " [**EditSecurity**](/windows/desktop/api/Aclui/nf-aclui-editsecurity)" muss der Aufrufer einen Zeiger auf eine Implementierung der [**ISecurityInformation**](/windows/win32/api/aclui/nn-aclui-isecurityinformation) -Schnittstelle übergeben. Der Zugriffs Steuerungs-Editor Ruft die Methoden dieser Schnittstelle auf, um Zugriffs Steuerungsinformationen über das Objekt abzurufen, das bearbeitet wird, und um die Eingabe des Benutzers zurück an Ihre Anwendung zu übergeben. Die **ISecurityInformation** -Methoden haben folgende Zwecke:

-   , Um die Eigenschaften Seiten zu initialisieren.

    Ihre Implementierung der [**GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) -Methode übergibt eine [**Si \_ - \_ Objekt**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) Informationsstruktur an den Editor. Diese Struktur gibt die Eigenschaften Seiten an, die der Editor anzeigen soll, sowie weitere Informationen, die die für den Benutzer verfügbaren Bearbeitungs Optionen bestimmen.

-   Zum Bereitstellen von Sicherheitsinformationen über das Objekt, das bearbeitet wird.

    Ihre [**GetSecurity**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getsecurity) -Implementierung übergibt die anfängliche [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly) des Objekts an den Editor. Die Methoden [**GetAccessRights**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getaccessrights) und [**mapgeneric**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-mapgeneric) stellen Informationen zu den Zugriffsrechten des Objekts bereit. Die [**GetInheritTypes**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getinherittypes) -Methode stellt Informationen dazu bereit, wie die ACEs des Objekts von untergeordneten Objekten geerbt werden können.

-   , Wenn die Eingabe des Benutzers an Ihre Anwendung zurückgegeben werden soll.

    Wenn der Benutzer auf **OK oder über** nehmen **klickt, ruft** der Editor die [**SetSecurity**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-setsecurity) -Methode auf, um eine Sicherheits Beschreibung zurückzugeben, die die Änderungen des Benutzers enthält.

 

 
