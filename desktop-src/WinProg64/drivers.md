---
title: Treiber (Programmier Handbuch für 64-Bit-Windows)
description: Die 64-Bit-Version von Windows ist darauf ausgelegt, Entwicklern die Verwendung einer einzelnen Quell Code Basis für Ihre 32-Bit-und 64-Bit-Anwendungen zu ermöglichen. In großem Umfang gilt dies auch für 32-Bit-und 64-Bit-Windows-Treiber.
ms.assetid: 85d789c9-91dd-4cdc-a10b-c38a455fc940
keywords:
- Treiber 64-Bit-Windows-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6843a4efbb68652bf269c819c3a11ba102521318
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104340208"
---
# <a name="drivers-programming-guide-for-64-bit-windows"></a>Treiber (Programmier Handbuch für 64-Bit-Windows)

Die 64-Bit-Version von Windows ist darauf ausgelegt, Entwicklern die Verwendung einer einzelnen Quell Code Basis für Ihre 32-Bit-und 64-Bit-Anwendungen zu ermöglichen. In großem Umfang gilt dies auch für 32-Bit-und 64-Bit-Windows-Treiber.

32-Bit-Treiber können jedoch nicht auf 64-Bit-Fenstern ausgeführt werden und müssen portiert werden. Für Benutzermodusanwendungen enthält 64-Bit-Windows WOW64, das die Ausführung von 32-Bit-Windows-Anwendungen ermöglicht (mit einem gewissen Leistungsverlust) auf Systemen, auf denen 64-Bit-Windows ausgeführt wird. Für Treiber ist keine äquivalente übersetzungsebene vorhanden.

Informationen zum Portieren von Treibern in 64-Bit-Windows finden Sie unter [64-Bit-Probleme](https://msdn.microsoft.com/library/aa489627.aspx) im Windows-Treiberkit (WDK).

 

 




