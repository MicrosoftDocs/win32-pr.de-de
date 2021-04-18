---
description: Wenn das System ein Programm startet, das dynamische Verknüpfungen der Ladezeit verwendet, verwendet es die Informationen, die der Linker in der Datei abgelegt hat, um die Namen der DLLs zu suchen, die vom Prozess verwendet werden.
ms.assetid: 29a17116-bb08-4fdd-857c-b7a7f8d2278c
title: Dynamische Verknüpfung Load-Time
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28435fd6df4a3fc5311dc46dbb761b48c139a6fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530014"
---
# <a name="load-time-dynamic-linking"></a>Dynamische Verknüpfung Load-Time

Wenn das System ein Programm startet, das dynamische Verknüpfungen der Ladezeit verwendet, verwendet es die Informationen, die der Linker in der Datei abgelegt hat, um die Namen der DLLs zu suchen, die vom Prozess verwendet werden. Das System sucht dann nach den DLLs. Weitere Informationen finden Sie unter [Dynamic-Link Library Search Order](dynamic-link-library-search-order.md).

Wenn das System eine erforderliche DLL nicht finden kann, wird der Prozess beendet, und es wird ein Dialogfeld angezeigt, in dem der Fehler an den Benutzer gemeldet wird. Andernfalls ordnet das System die dll dem virtuellen Adressraum des Prozesses zu und erhöht den Verweis Zähler der dll.

Das System ruft die Einstiegspunkt Funktion auf. Die Funktion empfängt einen Code, der angibt, dass der Prozess die dll lädt. Wenn die Einstiegspunktfunktion nicht den Wert TRUE zurückgibt, beendet das System den Prozess mit einer entsprechenden Fehlermeldung. Weitere Informationen zur Einstiegspunkt Funktion finden Sie unter [Dynamic-Link Library Entry-Point Function](dynamic-link-library-entry-point-function.md).

Schließlich ändert das System die Funktions Adress Tabelle mit den Start Adressen für die importierten DLL-Funktionen.

Die dll wird während der Initialisierung dem virtuellen Adressraum des Prozesses zugeordnet und nur bei Bedarf in den physischen Speicher geladen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden Load-Time dynamischen Verknüpfungen](using-load-time-dynamic-linking.md)
</dt> </dl>

 

 



