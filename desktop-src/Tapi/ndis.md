---
description: Die ndis-Geräteklasse besteht aus Geräten, die mac-Treibern (Network Driver Interface Specification) zur Netzwerkzugriffssteuerung (Media Access Control, MAC) zugeordnet werden können, um die Netzwerkkommunikation zu unterstützen. Sie greifen mithilfe von Funktionen auf diese Geräte zu.
ms.assetid: 98cdd929-0bd7-4509-b2f5-4edd8d6a8080
title: Ndis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dda773591a3e3766a77b00925b9c15eacc5f45188900b12d6b9744c52f238ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761339"
---
# <a name="ndis"></a>Ndis

Die ndis-Geräteklasse besteht aus Geräten, die mac-Treibern (Network Driver Interface Specification) zur Netzwerkzugriffssteuerung (Media Access Control, MAC) zugeordnet werden können, um die Netzwerkkommunikation zu unterstützen. Sie greifen mithilfe von Funktionen auf diese Geräte zu.

Die [**Funktionen lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) und [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) füllen eine [**VARSTRING-Struktur**](/windows/desktop/api/Tapi/ns-tapi-varstring) aus, legen den **dwStringFormat-Member** auf den STRINGFORMAT BINARY-Wert und fügen diese \_ zusätzlichen Member an:

``` syntax
HANDLE  hDevice;          // NDIS connection identifier
CHAR    szDeviceType[1];  // name of device 
```

Das **hDevice-Mitglied** ist der Bezeichner, der an einen MAC übergeben werden soll, z. B. den asynchronen MAC für DFÜ-Netzwerke, um der Anruf-/Modemverbindung eine Netzwerkverbindung zu zuordnen. Der **szDeviceType-Member** ist eine auf NULL beendete Zeichenfolge, die den Namen des Geräts angibt, das dem Bezeichner zugeordnet ist.

 

 



