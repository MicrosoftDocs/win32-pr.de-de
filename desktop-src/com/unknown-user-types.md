---
title: Unbekannte Benutzer Typen
description: Unbekannte Benutzer Typen
ms.assetid: c2a4bd83-6eaf-4130-8f86-e99f1e18b63d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4843ca2e19508806bba952403a2211a39f5a5ca
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316575"
---
# <a name="unknown-user-types"></a>Unbekannte Benutzer Typen

Sie können die Produktlokalisierung vereinfachen, indem Sie den folgenden Registrierungsschlüssel hinzufügen:

**HKEY \_ LOCAL \_ Machines \\ Software \\ Microsoft \\ OLE2** \\ **unknownusertype**  =  *usertype*

Mit diesem Schlüssel können Funktionen eine angegebene Zeichenfolge anstelle des Standardwerts "unknown" zurückgeben, sodass Lokalisierer einen Benutzertyp einer anderen Sprache angeben können.

Die Implementierung von [**IOleObject:: GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) des com-Standard Handlers überprüft die Registrierung durch Aufrufen von [**olereggetusertype**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype). Wenn die Klasse des Objekts in der Registrierung nicht gefunden wird, wird der Benutzertyp aus der [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) -Instanz des Objekts zurückgegeben. Wenn die Klasse in der **IStorage** -Instanz des Objekts nicht gefunden wird, wird die Zeichenfolge "unknown" zurückgegeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrieren von com-Anwendungen](registering-com-applications.md)
</dt> </dl>

 

 