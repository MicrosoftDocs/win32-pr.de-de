---
title: Unbekannte Benutzertypen
description: Unbekannte Benutzertypen
ms.assetid: c2a4bd83-6eaf-4130-8f86-e99f1e18b63d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ce5ee88d36399187bab24ce51f0ef1c3c074182f98ce30ff6dc7d370992ffd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129462"
---
# <a name="unknown-user-types"></a>Unbekannte Benutzertypen

Sie können die Produktlokalisierung erleichtern, indem Sie den folgenden Registrierungsschlüssel hinzufügen:

**HKEY \_ LOCAL \_ MACHINES SOFTWARE Microsoft \\ \\ \\ OLE2** \\ **UnknownUserType-Benutzertyp**  =  

Mit diesem Schlüssel können Funktionen anstelle des Standardwerts "Unknown" eine angegebene Zeichenfolge zurückgeben, sodass Lokalisierer einen Benutzertyp einer anderen Sprache angeben können.

Die Implementierung von [**IOleObject::GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) durch den COM-Standardhandler untersucht die Registrierung, indem [**OleRegGetUserType aufgerufen wird.**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype) Wenn die Klasse des Objekts nicht in der Registrierung gefunden wird, wird der Benutzertyp aus der [**IStorage-Instanz**](/windows/desktop/api/objidl/nn-objidl-istorage) des Objekts zurückgegeben. Wenn die Klasse in der **IStorage-Instanz** des Objekts nicht gefunden wird, wird die Zeichenfolge "Unknown" zurückgegeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrieren von COM-Anwendungen](registering-com-applications.md)
</dt> </dl>

 

 