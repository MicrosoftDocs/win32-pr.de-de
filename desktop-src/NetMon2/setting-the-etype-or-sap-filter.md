---
description: Das Festlegen des ETYPE-oder SAP-Teils des Erfassungs Filters ist der erste Schritt bei der Erfassungs Filter Erstellung.
ms.assetid: 0a22f74b-5bb1-43df-a70a-9f30195177ea
title: Festlegen von ETYPE oder SAP-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aee117e992968265be5a973f3f4017832ee6ca0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959012"
---
# <a name="setting-the-etype-or-sap-filter"></a>Festlegen von ETYPE oder SAP-Filter

Das Festlegen des ETYPE-oder SAP-Teils des Erfassungs Filters ist der erste Schritt bei der Erfassungs Filter Erstellung.

Im folgenden Beispiel ist der Erfassungs Filter so festgelegt, dass nur IPX-Datenverkehr abgerufen wird:


```C++
BYTE Sap[]   = { 0x10, 0xE0 };
WORD Etype[] = { 0x8137 }; 

rc = SetNPPEtypeSapFilter(m_hBlob, 
     2,      //  nSaps,
     1,      //  nEtypes,
     &Sap,   //  LPBYTE lpSapTable,
     &Etype, //  LPWORD lpEtypeTable,
     0,      //  DWORD  FilterFlags,
     NULL
);
```



SAP-und ETYPE-Werte sind normalerweise in RFCs verfügbar. Sowohl die SAP-als auch die ETYPE-Werte können sich in einem Array befinden.

 

 



