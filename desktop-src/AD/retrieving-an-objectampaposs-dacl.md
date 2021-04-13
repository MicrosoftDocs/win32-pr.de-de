---
title: Abrufen der DACL eines Objekts
description: Die Sicherheits Beschreibung eines Objekts kann eine freigegebene Zugriffs Steuerungs Liste (DACL) enthalten.
ms.assetid: 93b16094-9923-4886-804f-4e989fbf6977
ms.tgt_platform: multiple
keywords:
- DACL-AD
- DACL-AD, Abrufen der DACL eines Objekts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3db74cb235b5cb322f0edf3dc4cfb32f50b4c00c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104314607"
---
# <a name="retrieving-an-objects-dacl"></a>Abrufen der DACL eines Objekts

Die Sicherheits Beschreibung eines Objekts kann eine freigegebene Zugriffs Steuerungs Liste (DACL) enthalten. Eine DACL enthält NULL oder mehr Zugriffs Steuerungs Einträge (ACEs), mit denen die Benutzer und Gruppen identifiziert werden, die auf das Objekt zugreifen können. Wenn eine DACL leer ist (d. h., Sie enthält NULL-ACEs), wird kein Zugriff explizit erteilt, sodass der Zugriff implizit verweigert wird. Wenn die Sicherheits Beschreibung eines Objekts jedoch nicht über eine DACL verfügt, ist das Objekt nicht geschützt, und jeder Benutzer verfügt über vollständigen Zugriff.

Zum Abrufen der DACL eines Objekts müssen Sie der Besitzer des Objekts sein oder über **Lesezugriff \_** auf das Objekt verfügen.

Verwenden Sie die [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) -Schnittstelle, um die DACL eines Verzeichnis Objekts zu erhalten und festzulegen. Mithilfe von C++ gibt die [**IADsSecurityDescriptor:: get \_ diskretionaryacl**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) -Methode einen [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Zeiger zurück. Aufrufen von **QueryInterface** für diesen **IDispatch** -Zeiger zum Abrufen einer [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist) -Schnittstelle und Verwenden der Methoden für diese Schnittstelle für den Zugriff auf die einzelnen ACEs in der DACL. Die Vorgehensweise zum Ändern einer DACL ist unter [Festlegen von Zugriffsrechten für ein Objekt](setting-access-rights-on-an-object.md)beschrieben.

Um die ACEs aufzulisten, verwenden Sie die [**IADsAccessControlList:: get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadsaccesscontrollist-get__newenum) -Methode. Die Methode gibt einen [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Zeiger zurück. Ruft **QueryInterface** für diesen **IUnknown** -Zeiger auf, um eine [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle zu erhalten. Verwenden Sie die [**IEnumVARIANT:: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) -Methode, um die ACEs in der ACL aufzuzählen. Jeder ACE wird als **Variant** zurückgegeben, der einen [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Zeiger enthält (das **VT** -Element ist **VT \_ Dispatch**). Ruft **QueryInterface** für diesen **IDispatch** -Zeiger auf, um eine [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) -Schnittstelle für den ACE zu erhalten. Sie können die Methoden der **IADsAccessControlEntry** -Schnittstelle verwenden, um die Komponenten eines ACE festzulegen oder abzurufen.

Weitere Informationen zu DACLs und ACEs finden Sie in den folgenden Themen im Platform Software Development Kit (SDK).

-   [Zugriffs Steuerungs Listen (ACLs)](/windows/desktop/SecAuthZ/access-control-lists)
-   [Zugriffs Steuerungs Einträge (ACEs)](/windows/desktop/SecAuthZ/access-control-entries)

 

 