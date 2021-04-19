---
description: Es gibt eine Reihe von konventionell unterstützten Sicherungs Typen&\# 8212; inkrementell, differenziell und vollständig&\# 8212;, die VSS kennt, sowie eine für VSS besondere Sicherungs Konfiguration.
ms.assetid: eddf29bc-221b-4b10-9842-a893b62fa846
title: VSS-Sicherungs Konfigurationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4e4c4f383a208781722053b47ba9ae5bcbf1db7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346948"
---
# <a name="vss-backup-configurations"></a>VSS-Sicherungs Konfigurationen

Es gibt eine Reihe von konventionell unterstützten Sicherungs Typen – inkrementell, differenziell und voll –, die VSS kennt, sowie eine für VSS besondere Sicherungs Konfiguration.

Beim Definieren einer Sicherungs Konfiguration geben eine Anforderer und die Writer auf einem System an, wie Daten auf ein Speichergerät geschrieben werden, wie der schattenkopiemechanismus bereitgestellt wird und welche Informationen gespeichert werden müssen. Die Interaktion zwischen Writern und Anforderern wird durch den Sicherungstyp bestimmt, der von einem Anforderer durchgeführt werden soll, und die Arten (oder Schemas), die jeder Writer unterstützen kann:

-   [VSS-Sicherungs Status](vss-backup-state.md)
-   [Unterstützung für Writer-Sicherungs Schema](writer-backup-schema-support.md)
-   [Schema Unterstützung auf Dateiebene](file-level-schema-support.md)

 

 



