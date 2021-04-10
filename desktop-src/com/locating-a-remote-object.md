---
title: Suchen eines Remote Objekts
description: Suchen eines Remote Objekts
ms.assetid: b329de53-646b-42a2-afa3-06473c3483d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d0ce1b2280faaed7be3b5afb25a48438ff1a2b7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103858511"
---
# <a name="locating-a-remote-object"></a>Suchen eines Remote Objekts

Mit der Einführung von com für verteilte Systeme verwendet com das grundlegende Modell für die Objekt Erstellung, das in [com-Klassen Objekten und CLSIDs](com-class-objects-and-clsids.md) beschrieben ist, und bietet mehr als eine Möglichkeit, ein Objekt zu finden, das sich auf einem anderen System in einem Netzwerk befinden kann, ohne die Client Anwendung zu überlasten.

COM hat Registrierungsschlüssel hinzugefügt, mit denen ein Server den Namen des Computers, auf dem er sich befindet, oder den Computer, auf dem sich ein vorhandener Speicher befindet, registrieren kann. Daher müssen Client Anwendungen nur die CLSID des Servers kennen.

In Fällen, in denen es gewünscht ist, hat com jedoch einen zuvor reservierten Parameter von [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) durch eine [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) -Struktur ersetzt, mit der ein Client den Speicherort eines Servers angeben kann. Ein weiterer wichtiger Wert in der **CoGetClassObject** -Funktion ist die [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) -Enumeration, die angibt, ob das erwartete Objekt Prozess interne, Prozess interne oder out-of-Process-Remote Vorgänge ausgeführt werden soll. Diese beiden Werte und die Werte in der Registrierung legen fest, wie und wo das Objekt ausgeführt werden soll.

> [!Note]  
> Beim Erstellen von Instanzen kann eine Registrierungs Einstellung überschrieben werden, wenn Sie einen Server Speicherort angeben. Der Algorithmus, den com hierfür verwendet, wird in der Referenz für die [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) -Enumeration beschrieben.

 

Die Remote Aktivierung hängt von der Sicherheits Beziehung zwischen Client und Server ab. Weitere Informationen finden Sie unter [Sicherheit in com](security-in-com.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM-Klassen Objekte und CLSIDs](com-class-objects-and-clsids.md)
</dt> <dt>

[Erstellen eines Objekts über ein Klassenobjekt](creating-an-object-through-a-class-object.md)
</dt> </dl>

 

 