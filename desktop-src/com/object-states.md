---
title: Objektzustände
description: Objektzustände
ms.assetid: 8ebef6d6-7a2f-4b95-91ca-999646cde82d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 268b9bc9c69009850a5172259ab7a13c760d2c72
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337145"
---
# <a name="object-states"></a>Objektzustände

Ein Verbund Objekt ist in einem von drei Zuständen vorhanden: passiv, geladen oder wird ausgeführt. Der Zustand eines Verbund Dokument Objekts beschreibt die Beziehung zwischen dem Objekt in seinem Container und der Anwendung, die für seine Erstellung verantwortlich ist. In der folgenden Tabelle werden diese Zustände zusammengefasst.



| Objektstatus       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Passiv<br/> | Das Verbund Dokument Objekt ist nur im Speicher vorhanden, entweder auf einem Datenträger oder in einer Datenbank. In diesem Zustand ist das Objekt zum Anzeigen oder bearbeiten nicht verfügbar.<br/>                                                                                                                                                                                                                                   |
| Geladen<br/>  | Die vom Objekt Handler erstellten Datenstrukturen des Objekts befinden sich im Arbeitsspeicher des Containers. Der Container hat die Kommunikation mit dem Objekt Handler hergestellt, und es stehen zwischengespeicherte Präsentationsdaten zum Rendern des Objekts zur Verfügung. Aufrufe werden vom Objekt Handler verarbeitet. Dieser Zustand wird aufgrund des niedrigen Aufwands verwendet, wenn ein Benutzer ein Objekt einfach anzeigen oder drucken kann.<br/> |
| Wird ausgeführt<br/> | Die Objekte, die Remoting steuern, wurden erstellt, und die OLE-Serveranwendung wird ausgeführt. Der Zugriff auf die Schnittstellen des Objekts ist möglich, und der Container kann Benachrichtigungen über Änderungen erhalten. In diesem Zustand kann ein Endbenutzer das Objekt bearbeiten oder anderweitig bearbeiten.<br/>                                                                                                                    |



 

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Eingabe des geladenen Zustands](entering-the-loaded-state.md)
-   [Eingeben des Status "wird ausgeführt"](entering-the-running-state.md)
-   [Eingabe des passiven Zustands](entering-the-passive-state.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbund Dokumente](compound-documents.md)
</dt> </dl>

 

 





