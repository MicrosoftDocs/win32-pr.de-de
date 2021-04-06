---
title: Enumerationshandles wieder aufnehmen
description: Enumerationshandles sind Bezeichner für den tatsächlichen Fortsetzungs Schlüssel, der in den Instanzdaten für die Funktion enthalten ist. Dies ist für Sicherheit, Interoperabilität und zur Vereinfachung des aufrufercodes für die Funktion erforderlich.
ms.assetid: 6734e99b-7f8c-43c9-96e3-44c9783960dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f20e7a7d5e1f9afb15e6adad4c0d7643bf841d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947745"
---
# <a name="enumeration-resume-handles"></a>Enumerationshandles wieder aufnehmen

Enumerationshandles sind Bezeichner für den tatsächlichen Fortsetzungs Schlüssel, der in den Instanzdaten für die Funktion enthalten ist. Dies ist für Sicherheit, Interoperabilität und zur Vereinfachung des aufrufercodes für die Funktion erforderlich.

Wenn ein **null** -Wert für den Zeiger auf das Fortsetzungs handle übermittelt wird, wird kein Handle gespeichert, und die enumerationssuche kann nicht fortgesetzt werden. Dies ist hilfreich in Fällen, in denen die Anwendung nicht alle Elemente auflisten möchte.

Wenn ein-enumerationsaufruf einen Fehler zurückgibt, muss der Fortsetzungs Handle als ungültig behandelt und nicht für nachfolgende enumerationsaufrufe verwendet werden. Wenn dies auftritt, müssen Sie die Enumeration von Anfang an neu starten.

 

 




