---
description: Die InstallFinalize-Aktion führt ein Skript aus, das alle Vorgänge in der Aktionssequenz seit dem Start der Installation oder der Ausführung der InstallExecute- oder InstallExecuteAndroin-Aktionen enthält.
ms.assetid: ed0e3c4f-d1ee-43b7-84a2-f4afe3ec28c6
title: InstallFinalize-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4db8bd3ac9473fab868e5f7d83e760b39ca4dd6136faec987b5a7d2a3777bdd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787040"
---
# <a name="installfinalize-action"></a>InstallFinalize-Aktion

Die InstallFinalize-Aktion führt ein Skript aus, das alle Vorgänge in der Aktionssequenz seit dem Start der Installation oder der Ausführung der [InstallExecute-](installexecute-action.md) oder [InstallExecuteAndroin-Aktionen](installexecuteagain-action.md) enthält. Diese Aktion markiert das Ende einer Transaktion, die mit der [InstallInitialize-Aktion](installinitialize-action.md) beginnt.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die [InstallInitialize-Aktion](installinitialize-action.md) muss vor der InstallFinalize-Aktion erfolgen.

## <a name="actiondata-messages"></a>ActionData-Nachrichten

Es sind keine ActionData-Meldungen vorhanden.

## <a name="remarks"></a>Hinweise

Wenn erkannt wird, dass das Produkt für die vollständige Entfernung markiert ist, werden dem Skript automatisch Vorgänge hinzugefügt, um die **Software** in den **Systemsteuerung** Informationen für das Produkt zu entfernen, die Registrierung aufzuheben und die Veröffentlichung des Produkts aufzuheben und die zwischengespeicherte lokale Datenbank aus %WINDOWS% zu entfernen, sofern vorhanden.

Systemänderungen, die vor der Aktion vorgenommen wurden, werden möglicherweise nicht wiederhergestellt, nachdem die InstallFinalize-Aktion ausgeführt wurde. Die InstallFinalize-Aktion aktualisiert das System mit allen an diesem Punkt festgelegten Vorgängen und beendet dann die Transaktion.

 

 



