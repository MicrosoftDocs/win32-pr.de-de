---
description: Die DisableRollback-Aktion deaktiviert das Rollback für den Rest der Installation.
ms.assetid: 5510b393-1f2e-44ba-97f5-663674d55b20
title: DisableRollback-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cbe500e3b810e5b06802e3a0face1da9b76441099a407882da08d5911a37d60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745370"
---
# <a name="disablerollback-action"></a>DisableRollback-Aktion

Die DisableRollback-Aktion deaktiviert [das Rollback](rollback-installation.md) für den Rest der Installation. Rollback ist nur für die Aktionen deaktiviert, die nach der DisableRollback-Aktion in den Sequenztabellen sequenziert werden. Rollback ist für die gesamte Installation deaktiviert, wenn die DisableRollback-Aktion vor der [InstallInitialize-Aktion sequenziert wird.](installinitialize-action.md)

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Es gibt keine Sequenzeinschränkungen.

## <a name="actiondata-message"></a>ActionData-Nachricht

Es sind keine ActionData-Meldungen enthalten.

 

 



