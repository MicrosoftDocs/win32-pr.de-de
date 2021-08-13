---
description: Mit der Aktion AllocateRegistrySpace wird sichergestellt, dass der von der AVAILABLEFREEREG-Eigenschaft angegebene freie Registrierungsspeicherplatz in der Registrierung vorhanden ist.
ms.assetid: bb6ac685-5ad8-48e6-9c03-9ca42268d727
title: AllocateRegistrySpace-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40e47a0a0ebc3edec4605cbfac45443e4d30ee25df82ad3eaeb9da9ec9d3a94b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118639577"
---
# <a name="allocateregistryspace-action"></a>AllocateRegistrySpace-Aktion

Mit der Aktion AllocateRegistrySpace wird sichergestellt, dass der von der [**AVAILABLEFREEREG-Eigenschaft**](availablefreereg.md) angegebene freie Registrierungsspeicherplatz in der Registrierung vorhanden ist.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die Aktion AllocateRegistrySpace muss nach [InstallInitialize aufgerufen werden.](installinitialize-action.md) Es empfiehlt sich, den AllocateRegistrySpace vor allen anderen Aktionen zu planen, um sicherzustellen, dass genügend Registrierungsspeicher verfügbar ist, um fortzufahren.

## <a name="actiondata-messages"></a>ActionData-Meldungen



| Feld | Beschreibung der Aktionsdaten     |
|-------|--------------------------------|
| \[1\] | Erforderlicher Registrierungsspeicherplatz in KB. |



 

 

 



