---
description: Die InstallFinalize-Aktion führt ein Skript aus, das alle Vorgänge in der Aktions Sequenz seit dem Start der Installation oder der Ausführung der InstallExecute-oder InstallExecuteAgain-Aktionen enthält.
ms.assetid: ed0e3c4f-d1ee-43b7-84a2-f4afe3ec28c6
title: InstallFinalize-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a96296c2241f5769296b7192ce89ab9f44364bb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753520"
---
# <a name="installfinalize-action"></a>InstallFinalize-Aktion

Die InstallFinalize-Aktion führt ein Skript aus, das alle Vorgänge in der Aktions Sequenz seit dem Start der Installation oder der Ausführung der [InstallExecute](installexecute-action.md) -oder [InstallExecuteAgain](installexecuteagain-action.md) -Aktionen enthält. Diese Aktion markiert das Ende einer Transaktion, die mit der [InstallInitialize](installinitialize-action.md) -Aktion beginnt.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die [InstallInitialize](installinitialize-action.md) -Aktion muss vor der InstallFinalize-Aktion erfolgen.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen

Es sind keine Aktions Daten Meldungen vorhanden.

## <a name="remarks"></a>Bemerkungen

Wenn erkannt wird, dass das Produkt zum Abschluss der Löschung markiert ist, werden die Vorgänge automatisch dem Skript hinzugefügt, um die Software in den **System Steuerungs** Informationen für das Produkt zu entfernen, die Registrierung aufzuheben und die **Veröffentlichung aufzuheben und** die zwischengespeicherte lokale Datenbank aus% Windows% zu entfernen, sofern vorhanden.

System Änderungen, die vor der Aktion vorgenommen wurden, werden möglicherweise nach dem Ausführen der Aktion "InstallFinalize" nicht wieder hergestellt. Die InstallFinalize-Aktion aktualisiert das System mit allen Vorgängen, die bis zu diesem Zeitpunkt festgelegt wurden, und beendet dann die Transaktion.

 

 



