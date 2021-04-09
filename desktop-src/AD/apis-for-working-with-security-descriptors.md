---
title: APIs für die Arbeit mit Sicherheits Deskriptoren
description: APIs für die Arbeit mit Sicherheits Deskriptoren
ms.assetid: eb5ee183-949c-41f5-9f74-f9c418fdf0a2
ms.tgt_platform: multiple
keywords:
- Sicherheits Deskriptoren AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfb798e036d5e30ba58a83499b92340bf30ee3cb
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103948593"
---
# <a name="apis-for-working-with-security-descriptors"></a>APIs für die Arbeit mit Sicherheits Deskriptoren

Jedes Objekt in Active Directory Domain Services verfügt über ein **ntSecurityDescriptor** -Attribut, das die Objekt Sicherheits Beschreibung enthält. Es gibt zwei Hauptmethoden, um eine Sicherheits Beschreibung für das Verzeichnis Objekt zu lesen und zu bearbeiten:

-   Verwenden Sie die [**IADs:: Get**](/windows/desktop/api/iads/nf-iads-iads-get) -Methode, um die Sicherheits Beschreibung als ADSI COM-Objekt mit einer [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) -Schnittstelle abzurufen. Die Schnittstellen **IADsSecurityDescriptor**, [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist)und [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) können verwendet werden, um die Sicherheits Beschreibung und ihre Komponenten (ACLs, ACEs usw.) zu verarbeiten. Weitere Informationen und ein Codebeispiel finden Sie [unter Verwenden von IADs, um eine Sicherheits Beschreibung zu erhalten](using-iads-to-get-a-security-descriptor.md).
-   Verwenden Sie die [**IDirectoryObject:: getobjectattributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-getobjectattributes) -Methode, um eine Objekt Sicherheits Beschreibung als Zeiger auf eine [**Sicherheits \_ deskriptorstruktur**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) abzurufen. Verwenden Sie diesen Zeiger mit einer Win32-Zugriffs Steuerungsfunktion, z. b. [**Access Check**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck) oder [**buildsecuritydescriptor**](/windows/desktop/api/aclapi/nf-aclapi-buildsecuritydescriptora). Weitere Informationen und ein Codebeispiel finden Sie [unter Verwenden von IDirectoryObject, um eine Sicherheits Beschreibung zu erhalten](using-idirectoryobject-to-get-a-security-descriptor.md).

Die empfohlene Vorgehensweise und die für die meisten Codebeispiele in diesem Leitfaden verwendete Methode besteht darin, die **IADs \*** -Schnittstellen zu verwenden, da Sie die Handhabung von Sicherheits Deskriptoren, ACLs und ACEs vereinfachen. Für Visual Basic Programmierer sind die **IADs \*** -Schnittstellen die effizienteste Methode zur Handhabung von Sicherheits Beschreibungen.

Die [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) -Technik ist hilfreich, wenn eine [**Sicherheits \_ deskriptorstruktur**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) erforderlich ist. Beispielsweise verwendet das Codebeispiel zum über [Prüfen eines Steuerungs Zugriffsrechts in der ACL eines Objekts](checking-a-control-access-right-in-an-objectampaposs-acl.md) diese Methode, um eine Sicherheits Beschreibung abzurufen, die an die [**accesscheckbytyperesultlist**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) -Funktion übergeben werden soll.

Weitere Informationen finden Sie unter

-   [Verwenden von IADs, um eine Sicherheits Beschreibung zu erhalten](using-iads-to-get-a-security-descriptor.md)
-   [Verwenden von IDirectoryObject, um eine Sicherheits Beschreibung zu erhalten](using-idirectoryobject-to-get-a-security-descriptor.md)
-   [Sicherheitsbeschreibungenkomponenten](security-descriptor-components.md)
-   [Abrufen der DACL eines Objekts](retrieving-an-objectampaposs-dacl.md)
-   [Abrufen der SACL eines Objekts](retrieving-an-objectampaposs-sacl.md)
-   [Die Sicherheits Beschreibung eines Objekts wird gelesen.](reading-an-objectampaposs-security-descriptor.md)
-   [Beispiel Code zum Erstellen einer Sicherheits Beschreibung](example-code-for-creating-a-security-descriptor.md)
-   [Beispiel Code für das Auflisten der ACL eines Objekts in Active Directory Domain Services](example-code-for-enumerating-the-acl-of-an-active-directory-object.md)

 

 