---
title: Treiber (Programmierhandbuch für 64-Bit-Windows)
description: Die 64-Bit-Version von Windows ist so konzipiert, dass Entwickler eine einzelne Quellcodebasis für ihre 32-Bit- und 64-Bit-Anwendungen verwenden können. Dies gilt in großem Umfang auch für 32-Bit- und 64-Bit-Windows Treiber.
ms.assetid: 85d789c9-91dd-4cdc-a10b-c38a455fc940
keywords:
- Treiber 64-Bit-Windows Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cda928bbfc8c7f83e3aeac0bacbaea1e1a46214d9c0785d4675a3042b87fa1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132853"
---
# <a name="drivers-programming-guide-for-64-bit-windows"></a>Treiber (Programmierhandbuch für 64-Bit-Windows)

Die 64-Bit-Version von Windows ist so konzipiert, dass Entwickler eine einzelne Quellcodebasis für ihre 32-Bit- und 64-Bit-Anwendungen verwenden können. Dies gilt in großem Umfang auch für 32-Bit- und 64-Bit-Windows Treiber.

32-Bit-Treiber können jedoch nicht auf 64-Bit-Windows ausgeführt werden und müssen portiert werden. Für Anwendungen im Benutzermodus enthält die 64-Bit-Windows WOW64, wodurch 32-Bit-Windows-Anwendungen auf Systemen mit 64-Bit-Windows. Für Treiber ist keine entsprechende Übersetzungsebene vorhanden.

Informationen zum Portieren von Treibern zu 64-Bit-Windows finden Sie unter [64-Bit-Probleme](https://msdn.microsoft.com/library/aa489627.aspx) im Windows Driver Kit (WDK).

 

 




