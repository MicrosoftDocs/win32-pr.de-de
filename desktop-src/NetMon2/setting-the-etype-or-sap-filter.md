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
# <a name="setting-the-etype-or-sap-filter"></a><span data-ttu-id="1dde1-103">Festlegen von ETYPE oder SAP-Filter</span><span class="sxs-lookup"><span data-stu-id="1dde1-103">Setting the Etype or SAP Filter</span></span>

<span data-ttu-id="1dde1-104">Das Festlegen des ETYPE-oder SAP-Teils des Erfassungs Filters ist der erste Schritt bei der Erfassungs Filter Erstellung.</span><span class="sxs-lookup"><span data-stu-id="1dde1-104">Setting the Etype or SAP portion of the capture filter is the first step in the capture filter creation process.</span></span>

<span data-ttu-id="1dde1-105">Im folgenden Beispiel ist der Erfassungs Filter so festgelegt, dass nur IPX-Datenverkehr abgerufen wird:</span><span class="sxs-lookup"><span data-stu-id="1dde1-105">In the following example, the capture filter is set to only retrieve IPX traffic:</span></span>


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



<span data-ttu-id="1dde1-106">SAP-und ETYPE-Werte sind normalerweise in RFCs verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1dde1-106">SAP and Etype values are usually available in RFCs.</span></span> <span data-ttu-id="1dde1-107">Sowohl die SAP-als auch die ETYPE-Werte können sich in einem Array befinden.</span><span class="sxs-lookup"><span data-stu-id="1dde1-107">Both SAP and Etype values can be in an array.</span></span>

 

 



