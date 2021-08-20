---
title: Abrufen der SACL eines Objekts
description: Die Sicherheitsbeschreibung eines Objekts in Active Directory Domain Services kann eine Systemzugriffssteuerungsliste (SACL) enthalten.
ms.assetid: b1da91a2-d9b0-48a3-9de5-1e588209032d
ms.tgt_platform: multiple
keywords:
- SACL AD
- SACL AD , Abrufen der SACL eines Objekts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2b259ba838dbd0245725990a0c849ec4c3543b2bcac0e3c1e90dd7abd873c91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118184178"
---
# <a name="retrieving-an-objects-sacl"></a>Abrufen der SACL eines Objekts

Die Sicherheitsbeschreibung eines Objekts in Active Directory Domain Services kann eine Systemzugriffssteuerungsliste (SACL) enthalten. Eine SACL enthält Zugriffssteuerungseinträge (Access Control Entries, ACEs), die die Typen von Zugriffsversuchen angeben, die Überwachungsdatensätze im Sicherheitsereignisprotokoll eines Domänencontrollers generieren. Beachten Sie, dass eine SACL Protokolleinträge nur auf dem Domänencontroller generiert, auf dem der Zugriffsversuch aufgetreten ist, nicht auf jedem Domänencontroller, der ein Replikat des Objekts enthält.

Zum Festlegen oder Abrufen der SACL aus einem Objektsicherheitsdeskriptor muss die **SE \_ SECURITY \_ NAME-Berechtigung** im Zugriffstoken des anfordernden Threads aktiviert sein. Die Administratorengruppe verfügt standardmäßig über diese Berechtigung und kann anderen Benutzern oder Gruppen zugewiesen werden. Weitere Informationen finden Sie unter [SACL-Zugriffsrecht.](/windows/desktop/SecAuthZ/sacl-access-right)

Verwenden Sie die [**IADsSecurityDescriptor-Schnittstelle,**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) um die SACL eines Verzeichnisobjekts abzurufen und festzulegen. Mit C++ gibt die [**IADsSecurityDescriptor::get \_ SystemAcl-Methode**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) einen [**IDispatch-Zeiger**](/windows/win32/api/oaidl/nn-oaidl-idispatch) zurück. Rufen Sie **QueryInterface** für diesen **IDispatch-Zeiger** auf, um eine [**IADsAccessControlList-Schnittstelle**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist) abzurufen, und verwenden Sie die Methoden auf dieser Schnittstelle, um auf die einzelnen ACEs in der SACL zuzugreifen. Weitere Informationen zum Verfahren zum Ändern einer SACL, die dem Verfahren zum Ändern einer DACL ähnelt, finden Sie unter [Festlegen von Zugriffsrechten für ein Objekt.](setting-access-rights-on-an-object.md)

Um die ACEs in einer SACL aufzulisten, verwenden Sie die [**IADsAccessControlList::get \_ \_ NewEnum-Methode,**](/windows/desktop/api/iads/nf-iads-iadsaccesscontrollist-get__newenum) die einen [**IUnknown-Zeiger**](/windows/win32/api/unknwn/nn-unknwn-iunknown) zurückgibt. Rufen Sie **QueryInterface** für diesen **IUnknown-Zeiger** auf, um eine [**IEnumVARIANT-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) abzurufen. Verwenden Sie die [**IEnumVARIANT::Next-Methode,**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) um die ACEs in der ACL aufzuzählen. Jeder ACE wird als **VARIANT** zurückgegeben, der einen [**IDispatch-Zeiger**](/windows/win32/api/oaidl/nn-oaidl-idispatch) enthält. Beachten Sie, dass der **vt-Member** **VT \_ DISPATCH** ist. Rufen Sie **QueryInterface** für diesen **IDispatch-Zeiger** auf, um eine [**IADsAccessControlEntry-Schnittstelle**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) für den ACE abzurufen. Verwenden Sie die **IADsAccessControlEntry-Schnittstellenmethoden,** um die Komponenten eines ACE festzulegen oder abzurufen.

Weitere Informationen zu SACLs finden Sie unter:

-   [Zugriffssteuerungslisten (ACLs)](/windows/desktop/SecAuthZ/access-control-lists)
-   [Generierung von Überwachungsdatensätzen](/windows/desktop/SecAuthZ/audit-generation)

 

 