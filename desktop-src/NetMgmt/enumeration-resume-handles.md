---
title: Enumeration Resume Handles
description: Enumerations-Wiederaufnahmehandles sind Bezeichner für den tatsächlichen Wiederaufnahmeschlüssel, der in den Instanzdaten für die Funktion enthalten ist. Dies ist erforderlich, um Sicherheit, Interoperabilität und den Aufrufercode für die Funktion zu vereinfachen.
ms.assetid: 6734e99b-7f8c-43c9-96e3-44c9783960dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10976661723af59af945b9dec1080196e682b308fa1a597edfc4cee6047aa783
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912190"
---
# <a name="enumeration-resume-handles"></a>Enumeration Resume Handles

Enumerations-Wiederaufnahmehandles sind Bezeichner für den tatsächlichen Wiederaufnahmeschlüssel, der in den Instanzdaten für die Funktion enthalten ist. Dies ist erforderlich, um Sicherheit, Interoperabilität und den Aufrufercode für die Funktion zu vereinfachen.

Wenn ein **NULL-Wert** für den Zeiger auf das Resume-Handle übergeben wird, wird kein Handle gespeichert, und die Enumerationssuche kann nicht fortgesetzt werden. Dies ist nützlich, wenn die Anwendung nicht alle Elemente aufzählen möchte.

Wenn ein Fehler von einem Enumerationsaufruf zurückgegeben wird, muss das Resume-Handle als ungültig behandelt und nicht für nachfolgende Enumerationsaufrufe verwendet werden. In diesem Fall müssen Sie die -Enumeration von Anfang an neu starten.

 

 




