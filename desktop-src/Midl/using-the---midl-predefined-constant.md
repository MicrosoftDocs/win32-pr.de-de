---
title: Verwenden der __midl vordefinierten Konstante
description: Wenn der Mittell-Compiler die Eingabe-IDL-und ACF-Dateien verarbeitet, \_ \_ wird die mittlere-Version standardmäßig definiert und zur bedingten Kompilierung verwendet, um die Konsistenz im gesamten Build zu erzielen.
ms.assetid: ba9557f8-d398-4c87-993d-f4e545894cdd
keywords:
- Mittlerer l-compilermittell, Verwendung der _midl vordefinierten Konstante
- _midl der vordefinierten Konstanten-Mittel l
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae49675b38dcc3cab2d3d41e4f48cd0637d78523
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037039"
---
# <a name="using-the-__midl-predefined-constant"></a>Verwenden der \_ \_ vordefinierten-Konstante (Mitte)

Wenn der Mittell-Compiler die Eingabe-IDL-und ACF-Dateien verarbeitet, \_ \_ wird die mittlere-Version standardmäßig definiert und zur bedingten Kompilierung verwendet, um die Konsistenz im gesamten Build zu erzielen. Dadurch wird die Verwendung von define-Anweisungen in den Header Dateien, wie z. b. " **Mittel l \_ Pass**", ausgeblendet und durch ein konsistentes Flag ersetzt. Der Wert der \_ \_ mittleren l-Konstante gibt die Compilerversion *Major. Minor* gemäß der Formel *Major* \* 100 + *Minor* an, z. b. mittlerer l-ver. bei 6.0. x ist die \_ \_ Mittel-l als 600 definiert.

Wenn Sie sich entscheiden, können Sie diese Standardeinstellung überschreiben, indem Sie Folgendes in der Befehlszeile angeben: **/U- \_ \_ Mittell**. Weitere Informationen finden Sie unter [**/U**](-u.md).

 

 




