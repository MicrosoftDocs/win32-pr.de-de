---
title: Lesen eines Steuerelement Zugriffsrechts, das in der ACL eines Objekts festgelegt ist
description: Die Eigenschaften der IADsAccessControlEntry-Schnittstelle werden verwendet, um Steuerungs Zugriffsrechte zu erteilen oder zu verweigern.
ms.assetid: 2c6fef91-990e-4954-9aff-c9ec72d13972
ms.tgt_platform: multiple
keywords:
- Lesen eines Steuerelement Zugriffsrechts, das in der ACL eines Objekts festgelegt ist Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4877c96a95fc94095c79ad129e8a07b1c786abe1
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038741"
---
# <a name="reading-a-control-access-right-set-in-an-objects-acl"></a>Lesen eines Steuerelement Zugriffsrechts, das in der ACL eines Objekts festgelegt ist

Mit ADSI lesen Sie einen Steuerungs Zugriffsrechten ACE genauso wie jeden anderen ACE in einer ACL. Beachten Sie, dass Sie auch die Win32-Sicherheits-APIs zum Lesen von ACLs für Verzeichnisobjekte verwenden können. Steuerungs Zugriffsrechte verwenden jedoch die Eigenschaften der [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) -Schnittstelle auf eine Weise, die für das erteilen und Verweigern von Steuerungs Zugriffsrechten spezifisch ist:

-   [**AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) muss ADS mit dem **\_ rechten \_ DS- \_ Steuerungs \_ Zugriff** enthalten.
-   Der [**Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) -Wert ist ein Anzeige Kennzeichen- **\_ \_ \_ Objekttyp \_**.
-   [**ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) ist die Zeichen folgen Form des **rightsguid** -Attributs des Zugriffsrechts für das Steuerelement. Das Zeichen folgen Format der GUID ist dasselbe Zeichen folgen Format wie die [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) -com-Bibliotheksfunktion.
-   Der [**AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) ist entweder **ADS \_ AceType \_ Access \_ Allowed \_ Object** , um dem Vertrauens nehmer den Zugriff auf das Zugriffsrecht für den Vertrauens nehmer und das Zugriff auf das **\_ \_ Zugriffs \_ Verweigerungs \_ Objekt** für den Vertrauens nehmer zu verweigern
-   Der Vertrauens [**nehmer ist der**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) Sicherheits Prinzipal. Dies ist der Benutzer, die Gruppe, der Computer usw., auf den der ACE angewendet wird.

Verwenden Sie das folgende Verfahren zum Lesen eines ACE für ein ADSI-Objekt. Das folgende Verfahren gilt für C-und C++-Anwendungen.

**So lesen Sie einen ACE für ein ADSI-Objekt**

1.  Einen [**IADs**](/windows/desktop/api/iads/nn-iads-iads) -Schnittstellen Zeiger auf das-Objekt zu erhalten.
2.  Verwenden Sie die [**IADs:: Get**](/windows/desktop/api/iads/nf-iads-iads-get) -Methode, um die Sicherheits Beschreibung des-Objekts zu erhalten. Der Name der Eigenschaft, die die Sicherheits Beschreibung enthält, ist "ntSecurityDescriptor". Die-Eigenschaft wird als **Variant** zurückgegeben, der einen [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Zeiger enthält. Beachten Sie, dass das **VT** -Element **VT \_ Dispatch** ist. Aufrufen von **QueryInterface** für diesen **IDispatch** -Zeiger zum Abrufen einer [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) -Schnittstelle, um die Methoden für diese Schnittstelle für den Zugriff auf die Sicherheits Deskriptor-ACL zu verwenden.
3.  Verwenden Sie die [**IADsSecurityDescriptor:: get \_ diskretionaryacl**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) -Methode, um die ACL zu erhalten. Die-Methode gibt einen [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Zeiger zurück. Ruft **QueryInterface** für diesen **IDispatch** -Zeiger auf, um eine [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist) -Schnittstelle zu erhalten, mit der die Methoden für diese Schnittstelle für den Zugriff auf die einzelnen ACEs in der ACL verwendet werden.
4.  Verwenden Sie die [**IADsAccessControlList:: get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadsaccesscontrollist-get__newenum) -Methode, um die ACEs aufzulisten. Die Methode gibt einen [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Zeiger zurück. Ruft **QueryInterface** für diesen **IUnknown** -Zeiger auf, um eine [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle zu erhalten.
5.  Verwenden Sie die [**IEnumVARIANT:: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) -Methode, um die ACEs in der ACL aufzuzählen. Die-Eigenschaft wird als **Variant** zurückgegeben, der einen [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Zeiger enthält. Beachten Sie, dass das **VT** -Element **VT \_ Dispatch** ist. Ruft **QueryInterface** für diesen **IDispatch** -Zeiger auf, um eine [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) -Schnittstelle zum Lesen des ACE abzurufen.
6.  Aufrufen der [**IADsAccessControlEntry:: get \_ AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) -Methode, um die **AccessMask** abzurufen und zu überprüfen, ob der **AccessMask** -Wert für das ADS-Zugriffs Flag für das **\_ \_ Zugriffsrecht DS- \_ Steuer \_** Element Wenn Sie über dieses Flag verfügt, enthält der ACE ein Zugriffsrecht für das Steuerelement.
7.  Ruft die [**IADsAccessControlEntry:: get \_ Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) -Methode auf, um das Flag für den Objekttyp zu erhalten.
8.  Überprüfen Sie die [**Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) für **ADS \_ Flag- \_ \_ Objekttyp \_ vorhanden** Flag. Wenn **Flags** auf **ADS Flag- \_ \_ \_ Objekttyp \_ vorhanden** festgelegt ist, müssen Sie die **IADsAccessControlEntry:: get \_ ObjectType** -Methode aufrufen, um eine Zeichenfolge abzurufen, die die rightsguid des Steuerelement Zugriffsrechts enthält, für das der ACE gilt.
9.  Wenden Sie die [**IADsAccessControlEntry:: get \_ AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) -Methode an, um den ACE-Typ abzurufen. Der Typ ist ein ADS-AceType-Objekt, das auf das **\_ \_ \_ zulässige \_ Objekt** zugreifen kann, um dem Vertrauens nehmer das Zugriffsrecht für den Zugriff auf das Zugriffsrecht zu gewähren oder das Zugriff auf das **\_ \_ Zugriffs \_ \_** Recht "ADS
10. Wenden Sie die Methode [**IADsAccessControlEntry:: get \_ Treuhänder**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) an, um den Sicherheits Prinzipal abzurufen. Hierbei handelt es sich um Benutzer, Gruppen, Computer usw., auf die der ACE angewendet wird.
11. Wenn Sie die Zeichen folgen [**ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) und **Treuhänder** abgeschlossen haben, verwenden Sie [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) , um den Arbeitsspeicher für diese Zeichen folgen freizugeben.
12. Wenn Sie mit den Schnittstellen fertig sind, müssen Sie **Release** zum Dekrement oder Release aller Schnittstellen Verweise aufzurufen.

 

 