---
title: Abrufen der SACL eines Objekts
description: Die Sicherheits Beschreibung eines Objekts in Active Directory Domain Services kann eine SACL (System Access-Control List) enthalten.
ms.assetid: b1da91a2-d9b0-48a3-9de5-1e588209032d
ms.tgt_platform: multiple
keywords:
- SACL-AD
- SACL AD, Abrufen der SACL eines Objekts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 537846f2080aecdab8e22f5fce5bdfa36298fb74
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104314612"
---
# <a name="retrieving-an-objects-sacl"></a>Abrufen der SACL eines Objekts

Die Sicherheits Beschreibung eines Objekts in Active Directory Domain Services kann eine SACL (System Access-Control List) enthalten. Eine SACL enthält Zugriffs Steuerungs Einträge (Access Control Entries, ACEs), die die Typen der Zugriffsversuche angeben, mit denen Überwachungsdaten Sätze im Sicherheits Ereignisprotokoll eines Domänen Controllers generiert werden. Beachten Sie, dass eine SACL Protokolleinträge nur auf dem Domänen Controller generiert, auf dem der Zugriffs Versuch aufgetreten ist, nicht auf allen Domänen Controllern, die ein Replikat des Objekts enthalten.

Um die SACL aus einer Objekt Sicherheits Beschreibung festzulegen oder zu erhalten, muss die Berechtigung " **SE \_ Security \_ Name** " im Zugriffs Token des anfordernden Threads aktiviert werden. Die Administratoren Gruppe verfügt standardmäßig über diese Berechtigung und kann anderen Benutzern oder Gruppen zugewiesen werden. Weitere Informationen finden Sie unter [SACL-Zugriffsrecht](/windows/desktop/SecAuthZ/sacl-access-right).

Um die SACL eines Verzeichnis Objekts zu erhalten und festzulegen, verwenden Sie die [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) -Schnittstelle. Mithilfe von C++ gibt die [**IADsSecurityDescriptor:: get \_ SystemAcl**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) -Methode einen [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Zeiger zurück. Aufrufen von **QueryInterface** für diesen **IDispatch** -Zeiger, um eine [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist) -Schnittstelle abzurufen, und verwenden die Methoden für diese Schnittstelle, um auf die einzelnen ACEs in der SACL zuzugreifen. Weitere Informationen zur Vorgehensweise beim Ändern einer SACL, die dem zum Ändern einer DACL ähnelt, finden Sie unter [Festlegen von Zugriffsrechten für ein Objekt](setting-access-rights-on-an-object.md).

Um die ACEs in einer SACL aufzulisten, verwenden Sie die [**IADsAccessControlList:: get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadsaccesscontrollist-get__newenum) -Methode, die einen [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Zeiger zurückgibt. Ruft **QueryInterface** für diesen **IUnknown** -Zeiger auf, um eine [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle zu erhalten. Verwenden Sie die [**IEnumVARIANT:: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) -Methode, um die ACEs in der ACL aufzuzählen. Jeder ACE wird als **Variant** zurückgegeben, der einen [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Zeiger enthält. Beachten Sie, dass das **VT** -Element **VT \_ Dispatch** ist. Ruft **QueryInterface** für diesen **IDispatch** -Zeiger auf, um eine [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) -Schnittstelle für den ACE zu erhalten. Verwenden Sie die **IADsAccessControlEntry** -Schnittstellen Methoden, um die Komponenten eines ACE festzulegen oder zu erhalten.

Weitere Informationen zu SACLs finden Sie unter:

-   [Zugriffs Steuerungs Listen (ACLs)](/windows/desktop/SecAuthZ/access-control-lists)
-   [Generierung von Überwachungsdatensätzen](/windows/desktop/SecAuthZ/audit-generation)

 

 