---
description: Mit der Aktion "Zuweisung zuweisen" wird sichergestellt, dass der von der Eigenschaft availablefreereg angegebene freie Registrierungs Speicherplatz in der Registrierung vorhanden ist.
ms.assetid: bb6ac685-5ad8-48e6-9c03-9ca42268d727
title: Zuordnung von "depjeeregistryspace"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e6f986561595c73bf3bb1188d899af3d3d7d528
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348345"
---
# <a name="allocateregistryspace-action"></a>Zuordnung von "depjeeregistryspace"

Mit der Aktion "Zuweisung zuweisen" wird sichergestellt, dass der von der Eigenschaft [**availablefreereg**](availablefreereg.md) angegebene freie Registrierungs Speicherplatz in der Registrierung vorhanden ist.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die Aktion "zustelleregistryspace" muss nach " [InstallInitialize](installinitialize-action.md)" aufgerufen werden. Es empfiehlt sich, den zustellereregistryspace vor allen anderen Aktionen zu planen, um sicherzustellen, dass ausreichend Registrierungs Speicher verfügbar ist, um den Vorgang fortzusetzen.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen



| Feld | Beschreibung der Aktions Daten     |
|-------|--------------------------------|
| \[1\] | Benötigtes Registrierungs Speicher in KB. |



 

 

 



