---
title: Suchen eines Remoteobjekts
description: Suchen eines Remoteobjekts
ms.assetid: b329de53-646b-42a2-afa3-06473c3483d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96577ddd018ab6b00c5af59a9824984c1ffe255dc91849b4391b256b493b765a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992450"
---
# <a name="locating-a-remote-object"></a>Suchen eines Remoteobjekts

Mit der Einführung von COM für verteilte Systeme verwendet COM das grundlegende Modell für die Objekterstellung, das unter [COM-Klassenobjekte und CLSIDs](com-class-objects-and-clsids.md) beschrieben wird, und fügt mehrere Möglichkeiten hinzu, ein Objekt zu finden, das sich möglicherweise in einem anderen System in einem Netzwerk befindet, ohne die Clientanwendung zu überlasten.

COM hat Registrierungsschlüssel hinzugefügt, mit denen ein Server den Namen des Computers registrieren kann, auf dem er sich befindet, oder des Computers, auf dem sich ein vorhandener Speicher befindet. Daher müssen Clientanwendungen nur die CLSID des Servers kennen.

In Fällen, in denen dies gewünscht ist, hat COM jedoch einen zuvor reservierten Parameter von [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) durch eine [**COSERVERINFO-Struktur**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) ersetzt, die es einem Client ermöglicht, den Speicherort eines Servers anzugeben. Ein weiterer wichtiger Wert in der **CoGetClassObject-Funktion** ist die [**CLSCTX-Enumeration,**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) die angibt, ob das erwartete Objekt in-process, out-of-process local oder out-of-process remote ausgeführt werden soll. Zusammen bestimmen diese beiden Werte und die Werte in der Registrierung, wie und wo das Objekt ausgeführt werden soll.

> [!Note]  
> Aufrufe der Instanzerstellung, wenn sie einen Serverspeicherort angeben, können eine Registrierungseinstellung überschreiben. Der Algorithmus, den COM hierfür verwendet, wird in der Referenz für die [**CLSCTX-Enumeration**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) beschrieben.

 

Die Remoteaktivierung hängt von der Sicherheitsbeziehung zwischen Client und Server ab. Weitere Informationen finden Sie unter [Sicherheit in COM.](security-in-com.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM-Klassenobjekte und CLSIDs](com-class-objects-and-clsids.md)
</dt> <dt>

[Erstellen eines Objekts über ein Klassenobjekt](creating-an-object-through-a-class-object.md)
</dt> </dl>

 

 