---
description: Sie können die folgenden Funktionen verwenden, um in Visual Basic mit Leistungsdaten zu arbeiten.
ms.assetid: c78eeb43-c713-42cc-a38f-f8aaa04f8dae
title: Leistungsindikator Funktionen für Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c777aa887b9dc42a061de95fb6f33dbf9d3dff7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865103"
---
# <a name="performance-counters-functions-for-visual-basic"></a>Leistungsindikator Funktionen für Visual Basic

> [!IMPORTANT]
> Die Funktionen, die in diesem Thema beschrieben werden, können in Zukunft geändert oder nicht mehr verfügbar sein. Stattdessen empfiehlt Microsoft die Verwendung der Funktionen, die unter [Funktionen von Leistungsindikatoren](performance-counters-functions.md)beschrieben werden.

Sie können die folgenden Funktionen verwenden, um in Visual Basic mit Leistungsdaten zu arbeiten.

- [**Pdhclosequery**](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery)
- [**Pdhcollectquerydata**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata)
- [**PdhRemoveCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhremovecounter)
- [**Pdhvbaddcounter**](pdhvbaddcounter.md)
- [**Pdhvbkreatecounterpathlist**](pdhvbcreatecounterpathlist.md)
- [**Pdhvbgetcounterpathelements**](pdhvbgetcounterpathelements.md)
- [**Pdhvbgetcounterpathfromlist**](pdhvbgetcounterpathfromlist.md)
- [**Pdhvbgetdoublecountervalue**](pdhvbgetdoublecountervalue.md)
- [**Pdhvbgetlogfilesize**](pdhvbgetlogfilesize.md)
- [**Pdhvbgetonecounterpath**](pdhvbgetonecounterpath.md)
- [**Pdhvbisgoodstatus**](pdhvbisgoodstatus.md)
- [**Pdhvbopenlog**](pdhvbopenlog.md)
- [**Pdhvbopenquery**](pdhvbopenquery.md)
- [**Pdhvbupdatelog**](pdhvbupdatelog.md)

> [!NOTE]
> Die `PdhVb***` -Funktionen funktionieren in einer Prozess internen Sitzung und sind nicht Thread sicher. Diese Funktionen sollten nur von einfachen Single Thread-Anwendungen verwendet werden.
