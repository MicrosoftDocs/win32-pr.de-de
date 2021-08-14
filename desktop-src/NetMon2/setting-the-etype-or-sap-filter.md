---
description: Das Festlegen des Etype- oder SAP-Teils des Erfassungsfilters ist der erste Schritt beim Erstellen des Erfassungsfilters.
ms.assetid: 0a22f74b-5bb1-43df-a70a-9f30195177ea
title: Festlegen des Etype- oder SAP-Filters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abac637594debf03ca9f82c79382ababc4c696d79d5351b2d0be0a3e5b4ffa8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118363165"
---
# <a name="setting-the-etype-or-sap-filter"></a>Festlegen des Etype- oder SAP-Filters

Das Festlegen des Etype- oder SAP-Teils des Erfassungsfilters ist der erste Schritt beim Erstellen des Erfassungsfilters.

Im folgenden Beispiel wird der Erfassungsfilter so festgelegt, dass nur IPX-Datenverkehr abgerufen wird:


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



SAP- und Etype-Werte sind in der Regel in RFCs verfügbar. Sowohl SAP- als auch Etype-Werte können in einem Array enthalten sein.

 

 



