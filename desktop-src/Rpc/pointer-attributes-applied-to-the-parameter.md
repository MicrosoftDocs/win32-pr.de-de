---
title: Zeigerattribute, die auf den Parameter angewendet werden
description: Jedes Zeigerattribut (\ ref\ , \ unique\ und \ ptr\ ) weist Merkmale auf, die sich auf die Speicherbelegung auswirken. In der folgenden Tabelle sind diese Merkmale zusammengefasst.
ms.assetid: 25a609cd-efe7-4cbb-b80e-b6a3ad8cda38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bcc6649dc663d7b029a7d7f345719330719d2eb19b6b7a63fa02797c17df16c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927495"
---
# <a name="pointer-attributes-applied-to-the-parameter"></a>Zeigerattribute, die auf den Parameter angewendet werden

Jedes Zeigerattribut ( \[ [ref](/windows/desktop/Midl/ref) \] , \[ [unique](/windows/desktop/Midl/unique) \] und \[ [ptr](/windows/desktop/Midl/ptr)) weist Merkmale \] auf, die sich auf die Speicherbelegung auswirken. In der folgenden Tabelle sind diese Merkmale zusammengefasst.



| Zeigerattribut       | Client                                                                                                                                                                                                            | Server                                                              |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| Referenz ( \[ **ref** \] ) | Clientanwendung muss zuordnen.                                                                                                                                                                                 | Spezielle Behandlung, die für **\[ \]** Out-Only-Zeiger auf nichttopebene erforderlich ist. |
| Eindeutig ( \[ **eindeutig** \] ) | Wenn ein Parameter vorhanden ist, muss die Clientanwendung zuordnen. wenn eingebettet, kann NULL sein. Wenn Sie von NULL in Nicht-NULL ändern, wird der Clientstub zugeordnet. Die Änderung von ungleich NULL in NULL kann zu Verwaisten führen.<br/> |                                                                     |
| Full ( \[ **ptr** \] )      | Wenn ein Parameter vorhanden ist, muss die Clientanwendung zuordnen. wenn eingebettet, kann NULL sein. Wenn Sie von NULL in Nicht-NULL ändern, wird der Clientstub zugeordnet. Die Änderung von ungleich NULL in NULL kann zu Verwaisten führen.<br/> |                                                                     |



 

Das **\[ \] ref-Attribut** gibt an, dass der Zeiger auf gültigen Arbeitsspeicher zeigt. Definitionsgemäß muss die Clientanwendung den gesamten Arbeitsspeicher zuordnen, den die Verweiszeiger benötigen.

Der eindeutige Zeiger kann von NULL in Nicht-NULL geändert werden. Wenn sich der eindeutige Zeiger von NULL in Nicht-NULL ändert, wird auf dem Client neuer Arbeitsspeicher zugeordnet. Wenn sich der eindeutige Zeiger von ungleich NULL in NULL ändert, kann verwaist werden. Weitere Informationen finden Sie unter [Verwaister Speicher.](memory-orphaning.md)

 

