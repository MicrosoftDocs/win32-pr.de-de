---
title: Syntaxen für Attribute in Active Directory Domain Services
description: Active Directory Domain Services einen Satz von Attributsyntaxen zum Angeben des Datentyps, der in einem Attribut enthalten ist.
ms.assetid: 79d27d47-5d03-4ad6-bf97-c387c34fa454
ms.tgt_platform: multiple
keywords:
- Syntaxen für Active Directory Domain Services Attribute Active Directory
- Attribute Active Directory , Syntaxen für
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c324fef5267ce37b42ede66b618b33148d266ac52dd69662a15bbce6094951ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118182838"
---
# <a name="syntaxes-for-attributes-in-active-directory-domain-services"></a>Syntaxen für Attribute in Active Directory Domain Services

Active Directory Domain Services einen Satz von Attributsyntaxen zum Angeben des Datentyps, der in einem Attribut enthalten ist. Die vordefinierten Syntaxen werden nicht tatsächlich im Verzeichnis angezeigt, und Sie können keine neuen Syntaxen hinzufügen. Es können mehrere Methoden verwendet werden, um die Syntax einer Attributklasse zu identifizieren:

-   Die [**Methoden IADs.Get,**](/windows/desktop/api/iads/nf-iads-iads-get) [**IADs.GetEx,**](/windows/desktop/api/iads/nf-iads-iads-getex) [**IADs.Put**](/windows/desktop/api/iads/nf-iads-iads-put)und [**IADs.PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) verwenden die [**VARIANT-Struktur,**](/windows/win32/api/oaidl/ns-oaidl-variant) um die Werte der Attribute eines Objekts zu erhalten und fest zu legen. Der **vt-Member** dieser Struktur ist ein **VARTYPE-Wert,** der den Datentyp identifiziert.
-   Die Methoden der [**Schnittstellen IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) und [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) verwenden einen Wert aus der [**ADSTYPEENUM-Enumeration,**](/windows/win32/api/iads/ne-iads-adstypeenum) um den Datentyp anzugeben.
-   Um die Syntax einer neuen Attributklasse anzugeben, legen Sie die [**attributeSyntax-**](/windows/desktop/ADSchema/a-attributesyntax) und [**oMSyntax-Attribute**](/windows/desktop/ADSchema/a-omsyntax) eines [**attributeSchema-Objekts**](/windows/desktop/ADSchema/c-attributeschema) fest. Wenn der Wert **von oMSyntax** 127 ist, müssen Sie auch das [**oMObjectClass-Attribut**](/windows/desktop/ADSchema/a-omobjectclass) festlegen. Weitere Informationen finden Sie unter [Auswählen einer Syntax.](choosing-a-syntax.md)

Eine vollständige Liste der von Active Directory Domain Services bereitgestellten Syntaxen, einschließlich des entsprechenden **VARTYPE-** und [**ADSTYPEENUM-Werts**](/windows/win32/api/iads/ne-iads-adstypeenum) jeder Syntax, finden Sie [unter Syntaxs](/windows/desktop/ADSchema/syntaxes).

 

 