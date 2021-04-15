---
description: Die ExecuteAction-Aktion initiiert die Ausführungssequenz mithilfe der ExecuteAction-Eigenschaft, um zu bestimmen, welcher Installationstyp ausgeführt werden soll.
ms.assetid: 61878317-ac87-4f6e-9375-12a78969e29e
title: ExecuteAction-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2970a0fb4e9297264071769ac7415cd2acf866b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485387"
---
# <a name="executeaction-action"></a>ExecuteAction-Aktion

Die ExecuteAction-Aktion initiiert die Ausführungssequenz mithilfe der [**ExecuteAction**](executeaction.md) -Eigenschaft, um zu bestimmen, welcher Installationstyp ausgeführt werden soll.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Diese Aktion sollte nacheinander ausgeführt werden, nachdem alle für den Beginn der Installation erforderlichen Informationen zum Sammeln von Informationen vollständig sind. Weitere Aktionen können nach der ExecuteAction-Aktion in der [Tabelle "InstallUISequence](installuisequence-table.md)" und der [Tabelle "AdminUISequence](adminuisequence-table.md)" sequenziert werden. Eine Sequenz beginnt in der Regel mit [*Kosten*](c-gly.md) Vorgängen, wie z. b. der [Aktion "costinitialize](costinitialize-action.md)", gefolgt von den Aktionen der Benutzeroberfläche und der ExecuteAction-Aktion.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen

Es sind keine Aktions Daten Meldungen vorhanden.

## <a name="remarks"></a>Bemerkungen

Die ExecuteAction-Aktion wird mit System Berechtigungen ausgeführt, wenn der Installer-Dienst aktiviert ist. Die Aktionen der obersten Ebene, z. b. [Installations Aktion](install-action.md), Ankündigungs [Aktion](advertise-action.md)und [Administrator Aktion](admin-action.md) , enthalten interne Logik, die bestimmt, ob das Aufrufen der ExecuteAction-Aktion erfordert, dass entweder die Ausführungssequenz oder die Benutzeroberflächen Sequenz ausgeführt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[InstallUISequence-Tabelle](installuisequence-table.md)
</dt> <dt>

[AdminUISequence-Tabelle](adminuisequence-table.md)
</dt> <dt>

[Costinitialize-Aktion](costinitialize-action.md)
</dt> </dl>

 

 



