---
title: Abrufen der DACL eines Objekts
description: Die Sicherheitsbeschreibung eines Objekts kann eine DACL (Discretionary Access Control List) enthalten.
ms.assetid: 93b16094-9923-4886-804f-4e989fbf6977
ms.tgt_platform: multiple
keywords:
- DACL AD
- DACL AD , Abrufen der DACL eines Objekts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b515e6c5d28be7003734510300fc7f6d2de776b479b56e62ad521567c76dce4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025108"
---
# <a name="retrieving-an-objects-dacl"></a>Abrufen der DACL eines Objekts

Die Sicherheitsbeschreibung eines Objekts kann eine DACL (Discretionary Access Control List) enthalten. Eine DACL enthält null oder mehr Zugriffssteuerungseinträge (ACCESS Control Entries, ACEs), die die Benutzer und Gruppen identifizieren, die auf das Objekt zugreifen können. Wenn eine DACL leer ist (d. h., sie enthält null ACEs), wird kein Zugriff explizit gewährt, sodass der Zugriff implizit verweigert wird. Wenn der Sicherheitsdeskriptor eines Objekts jedoch über keine DACL verfügt, ist das Objekt nicht geschützt, und alle Benutzer haben vollständigen Zugriff.

Um die DACL eines Objekts abzurufen, müssen Sie besitzer des Objekts sein oder **über READ \_ CONTROL-Zugriff** auf das Objekt verfügen.

Verwenden Sie die [**IADsSecurityDescriptor-Schnittstelle,**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) um die DACL eines Verzeichnisobjekts abzurufen und festzulegen. Mit C++ gibt die [**IADsSecurityDescriptor::get \_ DiscretionaryAcl-Methode**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) einen [**IDispatch-Zeiger**](/windows/win32/api/oaidl/nn-oaidl-idispatch) zurück. Rufen Sie **QueryInterface** für diesen **IDispatch-Zeiger** auf, um eine [**IADsAccessControlList-Schnittstelle**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist) abzurufen, und verwenden Sie die Methoden auf dieser Schnittstelle, um auf die einzelnen ACEs in der DACL zuzugreifen. Das Verfahren zum Ändern einer DACL wird unter [Festlegen von Zugriffsrechten für ein Objekt](setting-access-rights-on-an-object.md)beschrieben.

Um die ACEs aufzulisten, verwenden Sie die [**IADsAccessControlList::get \_ \_ NewEnum-Methode.**](/windows/desktop/api/iads/nf-iads-iadsaccesscontrollist-get__newenum) Die -Methode gibt einen [**IUnknown-Zeiger**](/windows/win32/api/unknwn/nn-unknwn-iunknown) zurück. Rufen Sie **QueryInterface** für diesen **IUnknown-Zeiger** auf, um eine [**IEnumVARIANT-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) abzurufen. Verwenden Sie die [**IEnumVARIANT::Next-Methode,**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) um die ACEs in der ACL aufzuzählen. Jeder ACE wird als **VARIANT** zurückgegeben, der einen [**IDispatch-Zeiger**](/windows/win32/api/oaidl/nn-oaidl-idispatch) enthält (der **vt-Member** ist **VT \_ DISPATCH).** Rufen Sie **QueryInterface** für diesen **IDispatch-Zeiger** auf, um eine [**IADsAccessControlEntry-Schnittstelle**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) für den ACE abzurufen. Sie können die Methoden der **IADsAccessControlEntry-Schnittstelle** verwenden, um die Komponenten eines ACE festzulegen oder abzurufen.

Weitere Informationen zu DACLs und ACEs finden Sie in den folgenden Themen im Platform Software Development Kit (SDK).

-   [Zugriffssteuerungslisten (ACLs)](/windows/desktop/SecAuthZ/access-control-lists)
-   [Zugriffssteuerungseinträge (ACEs)](/windows/desktop/SecAuthZ/access-control-entries)

 

 