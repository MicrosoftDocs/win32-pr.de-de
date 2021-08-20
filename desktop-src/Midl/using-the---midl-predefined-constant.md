---
title: Verwenden der __midl vordefinierten Konstante
description: Wenn der MIDL-Compiler die Eingabe-IDL- und ACF-Dateien verarbeitet, wird midl standardmäßig definiert und für die bedingte Kompilierung verwendet, um im gesamten Build Konsistenz \_ \_ zu erzielen.
ms.assetid: ba9557f8-d398-4c87-993d-f4e545894cdd
keywords:
- MIDL-Compiler-MIDL mithilfe _midl vordefinierten Konstante
- _midl VORDEFINIERTE MIDL-Konstante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60fbc111ad07839d891f7bdffaf7ecaae83fbf277a0fc2c93fc483f526f9dda5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382821"
---
# <a name="using-the-__midl-predefined-constant"></a>Verwenden der \_ \_ vordefinierten midl-Konstante

Wenn der MIDL-Compiler die Eingabe-IDL- und ACF-Dateien verarbeitet, wird midl standardmäßig definiert und für die bedingte Kompilierung verwendet, um im gesamten Build Konsistenz \_ \_ zu erzielen. Dadurch wird die Verwendung von define-Anweisungen in den Headerdateien, z. B. **MIDL \_ PASS,** in Phasen unterteilt und durch ein konsistentes Flag ersetzt. Der Wert der midl-Konstante gibt die Compilerversion major.minor gemäß der Formel \_ \_   \* Hauptversion 100 + *Nebenversion* an, z. B. MIDL ver. In 6.0.x ist \_ \_ midl als 600 definiert.

Wenn Sie sich dafür entscheiden, können Sie diese Standardeinstellung überschreiben, indem Sie in der Befehlszeile Folgendes angeben: **/U \_ \_ midl**. Weitere Informationen finden Sie unter [**/U**](-u.md).

 

 




