---
title: Zeiger Attribute, die auf den Parameter angewendet werden
description: Jedes Zeiger Attribut (\ Ref \, \ Unique \ und \ PTR \) verfügt über Eigenschaften, die die Speicher Belegung beeinflussen. In der folgenden Tabelle werden diese Eigenschaften zusammengefasst.
ms.assetid: 25a609cd-efe7-4cbb-b80e-b6a3ad8cda38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c7710fb3c39702b2b2fdb789ed1218dc88d44ea
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039437"
---
# <a name="pointer-attributes-applied-to-the-parameter"></a>Zeiger Attribute, die auf den Parameter angewendet werden

Jedes Zeiger Attribut ( \[ [ref](/windows/desktop/Midl/ref) \] , \[ [Unique](/windows/desktop/Midl/unique) \] und \[ [ptr](/windows/desktop/Midl/ptr) \] ) verfügt über Eigenschaften, die die Speicher Belegung beeinflussen. In der folgenden Tabelle werden diese Eigenschaften zusammengefasst.



| Zeiger Attribut       | Client                                                                                                                                                                                                            | Server                                                              |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| Verweis ( \[ **ref** \] ) | Die Client Anwendung muss zuordnen.                                                                                                                                                                                 | Spezielle Behandlung **\[ , \]** die nur für nicht auf oberster Ebene basierende Zeiger erforderlich ist. |
| Eindeutig ( \[ **eindeutig** \] ) | Wenn ein Parameter ist, muss die Client Anwendung Wenn eingebettet, kann NULL sein. Wenn Sie von NULL in einen nicht-NULL-Wert wechseln, weist der Clientstub zu. Das Ändern von ungleich NULL in NULL kann zu einem verwaisen führen.<br/> |                                                                     |
| Vollständig ( \[ **ptr** \] )      | Wenn ein Parameter ist, muss die Client Anwendung Wenn eingebettet, kann NULL sein. Wenn Sie von NULL in einen nicht-NULL-Wert wechseln, weist der Clientstub zu. Das Ändern von ungleich NULL in NULL kann zu einem verwaisen führen.<br/> |                                                                     |



 

Das **\[ ref \]** -Attribut gibt an, dass der Zeiger auf einen gültigen Speicher zeigt. Definitionsgemäß muss die Client Anwendung den gesamten Arbeitsspeicher zuordnen, der für die Verweis Zeiger erforderlich ist.

Der eindeutige Zeiger kann von NULL in einen nicht-NULL-Wert geändert werden. Wenn der eindeutige Zeiger von NULL in einen nicht-NULL-Wert geändert wird, wird auf dem Client neuer Arbeitsspeicher zugeordnet. Wenn sich der eindeutige Zeiger von einem nicht-NULL-Wert in NULL ändert, kann das verwaisen Ergebnis sein. Weitere Informationen finden Sie unter Arbeits [Speicher verwaisen](memory-orphaning.md).

 

