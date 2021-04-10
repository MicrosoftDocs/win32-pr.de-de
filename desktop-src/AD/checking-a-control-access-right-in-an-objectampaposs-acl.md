---
title: Überprüfen des Zugriffs auf das Steuerungs Recht in der ACL eines Objekts
description: Verwenden Sie die accesscheckbytyperesultlist-Funktion, um ein Zugriffsrecht für das Steuerelement auf der ACL eines Objekts zu überprüfen.
ms.assetid: 5a609622-6a1a-46ae-a336-afec504225c7
ms.tgt_platform: multiple
keywords:
- Überprüfen des Zugriffs auf das Zugriffsrecht in einer Objekt-ACL-Werbung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10170bd496da14657356a2334015975da1cc02ff
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038797"
---
# <a name="checking-a-control-access-right-in-an-objects-acl"></a>Überprüfen des Zugriffs auf das Steuerungs Recht in der ACL eines Objekts

Verwenden Sie die [**accesscheckbytyperesultlist**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) -Funktion, um ein Zugriffsrecht für das Steuerelement auf der ACL eines Objekts zu überprüfen. Um diese Funktion verwenden zu können, benötigt eine Anwendung einen Zeiger auf die [**Sicherheits \_ Beschreibung**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) für das-Objekt anstelle einer [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) -Schnittstelle auf ein COM-Objekt des ADSI-Sicherheits Deskriptors.

Führen Sie die folgenden Schritte aus, um den Zugriff auf ein kontrolliertes Zugriffsrecht für ein Objekt zu überprüfen:

1.  Einen [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) -Schnittstellen Zeiger auf das-Objekt zu erhalten.
2.  Verwenden Sie die [**IDirectoryObject:: getobjectattributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-getobjectattributes) -Methode, um die Sicherheits Beschreibung des-Objekts zu erhalten. Der Name der Eigenschaft, die die Sicherheits Beschreibung enthält, ist [**ntSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor). Die-Eigenschaft wird als Zeiger auf eine [**Sicherheits \_ deskriptorstruktur**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) zurückgegeben.
3.  Verwenden Sie die [**Sicherheits \_ deskriptorstruktur**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) mit der [**accesscheckbytyperesultlist**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) -Funktion, um die Berechtigungen für das angegebene Zugriffsrecht für den angegebenen Client zu überprüfen.

Der Beispielcode im [Beispielcode zum Überprüfen eines Steuerungs Zugriffsrechts in der ACL eines Objekts](example-code-for-checking-a-control-access-right-in-an-objectampaposs-acl.md) zeigt im Detail, wie dies geschieht.

 

 