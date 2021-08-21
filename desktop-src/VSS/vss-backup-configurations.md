---
description: Es gibt eine Reihe von konventionell unterstützten Sicherungstypen&\# 8212;inkrementelle, differenzielle und vollständige&\# 8212;, die VSS kennt, sowie eine Sicherungskonfiguration, die für VSS geeignet ist.
ms.assetid: eddf29bc-221b-4b10-9842-a893b62fa846
title: VSS-Sicherungskonfigurationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8552bc379be4fc2bf7301043355a1a4417a59154ea15c36061b9cfd13c5d209f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056338"
---
# <a name="vss-backup-configurations"></a>VSS-Sicherungskonfigurationen

Es gibt eine Reihe von konventionell unterstützten Sicherungstypen – inkrementell, differenziell und vollständig –, die VSS kennt, sowie eine Sicherungskonfiguration, die für VSS geeignet ist.

Beim Definieren einer Sicherungskonfiguration geben ein Anforderer und die Writer auf einem System an, wie Daten auf ein Speichergerät geschrieben werden, wie der Schattenkopiemechanismus bereitgestellt wird und welche Informationen gespeichert werden müssen. Die Interaktion zwischen Writern und Anforderern richtet sich nach dem Sicherungstyp, den ein Anforderer ausführen möchte, und den Arten (oder Schemas), die jeder Writer unterstützen kann:

-   [VSS-Sicherungsstatus](vss-backup-state.md)
-   [Unterstützung von Writer-Sicherungsschemas](writer-backup-schema-support.md)
-   [Schemaunterstützung auf Dateiebene](file-level-schema-support.md)

 

 



