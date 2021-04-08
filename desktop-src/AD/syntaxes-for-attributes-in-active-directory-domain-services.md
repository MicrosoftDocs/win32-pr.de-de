---
title: Syntaxen für Attribute in Active Directory Domain Services
description: Active Directory Domain Services einen Satz von Attribut Syntaxen definieren, um den Datentyp anzugeben, der in einem Attribut enthalten ist.
ms.assetid: 79d27d47-5d03-4ad6-bf97-c387c34fa454
ms.tgt_platform: multiple
keywords:
- Syntaxen für Active Directory Domain Services Attribute Active Directory
- Attribute Active Directory, Syntax für
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04386e1b4981a81585fe208afa4cca6ed02d4c3c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104101414"
---
# <a name="syntaxes-for-attributes-in-active-directory-domain-services"></a>Syntaxen für Attribute in Active Directory Domain Services

Active Directory Domain Services einen Satz von Attribut Syntaxen definieren, um den Datentyp anzugeben, der in einem Attribut enthalten ist. Die vordefinierten Syntaxen werden im Verzeichnis nicht tatsächlich angezeigt, und Sie können keine neuen Syntaxen hinzufügen. Es können mehrere Methoden verwendet werden, um die Syntax einer Attribut Klasse zu identifizieren:

-   Die Methoden " [**IADs. Get**](/windows/desktop/api/iads/nf-iads-iads-get)", " [**IADs. Getex**](/windows/desktop/api/iads/nf-iads-iads-getex)", " [**IADs. Put**](/windows/desktop/api/iads/nf-iads-iads-put)" und " [**IADs. PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) " verwenden die [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) -Struktur, um die Werte der Attribute eines Objekts zu erhalten und festzulegen. Der **VT** -Member dieser Struktur ist ein **VarType** -Wert, der den Datentyp identifiziert.
-   Die Methoden der [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) -Schnittstelle und der [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) -Schnittstelle verwenden einen Wert aus der [**adstyetenum**](/windows/win32/api/iads/ne-iads-adstypeenum) -Enumeration, um den Datentyp anzugeben.
-   Um die Syntax einer neuen Attribut Klasse anzugeben, legen Sie die Attribute [**attributeSyntax**](/windows/desktop/ADSchema/a-attributesyntax) und [**oMSyntax**](/windows/desktop/ADSchema/a-omsyntax) eines [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) -Objekts fest. Wenn der Wert von **oMSyntax** 127 ist, müssen Sie auch das [**oMObjectClass**](/windows/desktop/ADSchema/a-omobjectclass) -Attribut festlegen. Weitere Informationen finden Sie unter [Auswählen einer Syntax](choosing-a-syntax.md).

Eine umfassende Liste der Syntaxen, die von Active Directory Domain Services bereitgestellt werden, einschließlich der entsprechenden **VarType** -und [**adstypeer**](/windows/win32/api/iads/ne-iads-adstypeenum) -Werte der einzelnen Syntax [, finden Sie unter Syntax.](/windows/desktop/ADSchema/syntaxes)

 

 