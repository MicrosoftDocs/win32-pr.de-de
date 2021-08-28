---
description: Mit der Aktion InstallSFPCatalogFile werden die Kataloge installiert, die von Windows für Windows File Protection verwendet werden.
ms.assetid: 1c8253f1-ac7d-4346-a16e-887d16f521d9
title: InstallSFPCatalogFile-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75f3992a64e5e3150759fdbc2c8221e6bd8672a2c75e72343280fb3e552f3cae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787010"
---
# <a name="installsfpcatalogfile-action"></a>InstallSFPCatalogFile-Aktion

Mit der Aktion InstallSFPCatalogFile werden die Kataloge installiert, die von Windows für Windows File Protection verwendet werden. InstallSFPCatalogFile fragt [](component-table.md)die Component-Tabelle, die [Dateitabelle,](file-table.md)die [FileSFPCatalog-Tabelle](filesfpcatalog-table.md) und die [SFPCatalog-Tabelle ab.](sfpcatalog-table.md) Kataloge werden installiert, wenn sie einer Datei in einer Komponente zugeordnet sind, die für die lokale Installation festgelegt ist, oder wenn sie einer Datei zugeordnet sind, die in einer lokal installierten Komponente repariert wird.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die InstallSFPCatalogFile-Aktion muss vor [InstallFiles](installfiles-action.md) und nach [CostFinalize sequenziert werden.](costfinalize-action.md)

## <a name="actiondata-messages"></a>ActionData-Meldungen



| Feld | Beschreibung der Aktionsdaten                                    |
|-------|---------------------------------------------------------------|
| \[1\] | Name des Katalogs, der installiert wird.                          |
| \[2\] | Der Name des Katalogs, von dem die Installation dieses Katalogs abhängt. |



 

## <a name="remarks"></a>Hinweise

Ein Katalog, der von einem anderen Katalog abhängig ist, der nach dem übergeordneten Katalog installiert ist.

 

 



