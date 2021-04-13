---
title: Erstellen von Sicherheits Deskriptoren für neue Verzeichnisobjekte
description: Sie können ADSI verwenden, um eine Sicherheits Beschreibung zu erstellen und Sie als ntSecurityDescriptor-Eigenschaft eines neuen Objekts festzulegen, oder Sie verwenden, um die ntSecurityDescriptor-Eigenschaft eines vorhandenen Objekts zu ersetzen.
ms.assetid: b9ff626f-17f1-4fc1-9d6e-4f47e29a5aeb
ms.tgt_platform: multiple
keywords:
- Erstellen einer Sicherheits Beschreibung für ein neues Verzeichnis Objekt AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78265d27c52023d669e27fc9890fd2d5273e2ffd
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472628"
---
# <a name="creating-security-descriptors-for-new-directory-objects"></a>Erstellen von Sicherheits Deskriptoren für neue Verzeichnisobjekte

Sie können ADSI verwenden, um eine Sicherheits Beschreibung zu erstellen und Sie als **ntSecurityDescriptor** -Eigenschaft eines neuen Objekts festzulegen, oder Sie verwenden, um die **ntSecurityDescriptor** -Eigenschaft eines vorhandenen Objekts zu ersetzen.

So erstellen Sie eine Sicherheits Beschreibung für ein Objekt:

1.  Verwenden Sie [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , um das ADSI COM-Objekt für die neue Sicherheits Beschreibung zu erstellen, und rufen Sie einen [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) -Schnittstellen Zeiger auf dieses Objekt ab. Beachten Sie, dass die Klassen-ID **CLSID \_ securityDescriptor** ist.
2.  Verwenden Sie die [**IADsSecurityDescriptor::p UT- \_ Besitzer**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) Methode, um den Besitzer des Objekts festzulegen. Der Vertrauens nehmer ist ein Benutzer, eine Gruppe oder ein anderer Sicherheits Prinzipal. Eine Anwendung sollte den Wert aus der entsprechenden Eigenschaft aus dem Benutzer-oder Gruppen Objekt des Vertrauens nehmers verwenden, auf den der ACE angewendet werden soll.
3.  Verwenden Sie die [**IADsSecurityDescriptor::p UT- \_ Steuerungs**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) Methode, um zu steuern, ob DACLs und SACLs von dem Objekt von seinem übergeordneten Container geerbt werden.
4.  Verwenden Sie [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , um das ADSI COM-Objekt für die DACL für die neue Sicherheits Beschreibung zu erstellen, und rufen Sie einen [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist) -Schnittstellen Zeiger auf dieses Objekt ab. Beachten Sie, dass die Klassen-ID **CLSID \_ AccessControlList** ist.
5.  Verwenden Sie für jeden ACE, der der DACL hinzugefügt werden soll, [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , um das ADSI COM-Objekt für den neuen ACE zu erstellen, und rufen Sie einen [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) -Schnittstellen Zeiger auf dieses Objekt ab. Beachten Sie, dass die Klassen-ID CLSID \_ AccessControlEntry ist.
6.  Legen Sie für jeden ACE, der der DACL hinzugefügt werden soll, die Eigenschaften des ACE mithilfe der Eigenschafts Methoden des [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) -Objekts des ACE fest. Weitere Informationen zu den Eigenschaften, die für einen ACE festgelegt werden, finden Sie unter [Festlegen von Zugriffsrechten für ein Objekt](setting-access-rights-on-an-object.md).
7.  Verwenden Sie für jeden ACE, der der DACL hinzugefügt werden soll, die **QueryInterface** -Methode für das [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) -Objekt, um einen [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Zeiger zu erhalten. Die [**IADsAccessControlList:: addace**](/windows/desktop/api/iads/nf-iads-iadsaccesscontrollist-addace) -Methode erfordert einen **IDispatch** -Schnittstellen Zeiger auf den ACE.
8.  Verwenden Sie für jeden ACE, der der DACL hinzugefügt werden soll, [**IADsAccessControlList:: addace**](/windows/desktop/api/iads/nf-iads-iadsaccesscontrollist-addace) , um den neuen ACE der DACL hinzuzufügen. Beachten Sie, dass sich die Reihenfolge der ACEs innerhalb der ACL auf die Auswertung des Zugriffs auf das Objekt auswirken kann. Der richtige Zugriff auf das Objekt erfordert möglicherweise, dass Sie eine neue ACL erstellen, die ACEs aus der vorhandenen ACL in der richtigen Reihenfolge der neuen ACL hinzufügen und dann die vorhandene ACL in der Sicherheits Beschreibung durch die neue ACL ersetzen. Weitere Informationen finden Sie unter [Reihenfolge von ACEs in einer DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).
9.  Führen Sie die Schritte 4-8 aus, um die SACL für den neuen Sicherheits Deskriptor zu erstellen.
10. Verwenden Sie die [**IADsSecurityDescriptor::p UT-Methode " \_ diskretionaryacl**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) ", um die DACL festzulegen. Weitere Informationen zu DACLs finden Sie unter [null-DACLs und leere DACLs](null-dacls-and-empty-dacls.md).
11. Verwenden Sie die [**IADsSecurityDescriptor::p UT \_ SystemAcl**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) -Methode, um die SACL festzulegen.
12. Konvertieren Sie das [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) -Objekt in eine [**Variante**](/windows/win32/api/oaidl/ns-oaidl-variant) , indem Sie mithilfe der **QueryInterface** -Methode des **IADsSecurityDescriptor** -Objekts eine [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle abrufen. Legen Sie dann den **VT** -Member **der Variante** auf **VT \_ Dispatch** fest, und legen Sie den **pdispVal** -Member der **Variante** gleich dem **IDispatch** -Zeiger fest.
13. Rufen Sie einen [**IADs**](/windows/desktop/api/iads/nn-iads-iads) -Schnittstellen Zeiger auf das-Objekt ab.
14. Verwenden Sie die [**IADs::P UT**](/windows/desktop/api/iads/nf-iads-iads-put) -Methode mit "ntSecurityDescriptor" und die oben erstellte [**Variante**](/windows/win32/api/oaidl/ns-oaidl-variant) , um die neue Sicherheits Beschreibung in den Eigenschaften Cache zu schreiben.
15. Verwenden Sie die [**IADs:: SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) -Methode, um die-Eigenschaft für das Objekt im Verzeichnis zu aktualisieren.

 

 