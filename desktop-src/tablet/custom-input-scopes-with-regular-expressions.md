---
description: Sie können benutzerdefinierte Eingabe Bereiche mithilfe von Sprachmodellen definieren, die aus regulären Ausdrücken für Handschrift bestehen, und Sie den Feldern zuweisen. Wenn Sie z. b. eine Datenbankanwendung für Lagerteile erstellen und möchten, dass Benutzer mithilfe des Schreib Bereichs des Tablet PC-Eingabe Bereichs Teile eingeben können. Besteht die Syntax der Teilenummer aus drei Buchstaben, gefolgt von vier Zahlen gefolgt von einem anderen Buchstaben (z. b. ABC1234D), hätte die Handschrifterkennung eine schwierige Zeit, diese Eingabe zu erkennen, da Sie nicht im Sprachmodell definiert ist. Es ist kein vordefiniertes Faktoid vorhanden, das dieser Syntax entspricht, und Microsoft kann die Syntax nicht für jedes mögliche Feld einschließen, das eine Anwendung benötigt. Reguläre Ausdrücke für die Handschrift stellen eine einfache Möglichkeit für Anwendungen dar, Ihr eigenes Sprachmodell für ein bestimmtes sonderverwendungs Feld zu definieren. Beachten Sie, dass Sie bei der Arbeit in einer frei Hand fähigen Anwendung, die die Eigenschaft "Faktoid" des erkenzercontext-Objekts verwendet, nicht die Version 1-Faktoide in einem regulären Ausdruck verwenden können.
ms.assetid: 71f80196-0a36-4a14-a115-712bc909f6d7
title: Benutzerdefinierte Eingabe Bereiche mit regulären Ausdrücken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bdd7807221aca7b05ed4dc1facf7ddb01470c8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041538"
---
# <a name="custom-input-scopes-with-regular-expressions"></a>Benutzerdefinierte Eingabe Bereiche mit regulären Ausdrücken

Sie können benutzerdefinierte Eingabe Bereiche mithilfe von Sprachmodellen definieren, die aus regulären Ausdrücken für Handschrift bestehen, und Sie den Feldern zuweisen.

Wenn Sie z. b. eine Datenbankanwendung für Lagerteile erstellen und möchten, dass Benutzer mithilfe des Schreib Bereichs des Tablet PC-Eingabe Bereichs Teile eingeben können. Besteht die Syntax der Teilenummer aus drei Buchstaben, gefolgt von vier Zahlen gefolgt von einem anderen Buchstaben (z. b. ABC1234D), hätte die Handschrifterkennung eine schwierige Zeit, diese Eingabe zu erkennen, da Sie nicht im Sprachmodell definiert ist. Es ist kein vordefiniertes Faktoid vorhanden, das dieser Syntax entspricht, und Microsoft kann die Syntax nicht für jedes mögliche Feld einschließen, das eine Anwendung benötigt. Reguläre Ausdrücke für die Handschrift stellen eine einfache Möglichkeit für Anwendungen dar, Ihr eigenes Sprachmodell für ein bestimmtes sonderverwendungs Feld zu definieren.

> [!Note]  
> Wenn Sie in einer frei Hand fähigen Anwendung arbeiten, die die Eigenschaft " [**Faktoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) " des " [**erkennzercontext**](inkrecognizercontext-class.md) "-Objekts verwendet, können Sie die Faktoide der Version 1 nicht in einem regulären Ausdruck verwenden.

 

 

 



