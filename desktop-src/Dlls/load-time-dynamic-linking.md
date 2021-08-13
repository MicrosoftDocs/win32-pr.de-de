---
description: Wenn das System ein Programm startet, das dynamische Verknüpfungen zur Ladezeit verwendet, verwendet es die Informationen, die der Linker in der Datei platziert hat, um die Namen der dlLs zu finden, die vom Prozess verwendet werden.
ms.assetid: 29a17116-bb08-4fdd-857c-b7a7f8d2278c
title: Load-Time Dynamisches Verknüpfen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a0adac32841d822bba67031dd79171c52f25d8308b055aee2c55bb804ebefe9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118649358"
---
# <a name="load-time-dynamic-linking"></a>Load-Time Dynamisches Verknüpfen

Wenn das System ein Programm startet, das dynamische Verknüpfungen zur Ladezeit verwendet, verwendet es die Informationen, die der Linker in der Datei platziert hat, um die Namen der dlLs zu finden, die vom Prozess verwendet werden. Das System sucht dann nach den DLLs. Weitere Informationen finden Sie unter [Dynamic Link Library Search Order](dynamic-link-library-search-order.md).

Wenn das System eine erforderliche DLL nicht finden kann, beendet es den Prozess und zeigt ein Dialogfeld an, in dem der Fehler dem Benutzer angezeigt wird. Andernfalls ordnet das System die DLL dem virtuellen Adressraum des Prozesses zu und erhöht die DLL-Verweisanzahl.

Das System ruft die Einstiegspunktfunktion auf. Die Funktion empfängt einen Code, der angibt, dass der Prozess die DLL lädt. Wenn die Einstiegspunktfunktion nicht den Wert TRUE zurückgibt, beendet das System den Prozess mit einer entsprechenden Fehlermeldung. Weitere Informationen zur Einstiegspunktfunktion finden Sie unter [Dynamic Link Library Entry-Point Function](dynamic-link-library-entry-point-function.md).

Schließlich ändert das System die Funktionsadressentabelle mit den Startadressen für die importierten DLL-Funktionen.

Die DLL wird während der Initialisierung dem virtuellen Adressraum des Prozesses zugeordnet und nur bei Bedarf in den physischen Speicher geladen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden Load-Time dynamischen Verknüpfung](using-load-time-dynamic-linking.md)
</dt> </dl>

 

 



