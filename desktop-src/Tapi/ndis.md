---
description: Die NDIS-Geräteklasse besteht aus Geräten, die mit Network Driver Interface Specification (NDIS)-Media Access Control (Mac)-Treibern verknüpft werden können, um die Netzwerkkommunikation zu unterstützen. Sie greifen auf diese Geräte mithilfe von Funktionen zu.
ms.assetid: 98cdd929-0bd7-4509-b2f5-4edd8d6a8080
title: NDIS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a0be1a69f98f9a4ff8cdc2f8ea173b208c0011d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343729"
---
# <a name="ndis"></a>NDIS

Die NDIS-Geräteklasse besteht aus Geräten, die mit Network Driver Interface Specification (NDIS)-Media Access Control (Mac)-Treibern verknüpft werden können, um die Netzwerkkommunikation zu unterstützen. Sie greifen auf diese Geräte mithilfe von Funktionen zu.

Die Funktionen " [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) " und " [**phonegetid**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) " füllen eine [**varstring**](/windows/desktop/api/Tapi/ns-tapi-varstring) -Struktur aus, indem Sie das Element " **dwstringformat** " auf den Binär Wert StringFormat festlegen \_ und diese zusätzlichen Member anhängen:

``` syntax
HANDLE  hDevice;          // NDIS connection identifier
CHAR    szDeviceType[1];  // name of device 
```

Das **hdevice** -Mitglied ist der Bezeichner, der an einen Mac übergeben werden soll, z. b. der asynchrone Mac für das DFÜ-Netzwerk, um eine Netzwerkverbindung mit der Telefon-/Modem Verbindung zuzuordnen. Der **szenvicetype** -Member ist eine NULL-terminierte Zeichenfolge, die den Namen des Geräts angibt, das mit dem Bezeichner verknüpft ist.

 

 



