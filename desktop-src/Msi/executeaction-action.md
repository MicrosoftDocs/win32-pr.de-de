---
description: Die ExecuteAction-Aktion initiiert die Ausführungssequenz mithilfe der EXECUTEACTION-Eigenschaft, um zu bestimmen, welcher Installationstyp ausgeführt werden soll.
ms.assetid: 61878317-ac87-4f6e-9375-12a78969e29e
title: ExecuteAction-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20555af337f8774aec6c58769f2235da97ae763e044665e407a8dc29e75de750
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118636887"
---
# <a name="executeaction-action"></a>ExecuteAction-Aktion

Die ExecuteAction-Aktion initiiert die Ausführungssequenz mithilfe der [**EXECUTEACTION-Eigenschaft,**](executeaction.md) um zu bestimmen, welcher Installationstyp ausgeführt werden soll.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Diese Aktion sollte sequenziert werden, nachdem alle Informationen, die zum Starten der Installation erforderlich sind, abgeschlossen sind. Zusätzliche Aktionen können nach der ExecuteAction-Aktion in der [InstallUISequence-Tabelle](installuisequence-table.md)und der [AdminUISequence-Tabelle sequenziert werden.](adminuisequence-table.md) Eine Sequenz beginnt in [](c-gly.md) der Regel mit Kostenaktionen, z. B. der [CostInitialize-Aktion,](costinitialize-action.md)gefolgt von den Benutzeroberflächenaktionen und der ExecuteAction-Aktion.

## <a name="actiondata-messages"></a>ActionData-Meldungen

Es sind keine ActionData-Meldungen enthalten.

## <a name="remarks"></a>Hinweise

Die ExecuteAction-Aktion wird mit Systemberechtigungen ausgeführt, wenn der Installerdienst aktiviert ist. Die Aktionen der obersten Ebene, z. B. die [INSTALL-Aktion,](install-action.md)die [ADVERTISE-Aktion](advertise-action.md)und die [ADMIN-Aktion,](admin-action.md) enthalten interne Logik, die bestimmt, ob zum Aufrufen der ExecuteAction-Aktion die Ausführung der Ausführungssequenz oder der Benutzeroberflächensequenz erforderlich ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[InstallUISequence-Tabelle](installuisequence-table.md)
</dt> <dt>

[AdminUISequence-Tabelle](adminuisequence-table.md)
</dt> <dt>

[CostInitialize-Aktion](costinitialize-action.md)
</dt> </dl>

 

 



